---
title: HowTo
permalink: /howto.html
---

# HowToBuilder

Шаги монтажа: JSON-LD + видимый HTML.

```php
$howto = HowToBuilder::fromProduct($product, [
  'canonical' => $canonical_url,
  'site_url' => 'https://salnik-ural.ru',
]);
echo $howto->renderJsonLd();
echo $howto->renderHtml();
```

Поля product: `installation_steps`, `howto_tools`, `howto_supplies`, `howto_total_time` (`1h 30m` → `PT1H30M`).

Legacy: `HowToBuilder::fromLegacy(getHowToData($page), …)`.
