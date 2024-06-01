---
date: "2024-05-06T14:07:41+03:00"
description: ""
id: ub59dasff5l3it6fsnzgqco
publish: true
title: Elasticsearch
updated: 1716895290893
---

- Размер scroll_id при запросе /scroll может отличаться в зависимости от количества шардов у индекса, его рекомендуется передавать через body, потому что в url params он может просто не поместиться

- Если проблемы с elastic и kibana docker image, можно использовать образы от bitnami