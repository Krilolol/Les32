AWS - Ansible

# 1. Створення ролі "baseline" для базових налаштувань серверів.
#### Налаштування SSH-ключів.
#### За допомогою terraform створив два сервери на AWS.
![1](https://github.com/user-attachments/assets/de4fec1a-4964-491c-892f-4d8978307600)


#### В файлі inventory.ini зробив налаштування до цих серверів та за допомогою модуля ping перевірив доступ.
#### Встановлення базових пакетів (vim, git, mc, ufw).
#### За допомогою команди ansible-galaxy init roles/baseline створив відповідну роль та описав порядок встановлення необхідних пакетів в tasks/main.yml.
![2](https://github.com/user-attachments/assets/59b10fbd-98af-4d6d-9b82-ca06a8462439)

# 2. Створення ролі для налаштування firewall.
#### За допомогою команди ansible-galaxy init roles/firewall створив відповідну роль та описав порядок необхідних дій в tasks/main.yml.
![3](https://github.com/user-attachments/assets/4258596e-4bc2-4dbe-8891-3344cb704412)

# 3. Створення ролі для налаштування Nginx.
#### За допомогою команди ansible-galaxy init roles/nginx створив відповідну роль та описав порядок необхідних дій в tasks/main.yml.
#### В templates/ додав 2 файли: index.html.j2 та nginx.conf.j2 (Стартова сторінка та налаштування сервера).
#### В defaults/main.yml додав дві змінні, які вивів на головній сторінці.
![4](https://github.com/user-attachments/assets/3a4a158d-ac5b-453b-b3e0-bd503b937678)
![5](https://github.com/user-attachments/assets/619fb031-9863-48c4-aabc-57096ca4a9d9)
