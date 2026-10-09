# Практична робота: Git і GitHub

**Мета:** навчитися створювати репозиторії Git, робити коміти, створювати й об'єднувати гілки, розв'язувати конфлікти та публікувати проєкт на GitHub.

## Основні команди

| Команда | Призначення |
| --- | --- |
| `git init -b main` | Ініціалізація репозиторію з головною гілкою `main` |
| `git status` | Перегляд поточного стану |
| `git add .` | Додавання змін до індексу |
| `git commit -m "Опис"` | Створення коміту |
| `git branch` | Перегляд гілок |
| `git switch -c feature-description` | Створення та відкриття нової гілки |
| `git switch main` | Перехід до головної гілки |
| `git merge feature-description` | Об'єднання змін із гілки |
| `git log --oneline --graph --all` | Відображення історії та графа комітів |
| `git remote add origin URL` | Прив'язування репозиторію GitHub |
| `git push -u origin main` | Завантаження гілки на GitHub |

## Що виконано

1. Створено локальний репозиторій і початковий коміт у гілці `main`.
2. Створено гілку `feature-description` та файл `feature.md`.
3. Об'єднано `feature-description` з `main` за допомогою `merge`.
4. Створено гілку `conflict-feature` та внесено різні зміни в один рядок файлу `conflict.txt` у двох гілках.
5. Виконано злиття, отримано конфлікт і збережено його початковий вигляд у `docs/conflict_before_resolution.txt`.
6. Розв'язано конфлікт, залишивши інформацію з обох гілок, і зроблено коміт.

**Важливо:** `docs/conflict_before_resolution.txt` — збережений ПРИКЛАД конфлікту, а не поточний невиправлений конфлікт. Файл `conflict.txt` містить узгоджений результат.

## Як перевірити

Відкрийте Git Bash у цій папці та виконайте:

```bash
git status
git branch
git log --oneline --graph --all
git show --stat HEAD
```

У папці `docs` є підтвердження конфлікту та короткий звіт `ZVIT.md`.

## Як опублікувати на GitHub

1. На https://github.com/new створіть **порожній** репозиторій `git-github-practice`. Не додавайте README, .gitignore чи ліцензію на GitHub.
2. У командному рядку в папці проєкту виконайте (замініть `USERNAME`):

```bash
git remote add origin https://github.com/USERNAME/git-github-practice.git
git push -u origin main
git push origin feature-description conflict-feature
```

Якщо під час запуску сценарію вже було виконано `git remote add origin`, повторно додавати `origin` не треба.