# Конфигурация безопасности коммутатора 
## Топология
![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/TOP.png)
## Таблица адресации
![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/TA.png)
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

>b.	Проверьте текущую конфигурацию на R1, используя следующую команду:
>
>R1# show ip interface brief
>
>c.	Убедитесь, что IP-адресация и интерфейсы находятся в состоянии up / up (при необходимости устраните неполадки).

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/R1_int.png)

### Настройка и проверка основных параметров коммутатора
>a.	Настройте имя хоста для коммутаторов S1 и S2.
>
>Откройте окно конфигурации
>
>b.	Запретите нежелательный поиск в DNS.
>
>c.	Настройте описания интерфейса для портов, которые используются в S1 и S2.
>
>d.	Установите для шлюза по умолчанию для VLAN управления значение 192.168.10.1 на обоих коммутаторах.

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/S1_shr.png)

## Настройка сетей VLAN на коммутаторах
### Конфигурация VLAN 10
> Добавьте VLAN 10 на S1 и S2 и назовите VLAN - Management.

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/S2_defg.png)

### Конфигурация SVI для VLAN 10
> Настройте IP-адрес в соответствии с таблицей адресации для SVI для VLAN 10 на S1 и S2. Включите интерфейсы SVI и предоставьте описание для интерфейса.

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/S1_1.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/S2_1.png)

### Настройка VLAN 333 с именем Native на S1 и S2, настройка VLAN 999 с именем ParkingLot на S1 и S2

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/S1_shv.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/S2_shv.png)

## Настройки безопасности коммутатора
### Релизация магистральных соединений 802.1Q
>a.	Настройте все магистральные порты Fa0/1 на обоих коммутаторах для использования VLAN 333 в качестве native VLAN.
>
>b.	Убедитесь, что режим транкинга успешно настроен на всех коммутаторах.
>
>S1# show interface trunk
>
>Port Mode Encapsulation Status Native vlan
>
>Fa0/1 on 802.1q trunking 333
>
>Port Vlans allowed on trunk
>
>Fa0/1 1-4094
>
>Port Vlans allowed and active in management domain
>
>Fa0/1 1,10,333,999
>
>Port Vlans in spanning tree forwarding state and not pruned
>
>Fa0/1 1,10,333,999
>
>S2# show interface trunk
>
>Port Mode Encapsulation Status Native vlan
>
>Fa0/1 on 802.1q trunking 333
>
>Port Vlans allowed on trunk
>
>Fa0/1 1-4094
>
>Port Vlans allowed and active in management domain
>
>Fa0/1 1,10,333,999
>
>Port Vlans in spanning tree forwarding state and not pruned
>
>Fa0/1 1,10,333,999
>
>c.	Отключить согласование DTP F0/1 на S1 и S2. 
>
>d.	Проверьте с помощью команды show interfaces.
>
>S1# show interfaces f0/1 switchport | include Negotiation
>
>Negotiation of Trunking: Off
>
>S1# show interfaces f0/1 switchport | include Negotiation
>
>Negotiation of Trunking: Off
>
![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/S1_2.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/S1_3.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/S2_2.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/1.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/2.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/3.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/4.png)

### Настройка портов доступа

>a.	На S1 настройте F0/5 и F0/6 в качестве портов доступа и свяжите их с VLAN 10.
>
>b.	На S2 настройте порт доступа Fa0/18 и свяжите его с VLAN 10.
>
![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/S1_11_1.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/S2_11_1.png)

### Безопасность неиспользуемых портов коммутатора

>a.	На S1 и S2 переместите неиспользуемые порты из VLAN 1 в VLAN 999 и отключите неиспользуемые порты.
>
>b.	Убедитесь, что неиспользуемые порты отключены и связаны с VLAN 999, введя команду  show.
>
>S1# show interfaces status
>
>S2# show interfaces status
>

При просмотре свойств интерфейсов видно описание, а в show interfaces status - нет (почему?): 

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/S1_11_2.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/S1_4.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/S2_4.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/S1_5.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab9/IMG/S2_5.png)



