---
title: Внедрение
permalink: /implementation.html
---

# Чеклист внедрения

## Этап A

- [ ] `lib/` на сервер  
- [ ] Правки template (цена, InStock, LCP)  
- [ ] Пилот 1 серии (РО) через adapter + mapper  

## Этап B

- [ ] ProductSchemaBuilder вместо дублей schema-ld  
- [ ] HowTo на страницах с монтажом  
- [ ] Sitemap моделей  

## Этап C

- [ ] Миграция остальных series  
- [ ] `/data/products/*.json`  
- [ ] CI обязателен для merge в main  

## Критерий готовности товара

Одна запись данных → страница группы, модели, таблица, specs, SEO, JSON-LD, FAQ, sitemap.
