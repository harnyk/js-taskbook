### Задание: Уникализация массива доменов

#### Описание задачи
Напишите функцию `toUniqueList`, которая принимает массив объектов типа `Domain` и возвращает новый массив, содержащий только уникальные домены.

Домен считается уникальным, если в массиве нет другого объекта с таким же сочетанием свойств `sld` и `tld`. Для проверки уникальности нужно учитывать оба свойства.

#### Требования
1. Функция должна принимать массив объектов `domains` с элементами интерфейса:
   ```typescript
   interface Domain {
       sld: string; // Second-Level Domain
       tld: string; // Top-Level Domain
   }
   ```
2. Функция должна иметь следующую сигнатуру:
   ```typescript
   function toUniqueList(domains: Domain[]): Domain[];
   ```
3. Функция должна возвращать новый массив, состоящий только из уникальных доменов.
4. Оригинальный массив `domains` не должен быть изменён.
5. Порядок элементов в результирующем массиве должен соответствовать их первому вхождению в исходный массив.

#### Пример
```typescript
const domains: Domain[] = [
    { sld: "example", tld: "com" },
    { sld: "example", tld: "org" },
    { sld: "example", tld: "com" },
    { sld: "test", tld: "com" },
];

const uniqueDomains = toUniqueList(domains);

console.log(uniqueDomains);
// Результат:
// [
//     { sld: "example", tld: "com" },
//     { sld: "example", tld: "org" },
//     { sld: "test", tld: "com" },
// ]
```

---

### Тест-кейсы

1. **Пустой массив:**
   ```typescript
   const domains: Domain[] = [];
   console.log(toUniqueList(domains)); // []
   ```

2. **Массив с одним элементом:**
   ```typescript
   const domains: Domain[] = [{ sld: "example", tld: "com" }];
   console.log(toUniqueList(domains)); 
   // [{ sld: "example", tld: "com" }]
   ```

3. **Массив с несколькими одинаковыми доменами:**
   ```typescript
   const domains: Domain[] = [
       { sld: "example", tld: "com" },
       { sld: "example", tld: "com" },
   ];
   console.log(toUniqueList(domains)); 
   // [{ sld: "example", tld: "com" }]
   ```

4. **Массив с уникальными доменами:**
   ```typescript
   const domains: Domain[] = [
       { sld: "example", tld: "com" },
       { sld: "test", tld: "org" },
   ];
   console.log(toUniqueList(domains)); 
   // [
   //     { sld: "example", tld: "com" },
   //     { sld: "test", tld: "org" }
   // ]
   ```

5. **Смешанный массив:**
   ```typescript
   const domains: Domain[] = [
       { sld: "example", tld: "com" },
       { sld: "example", tld: "org" },
       { sld: "example", tld: "com" },
       { sld: "test", tld: "com" },
   ];
   console.log(toUniqueList(domains)); 
   // [
   //     { sld: "example", tld: "com" },
   //     { sld: "example", tld: "org" },
   //     { sld: "test", tld: "com" }
   // ]
   ```