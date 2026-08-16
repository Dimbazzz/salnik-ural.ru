---
title: CI/CD
permalink: /ci-cd.html
---

# CI/CD

## CI (GitHub Actions)

- `php -l` на lib/*.php  
- Запуск example-*.php  
- Валидация структуры product JSON  
- Запрет `display_errors=1` в template на main  

## CD

- Deploy с `main` через rsync/SSH  
- Не выкладывать `example-*.php` и tests в web-root  
- Сброс opcache / файлового кэша модели  

## GitHub Pages (эта документация)

Workflow: `.github/workflows/docs.yml`  
Источник: папка `/docs`  
URL: `https://<user>.github.io/<repo>/` (project pages)  
или `https://<user>.github.io/` (user pages)
