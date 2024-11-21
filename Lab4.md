Для начала пропишем Dockerfile, соотвествующий требованиям задания:

![image](https://github.com/user-attachments/assets/de6ecffd-7f13-4b91-b965-1d6468f5dd07)

Теперь нам понадобится скомпилировать 2 докер контейнера mycontainer1 и mycontainer2:

![image](https://github.com/user-attachments/assets/51f7a4a0-0705-4278-9b9f-77229c17a17e)

Запустим в них aafire:

![image](https://github.com/user-attachments/assets/8b0f2964-7e02-45e3-a1aa-ae35ac630bfb)

После этого, создадим общую сеть для 2 контейнеров:

![image](https://github.com/user-attachments/assets/1c1178ac-1d64-409d-8225-4dc30cad4e8f)

Теперь в отдельных терминалах запустим каждый из контейнеров:

![image](https://github.com/user-attachments/assets/c0ce7f75-3374-4658-81f6-8ffe6faaa572)

![image](https://github.com/user-attachments/assets/0860333b-ce59-4ae4-8b0b-1110587ea4aa)

Затем проверим подключение между контейнерами с помощью команды ping:

![image](https://github.com/user-attachments/assets/ba0a7b3d-bf6c-4f5e-92f6-9921651a4026)

Успешно. Задачи поставленные в лабораторной работе выполнены.
