# Telegram Reminder Bot with Async Queue Processing

[![PHP](https://img.shields.io/badge/PHP-8.2-777BB4?logo=php)](https://php.net)
[![RabbitMQ](https://img.shields.io/badge/RabbitMQ-3.x-FF6600?logo=rabbitmq)](https://rabbitmq.com)

Telegram-бот для управления напоминаниями с асинхронной обработкой задач через RabbitMQ.

## Основные возможности

- Создание и управление напоминаниями через Telegram Bot API
- Асинхронная обработка задач с использованием RabbitMQ
- Архитектура Producer/Consumer для масштабируемой обработки сообщений
- Фоновое выполнение задач через Supervisor
- Покрытие бизнес-логики модульными тестами (PHPUnit)

## Технологии

- PHP 8
- RabbitMQ
- Supervisor
- PHPUnit
- Telegram Bot API

## Реализовано

- Backend-сервис на PHP — асинхронный Telegram-бот для напоминаний
- Интеграция с Telegram Bot API — обработка сообщений и команд
- Архитектура Producer / Consumer на базе RabbitMQ
- Фоновые воркеры для событийно-ориентированной обработки задач
- Управление процессами через Supervisor (демонизация воркеров)
- Тестируемый код — модульные тесты бизнес-логики (PHPUnit)

**Проект находится в папке [`/cur`](./cur)** — это основная директория с исходным кодом.

👉 [Перейти к полной документации и коду](./cur/README.md)

## Быстрый старт

```bash
cd cur
composer install
# Далее смотрите инструкцию в ./cur/README.md
