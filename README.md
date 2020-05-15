# Задание 2. Напишите линтер

[Описание задания](TASK_DESCRIPTION.md)

## Комментарии к заданию

### 1. Архитектура приложения

##### Файловая структура:

    src/
    ├── linter.js   // Главный файл, содержащий функцию lint
    └── lib/
        ├── ast-handler/    // Сюда вынесены функции для работы с ast-деревом
        |    ├── ast-handler.js     // Экспортирует функции, использующиеся в правилах линтинга
        |    └── ast-walker/
        |        └── simple-ast-walker.js   // Экспортирует простейшие функции для хождения по ast-дереву
        └── lint-rules/     // Папка с правилами линтинга
            ├── headers/
            |    ├── number-of-h1.js
            |    ├── position-of-h2.js
            |    └── position-of-h3.js
            ├── proportions/
            |    └── marketing-blocks-proportion.js
            └── warning/
                ├── button-position.js
                ├── button-size.js
                ├── placeholder-size.js
                └── text-size.js


##### Использованные фреймворки, библиотеки и пакеты:

* [json-to-ast](https://github.com/vtrushin/json-to-ast)

* [Webpack](https://webpack.js.org/)

* [Babel](https://babeljs.io/)

* [ESLint](https://eslint.org/)

### 2. Автотесты

Тесты располагаются в папке tests. Чтобы их запустить, надо запустить index.html через live server.

Тестирование я организовал в браузере, потому что в нём мне было удобнее смотреть подробности результатов тестов.

Для написания тестов я воспользовался фреймворком [Mocha](https://mochajs.org/). Также использовал [Chai](https://www.chaijs.com/) для получения функции assert.equal().Сами тесты находятся в tests.js. Данные, которые подаются на вход тестов, лежат отдельно в папке inputs.

### 3. Итоги

Необходимый функционал реализован, все автотесты проходят успешно.
