# carusel_spa

Тестовое задание

## Github Pages
Демонстраия развернута на 
https://chochief.github.io/carusel_spa/

## Описание тестового задания

Создать SPA с использованием Vue.js

В приложении должно быть реализовано: 
* sticky header
* карусель картинок
* форма обратной связи
* отзывчивость (responsive)

### Заголовок

* Home, About Us, Contact Us
* Оформление любое
* Добавить место внизу страницы, чтобы проверить липкость

### Карусель

* Содержит набор картинок, являющихся ссылками
* Возможность свайпить (как на мобильных, так и на десктоп)
* Должна быть адаптивной. На мобильных устройствах - 1 картинка, на настольных - 3
* Вся функциональность должна работать на моб. устройствах
* Дизайн любой

### Форма связи

* Сделать маршрут /contact и переход по нему из меню
* Форма с полями (поля хранить в Vuex)
* Поле Name - заполняется значением по умолчанию из Vuex. Валидация - не короче 3 символов.
* Поле Phone - маска номера телефона страны пользователя. Валидация - 11 символов (включая код страны)
* Поле Message - textarea. Счетчик введенных символов (максимум 250).
* После отправки формы, обновить данные в Vuex.
* Разместить json-файл с ответом сервера об успешной отправке формы. Сделать иммитацию запроса к серверу. Ответ с сообщением об успешной отправке показать пользователю.

### Что можно использовать

* Vue Cli
* Любые ccs/js-библиотеки
* Любые изображения
* Любые mixin/sass/less

### Что нужно в итоге

* Разместить собранный проект, чтобы можно было визуально оценить выполнение задания (GitHub Pages).
* Учитывается не только качество кода, но и проработка визуальной части.
* Качество кода: чистый, читаемый, отформатированный код с правильной архитектурой.
* Разместить кода в публичном репозитории (GitHub).
* Сообщить сколько времени потребовалось на задание.

---

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### Run your tests
```
npm run test
```

### Lints and fixes files
```
npm run lint
```

## Dist
```
serve -s dist
```
https://cli.vuejs.org/ru/guide/deployment.html#общие-рекомендации