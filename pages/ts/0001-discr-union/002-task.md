### Задание: Обработка различных типов запросов к API

#### Цель:

Практика использования дискриминированных юнионов для представления разных типов запросов к бэкенд-сервису.

#### Описание:

Определить дискриминированный юнион `ApiRequest`, который может представлять различные типы запросов к серверу: получение данных (`"getData"`), отправка данных (`"postData"`), и обновление данных (`"updateData"`). Каждый тип запроса должен иметь разные поля, специфичные для своего действия:

-   `"getData"`: имеет поле `query`, содержащее параметры запроса в виде строки.
-   `"postData"`: содержит поля `path` (строка, указывающая на конечную точку API) и `body` (объект с данными для отправки).
-   `"updateData"`: включает поля `path`, `body`, и `updateMethod`, где `updateMethod` может быть `"put"` или `"patch"`.

#### Задача:

1. Создать функцию `handleRequest`, которая принимает параметр типа `ApiRequest` и возвращает результат в зависимости от типа запроса:
    - Для `"getData"` возвращать строку `"Fetching data with query: [query]"`.
    - Для `"postData"` возвращать строку `"Sending data to [path] with body: [body]"`.
    - Для `"updateData"` возвращать строку `"Updating data on [path] with method [updateMethod] and body: [body]"`.

#### Тест-кейсы:

-   Вызов `handleRequest` с каждым типом `ApiRequest` и проверка корректности возвращаемого значения.