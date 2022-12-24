# Реализация DHCPv4 
## Топология
![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/1_TP.png)
## Таблица адресации
![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/2_TAB.png)
## Таблица VLAN
![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/3_VLAN_.png)
## Задачи
Часть 1. Создание сети и настройка основных параметров устройства

Часть 2. Настройка и проверка двух серверов DHCPv4 на R1

Часть 3. Настройка и проверка DHCP-ретрансляции на R2

## Создание сети и настройка основных параметров устройства
### Создание схемы адресации

>Подсеть сети 192.168.1.0/24 в соответствии со следующими требованиями:
>
>a.	Одна подсеть «Подсеть A», поддерживающая 58 хостов (клиентская VLAN на R1).
>
>
>Запишите первый IP-адрес в таблице адресации для R1 G0/0/1.100. 
>
>b.	Одна подсеть «Подсеть B», поддерживающая 28 хостов (управляющая VLAN на R1). 
>
>
>Запишите первый IP-адрес в таблице адресации для R1 G0/0/1.200. Запишите второй IP-адрес в таблице адресов для S1 VLAN 200 и введите соответствующий шлюз по >умолчанию.
>
>c.	Одна подсеть «Подсеть C», поддерживающая 12 узлов (клиентская сеть на R2).
>
>
>Запишите первый IP-адрес в таблице адресации для R2 G0/0/1.
Подсеть A, поддерживающая 58 хостов: 192.168.1.1 - 192.168.1.62 (192.168.1.0/26);

Подсеть B, поддерживающая 28 хостов: 192.168.1.1 - 192.168.1.30 (192.168.1.0/27);
 
Подсеть C, поддерживающая 12 узлов: 192.168.1.1 - 192.168.1.14 (192.168.1.0/28).


### Создание сети согласно топологии
![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/10_scheme.png)
### Базовая настройка коммутаторов и маршрутизаторов
![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/4_S1.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/5_S2.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/6_R1.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/6_R2.png)
