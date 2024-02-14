### Задача 2: Группировка постов по пользователю

## Ссылки

-   [Использование объектов как ассоциативных структур в JavaScript](./notes/objects-as-dictionaries.md)

**Описание задачи:**

Вам предстоит написать функцию, принимающую массив объектов постов, где каждый пост содержит идентификатор пользователя `userId` в виде строки (например, "u1"), уникальный идентификатор поста `id`, заголовок `title` и текст `body`.

Задача функции - сгруппировать посты по `userId`, формируя итоговый объект, где ключами будут идентификаторы пользователей, а значениями - массивы постов, соответствующие каждому пользователю.

**Файл с тестами (ESM синтаксис):**

```javascript
import { deepStrictEqual } from 'node:assert';

function groupPostsByUser(postsArray) {
    // Ваша реализация функции
}

// Тест-кейсы
const posts = [
    {
        userId: 'u1',
        id: 'p1',
        title: 'Morning Routine',
        body: 'Sharing my productive morning routine.',
    },
    {
        userId: 'u2',
        id: 'p2',
        title: 'Healthy Eating',
        body: 'Exploring the benefits of vegan diet.',
    },
    {
        userId: 'u1',
        id: 'p3',
        title: 'Workout Tips',
        body: 'My top 5 exercises for a full-body workout.',
    },
    {
        userId: 'u3',
        id: 'p4',
        title: 'Mindfulness',
        body: 'Practicing mindfulness to reduce stress.',
    },
    {
        userId: 'u2',
        id: 'p5',
        title: 'Book Club',
        body: 'Join our monthly book club for avid readers.',
    },
];

const expected = {
    u1: [
        {
            userId: 'u1',
            id: 'p1',
            title: 'Morning Routine',
            body: 'Sharing my productive morning routine.',
        },
        {
            userId: 'u1',
            id: 'p3',
            title: 'Workout Tips',
            body: 'My top 5 exercises for a full-body workout.',
        },
    ],
    u2: [
        {
            userId: 'u2',
            id: 'p2',
            title: 'Healthy Eating',
            body: 'Exploring the benefits of vegan diet.',
        },
        {
            userId: 'u2',
            id: 'p5',
            title: 'Book Club',
            body: 'Join our monthly book club for avid readers.',
        },
    ],
    u3: [
        {
            userId: 'u3',
            id: 'p4',
            title: 'Mindfulness',
            body: 'Practicing mindfulness to reduce stress.',
        },
    ],
};

deepStrictEqual(
    groupPostsByUser(posts),
    expected,
    'The grouped object does not match the expected output.'
);

console.log('All tests passed!');
```
