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

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/12_s3.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/13_S1_S.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/14_S2_S.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/15_S3_S.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/16_S3_ROOT.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/17_cost_reduced.png)

Какой коммутатор является корневым мостом? 

**S3;**

Почему этот коммутатор был выбран протоколом spanning-tree в качестве корневого моста?

**У этого коммутатора самый низкий Bridge ID (Приоритет + Vlan +  MAC-адрес);**

Какие порты на коммутаторе являются корневыми портами?

**S1 Fa0/4; S2 Fa0/2;**

Какие порты на коммутаторе являются назначенными портами? 

**S1 Fa0/2; S3 Fa0/2; S3 Fa0/4;**

Какой порт отображается в качестве альтернативного и в настоящее время заблокирован? 

**S2 Fa0/2;**

Почему протокол spanning-tree выбрал этот порт в качестве невыделенного (заблокированного) порта?

**Если коммутатор имеет несколько путей равной стоимости к корневому мосту, коммутатор определяет порт, используя самое низкое значение идентификатора моста-отправителя**

## Наблюдение за процессом выбора протоколом STP порта, исходя из приоритета портов

Включите порты F0/1 и F0/3 на всех коммутаторах:

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/1_S1_1-4.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/2_S2_1-4.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/3_S3_1-4.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/4_S1.png)

![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/5_S1.png)

Какой порт выбран протоколом STP в качестве порта корневого моста на каждом коммутаторе некорневого моста? 

**S1 – FA0/3; S2 – FA0/3**

Почему протокол STP выбрал эти порты в качестве портов корневого моста на этих коммутаторах?

**Так как приоритет одинаковый (128), то выбирается порт с наименьшим значением, в нашем случае это порты S1 – FA0/3; S2 – FA0/3.**


![alt text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab7/IMG/final_scheme.png)

## Вопросы для повторения
1.	Какое значение протокол STP использует первым после выбора корневого моста, чтобы определить выбор порта?

**Стоимость пути (выбирается путь с наименьшей стоимостью).**

2.	Если первое значение на двух портах одинаково, какое следующее значение будет использовать протокол STP при выборе порта?

**Наименьший Bridge ID (BID).**

3.	Если оба значения на двух портах равны, каким будет следующее значение, которое использует протокол STP при выборе порта?
	
**Зависит от приоритета порта и его номера (приоритетны наименьшие значения).**
