# Лабораторная работа. Доступ к сетевым устройствам по протоколу SSH

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/0_%D0%A2%D0%BE%D0%BF%D0%BE%D0%BB%D0%BE%D0%B3%D0%B8%D1%8F.png)

## Задачи
Часть 1. Настройка основных параметров устройства

Часть 2. Настройка маршрутизатора для доступа по протоколу SSH

Часть 3. Настройка коммутатора для доступа по протоколу SSH

Часть 4. SSH через интерфейс командной строки (CLI) коммутатора

## Часть 1. Настройка основных параметров устройства

Настройка ПК PC-A и коммутатора S1:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/1_%D0%9D%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0_PCA_1.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/2_%D0%9D%D0%B0%D1%81%D1%82%D1%80%D0%BE%D0%B9%D0%BA%D0%B0_PCA_2.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/3_conf_vlan_1.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/4_conf_def_gateway.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/5_show_ip_brief.png)

Топология сети в CPT:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/2022-12-11%2014_09_33-Cisco%20Packet%20Tracer.png)

Проверка подключения:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/8_R1_ping_test.png)


## Часть 2. Настройка маршрутизатора для доступа по протоколу SSH

Первоначальная настройка маршрутизатора R1:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/6_R1_setup.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/7_R1_setup2.png)

Сначала настроил vty 0 4, после исправил на 0 15.

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/20_R1_enabling_ssh_and_telnet.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/9_banner_setup.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/10_domain_setup.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/11_generate_RSA.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/13_admin_password_setup.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/20_R1_enabling_ssh_and_telnet.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/21_SSH_test.png)

## Часть 3. Настройка коммутатора для доступа по протоколу SSH

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/12_vty_setup.png.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/15_S1_setup.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/16_S1_banner_setup.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/17_S1_RSA_.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/18_S1_SSH_setup.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/19_S1_vty_setup.png)


## Часть 4. SSH через интерфейс командной строки (CLI) коммутатора

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/22_SSH_QM.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab5/IMG/23_SSH_test2.png)


## Вопросы для повторения

Какие версии протокола SSH поддерживаются при использовании интерфейса командной строки?

**SSH1 и SSH2

Как предоставить доступ к сетевому устройству нескольким пользователям, у каждого из которых есть собственное имя пользователя?

**Создать несколько пользователей с помощью команды username 

