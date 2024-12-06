## Задание 1
Нам нужно добавить новый скрипт в hooks, чтобы недопускать коммита с файлами формата .txt, в которых отсутствует текст.
Для начала создадим место для скрипта, а затем откроем файл в терминале

![image](https://github.com/user-attachments/assets/43a633c0-8a2b-430a-b95c-b06e9bc45880)

После это напишем код

![image](https://github.com/user-attachments/assets/caf60c6a-48fb-4da8-b3e9-7611ef18ab57)

Теперь сохраним его и закроем (Ctrl + O, Ctrl + X)
Затем добавим его в правило запуска при коммите

![image](https://github.com/user-attachments/assets/53c3a2fb-1f1d-44c2-b8ff-5052806a609e)

А теперь создадим файл test.txt (пустой) и попробуем сделать коммит:

![image](https://github.com/user-attachments/assets/b0eea92c-9cb9-4906-935c-3b9e5acfb407)

## Задание 2
Для начала установим и запустим Git Flow

![image](https://github.com/user-attachments/assets/19aca0d3-d7eb-4207-80e3-a10d3d34c8d5)

Создадим task_management.py, куда впишем наш код

![image](https://github.com/user-attachments/assets/c1af120d-cad3-4d1f-a16c-9cc1d08e9026)

Теперь добавим его в коммит

![image](https://github.com/user-attachments/assets/e9e8ab5b-7a6a-45a4-86d1-08c1a197ac55)

После "завершения" разработки, объединим его с основной веткой

![image](https://github.com/user-attachments/assets/3d6f362b-07bc-44ae-b674-ba43c5bce0d0)

Затем выпустим hotfix

![image](https://github.com/user-attachments/assets/379d2edc-ddbe-4cf4-965e-7773ddc62e93)

А после объединим ветки

![image](https://github.com/user-attachments/assets/0108c71c-f6b1-400b-a7da-81a63bd8f77e)
