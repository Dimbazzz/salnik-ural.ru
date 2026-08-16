---
title: Документация каталога
permalink: /
---

# Промышленный каталог — документация

Рабочая документация по **единой системе динамических страниц** промышленных товаров (PHP + Product Model).

## Быстрый старт

1. [Обзор архитектуры](architecture.html)
2. [ТЗ шаблона template-product](tz-template.html)
3. [Модель данных (schema)](data-model.html)
4. [Адаптер param1 → semantic](adapter.html)
5. [Mapper → переменные шаблона](mapper.html)
6. [JSON-LD / Schema.org](schema-ld.html)
7. [HowTo (монтаж)](howto.html)
8. [CI/CD](ci-cd.html)
9. [Внедрение (чеклист)](implementation.html)

## Комплект файлов

| Файл | Назначение |
|------|------------|
| `product.schema.json` | Контракт Product Model |
| `ProductDataAdapter.php` | Legacy → Model |
| `WeightMapper.php` | Масса / единицы |
| `productToTemplateVars.php` | Model → view |
| `ProductSchemaBuilder.php` | JSON-LD @graph |
| `HowToBuilder.php` | HowTo schema + HTML |
| `template-product.php` | Боевой шаблон (на сервере) |

## Формула системы

```
PRODUCT DATA → VALIDATOR → PRODUCT MODEL
        → HTML (template-product.php)
        → SEO / JSON-LD
        → API / AI / Sitemap
```

## Версии

| Документ | Версия |
|----------|--------|
| Единое ТЗ | 2.1 |
| ТЗ шаблона | 3.1 |

Репозиторий с исходниками и архивом комплекта — в корне проекта (после публикации).
