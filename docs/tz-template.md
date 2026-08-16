---
title: ТЗ шаблона
permalink: /tz-template.html
---

# ТЗ шаблона template-product.php v3.1

## Цель

Сохранить боевой UI v3.0, добавить слой данных и безопасную разметку.

## Переменные view (контракт)

- `$product_name`, `$product_price`, `$product_images`
- `$product_features`, `$product_sections`
- `$quick_answer`, `$page_h1`, `$page_lead`
- `$canonical_url`, `$json_ld_product`
- `$product_has_fixed_price`, `$product_price_numeric` (добавлены mapper’ом)

## Обязательные правки v3.0 → v3.1

1. `display_errors` off на production  
2. `itemprop="price"` только при fixed-цене  
3. Не ставить InStock для «по запросу»  
4. LCP-image: `eager` + `fetchpriority="high"`  
5. `target="_blank"` только для внешних/файлов  
6. Не дублировать Product JSON-LD  

## Подключение

```php
extract(productToTemplateVars($product, $variant, [
  'base_url' => 'https://example.com',
]), EXTR_OVERWRITE);

$json_ld_product = (new ProductSchemaBuilder([...]))
  ->renderAll($product, $variant, ['canonical' => $canonical_url]);

require __DIR__ . '/../template-product.php';
```

Полный текст: `ТЗ_ШАБЛОН_template-product_v3.1.md` в архиве комплекта.
