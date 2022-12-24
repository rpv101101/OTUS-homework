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

Подсеть A, поддерживающая 58 хостов: **192.168.1.1 - 192.168.1.63 (192.168.1.0/26)**;

Подсеть B, поддерживающая 28 хостов: **192.168.1.65 - 192.168.1.95 (192.168.1.64/27)**;
 
Подсеть C, поддерживающая 12 узлов: **192.168.1.97 - 192.168.1.111 (192.168.1.96/28)**.

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/11_TAB.png)

### Создание сети согласно топологии
![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/10_scheme.png)
### Базовая настройка коммутаторов и маршрутизаторов
![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/4_S1.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/5_S2.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/6_R1.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/6_R2.png)
### Настройка маршрутизации между сетями VLAN на маршрутизаторе R1
>a.	Активируйте интерфейс G0/0/1 на маршрутизаторе.
>
>b.	Настройте подинтерфейсы для каждой VLAN в соответствии с требованиями таблицы IP-адресации. Все субинтерфейсы используют инкапсуляцию 802.1Q и назначаются первый полезный адрес из вычисленного пула IP-адресов. Убедитесь, что подинтерфейсу для native VLAN не назначен IP-адрес. Включите описание для каждого подинтерфейса.
>
>c.	Убедитесь, что вспомогательные интерфейсы работают.


![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/12_G000.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/13_R1.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/14_R1.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/15_R1.png)

### Настройка G0/0/1 на R2, затем G0/0/0 и статическую маршрутизацию для обоих маршрутизаторов

>a.	Настройте G0/0/1 на R2 с первым IP-адресом подсети C, рассчитанным ранее.

>b.	Настройте интерфейс G0/0/0 для каждого маршрутизатора на основе приведенной выше таблицы IP-адресации.

>c.	Настройте маршрут по умолчанию на каждом маршрутизаторе, указываемом на IP-адрес G0/0/0 на другом маршрутизаторе.

>d.	Убедитесь, что статическая маршрутизация работает с помощью пинга до адреса G0/0/1 R2 от R1.

>e.	Сохраните текущую конфигурацию в файл загрузочной конфигурации.

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/16.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/17.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/18.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/19.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/20.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/21.png)

### Создание VLAN на коммутаторе S1

> a.	Создайте необходимые VLAN на коммутаторе 1 и присвойте им имена из приведенной выше таблицы.
> 
>b.	Настройте и активируйте интерфейс управления на S1 (VLAN 200), используя второй IP-адрес из подсети, рассчитанный ранее. Кроме того установите шлюз по умолчанию на S1.
>
>c.	Настройте и активируйте интерфейс управления на S2 (VLAN 1), используя второй IP-адрес из подсети, рассчитанный ранее. Кроме того, установите шлюз по умолчанию на S2
>d.	Назначьте все неиспользуемые порты S1 VLAN Parking_Lot, настройте их для статического режима доступа и административно деактивируйте их. На S2 административно деактивируйте все неиспользуемые порты.
>
>Примечание. Команда interface range полезна для выполнения этой задачи с минимальным количеством команд.


![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/22.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/23.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/24.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/25.png)


Почему интерфейс F0/5 указан в VLAN 1? **Настройка этого порта не выполнялась**

### Назначение VLAN соответствующим интерфейсам коммутатора
![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/26.png)
### Ручная настройка интерфейса S1 F0/5 в качестве транка 802.1Q

>a.	Измените режим порта коммутатора, чтобы принудительно создать магистральный канал.
>
>b.	В рамках конфигурации транка  установите для native  VLAN значение 1000.
>
>c.	В качестве другой части конфигурации магистрали укажите, что VLAN 100, 200 и 1000 могут проходить по транку.
>
>d.	Сохраните текущую конфигурацию в файл загрузочной конфигурации.
>
>e.	Проверьте состояние транка.

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/27.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/28.png)
## Настройка и проверка двух серверов DHCPv4 на R1
### Настройка R1 с пулами DHCPv4 для двух поддерживаемых подсетей
>a.	Исключите первые пять используемых адресов из каждого пула адресов.
>
>Откройте окно конфигурации
>
>b.	Создайте пул DHCP (используйте уникальное имя для каждого пула).
>
>c.	Укажите сеть, поддерживающую этот DHCP-сервер.
>
>d.	В качестве имени домена укажите CCNA-lab.com.
>
>e.	Настройте соответствующий шлюз по умолчанию для каждого пула DHCP.
>
>f.	Настройте время аренды на 2 дня 12 часов и 30 минут.
>
>g.	Затем настройте второй пул DHCPv4, используя имя пула R2_Client_LAN и вычислите сеть, маршрутизатор по умолчанию, и используйте то же имя домена и время аренды, что и предыдущий пул DHCP.

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/29.png)

Вопрос: мой маршрутизатор отказывается работать с lease - почему? 

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/30.png)

### Проверка конфигурации сервера DHCPv4
>a.	Чтобы просмотреть сведения о пуле, выполните команду show ip dhcp pool.
>
>b.	Выполните команду show ip dhcp binding для проверки установленных назначений адресов DHCP.
>
>c.	Выполните команду show ip dhcp server statistics для проверки сообщений DHCP.

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/31.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/32.png)

### Попытка получить IP-адрес от DHCP на PC-A

>a.	Из командной строки компьютера PC-A выполните команду ipconfig /all.
>
>b.	После завершения процесса обновления выполните команду ipconfig для просмотра новой информации об IP-адресе.
>
>c.	Проверьте подключение с помощью пинга IP-адреса интерфейса R0 G0/0/1.
>
![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/33.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8%20(4)/IMG/34.png)

## Настройка и проверка DHCP-ретрансляции на R2
### Настройка R2 в качестве агента DHCP-ретрансляции для локальной сети на G0/0/1

### Попытка получить IP-адрес от DHCP на PC-B
