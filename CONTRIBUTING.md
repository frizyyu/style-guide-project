# Участие в проекте

## Как предложить изменение

1. Создайте отдельную ветку от актуальной ветки `main`.
2. Внесите изменение в документацию.
3. Запустите Markdown lint.
4. Проверьте строгую сборку MkDocs.
5. Создайте commit.
6. Отправьте ветку в GitHub.
7. Создайте Pull Request в `main`.

## Conventional Commits

Сообщение коммита должно кратко описывать изменение в формате Conventional Commits. Для документации используйте `docs`, для исправления ошибки — `fix`.

Примеры:

```text
docs: add accessibility rules
docs: clarify heading rules
fix: correct broken link
```

## Процесс review

После создания Pull Request другой участник изучает изменения и оставляет комментарии. Автор вносит исправления, повторяет проверки и создаёт новый commit. После approve изменения можно объединить с `main`.

## Локальная сборка

В PowerShell создайте и активируйте виртуальное окружение, затем установите зависимости:

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
python -m pip install -r requirements.txt
```

Запустите локальный сервер:

```powershell
mkdocs serve
```

Перед отправкой изменений выполните обе проверки:

```powershell
npx --yes markdownlint-cli@0.45.0 "**/*.md" "#site"
mkdocs build --strict
```

## Как добавить новый раздел

1. Создайте Markdown-файл в каталоге `docs`.
2. Напишите содержимое по правилам стайлгайда.
3. Добавьте страницу в `nav` файла `mkdocs.yml`.
4. Запустите Markdown lint.
5. Запустите `mkdocs build --strict`.
6. Создайте commit с понятным сообщением.
