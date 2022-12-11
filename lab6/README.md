# Лабораторная работа - Внедрение маршрутизации между виртуальными локальными сетями
## Топология

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/2022-12-11%2014_28_59-lab5.docx%20-%20Word.png)

## Таблица адресации

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/2022-12-11%2014_29_05-lab5.docx%20-%20Word.png)

## Таблица VLAN

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/2022-12-11%2014_29_14-lab5.docx%20-%20Word.png)

## Задачи
1. Создание сети и настройка основных параметров устройства

2. Создание сетей VLAN и назначение портов коммутатора

3. Настройка транка 802.1Q между коммутаторами

4. Настройка маршрутизации между сетями VLAN

5. Проверка, что маршрутизация между VLAN работает

## Часть 1. Создание сети и настройка основных параметров устройства

Создание сеть согласно топологии:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/2022-12-11%2014_36_55-Cisco%20Packet%20Tracer%20-%20C__Users_user_Documents_OTUS_lab6_6.pkt.png)

Первоначальная настройка R1:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/2022-12-11%2014_39_13-PC-A.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/2_R1_setup.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/7_R1_setup2.png)

Настройка компьютеров:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/3_PCA_setup.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/4_PCA_setup.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/5_PCB_setup.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/6_PCB_setup.png)

Настройка S1 и S2:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/8_S1_setup1.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/9_S1_setup2.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/10_S1_setup3.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/11_S1_setup4.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/12_S1_setup5.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/13_S2_setup.png)

## Часть 2. Создание сетей VLAN и назначение портов коммутатора

Создание сети VLAN на коммутаторах:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/14_S1_vlan_p1.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/15_S1_vlan_p2.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/16_S2_vlan_p1.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/17_S1_vlan_p3.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/18_S2_vlan_p2.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/19_S1_999.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/20_S1_999.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/21_S2_999.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/22_S2_999.png)

Назначение используемых портов соответствующей VLAN:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/23_interface1.png)

Проверка настройки VLAN на коммутаторах:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/24_S1_vlan_info.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/25_S2_vlan_info.png)

## Часть 3. Конфигурация магистрального канала стандарта 802.1Q между коммутаторами

Шаг 1. Вручную настройте магистральный интерфейс F0/1 на коммутаторах S1 и S2.
Настройка статического транкинга на интерфейсе F0/1 для обоих коммутаторов:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/26_S1_F01.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/27_S2_F01.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/28_S1.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/29_s1.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/30_s2.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/31_S2.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/32_s1.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/33_S1.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/34_s2.png)

Что произойдет, если G0/0/1 на R1 будет отключен?

**f0/5 на S1 не будет отображаться 

## Часть 4. Настройка маршрутизации между сетями VLAN

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/2022-12-11%2016_27_08-PC-B.png)

В начале работы ошибочно был присвоен адрес для интерфейса G0/0/1, поэтому была получена такая ошибка:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/2022-12-11%2016_29_52-PC-B.png)

Выполнена замена:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/2022-12-11%2016_31_13-PC-B.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/2022-12-11%2016_37_32-PC-B.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/2022-12-11%2016_38_21-PC-B.png)




## Часть 5. Проверка работы маршрутизации между VLAN

a.	Отправьте эхо-запрос с PC-A на шлюз по умолчанию.

b.	Отправьте эхо-запрос с PC-A на PC-B.

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/2022-12-11%2016_42_53-PC-A.png)

c.	Отправьте команду ping с компьютера PC-A на коммутатор S2.

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/2022-12-11%2016_43_35-PC-A.png)

В окне командной строки на PC-B выполните команду tracert на адрес PC-A:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab6/IMG/2022-12-11%2016_44_00-PC-B.png)

Какие промежуточные IP-адреса отображаются в результатах?

**Адрес интерфейса G0/0/1.30 на R1 и адрес компьютера PC-A

