---
date: "2024-04-19T12:01:32+03:00"
description: |
  идеи по улучшению работы с dendron
id: jvq5nprug7550v6ltnug6hy
publish: true
title: Dendron Workflow
updated: 1714993659625
---

## Ресурсы

Нашел такое описание workflow для работы с PKM:
#source/link <https://mstempl.netlify.app/post/pkm-websites/>.
Чел использует несколько инструментов для ведения PKM

- Захватывает новые статьи через [[capture.source.app.omnivore|Omnivore]]
- Редактирует в [[capture.source.app.logseq|Logseq]]
- Управление ссылками в [[capture.source.app.nb|nb]]

## Поиск по заметкам

В Cookbook есть такая идея:
#source/link <https://wiki.dendron.so/notes/401c5889-20ae-4b3a-8468-269def4b4865/#analyze-notes-using-elasticsearch>

Идея заключается в том, чтобы использовать экспорт из dendron в JSON и импортировать результат в [[organize.resource.it.db.elasticsearch|Elasticsearch]], чтобы искать по заметкам.

Можно подумать на тему того, что еще можно делать с JSON экспортом и импортом, раз есть такая возможность. Мне кажется это главный момент, за который можно зацепиться при разработке прикладных программ на основе dendron.
