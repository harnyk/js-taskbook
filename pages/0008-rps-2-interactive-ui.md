## Вторая часть задачи - Интерфейс пользователя и "ход компьютера"

См. [первую часть](0007-rock-paper-scissors.md)

После реализации логики игры "Камень, ножницы, бумага", пора добавить интерактивность и автоматизацию. В этой части задачи нужно создать пользовательский интерфейс с использованием библиотеки inquirer для Node.js, а также реализовать генерацию случайного выбора компьютера, чтобы играть против него.
Цели задачи:

-   Интеграция с `inquirer`: Используйте `inquirer` для создания интерактивного интерфейса, который позволяет пользователю выбирать между "камень", "ножницы" и "бумага".

-   Генерация случайного выбора компьютера: Создайте функцию, которая случайным образом выбирает между "камень", "ножницы" и "бумага" для компьютера. Это будет "ход компьютера". Можно воспользоваться `Math.random()`.

-   Игра против компьютера: Интегрируйте генерацию случайного выбора компьютера с логикой игры, чтобы пользователь мог играть против компьютера.

-   Вывод результатов: После каждого раунда выводите результат игры, указывая, кто выиграл - пользователь или компьютер, или же произошла ничья.
