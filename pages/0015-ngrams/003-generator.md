## Генератор текстов

Напишите функцию generateTokensFromIndex(), которая принимает на вход: - n-граммный индекс - стартовую n-грамму
и генерирует случайные массивы токенов.

Пример индекса:

```js
const idx = {
    'do|you': new Set(['know', 'see']),
    'you|know': new Set(['what', 'where']),
    'you|see': new Set(['me']),
    'know|what': new Set(['it']),
    'what|it': new Set(['is']),
    'know|where': new Set(['i']),
    'where|i': new Set(['am']),
};
```

Пример вызова функции:

```js
const tokens = generateTokensFromIndex(idx, ['do', 'you']);
console.log(tokens);
```

Должен вывести:

```
['do', 'you', 'know', 'what', 'it', 'is']

или

['do', 'you', 'know', 'where', 'i', 'am']

или

['do', 'you', 'see', 'me']
```

Функция должна работать по следующему принципу:

1. По данной n-грамме (допустим это `['do', 'you']`) в индексе находим множество возможных токенов, связанных с ней. В нашем случае это будет `new Set(['know', 'see'])`.
2. Выбираем случайный токен из этого множества
    - Если множество возможных токенов не найдено или пусто, останавливаемся и возвращаем результат
3. Дописываем к результату выбранный в пункте 2 токен. Допустим это `'know'`
4. Из куска текущей n-граммы и выбранного токена формируем новую текущую n-грамму. В нашем случае это будет `['you', 'know']`.
5. Возвращаемся к пункту 1