# История работы над проектом Frontend/Backend

## Общая информация
- **Проект**: Сайт кофейни
- **Репозиторий**: https://github.com/Kusatka/frontendbackendmirea
- **GitHub Pages**: https://Kusatka.github.io/frontendbackendmirea/
- **Путь к проекту**: `C:\Users\sudov\Downloads\frontendbackend`

---

## Практическое занятие 1: Инициализация проекта и Git

### Выполненные задачи:
1. Создан репозиторий на GitHub
2. Инициализирован Git в проекте
3. Создан `.gitignore`
4. Создан `README.md`
5. Создан базовый `index.html` с семантической разметкой
6. Добавлен favicon (`assets/icons/favicon.ico`)
7. Добавлен viewport meta tag для адаптивности
8. Созданы ветки `main` и `dev`
9. Настроен GitHub Pages

### Структура проекта:
```
frontendbackend/
├── index.html
├── README.md
├── .gitignore
├── assets/
│   ├── img/
│   ├── icons/
│   └── fonts/
└── styles/
```

### Git команды, которые были выполнены:
```bash
git init
git config user.name "Kusatka"
git config user.email "sudovskiyandrey@yandex.ru"
git remote add origin https://github.com/Kusatka/frontendbackendmirea.git
git add .
git commit -m "feat: initialize project structure with README and gitignore"
git branch -M main
git push -u origin main
git checkout -b dev
git push -u origin dev
```

### Проблемы и решения:
- **Проблема**: Файлы с пробелами в именах (`image (1).png`) вызывали ошибки валидации HTML
- **Решение**: Переименованы все файлы, убраны пробелы и скобки:
  - `image (1).png` → `image-1.png`
  - `IMAGE (2).png` → `image-2.png`
  - `Баннер.png` → `banner.png`

---

## Практическое занятие 2: Семантическая HTML-разметка

### Выполненные задачи:
1. Добавлена семантическая HTML-разметка (header, nav, main, section, article, footer)
2. Создана структура сайта кофейни с секциями:
   - Главная (home)
   - О нас (about)
   - Меню (menu)
   - Галерея (gallery)
   - Контакты (contact)
3. Добавлены изображения из макета "Вариант 1. Кофе"
4. Применена типографика (неразрывные пробелы, тире)
5. Исправлены ошибки валидации HTML

### Структура HTML:
- `<header>` с логотипом и навигацией
- `<nav>` с якорными ссылками
- `<main>` с секциями контента
- `<section>` для каждой секции с уникальным id
- `<article>` для карточек меню
- `<footer>` с копирайтом

### Git команды:
```bash
git add .
git commit -m "feat: add semantic HTML structure with coffee shop content and assets"
git commit -m "fix: rename image files to remove spaces and fix HTML validation errors"
git push origin dev
```

---

## Практическое занятие 3: CSS методологии (BEM)

### Выполненные задачи:
1. Создан файл `styles/style.css`
2. Применена методология BEM (Блок-Элемент-Модификатор)
3. Подключен шрифт Google Fonts (Inter)
4. Добавлены интерактивные состояния (`:hover`, `:focus`, `:active`)
5. Добавлены плавные переходы и анимации
6. Добавлена плавная прокрутка (`scroll-behavior: smooth`)
7. Добавлена адаптивность (responsive design)

### Структура CSS (BEM):
- `.header`, `.header__logo`, `.header__nav`
- `.nav`, `.nav__list`, `.nav__item`, `.nav__link`, `.nav__item--active`
- `.card`, `.card__title`, `.card__text`, `.card--featured`
- `.gallery`, `.gallery__item`, `.gallery__image`
- `.section`, `.section__title`

### Интерактивные элементы:
- Hover-эффекты на карточках, ссылках, изображениях
- Focus-стили для доступности
- Плавные переходы (`transition`)
- Анимация `fadeIn` для заголовков

### Git команды:
```bash
git add .
git commit -m "feat: add CSS styling with BEM methodology, interactive states and animations"
git push origin main
```

---

## Практическое занятие 4: Адаптивная вёрстка (Flexbox, Grid, Masonry)

### Выполненные задачи:
1. Улучшена адаптивность навигации (Flexbox)
   - Desktop: горизонтальное меню
   - Mobile: вертикальное меню
2. Добавлена секция "Преимущества" с Grid-сеткой
   - Использует `grid-template-columns: repeat(auto-fit, minmax(250px, 1fr))`
3. Добавлена секция "Дополнительные материалы" с Masonry-раскладкой
   - Использует `column-count` для элементов разной высоты
4. Переработаны медиазапросы на Desktop First подход
5. Исправлена прокрутка к якорным ссылкам (добавлен `scroll-padding-top`)

### Breakpoints (Desktop First):
- Ноутбуки: < 1200px
- Планшеты: < 992px
- Мобильные (альбом): < 768px
- Мобильные: < 576px
- Очень маленькие: < 400px

### Проблемы и решения:
- **Проблема**: Sticky header перекрывал секции при прокрутке к якорям
- **Решение**: Добавлен `scroll-padding-top: 100px` в `html` (адаптивный для мобильных)

### Git команды:
```bash
git add .
git commit -m "feat: add responsive layout with Flexbox, Grid, Masonry and Desktop First media queries"
git commit -m "fix: add scroll-padding-top for correct anchor scrolling with sticky header"
git commit -m "fix: improve mobile header size and scroll padding for better mobile experience"
git push origin main
```

---

## Практическое занятие 5: Мобильный интерфейс

### Выполненные задачи:
1. Создана папка `scripts/` и файл `menu.js`
2. Создан файл `styles/mobile.css` для мобильных стилей
3. Добавлено гамбургер-меню для мобильных устройств
4. Добавлена кнопка "Наверх" (Scroll to Top)
5. Реализован JavaScript для работы меню и кнопки
6. Проверены размеры шрифтов по гайдлайнам:
   - Material Design: 16px (основной текст)
   - iOS HIG: 17px (на мобильных)
   - Навигация: 18px (на мобильных)

### Структура файлов:
```
frontendbackend/
├── index.html
├── styles/
│   ├── style.css (основные стили)
│   └── mobile.css (мобильные стили)
├── scripts/
│   └── menu.js (скрипт меню и кнопки "Наверх")
└── assets/
```

### Функционал гамбургер-меню:
- Открытие/закрытие меню по клику
- Выезжающая панель справа на мобильных
- Затемнение фона при открытом меню
- Закрытие по Escape
- Закрытие при клике на overlay
- Закрытие при изменении размера окна (переход на desktop)
- Блокировка скролла при открытом меню

### Функционал кнопки "Наверх":
- Появляется после прокрутки > 300px
- Плавная прокрутка к началу страницы
- Адаптивные размеры для мобильных (52px на мобильных, 56px на desktop)
- Touch-зоны минимум 44px

### Git команды (к выполнению):
```bash
git add .
git commit -m "feat: add mobile interface with hamburger menu and scroll-to-top button"
git push origin main
```

---

## Текущее состояние проекта

### Структура:
```
frontendbackend/
├── index.html (семантическая разметка с гамбургер-меню и кнопкой "Наверх")
├── README.md
├── .gitignore
├── styles/
│   ├── style.css (BEM методология, Desktop First)
│   └── mobile.css (мобильные стили)
├── scripts/
│   └── menu.js (гамбургер-меню и кнопка "Наверх")
└── assets/
    ├── img/ (изображения: banner.png, image-1.png - image-8.png, LOGO.png, IMAGE.png, pr-0018-r.png)
    ├── icons/ (favicon.ico и другие иконки)
    └── fonts/ (для будущего использования)
```

### Секции сайта:
1. **Главная (home)** - приветствие и баннер
2. **Преимущества (features)** - Grid-сетка с 4 карточками
3. **О нас (about)** - информация о кофейне с изображением
4. **Меню (menu)** - Grid-сетка с карточками кофе
5. **Галерея (gallery)** - Grid-сетка с изображениями
6. **Дополнительные материалы (materials)** - Masonry-раскладка
7. **Контакты (contact)** - контактная информация

### Технологии:
- HTML5 (семантическая разметка)
- CSS3 (BEM методология, Flexbox, Grid, Masonry)
- JavaScript (ES6+)
- Git & GitHub
- GitHub Pages

### Методология CSS:
- **BEM** (Блок-Элемент-Модификатор)
- Примеры:
  - `.header`, `.header__logo`, `.header__nav`
  - `.nav`, `.nav__list`, `.nav__item`, `.nav__link`
  - `.card`, `.card__title`, `.card__text`, `.card--featured`

### Адаптивность:
- **Desktop First** подход
- Breakpoints: 1200px, 992px, 768px, 576px, 400px
- Мобильное меню появляется на < 768px
- Grid и Masonry адаптируются под размер экрана

### Особенности мобильной версии:
- Гамбургер-меню с выезжающей панелью
- Фиксированный header при скролле
- Кнопка "Наверх" для быстрой прокрутки
- Размеры шрифтов по гайдлайнам (16px/17px)
- Touch-зоны минимум 44px

---

## Важные заметки

### Проблемы, которые были решены:
1. Файлы с пробелами в именах → переименованы
2. Sticky header перекрывал секции → добавлен `scroll-padding-top`
3. Header слишком большой на мобильных → уменьшены padding и размеры
4. Прокрутка к якорям работала некорректно → добавлен адаптивный `scroll-padding-top`

### Рекомендации для дальнейшей работы:
- Проверить сайт на реальных мобильных устройствах через QR-код
- Протестировать все интерактивные элементы
- Убедиться, что нет горизонтального скролла
- Проверить валидацию HTML/CSS/JS

### Ссылки:
- **GitHub**: https://github.com/Kusatka/frontendbackendmirea
- **GitHub Pages**: https://Kusatka.github.io/frontendbackendmirea/
- **QR-код генератор**: https://qr-online.ru/
- **HTML валидатор**: https://validator.w3.org/
- **CSS валидатор**: https://jigsaw.w3.org/css-validator/

---

## Команды Git для быстрого старта

```bash
# Переход в директорию проекта
cd C:\Users\sudov\Downloads\frontendbackend

# Проверка статуса
git status

# Добавление всех изменений
git add .

# Коммит
git commit -m "описание изменений"

# Push в main
git push origin main

# Просмотр истории
git log --oneline -5
```

---

**Дата создания**: 2025-02-08
**Последнее обновление**: Практическое занятие 5 (мобильный интерфейс)
