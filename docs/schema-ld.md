---
title: JSON-LD
permalink: /schema-ld.html
---

# ProductSchemaBuilder

Один `@graph`:

- Organization, WebPage, Product (+ PropertyValue)
- Offer — **только** fixed + число
- BreadcrumbList, FAQPage, HowTo

**Запрещено:** фиктивные цены, InStock при «по запросу», фейковые Review.

```php
echo (new ProductSchemaBuilder([
  'site_url' => 'https://salnik-ural.ru',
  'site_name' => 'Сальник-Урал',
]))->renderAll($product, $variant, [
  'canonical' => $canonical_url,
  'include_faq' => true,
  'include_howto' => true,
]);
```

Проверка: [Rich Results Test](https://search.google.com/test/rich-results).
