# Конфигурация безопасности коммутатора 
## Топология
![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/TOP.png)
## Таблица адресации
![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/TA.png)
## Цели
### Часть 1. Настройка основного сетевого устройства
•	Создайте сеть.

•	Настройте маршрутизатор R1.

•	Настройка и проверка основных параметров коммутатора

### Часть 2. Настройка сетей VLAN
•	Сконфигруриуйте VLAN 10.

•	Сконфигруриуйте SVI для VLAN 10.

•	Настройте VLAN 333 с именем Native на S1 и S2.

•	Настройте VLAN 999 с именем ParkingLot на S1 и S2.

### Часть 3: Настройки безопасности коммутатора

•	Реализация магистральных соединений 802.1Q.

•	Настройка портов доступа

•	Безопасность неиспользуемых портов коммутатора

•	Документирование и реализация функций безопасности порта.

•	Реализовать безопасность DHCP snooping .

•	Реализация PortFast и BPDU Guard

•	Проверка сквозной связанности.

## Настройка основного сетевого устройства
### Создание сети 
>a.	Создайте сеть согласно топологии.
>
>b.	Инициализация устройств

### Настройка маршрутизатора R1

>a.	Загрузите следующий конфигурационный скрипт на R1.

>Откройте окно конфигурации

>enable
>
>configure terminal
>
>hostname R1
>
>no ip domain lookup
>
>ip dhcp excluded-address 192.168.10.1 192.168.10.9
>
>ip dhcp excluded-address 192.168.10.201 192.168.10.202
>
>!
>ip dhcp pool Students
>
> network 192.168.10.0 255.255.255.0
> 
> default-router 192.168.10.1
> 
> domain-name CCNA2.Lab-11.6.1
> 
>!
>interface Loopback0
>
> ip address 10.10.1.1 255.255.255.0
> 
>!
>interface GigabitEthernet0/0/1
>
> description Link to S1
> 
> ip dhcp relay information trusted
> 
> ip address 192.168.10.1 255.255.255.0
> 
> no shutdown
> 
>!
>
>line con 0
>
> logging synchronous
> 
> exec-timeout 0 0


