# Задание 1
Для создания независимых фронтендов решено использовать Webpack Module Federation и разделить решение на несколько микрофронтендов:
- auth
- Cards
- profile

Почему выбран Module Federation
- Возможность динамически загружать модули без пересборки
- При неолбходимости возможно шарить зависимости между приложениями
- Возможность гибко управлять версиями и изоляцией
- Интеграция микрофронтендов без сложной оркестрации

/auth (8081,react,javascript,css)
    /src
        /components
            Login.js                // Компонент входа пользователя
            Register.js             // Компонент регистрации пользователя
        /styles
            login.css               // Стили для компонента входа
            /auth-form              // Стили для элементов компонента регистрации
        /utils
            auth.js                 // Утилиты для аутентификации
    index.js                        // Точка входа микрофронтенда
    package.json                    // Зависимости и скрипты микрофронтенда
    webpack.config.js
/profile (8082,react,javascript,css)
    /src
        /components
            EditAvatarPopup.js      // Компонент редактирования аватара
            EditProfilePopup.js     // Компонент редактирования профиля пользователя
            PopupWithForm.js        // Компонента форма редактирования профиля пользователя 
    /styles
        profile.css                 // Стили для компонента профиля
        /profile                    // Стили для элементов компонента профиля
    /contexts 
        CurrentUserContext.css      // Контекст пользователя JWT и прочее
    index.js                        // Точка входа микрофронтенда
    package.json                    // Зависимости и скрипты микрофронтенда
    webpack.config.js
/cards (8083,react,javascript,css)
    /src
        /components
            Card.js                 // Компонент работы с карточками
    /styles
        card.css                    // Стили для компонента карточки
        /card                       // Стили для элементов компонента карточки
    index.js                        // Точка входа микрофронтенда
    package.json                    // Зависимости и скрипты микрофронтенда
    webpack.config.js
/main-page

# Задание 2
[Решение задания 2](/docs/arch_template_task2.drawio "решено на второй страницы в drawio")