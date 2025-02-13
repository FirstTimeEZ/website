---
title: Обновления протокола ACME
slug: acme-protocol-updates
lastmod: 2019-10-07
show_lastmod: 1
---


[Стандартизованный IETF](https://letsencrypt.org/2019/03/11/acme-protocol-ietf-standard.html) протокол ACME, [RFC 8555](https://datatracker.ietf.org/doc/rfc8555/) — краеугольный камень в концепции работы Let's Encrypt.

# Конечные точки API

В настоящее время у нас есть следующие конечные точки API. Пожалуйста, ознакомьтесь с [отступлениями от протокола ACME](https://github.com/letsencrypt/boulder/blob/main/docs/acme-divergences.md) для сравнения реализаций.

## ACME v2 (RFC 8555)

* [Production] `https://acme-v02.api.letsencrypt.org/directory`
* [Staging] `https://acme-staging-v02.api.letsencrypt.org/directory`

## ACME v1 (устарел)

* [Production] `https://acme-v01.api.letsencrypt.org/directory`
* [Staging] `https://acme-staging.api.letsencrypt.org/directory`

# Новые возможности протокола ACME, с обратной совместимостью

Время от времени Let's Encrypt внедряет новые функции с обратной совместимостью для существующих конечных точек API. Обычно такие новые функции вводятся, потому что мы решили реализовать часть спецификации ACME, которая ранее не была реализована.

Когда новые функции вводятся в существующие конечные точки API, эти функции всегда будут четко указаны в общедоступной спецификации ACME и не нарушат работу правильно реализованных клиентов.

# Новые версии протокола ACME, без обратной совместимости

Мы не планируем вносить изменения без обратной совместимости в нашу поддержку протокола ACME, но если мы сочтем это важным, мы постараемся обеспечить плавный переход в течение достаточного времени и сообщим об этом заранее. Системные администраторы должны поддерживать возможность своевременного развертывания обновлений для своих клиентов ACME в случае необходимости внесения таких критических изменений.
