---
date: "2024-07-18T13:21:16+03:00"
description: ""
id: j6lzb5pxe6337mfqfcggxc2
publish: true
title: Lsm Tree
updated: 1721298651370
---

Log-Structured Merge-tree - древоподобная структура данных, состоящая из двух структур - хранимого в ram дерева вставки и хранимого на диске долговременного хранилища. При накоплении некоторого количества данных на одном уровне они сливаются, сортируются и перемещаются на уровень ниже.
Зачастую используется несколько уровней.
Операции вставки происходят за *O(1)*, а остальные операции за *O(n)*.

**Оптимальны для операций записи**