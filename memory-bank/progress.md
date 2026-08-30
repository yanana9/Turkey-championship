# Progress

## Работает
- Полный hero: анимированный заголовок, счётчики, hero-визуал с kenburns и параллаксом.
- Секции about/дисциплины/расписание/билеты (verify по коду при следующем касании).
- Reveal-анимации и счётчики на IntersectionObserver.

## Сделано недавно
- [2026-08-30] Hero-фото: `aerial-silks-sky-hq.jpg` — апскейл+enханс из `jnfdksmc;.webp`
  (Lanczos 1600px, unsharp, цветокоррекция; скрипт /tmp/enhance.py). Caption удалён ранее.
- [2026-08-30] Hero-фото: заменено на `gnbkglrbklr.jpg` (1100×1100, кольцо + прожекторы),
  object-position 50% 0% (верх, логотип Water Circus ушёл из кадра). Caption-пилюля удалена
  (не понравилась): HTML + CSS восстановимы из git-истории.
- [2026-08-30] Hero: добавлены облака программным композитом (Pillow, /tmp/clouds.py) —
  `aerial-silks-arena-clouds.jpg` подключен вместо чистого фото; оригинал сохранён для отката.
- [2026-08-30] Hero-фото под счётчиками: финально `aerial-silks-arena.jpg` (853×1280,
  переименовано из «2026-08-30 02.28.52.jpg»; полотна, синий костюм, белая арена),
  inline object-position 50% 52%. История: jaric → avif 1731257339923 → webp 1791391py → текущее.
- [2026-08-30] Hero-фото заменено: `jaric-swart-J_7BJZYIOzk-unsplash.jpg` →
  `photo-1731257339923-25e40a0a0699.avif` (900×1353, портрет 2:3), alt переписан.
  Затем «девушка целиком в кадре»: height 460→680px (index.html:478),
  object-position 50% 67% inline (:912). Мобильные 300px без изменений.
- Ранее: фикс фото в карточке Silks (inline object-position, `discipline-photo-fit` удалён, diff +1/−20).
- [2026-08-30] Контакты (#contacts): почта заменена на WM@IAAA.TEAM (:1062);
  добавлена карта площадки — блок `.venue-map` (Google Maps embed, q=Antalya Sports Hall,
  Muratpaşa, iframe 360px/260px mobile) после `.contact-box` (:1082), CSS (:746, :846).
- [2026-08-30] Карточка «World-Class Arena» (index.html:936): эмодзи 🎪 → 🏟️.
- [2026-08-30] Карточка «Riviera Atmosphere» (index.html:942): фото заменено на
  `istockphoto-1394774679-612x612.webp` (612×434, ч/б набережная Ривьеры), alt переписан.
  object-position не нужен — cover при 200px окна показывает ~79% высоты.
- [2026-08-30] Создан memory-bank/ (6 файлов).
- [2026-08-30] Hero-фото заменено: `aerial-silks-red-sky-hq.jpg` → `aerial-hero-0830.jpg`.
  Сырое `2026-08-30 23.23.31.jpg` (PNG 2560×1920, 5.6MB) обработано /tmp/enhance_newhero.py:
  Lanczos-д downscale до 1800×1350 (2× коробка 900×680) → UnsharpMask(2.2/88/2) →
  Contrast 1.03 / Color 1.05 / Brightness 1.01 → JPEG progressive q88 (304KB).
  object-position 50% 50% (ландшафт почти без обрезки в cover-коробке 1.333≈1.324);
  alt `Aerial gymnastics artist performing in the championship arena`.

## Известные замечания
- Старый `jaric-swart-...jpg` остался на диске неиспользуемым (не удаляли — не запрашивалось).
- `aerial-silks-red-sky-hq.jpg` больше не используется после hero-замены (оставлен на диске;
  кандидат на удаление при согласовании). Сырой `2026-08-30 23.23.31.jpg` (PNG, 5.6MB) —
  источник для `aerial-hero-0830.jpg`, также оставлен для отката.
- Hero `<img>` имеет `loading="lazy"` — выше фолда; потенциально убрать/заменить на `fetchpriority="high"`.
- Инструментарий: периодически пустые результаты read/search; избегать гигантских heredoc.

## Дальше (кандидаты)
- Визуальная приёмка hero после замены (страница открыта в браузере; подстроить 62% при необходимости).
- Решить судьбу неиспользуемого jaric-файла и lazy-loading hero.
