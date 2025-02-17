---
date: "2024-06-29T20:13:06+03:00"
description: ""
id: qydtgqubxrefjjywwq5ophm
publish: true
title: Scheduler
updated: 1719826256695
---

<https://www.youtube.com/watch?v=P2Tzdg8n9hw>
<https://www.ardanlabs.com/blog/2018/08/scheduling-in-go-part1.html>
<https://www.ardanlabs.com/blog/2018/08/scheduling-in-go-part2.html>
<https://www.ardanlabs.com/blog/2018/12/scheduling-in-go-part3.html>

- web-service
  - большая IO-Bound нагрузка
    - большая часть времени тратится на ожидание ответа от других вебсервисов и ресурсов, чем на вычислительные операции

- IO
  - Во время IO должен происходить context switching
    - переключение контеста между OS thread дорого
      - планировщик системы снимает регистры одного потока
      - планировщик системы грузит регистры другого потока
    - golang должен сам реализовывать context switching, чтобы не заставлять планировщик OS работать
    - реализация управления горутинами и абстракция от OS thread - главная идея реализации golang scheduler

- Go Scheduler
  - программа, использующая N goroutine, использует M thread
    - в 1 thread исполяется некоторое количество goroutine, управлением которыми занимается go планировщик 
  - кооперативная многозадачность
    - компилятор добавляет пометки в код о том, когда можно переключиться на другую горутину
  -  GMP модель
     - Goroutine (что исполняем)
     - Machine (где исполняем)
       - очередь из goroutine для выполнения
     - Processor (права и ресурсы для исполнения)
       - абстракция над thкread
  - что происходит при Syscall
    - системные вызовы занимают thread, из-за чего он не может обрабатывать goroutine.
    - если системный вызов длится слишком долго, то thread открепляется от исполнения очереди goroutine и для обработки набора goroutine выделяется еще один поток.
  - что происходит при синхронизации между горутинами
    - в golang свои примитивы синхронизации, то есть OS планировщик ничего не знает про golang мьютексы, атомики и тд. примитивы синхронизации в golang действуют на goroutine, а не на OS thread
    - состояния горутин
      - running - goroutine исполняется thread'ом
      - runnable - goroutine стоит в очереди на выполнение связанной с thread
      - waiting - помещенные в очередь из заблокированных goroutine
  - что происходит при CPU-bound нагрузке
    - если горутина работает больше 10мс, то она вытесняется с выполнения 
