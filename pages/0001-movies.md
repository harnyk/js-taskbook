**Задание**

1. Дан исходный массив фильмов:
    ```javascript
    const movies = [
        { title: 'Inception', rating: 9.1 },
        { title: 'Interstellar', rating: 4.7 },
        { title: 'The Dark Knight', rating: 8.4 },
        { title: 'Batman Begins', rating: 3.3 },
        { title: 'Dunkirk', rating: 7.9 },
        { title: 'The Prestige', rating: 1.5 },
        { title: 'Memento', rating: 5.5 },
    ];
    ```
2. Ваша задача - написать функцию `convertMovies`, которая преобразует каждый объект, добавляя в него новое свойство `stars`. Это свойство должно содержать строку с количеством эмодзи-звёздочек, соответствующим рейтингу фильма. Рейтинг следует преобразовать в пятизвёздочную шкалу.

3. Выведите результат в консоль.

---

**Тест-кейс:**

После выполнения вашей функции, массив `movies` должен выглядеть примерно так (зависит от вашей реализации преобразования рейтинга в звёздочки):

```javascript
[
    { title: 'Inception', rating: 9.1, stars: '⭐⭐⭐⭐⭐' },
    { title: 'Interstellar', rating: 4.7, stars: '⭐⭐' },
    { title: 'The Dark Knight', rating: 8.4, stars: '⭐⭐⭐⭐' },
    { title: 'Batman Begins', rating: 3.3, stars: '⭐⭐' },
    { title: 'Dunkirk', rating: 7.9, stars: '⭐⭐⭐⭐' },
    { title: 'The Prestige', rating: 1.5, stars: '⭐' },
    { title: 'Memento', rating: 5.5, stars: '⭐⭐⭐' },
];
```

Обратите внимание на то, как рейтинг каждого фильма преобразуется в количество звёздочек, отражающее его рейтинг на пятизвёздочной шкале.

---

**Изучаемые темы:**

-   Использование [метода массива `map`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/map) для преобразования одного массива в другой
-   Использование [метод строки `repeat`](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/String/repeat) для повторения строки заданное количество раз
-   (_не обязательно_) Использование [object spread syntax (`...`)](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Spread_syntax#spread_in_object_literals) для копирования объекта и добавления в копию новых свойств
-   Использование [Math.round](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Math/round) для округления до ближайшего целого
