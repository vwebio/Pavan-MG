# Лендинг Pavan MG

## Общая информация

Лендинг представляет собой одностраничный сайт, предназначенный для представления информации о Pavan MG, его технологическом стеке и проектах. Сайт разработан с использованием HTML5, CSS3.

## Структура сайта

### Заголовок (Header)

- **Логотип**: Ссылка на главную страницу сайта.
- **Навигация**: Ссылки на разделы Home, About, Tech Stack, Projects и Contact.
- **Социальные ссылки**: Иконки для перехода на страницы в GitHub, Twitter и LinkedIn.

### Основное содержание (Main)

#### Обо мне (About)

- Приветственное сообщение с именем Pavan MG.
- Фотография Pavan MG.

#### Технологический стек (Tech Stack)

- Заголовок раздела.
- Описание технологий, с которыми работает Pavan MG.
- Логотипы технологий: HTML5, CSS3, JavaScript, React, Redux, Bootstrap, Tailwind CSS, SASS, Git, GreenSock, VSCode, GitHub.

#### Проекты (Projects)

- Заголовок раздела.
- Описание проектов.
- Список проектов с изображениями, заголовками, описаниями и использованными технологиями.
- Ссылки на живые превью и исходный код проектов.

### Подвал (Footer)

- **Логотип**: Ссылка на главную страницу сайта.
- **Контактная информация**: Номер телефона и электронная почта.
- **Социальные ссылки**: Иконки для перехода на страницы в GitHub, Twitter и LinkedIn.
- **Навигация**: Ссылки на разделы Home, About, Tech Stack, Projects и Contact.
- **Авторские права**: Информация о разработчике сайта.

## Используемые технологии

- HTML5
- CSS3
- SVG symbol (для иконок и логотипов)

## Файлы и папки

- `index.html`: Основной файл HTML.
- `css/index.css, fonts.css, style.css`: Файл стилей.
- `fonts/`: Шрифты.
- `images/`: Папка с изображениями, включая логотипы, фотографии и иконки.


## Инструкция по запуску статичного сайта с использованием Vite

## Структура проекта

```
root/
├── dist/
├── node_modules/
├── src/
│   ├── css/
│   │   ├── index.css
│   │   ├── style.css
│   │   └── fonts.css
│   ├── images/
│   └── index.html
├── package.json
├── package-lock.json
└── vite.config.js
```

## Шаги для запуска проекта

### 1. Установка зависимостей

Перед запуском проекта необходимо установить все зависимости. Для этого выполните следующую команду в корневой директории проекта:

```bash
npm install
```

### 2. Запуск проекта в режиме разработки

Для запуска проекта в режиме разработки выполните следующую команду:

```bash
npm run dev
```

Эта команда запустит Vite сервер, и ваш сайт будет доступен по адресу `http://localhost:3000`.

### 3. Сборка проекта для продакшн

Для сборки проекта в продакшн режиме выполните следующую команду:

```bash
npm run build
```

После выполнения этой команды, собранные файлы будут находиться в директории `dist/`.

### 4. Запуск собранного проекта

Для запуска собранного проекта вы можете использовать любой статический сервер. Например, с помощью `serve`:

1. Установите `serve` глобально, если он еще не установлен:

    ```bash
    npm install -g serve
    ```

2. Запустите собранный проект:

    ```bash
    serve -s dist
    ```

После выполнения этой команды, ваш сайт будет доступен по адресу `http://localhost:5000`.

## Конфигурация Vite

Конфигурация Vite находится в файле `vite.config.js`. 

```javascript
import { defineConfig } from "vite";

export default defineConfig({
  root: "src",
  base: '',
  build: {
    outDir: "../dist",
    rollupOptions: {
      input: "src/index.html",
    },
    assetsDir: 'assets',
  },
});
```

