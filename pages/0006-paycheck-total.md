## Задача - сума чека

Написать функцию `calculateTotal(items)`, которая принимает массив объектов, представляющих товары в чеке. Каждый объект содержит название товара, количество и цену за единицу (`pricePerUnit`). Функция должна возвращать общую сумму чека.

Например:

```javascript
console.log(
    calculateTotal([
        { name: 'Молоко', quantity: 2, pricePerUnit: 50 },
        { name: 'Хлеб', quantity: 1, pricePerUnit: 20 },
        { name: 'Яблоки', quantity: 5, pricePerUnit: 10 },
    ])
);
// Выводит: 170
```

Решить задачу двумя способами:

-   **Способ 1** - используя только цикл - `for` или `for...of`
-   **Способ 2** - используя `.map()` для получения массива стоимостей и `.reduce()` для их суммирования
