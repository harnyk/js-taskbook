## Подготовка

Создайте новый проект

```
mkdir <название проекта>
cd <название проекта>
npm init -y
```

В package.json добавьте:

```
...
"type": "module",
"private": true,
"scripts": {
    "test": "node --test",
}
...
```

Установите вспомогательные пакеты:

```
npm install -D @types/node
```

## Организация проекта

-   `ngrams.js` - библиотека функций
-   `ngrams.test.js` - юнит-тесты

## Первые тесты

Создайте в файле `ngrams.test.js` юнит-тест:

```js
import assert from 'node:assert';
import { describe, it } from 'node:test';

import { getNgramsFromTokens } from './ngrams.js';

describe('getNgramsFromTokens', () => {
    it('should return an array of ngrams', () => {
        const tokens = [
            'the',
            'quick',
            'brown',
            'fox',
            'jumps',
            'over',
            'the',
            'lazy',
            'dog',
        ];
        assert.deepStrictEqual(getNgramsFromTokens(tokens, 2), [
            ['the', 'quick'],
            ['quick', 'brown'],
            ['brown', 'fox'],
            ['fox', 'jumps'],
            ['jumps', 'over'],
            ['over', 'the'],
            ['the', 'lazy'],
            ['lazy', 'dog'],
        ]);
    });
});
```

## Запуск

Запустите тесты:

```
npm test
```

## Первое задание

Напишите функцию `getNgramsFromTokens` в файле `ngrams.js`.
Функция получает на вход список токенов и размер n-граммы.
Функция возвращает массив n-грамм.

```js
getNgramsFromTokens(['let', 'me', 'explain', 'how', 'it', 'works'], 2);
```

Должна возвращать массив следующего вида:

```js
[
    ['let', 'me'],
    ['me', 'explain'],
    ['explain', 'how'],
    ['how', 'it'],
    ['it', 'works'],
];
```
