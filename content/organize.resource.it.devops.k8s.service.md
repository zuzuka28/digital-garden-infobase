---
date: "2024-06-25T13:59:10+03:00"
description: ""
id: zud5itm45ijvxj7won7nvqq
publish: true
title: Service
updated: 1719316104511
---

<https://kubernetes.io/docs/concepts/services-networking/service/>

Сервисы - способ предоставить доступ к сети для подов в кластере.

```yaml
kind: Service
apiVersion: v1
metadata:
  name: service-name
spec:
  selector:
    app: my-pod-selector # селектор подов для которых работает сервис
  ports:
    - protocol: TCP
      port: 80 # порт, на который будут прилетать коннекты извне
      targetPort: 8080 # порт внутри пода, на который будут переноситься коннекты
```