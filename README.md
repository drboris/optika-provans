# Оптика «Прованс» — лендинг

Одностраничный сайт салона оптики «Прованс». Чистый HTML/CSS/JS в одном файле,
без сборки и зависимостей — всё лежит рядом с разметкой.

- Репозиторий: <https://github.com/drboris/optika-provans>
- Живой сайт: <https://drboris.github.io/optika-provans/>

## Быстрый старт

Открыть файл `index.html` двойным кликом в браузере. Всё работает локально,
интернет нужен только для шрифтов Google Fonts и записи через Dikidi.

Если нужен «как на хостинге» (с нормальными путями и без file://):

```powershell
python -m http.server 8000
# затем http://localhost:8000/index.html
```

## Что внутри

| Файл | Назначение |
| --- | --- |
| `index.html` | Вся страница: разметка, стили, скрипты |
| `hero-*.jpg` | Иллюстрации и фото в первом экране |
| `specialist-*.jpg`, `Борис.jpg`, `Вика.jpg` | Фотографии оптометристов |
| `hoya-logo.svg` | Логотип HOYA |
| `favicon.*`, `apple-touch-icon.png` | Иконки сайта |
| `ZnikomitNo24Thin.woff2` | Шрифт заголовков (`.otf` — исходник) |

Папка `.gigatool/` — служебная (инструмент разработки, ~50 МБ), в репозиторий не попадает.
`log.txt` — журнал правок, тоже исключён.

## Публикация на GitHub Pages

Уже включено: **Settings → Pages**, ветка `main`, папка `/ (root)`.
Любой `git push` в `main` пересобирает сайт за минуту.

Если нужно переехать на другой аккаунт — главный файл должен называться `index.html`
(GitHub Pages ищет именно его).

## Работа с другого компьютера

```powershell
git clone https://github.com/drboris/optika-provans.git
cd optika-provans
# правим, затем:
git add -A
git commit -m "описание правки"
git push
```

При первом `push` на новой машине Git Credential Manager откроет браузер
и попросит войти в GitHub — пароль в командах вводить не нужно.
