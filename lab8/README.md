# Настройка DHCPv6
## Топология
![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8/IMG/top1.png "Топология")
## Таблица адресации
![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8/IMG/RT1.png "Таблица адресации")

## Задачи
1. Создание сети и настройка основных параметров устройства
2. Проверка назначения адреса SLAAC от R1
3. Настройка и проверка сервера DHCPv6 без гражданства на R1
4. Настройка и проверка состояния DHCPv6 сервера на R1
5. Настройка и проверка DHCPv6 Relay на R2
## Часть 1. Создание сети и настройка основных параметров устройства

### Настройка базовых параметров коммутатора

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8/IMG/1_S1_setup.png "Настройка коммутатора S1")

### Настройка базовых параметров маршрутизаторов 

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8/IMG/3_R3_setup.png "Настройка маршрутизатора R1")

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8/IMG/3_R2_setup.png "Настройка маршрутизатора R2")

### Настройка интерфейсов и маршрутизации маршрутизаторов

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8/IMG/5_R2_setup.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8/IMG/6_R1_sh_int.png)



![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8/IMG/8_PCA_DHCP1.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8/IMG/9_PCB_DHCP1.png)

## Проверка назначения адреса SLAAC от R1


ipv6 dhcp relay destination к сожалению, не работает в CPT. 

=================================================================
## Попытка №2
>Поэтому предлагаю Вам такую схему: реализуйте dhcp с сохранением состояния сразу на R2 - обойдемся без ретрансляции. И не забудьте поправить dhcp без сохранения состояния, а то ipv6 адреса у узла нет.
>
>Успехов!

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8/IMG/1.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8/IMG/2.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8/IMG/3.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8/IMG/4.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8/IMG/5.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8/IMG/6.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8/IMG/7.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab8/IMG/8.png)




