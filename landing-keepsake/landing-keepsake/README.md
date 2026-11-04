# Keepsake — адаптивний лендінг

Односторінковий лендінг дизайн-агенції Keepsake за макетом у Figma.

**Демо:** https://USERNAME.github.io/landing-keepsake/

## Технології

- HTML5 (семантична розмітка: `header`, `nav`, `main`, `section`, `article`, `footer`, `form`)
- CSS3 без фреймворків і UI-бібліотек
- Шрифти з Google Fonts: Oswald, Open Sans, Dancing Script
- Іконки: інлайн-SVG (спрайт `<symbol>` + `<use>`)
- Без JavaScript

## Рішення

- **Mobile first.** Базові стилі для 375px, далі `@media (min-width: 768px)` і `@media (min-width: 1280px)`. Сторінка коректна на ширині 320–1920px, контент центрується з максимальною шириною 1100px.
- **CSS-змінні.** Кольори, шрифти, відступи, розміри тексту та брейкпоінт-залежні значення (поля, відступи секцій, розмір заголовків) оголошені в `:root` і перевизначаються в media-запитах.
- **Розкладка.** Flexbox для хедера, навігації, послуг, статистики, клієнтів, журналу та футера. CSS Grid для сітки робіт (1 / 2 / 3 колонки), `aspect-ratio` для карточок.
- **Мобільне меню без JS.** Прихований `checkbox` + `label`-бургер, стан `:checked ~` відкриває меню; бургер перетворюється на хрестик.
- **Фільтр портфоліо без JS.** `radio`-кнопки + `:checked ~` та атрибут `data-category` на карточках.
- **Ховер карточок.** Оверлей з'являється при `:hover` та `:focus-visible`.
- **Форма підписки без JS.** Стани focus, error (`:user-invalid` + `:has()`), success (`:target`); HTML-валідація email, обов'язковий прапорець згоди.
- **Fixed header** і кнопка «вгору» (fixed, 44×44).
- **Доступність.** Фокус завжди видно, іконочні кнопки мають `aria-label`, у форми є `label`, помилка пов'язана з полем через `aria-describedby`, декоративні зображення мають `alt=""`.
- **Продуктивність.** Зображення у WebP з `width` / `height` та `loading="lazy"`, шрифти з `font-display: swap`.

## Структура

```
landing-keepsake/
├── index.html
├── README.md
├── css/
│   └── style.css
└── images/
```

## Запуск

Відкрити `index.html` у браузері. Для публікації: Settings → Pages → Branch `main` / root.
