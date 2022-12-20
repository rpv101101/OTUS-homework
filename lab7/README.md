# Развертывание коммутируемой сети с резервными каналами
## Топология

![Alt](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/2022-12-20%2019_02_03-lab7.docx%20-%20Word.png "Топология")

## Таблица адресации

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/2022-12-20%2019_02_14-lab7.docx%20-%20Word.png "Таблица адресации")

## Цели
1. Создание сети и настройка основных параметров устройства
2. Выбор корневого моста
3. Наблюдение за процессом выбора протоколом STP порта, исходя из стоимости портов
4. Наблюдение за процессом выбора протоколом STP порта, исходя из приоритета портов
5. 
## Создание сети и настройка основных параметров устройства

Настройка базовых параметров коммутатора:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/1_s1_setup.png "Настройка коммутатора S1")

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/2_s2_setup.png  "Настройка коммутатора S2")

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/3_s3_setup.png "Настройка коммутатора S3")

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/4_no_domain_lookup.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/5_log.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/6_vlan_ip_add.png)

Успешно ли выполняется эхо-запрос от коммутатора S1 на коммутатор S2? **Да**

Успешно ли выполняется эхо-запрос от коммутатора S1 на коммутатор S3? **Да**

Успешно ли выполняется эхо-запрос от коммутатора S2 на коммутатор S3? **Да**

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/7_ping_test.png "Проверка связи")

Отключение всех портов на коммутаторах:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/8_ports_shutdown.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/9_ports_shutdown.png)

Настройка всех подключенных портов в качестве транковых:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/10_trunk.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/11_S3.png)



