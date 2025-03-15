# reminger-tg-bot

# Вокруг PHP – экосистема веб-приложений

## Задание 6. Очереди в PHP

## Команды для выполнения задания

```
sudo apt update
sudo apt install composer
sudo apt install sqlite3
sudo apt-get install php8.2-xml
sudo apt install curl
sudo apt install php-curl
```

### Настройка RabbitMQ и библиотеки для PHP

```
sudo apt install rabbitmq-server
```

📌 Устанавливает сервер сообщений RabbitMQ, который используется для асинхронной обработки задач и обмена сообщениями между микросервисами.

```
sudo rabbitmq-plugins enable rabbitmq_management
```

📌 Включает плагин управления RabbitMQ через веб-интерфейс.

```
composer require php-amqplib/php-amqplib

```

📌 Устанавливает библиотеку php-amqplib, которая реализует протокол AMQP для работы с очередями сообщений в PHP.

### Настройка общей папки в виртуальной машине (VirtualBox)

```

sudo usermod -aG vboxsf user

```

📌 Добавляет пользователя в группу vboxsf, чтобы он имел доступ к общей папке VirtualBox.

### Конфигурация Supervisor для фонового процесса

Создать файл конфигурации для Supervisor:

> /etc/supervisor/conf.d

```

[program:worker]
process*name=%(program_name)s*%(process_num)02d

command=php8.2 /home/reminder-bot/cur/runner -c handle_events_daemon
// Запускает процесс на PHP 8.2, который выполняет обработку событий.

autostart=true
// Процесс запускается автоматически при старте системы.

autorestart=true
// Если процесс падает, Supervisor автоматически перезапускает его.

user=reminder-bot
// Запускает процесс от имени пользователя reminder-bot.

numprocs=1
// Оставляет один экземпляр процесса.

redirect_stderr=true
// Перенаправляет ошибки в стандартный лог-файл.

stdout_logfile=/var/log/worker
// Лог-файл, в который записывается вывод процесса.

```

![hw6_img1](./img/hw6_1.png "hw6_img1")
![hw6_img2](./img/hw6_2.png "hw6_img2")
![hw6_img3](./img/hw6_3.png "hw6_img3")
