# githab-books — Учебник по GitHub

Полноценный учебник по работе с **GitHub и всеми его инструментами**, свёрстанный в виде HTML-страницы.

🔗 **Читать онлайн:** https://zigorminsk-debug.github.io/githab-books/

## О чём учебник

25 разделов: от регистрации и основ Git до CI/CD:

- Репозитории, ветки, коммиты, конфликты слияния
- Pull Requests и code review
- Issues, Projects, Wiki, Discussions
- **GitHub Actions** (CI/CD) и **GitHub Pages** (хостинг)
- Codespaces, Copilot, GitHub CLI, Desktop
- Безопасность (Dependabot, secret scanning), API, Webhooks
- Шпаргалка команд и глоссарий

## Сборка и деплой

Сайт публикуется автоматически средствами **GitHub Actions** при каждом изменении:

- **push в `main`** → сборка + деплой на GitHub Pages
- **pull request в `main`** → проверка сборки (без деплоя)

Workflow: [`.github/workflows/deploy.yml`](.github/workflows/deploy.yml)

## Локальный запуск

Статика без зависимостей — просто откройте `index.html` в браузере:

```bash
python3 -m http.server 8000
# http://localhost:8000
```
