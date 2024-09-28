---
date: "2024-09-22T21:18:56+03:00"
description: ""
id: kuv84g9u6j6iweyxyr5r0x5
publish: true
title: Coefficient of Determination
updated: 1727029870038
---

Coefficient of Determination $$R^2$$ - число от 0 до 1, которое показывает, насколько хорошо модель предсказывает значения.

Интерпритация

0 - модель не предсказывает значения
0-1 - модель предсказывает значения (больше - лучше)
1 - модель идеально предсказывает значения

$$R^2 = 1 - \frac{RSS}{TSS}$$

- ![[organize.resource.data-mining.rss|rss]]
- ![[organize.resource.data-mining.tss|tss]]

## Матричная форма

$$R^2 = 1 - \frac{(Y-\hat{Y})^T(Y-\hat{Y})}{(Y-\bar{Y})^T(Y-\bar{Y})}$$
