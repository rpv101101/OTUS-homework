# Лабораторная работа №2. Просмотр таблицы MAC-адресов коммутатора 
![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-21%2016_17_10-Lab___View_the_Switch_MAC_Address_Table-1801-6952c3%20(2).docx%20-%20Word.png)
## Подключение сети в соответствии с топологией
![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-22%2019_27_17-Cisco%20Packet%20Tracer%20-%20C__Users_user_Desktop_OTUS_lab2_lab2.pkt.png)
## Инициализация и перезагрузка коммутаторов
![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-21%2017_37_22-PC-A.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-21%2017_37_44-PC-B.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-21%2017_51_59-PC-A.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-21%2017_59_03-PC-A.png)

## Настройка базовых параметров коммутаторов

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-21%2017_55_16-PC-A.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-21%2017_54_08-PC-B.png)

Задания:
1) Назначьте cisco в качестве паролей консоли и VTY.
2) Назначьте class в качестве пароля доступа к привилегированному режиму EXEC.

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-21%2017_50_38-PC-A.png)

## Изучение таблицы МАС-адресов коммутатора
Результат выполнения команды **ipconfig /all** в командной строке компьютеров PC-A и PC-B:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-21%2018_01_43-PC-A.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-21%2018_02_01-PC-B.png)

MAC-адрес компьютера PC-A: 0002.16E1.4123

MAC-адрес компьютера PC-B: 0060.2FC6.2186

Результат выполнения команды **show interface F0/1** через консоль при подключении к каждому коммутатору:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-21%2018_03_20-PC-A.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-21%2018_03_35-PC-B.png)


МАС-адрес коммутатора S1 Fast Ethernet 0/1: 00d0.d360.3701

МАС-адрес коммутатора S2 Fast Ethernet 0/1: 0001.962d.a501

Результат выполнения команды **show mac address-table** 

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-21%2018_06_02-PC-B.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-21%2018_06_16-PC-A.png)

Результат выполнения команды **clear mac address-table dynamic** 

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-21%2018_11_24-PC-B.png)

После выполнения эхо-запросов на компьютеры и коммутаторы:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-21%2018_14_37-PC-B.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab2/img/2022-10-21%2018_15_08-PC-B.png)


