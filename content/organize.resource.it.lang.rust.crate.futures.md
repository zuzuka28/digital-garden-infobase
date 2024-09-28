---
date: "2024-08-03T23:03:49+03:00"
description: ""
id: vdhljx93w7xnxu8art4u93s
publish: true
title: Futures
updated: 1722715703811
---

## Read Stream Into Memory

```rust
use bytes::BytesMut; // подключаемый крейт bytes, содержит утилиты для работы с байтами 
use futures::stream::StreamExt; // подключаемый крейт futures - все для футур, Stream - функционал для обработки стримов

async fn recv_voice(...) -> ... {
    ...
    let mut voice_stream = bot.download_file_stream(voice_file.path.as_str()); // в конкретно данном случае стрим из teloxide

    let mut content = BytesMut::new(); // здесь сохраненный контент из стрима

    while let Some(item) = voice_stream.next().await {
        content.extend_from_slice(&item?)
    }
}
```
