[![Review Assignment Due Date](https://classroom.github.com/assets/deadline-readme-button-24ddc0f5d75046c5622901739e7c5dd533143b0c8e959d652212380cedb1ea36.svg)](https://classroom.github.com/a/dX_5t8J0)
# Практика по функциям

Перед началом работы ознакомьтесь с мэйкфайлом и заданиями.
Все задания выполняются в index.js и экспортируются не по дефолту.

#### Prettier

Обратите внимание, что в проекте добавился файл .prettierrc. Он отвечает за конфигурацию форматировщика, который будет подгонять ваш код под правила линтера. Чтобы он работал, вам следует добавить расширение prettier во вкладке extensions. Форматировщик стоит применять так же, как и сохранение файла, чтобы избежать потом траты времени на осознание изменений :) Чтобы узнать команду, которая запускает нашего помошника на файле, нажмите ctrl + shift + p, у вас откроется набор команд и строка с поиском, вот в ней и введите Format и узнайте сочетание нужное сочетание клавиш, если вдруг оно покажется вам неудобным, переопределите шорткаты.

### Задание №1

Напишите функцию `convertToLowerOrUpperCase()`, которая на вход принимает массив и вид регистра. Функция должна проходится по массиву и приводит все строки к указанному регистру

**Пример использования**

```javascript
convertToLowerOrUpperCase(['lower','upper'], 'upper'); // ['LOWER','UPPER']
convertToLowerOrUpperCase(['LOWER','UPPER'], 'lower'); // ['lower','upper']

```

### Задание №2

Напишите функцию `convertToFilteredLowerOrUpperCase()`,которая на вход принимает массив и вид регистра. Функция должна проходится по массиву и приводит все строки к указанному регистру.
Вы спросите, а чем второе задание отличается от первого?
Ответ: тут вам потребуется добавить фильтрацию так, чтобы возвращаемый массив содержал только строки

**Пример использования**

```javascript
convertToFilteredLowerOrUpperCas(['lower', 'upper'], 'upper'); //['LOWER', 'UPPER']
convertToFilteredLowerOrUpperCas(['LOWER', {a: 123}, 'UPPER'],'lower'); // ['lower', 'upper']
```

### Задание №3

Напишите функцию `filterUsersByAge()`, которая фильтрует пользователей по возрасту. Она должна возвращать массив со всеми совершеннолетними пользователями.

**Пример использования**

```javascript
const users = [
    { name: 'Alice', age: 25 },
    { name: 'Bob', age: 17 },
    { name: 'Charlie', age: 30 },
    { name: 'David', age: 16 },
];
filterUsersByAge(users); // [{name: 'Alice', age: 25 }, { name:'Charlie', age: 30 }]
```

### Задание №4

Напишите функцию `filterUsersByParam()`, которая фильтрует пользователей по указанному параметру и значению этого параметра. Она должна возвращать массив со всеми пользователями, прошедшими проверку. Для разных типом значения параметра должны использоваться разные конструкции, а если его тип - число, тогда нужен дополничетельный параметр, который укажет, по какому знаку должна проходить проверка (Допустимые знаки: >, <).

**Пример использования**

```javascript
const users = [
    { name: 'Alice', age: 25, capableOfMarathon: true },
    { name: 'Bob', age: 17, capableOfMarathon: false },
    { name: 'Charlie', age: 30, capableOfMarathon: false },
    { name: 'David', age: 16, capableOfMarathon: true },
];
filterUsersByParam(users, 'age', 18, '>'); // [{ name: 'Alice', age: 25 }, { name:'Charlie', age: 30 }]
filterUsersByParam(users, 'capableOfMarathon', true); // [{ name: 'Alice', age: 25 }, {name: 'David', age: 16, capableOfMarathon: true }]
```

### Задание №5

Напишите функцию `divisibleAverage()`, которая ищет все элементы в массиве, которые делятся на заданное число и возвращает их среднее арифметическое.

**Пример использования**

 ```javascript
 divisibleAverage([3, 6, 9, 12, 15]); // 9
 divisibleAverage([0, -1, 10, 20, 30, 40, 50]); // 15
 ```
