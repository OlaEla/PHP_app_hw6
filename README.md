# Telegram Reminder Bot с асинхронной обработкой событий

[![PHP](https://img.shields.io/badge/PHP-8.2-777BB4?logo=php)](https://php.net)
[![RabbitMQ](https://img.shields.io/badge/RabbitMQ-3.x-FF6600?logo=rabbitmq)](https://rabbitmq.com)

**Проект находится в папке [`/cur`](./cur)** — это основная директория с исходным кодом.

👉 [Перейти к полной документации и коду](./cur/README.md)

## Кратко о проекте

Telegram-бот для напоминаний с асинхронной обработкой задач через RabbitMQ. Демонстрирует:
- Работу с очередями сообщений (RabbitMQ)
- Паттерны Producer/Consumer
- Демонизацию PHP-воркеров через Supervisor
- Модульное тестирование (PHPUnit)

## Быстрый старт

```bash
cd cur
composer install
# Далее смотрите инструкцию в ./cur/README.md
