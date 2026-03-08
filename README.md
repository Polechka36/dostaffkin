# DoStaffkin

Веб-приложение для управления доставкой. Позволяет создавать заказы доставки и отслеживать статус отправлений.

## Функционал

- **Home** — главная страница приложения
- **Order** — создание заказа доставки:
  - Форма маршрута (адрес отправления, адрес получения)
  - Выбор размера и скорости доставки
  - Интеграция с Yandex Maps для выбора адресов
  - Форма данных получателя (имя, телефон, комментарий)
  - Расчёт стоимости доставки
- **Track** — отслеживание статуса заказа по номеру отправления

## Технологический стек

- **Frontend**: Angular 21.1.1
- **Forms**: Reactive Forms (@angular/forms)
- **Routing**: @angular/router
- **HTTP**: @angular/common/http
- **Maps**: Yandex Maps API
- **Notifications**: ngx-toastr (20.0.4)
- **State Management**: RxJS (7.8.2)
- **Language**: TypeScript 5.9.3
- **Testing**: Vitest 4.0.18

## Установка и запуск

```bash
# Установка зависимостей
npm install

# Запуск dev-сервера (http://localhost:4200)
npm start

# Сборка продакшена
npm build

# Watch режим разработки
npm run watch

# Запуск тестов
npm test
```

## API

- `POST https://testologia.ru/delivery/create` — создание заказа доставки
- `GET https://testologia.ru/delivery/info` — получение информации о статусе доставки

## Структура проекта

```
src/
├── app/
│   ├── pages/
│   │   ├── home/          — главная страница
│   │   ├── order/         — создание заказа (с конфигом размеров и скоростей)
│   │   └── track/         — отслеживание доставки
│   ├── header/            — компонент заголовка
│   ├── services/
│   │   └── delivery-api.ts — сервис API доставки
│   ├── app.routes.ts      — маршруты приложения
│   ├── app.config.ts      — конфигурация приложения
│   └── app.ts             — корневой компонент
├── index.html
├── main.ts
└── styles.css
```

## Конфигурация

- **Angular CLI**: 21.1.1
- **Node.js**: npm 10.9.2
- **TypeScript**: 5.9.3
