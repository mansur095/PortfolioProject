# Portfolio (Vue 3 + Vite)

## Описание

Это современное портфолио-фронтенд на Vue 3 + Vite с красивым UI, 3D-моделью (TresJS), секциями в стиле IDE и анимациями. Проект легко расширяем и адаптируем под себя.

## Секции
- **Главная**: приветствие, глитч-анимация, 3D-модель клавиатуры
- **About Me**: секция с древом папок, биографией, скиллами
- **Projects**: секция с древом папок, карточками проектов и ссылками на GitHub

## Быстрый старт

1. **Клонируйте репозиторий:**
   ```bash
   git clone https://github.com/mansur095/PortfolioProject.git
   cd PORTFOLIO
   ```
2. **Установите зависимости:**
   ```bash
   npm install
   ```
3. **Запустите проект:**
   ```bash
   npm run dev
   ```
4. **Откройте в браузере:**
   Перейдите по адресу [http://localhost:5173](http://localhost:5173)

## Основные зависимости
- [Vue 3](https://vuejs.org/)
- [Vite](https://vitejs.dev/)
- [TresJS](https://tresjs.org/) и [@tresjs/cientos](https://cientos.tresjs.org/) — для 3D-модели
- [three.js](https://threejs.org/)

## Структура проекта
- `src/components/` — основные компоненты (GlitchText, Keyboard3D, PersonalInfoSection, PersonalDetailsSection и др.)
- `public/keyboard2.glb` — 3D-модель клавиатуры
- `src/assets/` — изображения для проектов
- `src/App.vue` — главная страница и роутинг

## Автор
[mansur095]
