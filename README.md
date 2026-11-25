# githab-books — Учебник по GitHub

Полноценный учебник по работе с **GitHub и всеми его инструментами**, свёрстанный в виде HTML-страницы.

## О чём учебник

30 разделов: от регистрации и основ Git до CI/CD и Open Source:

- Репозитории, ветки, коммиты, конфликты слияния
- Pull Requests, **code review и CODEOWNERS**
- Issues, Projects, Wiki, Discussions
- **GitHub Actions** (включая кэш, environments и self-hosted раннеры) и **GitHub Pages**
- Releases, **GitHub Packages**, безопасность (Dependabot, secret scanning)
- Codespaces, Copilot, GitHub CLI, Desktop
- **Продвинутый Git**: cherry-pick, bisect, stash, worktree, reflog, submodules
- **Open Source**: как сделать первый вклад
- Профиль и организации, Markdown (GFM), API и Webhooks
- Шпаргалка команд и глоссарий

## Возможности страницы

- 🅰 **Регулировка размера шрифта** — кнопки A− / A / A+ в шапке (5 ступеней, выбор сохраняется)
- 🌓 Тёмная и светлая темы
- 🔍 Живой поиск по разделам (`Ctrl+K` или `/`)
- ⌨️ Горячие клавиши: `J`/`K` — следующий/предыдущий раздел
- 📍 Чип текущего раздела, прогресс чтения, scrollspy-меню
- 📖 Плашка «Продолжить чтение» — вернёт вас к месту, где вы остановились
- 🗂 Сгруппированное меню, якорные ссылки на разделы
- 📱 Адаптивная вёрстка для мобильных

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

Если захотите читать учебник онлайн: **Settings → Pages → Build and deployment → Source: «GitHub Actions»**, после чего добавьте в workflow джобу деплоя (`actions/configure-pages` + `actions/upload-pages-artifact` + `actions/deploy-pages`) — готовый пример есть в разделе 15 учебника.
