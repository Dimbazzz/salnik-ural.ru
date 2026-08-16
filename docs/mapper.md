---
title: productToTemplateVars
permalink: /mapper.html
---

# Mapper → template-product.php

Мост Product Model → переменные боевого шаблона.

```php
extract(productToTemplateVars($product, $variant, [
  'base_url' => 'https://salnik-ural.ru',
]), EXTR_OVERWRITE);
```

Автосекции: назначение, типоразмеры, specs, конструкция, материалы, монтаж, чертёж, документы, FAQ, КП.

Старые страницы с ручным `$product_sections` не ломаются.
