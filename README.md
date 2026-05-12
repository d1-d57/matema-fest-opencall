# matema-fest.ru

Сайт фестиваля Matema-фест. Хостится на GitHub Pages: ветка `main`, корень репо
→ деплоится на https://matema-fest.ru/ (custom domain через CNAME).

## Структура

- `index.html` — главная страница matema-fest.ru
- `opencall2026/` — лендинг open call'а фестиваля 2026, живёт по
  https://matema-fest.ru/opencall2026/
  - `index.html` — **актуальная версия:** open call закрыт, форма убрана
  - `privacy.html` — политика обработки данных (нужна была для формы,
    оставлена на всякий случай)
  - `index-old-with-form.html` — локальный бэкап, в репо не коммитится
    (см. `.gitignore`)

## Где старая версия с формой

На ветке **`archive/open-call-with-form`** (GitHub:
https://github.com/d1-d57/matema-fest-opencall/tree/archive/open-call-with-form).

Та ветка указывает на коммит до закрытия open call'а. Там в
`opencall2026/index.html` лежит полная версия с активной анкетой, sticky-progress
баром, превью-модалкой и POST-эндпоинтом в Google Apps Script. Эта ветка
**не деплоится** — Pages смотрит только на `main`.

### Как восстановить форму

Если когда-нибудь надо вернуть анкету (или подсмотреть, как она была устроена):

```bash
git fetch origin archive/open-call-with-form
git show origin/archive/open-call-with-form:opencall2026/index.html > opencall2026/index.html
```

Или просто слить ветку обратно в `main`. Endpoint Google Apps Script в коде
зашит — если он за это время отвалился, его нужно будет перевыпустить.
