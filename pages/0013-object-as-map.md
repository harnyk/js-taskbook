### Задача: Преобразование списка постов в объект

**Описание задачи:**

Ваша задача - написать функцию, которая преобразует массив объектов, представляющих собой посты пользователя, в объект. В каждом объекте поста содержится уникальный идентификатор `id`, заголовок `title` и текст поста `body`. Результатом работы функции должен быть объект, где ключами будут идентификаторы постов, а значениями - соответствующие объекты постов.

**Файл с тестами (ESM синтаксис):**

```javascript
import { deepStrictEqual } from 'node:assert';

function transformPostsArrayToObj(postsArray) {
    // Ваша реализация функции
}

// Тест-кейсы
const posts = [
    {
        id: 'p1',
        title: 'Morning Run',
        body: 'Today I enjoyed a peaceful morning run in the park.',
    },
    {
        id: 'p2',
        title: 'Favorite Coffee',
        body: 'I discovered a new coffee shop with the best espresso.',
    },
    {
        id: 'p3',
        title: 'Book Recommendation',
        body: 'I highly recommend reading "The Great Gatsby", a fascinating story.',
    },
    {
        id: 'p4',
        title: 'Travel Dreams',
        body: 'Dreaming of my next vacation to Japan. The culture fascinates me!',
    },
    {
        id: 'p5',
        title: 'Gardening Tips',
        body: 'Learned some great tips for succulent care. Overwatering is a no-no!',
    },
];

const expected = {
    p1: {
        id: 'p1',
        title: 'Morning Run',
        body: 'Today I enjoyed a peaceful morning run in the park.',
    },
    p2: {
        id: 'p2',
        title: 'Favorite Coffee',
        body: 'I discovered a new coffee shop with the best espresso.',
    },
    p3: {
        id: 'p3',
        title: 'Book Recommendation',
        body: 'I highly recommend reading "The Great Gatsby", a fascinating story.',
    },
    p4: {
        id: 'p4',
        title: 'Travel Dreams',
        body: 'Dreaming of my next vacation to Japan. The culture fascinates me!',
    },
    p5: {
        id: 'p5',
        title: 'Gardening Tips',
        body: 'Learned some great tips for succulent care. Overwatering is a no-no!',
    },
};

deepStrictEqual(
    transformPostsArrayToObj(posts),
    expected,
    'The transformed object does not match the expected output.'
);

console.log('All tests passed!');
```
