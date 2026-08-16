# Документация → GitHub Pages

## Включение

1. Залейте папки `docs/` и `.github/workflows/` в репозиторий.
2. **Settings → Pages → Build and deployment → Source: GitHub Actions**.
3. Push в `main` (или **Actions → Deploy docs → Run workflow**).
4. Сайт: `https://<USER>.github.io/<REPO>/`

## Project Pages (репозиторий не `username.github.io`)

В `docs/_config.yml` раскомментируйте и подставьте:

```yaml
baseurl: /ИМЯ_РЕПО
url: https://USER.github.io
```

Иначе CSS темы и ссылки могут «ломаться».

## Локальный просмотр

```bash
# Вариант 1: Docker
docker run --rm -v "$PWD/docs:/srv/jekyll" -p 4000:4000 jekyll/jekyll:4 jekyll serve

# Вариант 2: gem
cd docs && bundle exec jekyll serve
```

## Структура

```
docs/
  _config.yml
  index.md
  architecture.md
  tz-template.md
  data-model.md
  adapter.md
  mapper.md
  schema-ld.md
  howto.md
  ci-cd.md
  implementation.md
```

Workflow: `.github/workflows/docs.yml` (Jekyll build + deploy-pages).
