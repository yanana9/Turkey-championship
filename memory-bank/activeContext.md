# Active Context

## Текущий фокус
Hero-фото: **`aerial-hero-0830.jpg`** (index.html:933) — ландшафт 1800×1350, 304KB,
JPEG progressive q88. Получено из сырого PNG `2026-08-30 23.23.31.jpg` (2560×1920, 5.6MB)
скриптом /tmp/enhance_newhero.py: Lanczos-д downscale до 1800px ширины (2× коробка 900×680)
→ UnsharpMask(2.2/88/2) → Contrast 1.03 / Color 1.05 / Brightness 1.01 (та же цветокоррекция
для согласованности; GaussianBlur опущен — PNG без webp-артефактов). object-position 50% 50%:
ландшафтное соотн. сторон (1.333) почти совпадает с коробкой (1.324) → cover почти не обрезает.
Alt: `Aerial gymnastics artist performing in the championship arena` — сайт тематики
aerial silks/hoop; PNG не просмотрен, alt написан по тематике сайта (скорректировать при необходимости).

История hero-замен за день: jaric → avif 1731257339923 → webp 1791391py →
aerial-silks-arena (+облака) → gnbkglrbklr → aerial-silks-sky-hq → aerial-hero-0830 (текущее, ландшафт).
Прочее: «Riviera Atmosphere» (:942) → istockphoto ч/б; эмодзи 🏟️ (:936);
почта WM@IAAA.TEAM; карта `.venue-map` после contact-box.

История hero-замен за день: jaric → avif 1731257339923 → webp 1791391py → aerial-silks-arena.
Прочее: «Riviera Atmosphere» (:942) → istockphoto ч/б; эмодзи 🏟️ (:936); почта WM@IAAA.TEAM;
карта `.venue-map` после contact-box.

## Геометрия (почему именно так)
Фото 900×1353; фигура спортсменки ≈ y 515–1095 (580px, центр 805). Окно 460px
вмещало лишь 34% высоты — фигура резалась. При 680px: rest-кроп 680px,
пик kenburns (scale 1.08) → видимая полоса 630px ≥ 580px с полями 30/20.
Проверено аналитически для ширин 350–900px: единые 67% дают полный охват
фигуры на всех брейкпоинтах, отдельный media-query для object-position не нужен.

## Открытые вопросы
1. Визуальная приёмка (страница переоткрыта): хватает ли высоты 680px, не сделать ли 640–700.
2. `loading="lazy"` на hero (выше фолда) — кандидат на удаление/`fetchpriority="high"`.
3. Неиспользуемые файлы: `jaric-swart-...jpg`, `xavier-praillet-...jpg` (из карточки).
4. `xavier-praillet-...jpg` остался фоном hero (`.hero-backdrop`, index.html:103, cover,
   center 35%, scale 1.18): пользователь просил заменить только карточку Riviera.
   Если менять и фон — файл istock 612px мал для full-bleed (нужен ретина-размер).

## Следующие шаги
- Ждать фидбек по кадру; правки — высота в index.html:478 и процент в :912.
