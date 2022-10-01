# Лабораторная работа №1
![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab1/img/2022-10-01%2018_50_04-Lab_Basic_Switch_Configuration-1801-36784d.docx%20-%20WordPad.png)
### Часть 1. Проверка конфигурации коммутатора по умолчанию

Входим в привилегированный режим с помощью команды enable (en) и изучаем текущий файл running configuration:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab1/img/2022-10-01%2015_02_41-PC0.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab1/img/2022-10-01%2015_03_10-PC0.png)

⦁ Сколько интерфейсов FastEthernet имеется на коммутаторе 2960?

24, от

interface FastEthernet0/1

до

interface FastEthernet0/24

⦁ Сколько интерфейсов Gigabit Ethernet имеется на коммутаторе 2960?

Два, 

interface GigabitEthernet0/1

interface GigabitEthernet0/2

⦁ Каков диапазон значений, отображаемых в vty-линиях?

От 0 до 4 и от 5 до 15.

### Часть 2. Создание сети и настройка основных параметров устройства
##### ⦁	Настройте базовые параметры коммутатора.
##### ⦁	Настройте IP-адрес для ПК.
### Часть 3. Проверка сетевых подключений
##### ⦁	Отобразите конфигурацию устройства.
##### ⦁	Протестируйте сквозное соединение, отправив эхо-запрос.
##### ⦁	Протестируйте возможности удаленного управления с помощью Telnet.
