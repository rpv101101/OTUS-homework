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

