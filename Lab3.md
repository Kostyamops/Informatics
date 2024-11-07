У нас есть 3 виртуальные машины

![image](https://github.com/user-attachments/assets/2c4053f3-7144-4657-a37c-848d1c4f22b8)

Создадим локальную nat сеть, с маской 10.0.2.0/24 и обозначим машины:
10.0.2.4 - машина А
10.0.2.5 - машина Б
10.0.2.15 - машина В

Для начала убедимся, что с машины А есть доступ в интернет:

![image](https://github.com/user-attachments/assets/40290402-212f-4e07-b4e0-fd7e563e0918)

Теперь проверим, видит ли она машины Б и В

![image](https://github.com/user-attachments/assets/19cc3413-16bd-466b-aa3d-1abbb6eb224d)

Аналогичную картину мы наблюдаем на машинах Б и В. Блокировать соединение внутри локальной сети мы будем через iptables.
Для этого пропишем на машине Б команду:
"iptables -A INPUT -s 10.0.2.15 -j REJECT"
Теперь попробуем подключиться с нее к машине А, а затем к машине В:

![image](https://github.com/user-attachments/assets/f817ccd1-4bb8-4a89-bc1b-07db27d8add0)

![image](https://github.com/user-attachments/assets/583ed9ea-9792-424c-a257-c532eb3de0b0)

Как мы видим, мы успешно заблокировали соединение из машины Б к машине В, при этом оставив связь с машиной А.
Проверим подключение на машине В:

![image](https://github.com/user-attachments/assets/d327e776-ae26-42d4-b8ca-da78adf53d92)

![image](https://github.com/user-attachments/assets/234435e2-6b85-433a-9f4a-3a920f744351)

Из скриншотов следует, что машина В имеет доступ к машине А, но не имеет доступ к машине Б.
Проверим машину А, имеет ли она доступ к 2 другим машинам?

![image](https://github.com/user-attachments/assets/37083d2e-6f8d-4a08-b57c-8bb2aaeee1c5)

![image](https://github.com/user-attachments/assets/bcb7de4c-0dc2-42c6-a23b-60666046bebf)

Да, все настроено правильно! При желании разрешить доступ к машине Б для В, можно ввести команду:
"iptables -A INPUT -s 10.0.2.15 -j ACCEPT"
или же сбросить все настройки iptables:
"iptables -F"
