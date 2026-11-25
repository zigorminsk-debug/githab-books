# githab-books — Учебник по GitHub

Полноценный учебник по работе с **GitHub и всеми его инструментами**, свёрстанный в виде HTML-страницы.

## О чём учебник

25 разделов: от регистрации и основ Git до CI/CD:

- Репозитории, ветки, коммиты, конфликты слияния
- Pull Requests и code review
- Issues, Projects, Wiki, Discussions
- **GitHub Actions** (CI/CD) и **GitHub Pages** (хостинг)
- Codespaces, Copilot, GitHub CLI, Desktop
- Безопасность (Dependabot, secret scanning), API, Webhooks
- Шпаргалка команд и глоссарий

## Сборка (GitHub Actions)

Сборка запускается **автоматически сразу после внесения изменений**:

- **push в `main`** → сборка и проверка сайта
- **pull request в `main`** → проверка сборки до слияния

Workflow: [`.github/workflows/ci.yml`](.github/workflows/ci.yml)

Результат каждого запуска — артефакт **`site`** (готовый к публикации сайт), который можно скачать со страницы запуска: **Actions → нужный запуск → Artifacts → site**.

## Локальный запуск

Статика без зависимостей — просто откройте `index.html` в браузере:

```bash
python3 -m http.server 8000
# http://localhost:8000
```

## Публикация на GitHub Pages (опционально)

Если захотите читать учебник онлайн: **Settings → Pages → Build and deployment → Source: «GitHub Actions»**, после чего добавьте в workflow джобу деплоя (`actions/configure-pages` + `actions/upload-pages-artifact` + `actions/deploy-pages`) — готовый пример есть в разделе 13 учебника.
