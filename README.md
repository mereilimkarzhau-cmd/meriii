# Jarys

Jarys — статический каталог спортивных секций для детей в Казахстане. В демо включены 23 объявления, фильтрация, QR-код для офлайн-рекламы, форма поддержки, партнёрский лендинг, SEO-мета-данные и доступная семантическая разметка.

## Быстрый запуск

Откройте `index.html` в браузере или запустите локальный сервер:

```bash
python -m http.server 8000
```

Перейдите на `http://localhost:8000`. Для QR-кода используется CDN-версия `qrcode.js`; для шрифтов и фото используются Google Fonts и Unsplash.

## Настройка Firebase

1. Откройте [Firebase Console](https://console.firebase.google.com/) и создайте проект.
2. Добавьте Web App и скопируйте конфигурацию Firebase.
3. Подключите SDK Firebase перед `runtime.js` в `index.html`, затем вставьте конфиг в отдельный `firebase-config.js`.
4. Создайте Firestore Database и коллекции `listings`, `coaches`, `supportRequests`. Замените демо-массивы в `runtime.js` на чтение Firestore, а отправку формы подключите к `supportRequests`.
5. Настройте Firebase Authentication для кабинета партнёров и Storage для фотографий секций.

## GitHub Pages

1. Создайте репозиторий и загрузите файлы проекта в ветку `main`.
2. Откройте **Settings → Pages**.
3. В **Build and deployment** выберите **Deploy from a branch**, ветку `main` и папку `/ (root)`, затем нажмите **Save**.
4. После публикации обновите canonical URL, `robots.txt` и `sitemap.xml` под домен проекта.

## SEO и доступность

На странице есть `title`/`description`, Open Graph, canonical URL, JSON-LD WebSite, семантические `header/nav/main/section/article/footer`, `alt` у изображений, подписи форм, `aria-label`, skip-link, видимый фокус и контрастная палитра.
