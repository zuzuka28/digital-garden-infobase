---
date: "2024-09-08T16:37:29+03:00"
description: ""
id: rwzy1tlhacb0jj0wgqyti57
publish: true
title: Job
updated: 1725803282743
---

<https://kubernetes.io/docs/concepts/workloads/controllers/job/>

Job создает определенное количество [[organize.resource.it.devops.k8s.pod|pod]] и смотрит, пока они успешно не завершат работу. 
Если под завершился с ошибкой, то пересоздает его до тех пор, пока он не завершится успешно, либо пока не достигнет лимита по попыткам.
Если под успешно отработал, записывает это журнал.