# System Patterns

## Архитектура
Один `index.html`: `<style>` в head, `<script>` перед `</body>`. Никаких зависимостей.

## Ключевые блоки
- `.hero-visual#heroVisual` > `img`: `width:100%; height:460px (300px mobile); object-fit:cover`;
  kenburns scale 1→1.08; контейнер max-width 900px. JS-параллакс вешается на контейнер (src-независим).
- `.hero-stats` — счётчики (`data-target`, `data-prefix`, `data-separator`), анимируются IntersectionObserver'ом.
- Карточки дисциплин: фото + `object-position` inline для кадрирования.

## Принятые паттерны
- Кадрирование фото: inline `style="object-position: 50% NN%;"` на конкретном `<img>`,
  а не новые CSS-классы (после отказа от `discipline-photo-fit` в пользу inline-стилей).
- Портретные фото 2:3 в hero: при cover на десктопе видна средняя полоса ~34% высоты —
  подбирать вертикальный object-position по центру масс фигуры.

## Уроки инструментария
- Огромные heredoc-скрипты в shell зависают; файлы создавать через editor-инструмент по одному.
- Часть read/search результатов иногда приходит пустой; надёжнее точечные shell-команды
  (`sed -n 'X,Yp'`, `grep -n`).
