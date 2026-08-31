---
key: PIER-9
title: Ключ идемпотентности в схеме БД
type: Подзадача
status: Готово
status_category: done
priority: высокий
estimate: 2
assignee: oleg
sprint: "[[Спринт 11]]"
labels: ["[[оплата]]"]
created: 2026-07-06T09:00:00Z
updated: 2026-08-31T17:00:00Z
aliases: []
parent: "[[PIER-8 Идемпотентность по ключу операции]]"
---

Таблица `idempotency`, уникальный индекс по `(merchant_id, key)`, чистилка по
`expires_at`.
