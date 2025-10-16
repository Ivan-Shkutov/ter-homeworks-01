## Домашнее задание к занятию «Введение в Terraform»

### Цели задания

- Установить и настроить Terrafrom.

- Научиться использовать готовый код.

- Чек-лист готовности к домашнему заданию

- Скачайте и установите Terraform версии >=1.8.4 . Приложите скриншот вывода команды terraform --version.

- Скачайте на свой ПК этот git-репозиторий. Исходный код для выполнения задания расположен в директории 01/src.

- Убедитесь, что в вашей ОС установлен docker.

- Инструменты и дополнительные материалы, которые пригодятся для выполнения задания

- Репозиторий с ссылкой на зеркало для установки и настройки Terraform: ссылка.

- Установка docker: ссылка.

Внимание!! Обязательно предоставляем на проверку получившийся код в виде ссылки на ваш github-репозиторий!

### Задание 1

1. Перейдите в каталог src. Скачайте все необходимые зависимости, использованные в проекте.

2. Изучите файл .gitignore. В каком terraform-файле, согласно этому .gitignore, допустимо сохранить личную, секретную информацию?(логины,пароли,ключи,токены итд)

3. Выполните код проекта. Найдите в state-файле секретное содержимое созданного ресурса random_password, пришлите в качестве ответа конкретный ключ и его значение.

4. Раскомментируйте блок кода, примерно расположенный на строчках 29–42 файла main.tf. Выполните команду terraform validate. Объясните, в чём заключаются намеренно допущенные 
ошибки. Исправьте их.

5. Выполните код. В качестве ответа приложите: исправленный фрагмент кода и вывод команды docker ps.

6. Замените имя docker-контейнера в блоке кода на hello_world. Не перепутайте имя контейнера и имя образа. Мы всё ещё продолжаем использовать name = "nginx:latest". Выполните 
команду terraform apply -auto-approve. Объясните своими словами, в чём может быть опасность применения ключа -auto-approve. Догадайтесь или нагуглите зачем может пригодиться 
данный ключ? В качестве ответа дополнительно приложите вывод команды docker ps.

7. Уничтожьте созданные ресурсы с помощью terraform. Убедитесь, что все ресурсы удалены. Приложите содержимое файла terraform.tfstate.

8. Объясните, почему при этом не был удалён docker-образ nginx:latest. Ответ ОБЯЗАТЕЛЬНО НАЙДИТЕ В ПРЕДОСТАВЛЕННОМ КОДЕ, а затем ОБЯЗАТЕЛЬНО ПОДКРЕПИТЕ строчкой из документации 
terraform провайдера docker. (ищите в классификаторе resource docker_image )

### Решение

1. Скачиваем и устанавливаем Terraform на VM Ubuntu. Проверяем версию terrfotm --version.

2. В файле personal.auto.tfvars допустимо сохранить личную, секретную информацию?(логины,пароли,ключи,токены итд).

3. Выполняем код проекта. После выполнения в файле terraform.tfstate находим секретное содержимое созданного ресурса random_password.

4. Выполняем terrafrom validate и появляются ошибки. Исправляем ошибки в файле main.tf и снова запускаем terrafrom validate.

5. Выполняем terrafrom plan и видим, что все прошло без ошибок.

6. docker ps. Далее меняем имя контейнера на hello_world.

7. Выполняем terraform apply -auto-approvе. Чтобы уничтожить созданные ресурсы выполняем terraform destroy.

8. Если в файле конфигурации есть параметр keep_locally – true, то образ не удалится. Необходимо заменить на false.


   
![1](https://github.com/Ivan-Shkutov/ter-homeworks-01/blob/main/img/1.png)

![2](https://github.com/Ivan-Shkutov/ter-homeworks-01/blob/main/img/2.png)

![3](https://github.com/Ivan-Shkutov/ter-homeworks-01/blob/main/img/3.png)

![4](https://github.com/Ivan-Shkutov/ter-homeworks-01/blob/main/img/4.png)

![5](https://github.com/Ivan-Shkutov/ter-homeworks-01/blob/main/img/5.png)

![6](https://github.com/Ivan-Shkutov/ter-homeworks-01/blob/main/img/6.png)

![7](https://github.com/Ivan-Shkutov/ter-homeworks-01/blob/main/img/7.png)

![8](https://github.com/Ivan-Shkutov/ter-homeworks-01/blob/main/img/8.png)

![9](https://github.com/Ivan-Shkutov/ter-homeworks-01/blob/main/img/9.png)

![10](https://github.com/Ivan-Shkutov/ter-homeworks-01/blob/main/img/10.png)

![11](https://github.com/Ivan-Shkutov/ter-homeworks-01/blob/main/img/11.png)

![12](https://github.com/Ivan-Shkutov/ter-homeworks-01/blob/main/img/12.png)

