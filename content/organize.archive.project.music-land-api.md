---
date: "2024-05-06T12:50:40+03:00"
description: |
  проект API типа Spotify
id: qpwbs0ld1pcicsy11vmsqal
publish: true
title: Music Land API
updated: 1717253103908
---

## Цель

Создать API для стриминга музыки, см. Spotify

Получить срез навыка написания API с использованием [[organize.resource.it.lang.golang|Golang]]

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
09.05.2024 - Фича плейлистов
11.05.2024 - Фича лайков

## Результат

- [x] Рабочее приложение, готовое к деплою
- [ ] Пояснительная записка к проекту

## Задачи

- [x] API для сохранения/удаления/поиска треков
- [x] Авторизация пользователей
- [x] Обзор - трейсинг и логирование
- [x] Контейнеризация
- [x] Плейлисты
- [x] Лайки
- [-] Websocket стриминг
  - для этого лучше выделить отдельный проект. слишком много всего для простенького REST API
- [x] Access Controll - решить, какая часть приложения управляет доступом. Фичи плейлистов и лайков требуют доступа от конкретных пользователей, нельзя ставить лайки за другого человека.

## Заметки

В качестве базы данных выбрана [[organize.resource.it.db.postgre|PostgreSQL]] с [[organize.resource.it.orm|ORM]] коннектором [[organize.resource.it.lang.golang.pkg.xorm|xorm]]

Для хранения файлов выбрано объектное хранилище [[organize.resource.it.object-storage.minio|Minio]] с клиентом [[organize.resource.it.lang.golang.pkg.minio|Minio]] и поддержкой [[organize.resource.it.object-storage.s3|S3]]

Репозиторий тут - <https://github.com/zuzuka28/music_land_api>

## Обзор

Большую часть фич, которые хотел сделать - сделал.

Приложение готово к использованию по описанным юзкейсам. 
Документацию нужно еще написать - добавлять swagger пока нет времени, нужно будет переписать почти весь уровень контроллера, чтобы сделать доку. Сейчас нет времени реализовывать это.

Следующий раз, когда буду писать API в качестве проекта - начну с документации, чтобы в проекте все было описано четким контрактом.

Во время реализации проекта понял, что Websocket нужно разобрать отдельно. 
Нужно будет изучить специфику работы веб плееров, особенно момент с чтением произвольного места в файле (треке). 
