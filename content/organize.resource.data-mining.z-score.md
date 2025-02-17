---
date: "2024-04-21T22:19:32+03:00"
description: |
  Z-Score - статистическая оценка, показывающая отклонение значения от нормали.
id: h8b8gkqcoftpbd2behpcxdi
publish: true
tags:
- math/statistics
title: Z Score
updated: 1727018506337
---

Z-Score - статистичекая оценка, описывающая отклонение значение от нормали из группы. 

Используется для выявления [[organize.resource.data-mining.outlier|outlier]]

Формула:

$$z = ( x - \mu ) / \sigma$$

- $z$ = Z-score;
- $x$ = the value being evaluated
- $\mu$ = the mean
- $\sigma$ = the standard deviation

О значениях:

- Z-Score = 0 - данные соответствуют среднему
- Z-Score ~ 1 - данные соответствуют отклонению от нормали
- Z-Score < 3 - данные соответствуют правилу трех сигм

О знаке:

- Z-Score - позитивный (+) - отклонение больше среднего значения
- Z-Score - негативный (-) - отклонение меньше среднего значения
