# Публикация на GitHub Pages

Я не могу войти в ваш GitHub или создать удалённый репозиторий из этой сессии: в окружении нет подключённой авторизации GitHub. Не отправляйте пароль или Personal Access Token в чат.

Проект подготовлен для публичного репозитория `aurelion-website`; workflow автоматически развернёт статический сайт через GitHub Pages.

## Однократная настройка

1. На GitHub создайте **Public repository** с именем `aurelion-website`. Не добавляйте туда README, `.gitignore` или лицензию — они уже есть в проекте.
2. Распакуйте `aurelion-website.zip`.
3. В терминале перейдите в распакованную папку и выполните, заменив `YOUR-USERNAME` на ваш GitHub username:

```bash
git init -b main
git add .
git commit -m "Add AURELION website"
git remote add origin https://github.com/YOUR-USERNAME/aurelion-website.git
git push -u origin main
```

Git запросит авторизацию. Используйте вход через браузер/Git Credential Manager или GitHub CLI на своём компьютере; не вставляйте токен в этот файл или чат.

4. В репозитории откройте **Settings → Pages** и выберите **GitHub Actions** как источник публикации.
5. После завершения workflow адрес проекта будет примерно таким: `https://YOUR-USERNAME.github.io/aurelion-website/`.

Файл `.github/workflows/pages.yml` автоматически подставляет фактический Pages URL в Open Graph, canonical и structured metadata. Для действующей компании также замените демонстрационные адрес `concierge@aurelion.example`, телефон и остальные контактные данные на реальные.
