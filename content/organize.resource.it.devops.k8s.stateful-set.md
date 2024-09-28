---
date: "2024-09-08T16:29:28+03:00"
description: ""
id: q5i4gw37dcgtxo86n5e3hr5
publish: true
title: Stateful Set
updated: 1725802744142
---

<https://kubernetes.io/docs/concepts/workloads/controllers/statefulset/>

StatefulSets - так же как и [[organize.resource.it.devops.k8s.deployment|deployment]], управляет развертыванием и масштабированием набора подов, но сохраняет набор идентификаторов и состояние для каждого пода, а не генерирует случайный.

В основном используется для организации работы приложений с Persistent хранилищами.
