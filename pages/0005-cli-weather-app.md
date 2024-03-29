### Задание: Консольное приложение для отображения погоды по IP

**Цель:** Создать приложение на Node.js, которое определяет местоположение пользователя по IP и выводит погоду для этого места.

**Шаги выполнения:**

1. **Настройка проекта.** Инициировать проект Node.js и установить необходимые зависимости, в том числе `axios` для выполнения HTTP-запросов.
2. **Определение координат.** Реализовать функцию, которая делает запрос к [ip-api.com](http://ip-api.com/json) для получения текущих координат пользователя (широта и долгота).
3. **Получение и отображение погоды.** Используя полученные координаты, выполнить запрос к [Open-Meteo API](https://open-meteo.com/) для получения текущей погоды и отобразить её в консоли. Для этого нужно составить URL запроса, подставив широту и долготу в строку запроса к API Open-Meteo.
4. **Обработка ошибок.** Добавить обработку ошибок для **каждого** HTTP-запроса, чтобы приложение корректно реагировало на возможные проблемы с сетью или данные ошибки API.
