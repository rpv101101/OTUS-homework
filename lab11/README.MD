# Настройка и проверка расширенных списков контроля доступа
## Топология

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/TOP.png)

## Таблица адресации
![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/TA.png)

## Таблица VLAN
![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/VLAN.png)

## Задачи
### Часть 1. Создание сети и настройка основных параметров устройства

### Часть 2. Настройка и проверка списков расширенного контроля доступа

## Создание сети и настройка основных параметров устройства
### Создание сети согласно топологии

> Подключите устройства, как показано в топологии, и подсоедините необходимые кабели.

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/PC-A_1.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/PC-A_2.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/PC-B_1.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/PC-B_2.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/scheme.png)

### Базовая настройка маршрутизаторов
>Откройте окно конфигурации
>
>a. Назначьте маршрутизатору имя устройства.
>
>b.	Отключите поиск DNS, чтобы предотвратить попытки маршрутизатора неверно преобразовывать введенные команды таким образом, как будто они являются именами узлов.
>
>c.	Назначьте class в качестве зашифрованного пароля привилегированного режима EXEC.
>
>d.	Назначьте cisco в качестве пароля консоли и включите вход в систему по паролю.
>
>e.	Назначьте cisco в качестве пароля VTY и включите вход в систему по паролю.
>
>f.	Зашифруйте открытые пароли.
>
>g.	Создайте баннер с предупреждением о запрете несанкционированного доступа к устройству.
>
>h.	Сохраните текущую конфигурацию в файл загрузочной конфигурации.


![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/R1_setup.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/R2_setup.png)

### Базовая настройка коммутаторов
>a.	Присвойте коммутатору имя устройства.
>
>b.	Отключите поиск DNS, чтобы предотвратить попытки маршрутизатора неверно преобразовывать введенные команды таким образом, как будто они являются именами узлов.
>
>c.	Назначьте class в качестве зашифрованного пароля привилегированного режима EXEC.
>
>d.	Назначьте cisco в качестве пароля консоли и включите вход в систему по паролю.
>
>e.	Назначьте cisco в качестве пароля VTY и включите вход в систему по паролю.
>
>f.	Зашифруйте открытые пароли.
>
>g.	Создайте баннер с предупреждением о запрете несанкционированного доступа к устройству.
>
>h.	Сохраните текущую конфигурацию в файл загрузочной конфигурации.
>

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/S1_setup.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/S2_setup.png)

## Настройка сетей VLAN на коммутаторах
### Создание сети VLAN на коммутаторах
>a.	Создайте необходимые VLAN и назовите их на каждом коммутаторе из приведенной выше таблицы.
>
>b.	Настройте интерфейс управления и шлюз по умолчанию на каждом коммутаторе, используя информацию об IP-адресе в таблице адресации. 
>
>c.	Назначьте все неиспользуемые порты коммутатора VLAN Parking Lot, настройте их для статического режима доступа и административно деактивируйте их. 
>Примечание. Команда interface range полезна для выполнения этой задачи с помощью необходимого количества команд. 

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/S1_VLAN.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/S2_VLAN.png)

### Назначение сети VLAN соответствующим интерфейсам коммутатора
>a.	Назначьте используемые порты соответствующей VLAN (указанной в таблице VLAN выше) и настройте их для режима статического доступа.
>
>b.	Выполните команду show vlan brief, чтобы убедиться, что сети VLAN назначены правильным интерфейсам.

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/S1_VLAN_c.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/S2_VLAN_c.png)

### Настройка транков (магистральных каналов)
#### Ручная настройка магистрального интерфейса f0/1
>a.	Измените режим порта коммутатора на интерфейсе F0/1, чтобы принудительно создать магистральную связь. Не забудьте сделать это на обоих коммутаторах.
>
>b.	В рамках конфигурации транка установите для native vlan значение 1000 на обоих коммутаторах. При настройке двух интерфейсов для разных собственных VLAN сообщения 
>об ошибках могут отображаться временно.
>
>c.	В качестве другой части конфигурации транка укажите, что VLAN 10, 20, 30 и 1000 разрешены в транке.
>
>d.	Выполните команду show interfaces trunk для проверки портов магистрали, собственной VLAN и разрешенных VLAN через магистраль.

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/S2_tr_setup1.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/S2_tr_setup.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/S2_sh_tr.png)

#### Ручная настройка магистрального интерфейса f0/5 на комммутаторе S1
>a.	Настройте интерфейс S1 F0/5 с теми же параметрами транка, что и F0/1. Это транк до маршрутизатора.
>
>b.	Сохраните текущую конфигурацию в файл загрузочной конфигурации.
>
>c.	Используйте команду show interfaces trunk для проверки настроек транка.

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/S1_tr.png)

### Настройка маршрутизации
#### Настройка маршрутизации между сетями VLAN на R1
>a.	Активируйте интерфейс G0/0/1 на маршрутизаторе.
>
>b.	Настройте подинтерфейсы для каждой VLAN, как указано в таблице IP-адресации. Все подинтерфейсы используют инкапсуляцию 802.1Q. Убедитесь, что подинтерфейс для собственной VLAN не имеет назначенного IP-адреса. Включите описание для каждого подинтерфейса.
>
>c.	Настройте интерфейс Loopback 1 на R1 с адресацией из приведенной выше таблицы.
>
>d.	С помощью команды show ip interface brief проверьте конфигурацию подынтерфейса.

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/R1_G0.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/R1_1.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/R1_2.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/R1_3.png)

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/R1_4.png)

#### Настройка интерфейса R2 g0/0/1 с использованием адреса из таблицы и маршрута по умолчанию с адресом следующего перехода 10.20.0.1

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/R2_1.png)

### Настройка удаленного доступа
#### Настройка все сетевых устройств для базовой поддержки SSH
>a.	Создайте локального пользователя с именем пользователя SSHadmin и зашифрованным паролем $cisco123!
>
>b.	Используйте ccna-lab.com в качестве доменного имени.
>
>c.	Генерируйте криптоключи с помощью 1024 битного модуля.
>
>d.	Настройте первые пять линий VTY на каждом устройстве, чтобы поддерживать только SSH-соединения и с локальной аутентификацией.

![alt-text](https://raw.githubusercontent.com/rpv101101/OTUS-homework/main/lab11/IMG/R1_vty.png)


