# Git — личная инструкция

## Установка
Скачать с **git-scm.com** → установить с настройками по умолчанию.

Проверить:
```bash
git --version
```

---

## Первичная настройка (один раз)
```bash
git config --global user.email "твой@email.com"
git config --global user.name "Roman"
```

---

## Создать новый репозиторий
```bash
git init
```
Создаёт скрытую папку `.git` — там хранится вся история изменений.

---

## Базовый цикл работы

```bash
git add .                        # добавить все изменённые файлы
git commit -m "что я сделал"     # сохранить снимок с описанием
git push                         # отправить на GitHub
```

> Если файл новый — буква **U** (Untracked). После `git add` — **A**. После коммита — чисто.

---

## Создать файл из терминала
```bash
echo "текст" > filename.md
```

---

## Связать локальный репозиторий с GitHub
```bash
git remote add origin https://github.com/umyarr/weeek-api.git
git branch -M main
git push -u origin main
```

---

## Добавить второй remote (например GitVerse)
```bash
git remote add gitverse https://gitverse.ru/umyarovv/weeek_api.git
git push -u gitverse main
```

> GitVerse может требовать SSH вместо HTTPS — настроить отдельно.

---

## Посмотреть историю коммитов
```bash
git log --oneline
```

---

## Отменить изменения в файле (до коммита)
```bash
git restore README.md
```

---

## .env и .gitignore (обязательно для проектов с API)
```bash
echo "WEEEK_TOKEN=твой_токен" > .env
echo ".env" > .gitignore
```

> `.env` хранит секреты — токены, пароли. **Никогда не пушить в Git.**
> `.gitignore` говорит Git какие файлы игнорировать.

---

## Удалённые репозитории этого проекта
| Имя | URL |
|-----|-----|
| origin | https://github.com/umyarr/weeek-api |
| gitverse | https://gitverse.ru/umyarovv/weeek_api |

---

## Следующие шаги
- [ ] Настроить SSH для GitVerse
- [ ] Создать `.env` с токеном Weeek
- [ ] Написать первый запрос к Weeek API
