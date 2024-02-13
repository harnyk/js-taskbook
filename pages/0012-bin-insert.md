Задача: Модификация Функции Бинарного Поиска

## Часть 1 - изменение функции бинарного поиска

**Цель задачи**: Модифицировать функцию бинарного поиска так, чтобы в случае, если искомый элемент не найден в отсортированном массиве, функция возвращала индекс, по которому этот элемент мог бы быть вставлен с сохранением порядка сортировки массива.

**Описание задачи:**

-   Написать функцию `binSearch(arr, target)`, принимающую на вход отсортированный массив чисел и целевое значение.
-   Если целевое значение найдено в массиве, функция должна возвращать его индекс (это уже и так реализовано).
-   Если целевое значение не найдено, функция должна возвращать индекс, по которому значение должно быть вставлено, чтобы массив оставался отсортированным.

```js
import { strictEqual, deepStrictEqual } from 'node:assert';

// ...

strictEqual(binSearch([1, 2, 3, 4, 5, 6, 7, 8, 9, 10], 5), 4);
strictEqual(binSearch([1, 2, 3, 4, 5, 6, 7, 8, 9, 10], 1), 0);
strictEqual(binSearch([1, 2, 3, 4, 5, 6, 7, 8, 9, 10], 2.9), 2);
strictEqual(binSearch([1, 2, 3, 4, 5, 6, 7, 8, 9, 10], 500), 10);
strictEqual(binSearch([1, 2, 3, 4, 5, 6, 7, 8, 9, 10], -500), 0);
```

## Часть вторая - "вставка с сохранением порядка"

**Цель задачи**: Написать функцию sortedInsert, которая вставляет значение в отсортированный массив чисел так, чтобы после вставки порядок сортировки массива сохранялся.

**Описание задачи:**

-   Функция sortedInsert(arr, value) должна принимать два аргумента: отсортированный массив чисел arr и вставляемое значение value.
-   В случае, если value уже присутствует в массиве, новое значение должно быть вставлено после или перед последним вхождением существующего значения.
-   Массив должен быть изменен (мутирован) функцией, добавляя value в нужную позицию.

```js
import { strictEqual, deepStrictEqual } from 'node:assert';

// ...

{
    const arr = [];
    sortedInsert(arr, 200);
    sortedInsert(arr, 100);
    sortedInsert(arr, 300);
    sortedInsert(arr, 50);
    sortedInsert(arr, 100);
    deepStrictEqual(
        arr,
        [50, 100, 100, 200, 300],
        'multiple insertions should maintain sorted order'
    );
}

{
    const arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
    sortedInsert(arr, 5);
    deepStrictEqual(
        arr,
        [1, 2, 3, 4, 5, 5, 6, 7, 8, 9, 10],
        'should insert if an element exists'
    );
}

{
    const arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
    sortedInsert(arr, 11);
    deepStrictEqual(
        arr,
        [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11],
        'should insert an element after the end of the array'
    );
}

{
    const arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
    sortedInsert(arr, 4.5);
    deepStrictEqual(
        arr,
        [1, 2, 3, 4, 4.5, 5, 6, 7, 8, 9, 10],
        'should insert between two elements'
    );
}

{
    const arr = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
    sortedInsert(arr, 0);
    deepStrictEqual(
        arr,
        [0, 1, 2, 3, 4, 5, 6, 7, 8, 9, 10],
        'should insert an element at the beginning of the array'
    );
}
```
