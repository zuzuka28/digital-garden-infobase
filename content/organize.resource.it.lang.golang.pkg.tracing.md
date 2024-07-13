---
date: "2024-05-26T12:16:46+03:00"
description: ""
id: vl3y0b7axfo3ctxnrzttqcj
publish: true
title: Tracing
updated: 1716716732175
---

Интеграция OTEL с net/http - <go.opentelemetry.io/contrib/instrumentation/net/http/otelhttp>.
Тут есть мидлвари и обертки для хэндлеров, чтобы инжектить спаны в запрос.

Sentry с otel - совместить приятное с полезным и использовать sentryotel для всего трейсинга не выйдет.
Спаны не энричатся данными, которые проставляет sentryhttp, в jaeger дополнительная информация не будет отображена.
Нужно поисследовать этот момент, может я где-то накосячил.