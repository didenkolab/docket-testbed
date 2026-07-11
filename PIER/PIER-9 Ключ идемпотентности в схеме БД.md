---
key: PIER-9
title: Ключ идемпотентности в схеме БД
type: Подзадача
status: В работе
status_category: doing
priority: высокий
assignee: oleg
labels: ["[[оплата]]"]
created: 2026-07-06T09:00:00Z
updated: 2026-07-11T12:16:00Z
aliases: []
tags: [area/платежи]
parent: "[[PIER-8 Идемпотентность по ключу операции]]"
---

Таблица `idempotency`, уникальный индекс по `(merchant_id, key)`, чистилка по
`expires_at`.
