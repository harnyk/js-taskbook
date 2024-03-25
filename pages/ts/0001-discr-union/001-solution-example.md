### Задание: Простая система управления задачами

#### Цель:

Понять, как использовать дискриминированные юнионы для обработки различных типов действий в системе управления задачами.

#### Описание:

Определить дискриминированный юнион `TaskAction`, который может представлять два действия над задачей: добавление новой задачи (`"add"`) и завершение задачи (`"complete"`). Каждый тип действия должен иметь разные поля:

-   `"add"`: содержит поле `title`, которое является строкой с названием новой задачи.
-   `"complete"`: имеет поле `taskId`, которое является числом, идентификатором задачи для завершения.

#### Задача:

1. Создать функцию `performTaskAction`, которая принимает параметр типа `TaskAction` и обрабатывает его, возвращая строку, описывающую действие:
    - Для `"add"` возвращать строку `"Adding task: [title]"`.
    - Для `"complete"` возвращать строку `"Completing task with ID: [taskId]"`.

### Пример решения:

```typescript
// Определение типа TaskAction
type TaskAction =
    | { type: 'add'; title: string }
    | { type: 'complete'; taskId: number };

// Функция для выполнения действия над задачей
function performTaskAction(action: TaskAction): string {
    switch (action.type) {
        case 'add':
            return `Adding task: ${action.title}`;
        case 'complete':
            return `Completing task with ID: ${action.taskId}`;
        default:
            return 'Unknown action';
    }
}

// Примеры использования
const addAction: TaskAction = { type: 'add', title: 'Learn TypeScript' };
const completeAction: TaskAction = { type: 'complete', taskId: 1 };

console.log(performTaskAction(addAction)); // "Adding task: Learn TypeScript"
console.log(performTaskAction(completeAction)); // "Completing task with ID: 1"
```
