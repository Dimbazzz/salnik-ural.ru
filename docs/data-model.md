---
title: Модель данных
permalink: /data-model.html
---

# Модель данных

Контракт: **`product.schema.json`** (JSON Schema draft 2020-12).

## Spec

```json
{
  "value": 188,
  "unit": "кг",
  "label": "Масса",
  "status": "verified",
  "source": "Паспорт изделия",
  "source_type": "passport"
}
```

| status | Отображение |
|--------|-------------|
| verified | `188 кг` |
| calculated | `188 кг (расчётная)` |
| estimated | `188 кг (оценка)` |
| not_available | `уточняется` |

## Pricing

- `fixed` + число → цена и Offer  
- `formula` → не как паспортная цена на витрине  
- `request` → «по запросу», без Offer  

## Эталон

`example-product-ro.json` — серия рыбозащитных оголовков РО.
