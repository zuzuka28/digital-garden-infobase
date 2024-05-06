---
date: "2024-05-06T12:50:40+03:00"
description: |
  проект API типа Spotify
id: 2x1hrwzgk44rlzzm71m9ylb
publish: true
title: Music Land API
updated: 1714990847552
---
## Цель

Создать API для стриминга музыки, см. Spotify 

Получить срез навыка написания API с использованием [[organize/resource/it/golang|Golang]]

## Контекст

Данный проект предлагался в качестве курсовой работы.
Требования:

- Проект и описание актуальности сервиса
- API для сохранения/удаления/поиска треков
- Стриминг аудиофайлов
- Авторизация пользователей

## Критерий успеха

Удовлетворение требований из контекста

Документирование проекта

## Лог

05.05.2024 - реализация CRUD для треков и авторизация пользователей через Basic Auth

## Результат

- [ ] Рабочее приложение, готовое к деплою
- [ ] Пояснительная записка к проекту

## Задачи

- [x] API для сохранения/удаления/поиска треков
- [x] Авторизация пользователей
- [ ] Обзор - трейсинг и логирование
- [ ] Контейнеризация
- [ ] Плейлисты
- [ ] Лайки
- [ ] Websocket стриминг
 
## Заметки

В качестве базы данных выбрана [[organize/resource/it/db/postgre|PostgreSQL]] с [[organize/resource/it/orm|ORM]] коннектором [[organize/resource/it/golang/pkg/xorm|xorm]]

Для хранения файлов выбрано объектное хранилище [[organize/resource/it/object-storage/minio|Minio]] с клиентом [[organize/resource/it/golang/pkg/minio|Minio]] и поддержкой [[organize/resource/it/object-storage/s3|S3]]

## Обзор

Репозиторий тут - <https://github.com/zuzuka28/music_land_api>