---
title: Архитектура
permalink: /architecture.html
---

# Архитектура

## Слои

```
prices-*.php / JSON
        ↓
ProductDataAdapter + WeightMapper   (legacy)
        ↓
PRODUCT MODEL (product.schema.json)
        ↓
┌───────────────┼────────────────┐
▼               ▼                ▼
productToTemplateVars   ProductSchemaBuilder   HowToBuilder
▼               ▼                ▼
template-product.php    JSON-LD @graph         HTML шагов
```

## URL

| Тип | Пример |
|-----|--------|
| Каталог | `/proizvodstvo/` |
| Группа | `/proizvodstvo/rybozaschitnyy-ogolovok/` |
| Модель | `/proizvodstvo/rybozaschitnyy-ogolovok-tm-ro-500/` |

ЧПУ через `.htaccess` → `{slug}.php` / `{slug}-dynamic.php?model=`.  
**Whitelist** `model` по `variants[].id`, иначе 404.

## Принцип

Один параметр (например масса) не дублируется вручную в prices, meta, schema и HTML.  
Единый источник → Product Model → все потребители.

Подробнее: Единое ТЗ v2.1 в комплекте репозитория.
