# React WebSockets Потоковое Приложение README

## Обзор Проекта

Этот проект на React демонстрирует, как установить соединение WebSocket для потоковой передачи данных (в частности, изображений) с сервера (в данном случае, сервера WebSocket на Python) в приложение React в реальном времени. Приложение получает данные изображений, закодированные в base64, для четырех разных потоков, декодирует их и отображает изображения на веб-странице. Если данные потока недоступны, вместо них отображается изображение-заполнитель.

## Начало Работы

### Предварительные Требования

- Node.js (рекомендуется версия 12.x или выше)
- Современный веб-браузер, поддерживающий ES6 и WebSockets
- Запущенный сервер WebSocket по адресу `ws://localhost:5678`, отправляющий данные изображений в формате base64, разделенные точкой с запятой (`;`)

### Установка

1. Клонируйте репозиторий на локальную машину:
```bash
git clone https://github.com/yskaak/soccer-demo-react
```

2. Перейдите в директорию проекта:
```bash
cd Soccer-Analysis-Dashboard
```
3. Установите необходимые npm пакеты:
```bash
npm install
```

### Запуск Приложения

1. Запустите приложение React:
```bash
npm start
```
Эта команда запускает приложение в режиме разработки. Откройте [http://localhost:3000](http://localhost:3000)для просмотра его в браузере. Страница будет перезагружаться, когда вы вносите изменения.

## Структура Проекта


- `src/App.js`: Содержит основной компонент React, который управляет соединением WebSocket и отображает потоки изображений.
- `src/App.css`: Обеспечивает базовое стилизация для макета потоковых изображений.
- `public/images/link.png`:Изображение-заполнитель, показываемое, когда данные потока недоступны.
- `public/placeholder-image.jpg`: Отображается, когда изображение не загружается.

## Ключевые Особенности

- **Потоковая Передача в Реальном Времени**:  Приложение подключается к серверу WebSocket по адресу `ws://localhost:5678`  и прослушивает входящие сообщения с данными изображений.
- **Динамическое Декодирование Изображений**:После получения сообщения приложение декодирует данные изображений, закодированные в base64, для каждого из четырех потоков и обновляет пользовательский интерфейс для отображения этих изображений.

## Настройка Приложения

- **URL Сервера WebSocket**:  Чтобы изменить URL сервера WebSocket, модифицируйте строку подключения в хуке useEffect внутри `src/App.js`.
- **Стилизация**:Настройте макет и стилизацию, редактируя `src/App.css`.
- **Изображения-Заполнители:**: Замените `public/images/link.png` и `public/placeholder-image.jpg` на свои собственные изображения, если это необходимо.

## Technologies Used

- React.js для пользовательского интерфейса.
- Bootstrap для адаптивного макета и стилизации.
- API WebSocket для реального времени коммуникации между клиентом и сервером.