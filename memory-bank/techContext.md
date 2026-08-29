# Tech Context

## Стек
Чистые HTML/CSS/JS, без сборки, без npm. Запуск — открыть `index.html` в браузере (`open index.html`).

## Изображения
- Форматы: JPG и AVIF (AVIF — Safari 16+/Chrome 85+, для локального сайта ок).
- Превью AVIF в терминале: `sips -s format jpeg file.avif --out /tmp/preview.jpg` (macOS), затем читать jpg.

## Рабочее окружение
- macOS, VS Code, git (origin: https://github.com/yanana9/Turkey-championship.git).
- Верификация правок: `grep -c`, `sed -n 'X,Yp'`, `git --no-pager diff --stat`, `open index.html`.

## Ограничения
- Никаких новых библиотек/фреймворков без явного запроса.
- Правки только в `index.html` (плюс файлы изображений).
