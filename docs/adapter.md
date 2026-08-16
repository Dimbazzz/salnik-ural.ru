---
title: Адаптер
permalink: /adapter.html
---

# Адаптер legacy (param1 → semantic)

```php
$adapter = new ProductDataAdapter($mappings['rybozaschitnyy-ogolovok']);
$product = $adapter->adaptSeries($seriesMeta, $oldData);
```

## param_map (РО)

| Legacy | Semantic | Unit |
|--------|----------|------|
| param1 | dn | — |
| param2 | diameter | мм |
| param3 | flow | м³/ч |
| mass | weight | кг |

Масса обрабатывается **WeightMapper**: `"188 кг"`, `"0,188 т"`, `"5000 г"` → кг.

Файлы: `ProductDataAdapter.php`, `WeightMapper.php`, `adapter-mappings.php`.
