---
date: "2024-07-01T12:39:07+03:00"
description: ""
id: xdvevj3r5gxo54gvfjnv2dy
publish: true
title: Golang Concurrency
updated: 1725183134435
---

- [ ] Векторизация
- [ ] Pipeline процессора
- [ ] Устройство процессора и шина


Кэши процессора

- [x] когерентность кэша (MESI)
- [x] false sharing
- [x] store bufer
- [ ] invalidation queue


Виртуальная память

- [ ] MMU
- [ ] TLB
- [ ] swapping


Алгоритмы планирования

- [ ] FCFS (First Come First Serve)
- [ ] SJN (Shortest Job Next)
- [ ] RR (Round Robin)
- [ ] приоритетное планирование
- [ ] многоуровневая очередь


- [x] Кооперативная и вытесняющая многозадачность
- [x] Процессы и потоки
- [x] Context switching
- [x] Hyper-threading
- [/] Сопрограммы – stackfull, stackless

Внутреннее устройство горутины

- [ ] контекст и состояние горутины
- [ ] расширение стэка (contiguous и segmented)


Внутреннее устройство планировщика Go

- [ ] sysmon
- [ ] netpoller
- [ ] LRQ и GRQ
- [ ] asynchronous preemption
- [ ] work sharing и work stealing
- [ ] внутреннее устройство очередей

Примитивы синхронизации

- [ ] sync.WaitGroup
- [ ] sync.Mutex
- [ ] sync.Once


Проблемы конкурентного программирования

- [x] deadlock
- [x] livelock
- [x] data race
- [x] starvation
- [ ] инверсия приоритетов


- [ ] Внутреннее устройство mutex
- [ ] Go race detector
- [ ] Диаграммы Холта

Примитивы синхронизации

- [ ] sync.RWMutex
- [ ] sync.Map
- [ ] sync.Cond
- [ ] sync.Pool
- [ ] sync.atomic (CAS паттерны)


Дополнительные примитивы синхронизации

- [x] spin lock
    - [[organize.resource.it.os.mutex|mutex]]
- [x] ticket lock
    - [[organize.resource.it.os.mutex|mutex]]
- [ ] recursive mutex
- [ ] timed mutex
- [ ] rw mutex
- [ ] once


- [ ] Cache contention
- [ ] Spurious wakeup

Каналы

- [x] Однонаправленные каналы
- [x] Внутреннее устройство каналов
- [x] Буферизованные и небуферизованные каналы
- [x] Share memory by communicating
- [x] Producer and consumer
- [ ] Gracefull Shutdown
- [x] Утечки горутин

Паттерны использования каналов

- [ ] Pipeline
- [ ] Bridge
- [ ] Generator
- [ ] Error group
- [ ] Transformer
- [ ] Promise и Future
- [ ] Fan-In, Fan-Out и Tee
- [ ] Done channel
- [ ] Or-done channel
- [ ] Or channel
- [ ] Moving later
- [ ] Работа со временем
- [ ] Gracefull shutdown на каналах
- [ ] Дополнительные примитивы синхронизации – semaphore и barrier

Контексты

- [ ] TODO
- [ ] Background
- [ ] WithCancel
- [ ] WithCancelCause
- [ ] WithDeadline
- [ ] WithTimeout
- [ ] WithValue


- [ ] Внутреннее устройство контекстов
- [ ] Gracefull shutdown на контекстах
- [ ] Memory reordering


Барьеры памяти

- [ ] полный барьер
- [ ] барьер чтения
- [ ] барьер записи
- [ ] acquire барьер
- [ ] release барьер

Lock-free и алгоритмы синхронизации

- [ ] Шардирование структур данных
- [ ] RCU (Read Copy Update)


Алгоритмы синхронизации

- [ ] грубая
- [ ] тонкая
- [ ] оптимистичная
- [ ] неблокирующая


Lock-free структуры данных

- [ ] Стэк Трайбера
- [ ] Очередь Майкла и Скотта


ABA проблема

- [ ] hazard pointers
- [ ] tagged pointers

Архитектура web-серверов

- [ ] синхронный web-сервер
- [ ] асинхронный web-сервер


Изоляция транзакций в базах данных

- [ ] 2PL подход
- [ ] MVCC подход
- [ ] сериализуемость


- [ ] Event loop
- [ ] Закон Амдала
- [ ] Акторная модель