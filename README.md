# Style Guide Project

Учебный Docs as Code проект: руководство по стилю технической документации веб-приложения.

Опубликованная документация: [frizyyu.github.io/style-guide-project](https://frizyyu.github.io/style-guide-project/).

## Назначение

Руководство помогает разработчикам и техническим писателям создавать понятную и единообразную документацию для пользователей и разработчиков.

## Структура

Правила находятся в каталоге `docs`, конфигурация сайта — в `mkdocs.yml`, а ход лабораторной работы описан в `REPORT.md`.

## Требования и установка

Для работы нужны Python 3, Node.js и npm.

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

## Локальный запуск

```powershell
mkdocs serve
```

## Проверки

```powershell
npx --yes markdownlint-cli@0.45.0 "**/*.md" "#site"
mkdocs build --strict
```

Правила участия в проекте приведены в [CONTRIBUTING.md](CONTRIBUTING.md).
