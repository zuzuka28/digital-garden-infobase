---
date: "2024-05-05T18:32:21+03:00"
description: |
  генерация уникальных ключей без коллизий в приложении
id: n34013f2h8dle8s5dhjtiz4
publish: true
title: Uniqkey
updated: 1714983375675
---

Генерация уникальных ключей.
Хоть передача невидимых параметров нежелательна, иногда приходится прибегать к ней.

Данный код можно использовать для генерации ключей, которые можно использовать вместе с context.Context и map.

```go
var lastID int32 = 1

// DataKey used to maintain the uniqueness of properties between different packages.
type DataKey struct{ id int32 }

func (d DataKey) String() string {
	return strconv.Itoa(int(d.id))
}

// Gen generates new unique key for property.
func Gen() DataKey { return DataKey{id: atomic.AddInt32(&lastID, 1)} }
```
