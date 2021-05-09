---
__Advertisement :)__

В данном руководстве предоставлены 10 лучших и уже давно устоявшихся практик о том, как красиво и правильно писать на JavaScript. 

---

# JavaScript Style Guide
#### Используйте camelCase для именования объектов, функций и экземпляров. 
 ```javascript
 // плохо
const OBJEcttsssss = {};
const this_is_my_object = {};
function c() {}

// хорошо
const thisIsMyObject = {};
function thisIsMyFunction() {} 
```
####  Используйте PascalCase только для именования конструкторов и классов.
 ```javascript
// плохо
function user(options) {
  this.name = options.name;
}

const bad = new user({
  name: 'nope',
});

// хорошо
class User {
  constructor(options) {
    this.name = options.name;
  }
}

const good = new User({
  name: 'yup',
});
```
#### Избегайте названий из одной буквы. Имя должно быть наглядным.
 ```javascript
// плохо
function q() {
  // ...
}

// хорошо
function query() {
  // ...
}
```
#### Используйте существительные для имен классов
 ```javascript
// плохо
class MakeCar {...}.

// хорошо
class Car = {…}
```
#### Для объявления переменных следует всегда использовать let или const. Если переменная не переназначается - следует использовать const.
 ```javascript
// плохо
var age = 20;
let pi = 10;

// хорошо
const myName = "Zamira";
let count = 1;
if (true) {
    count += 1;
    }
```
#### Каждая инструкция должна заканчиваться точкой с запятой.
 ```javascript
// плохо - выбрасывает исключение
const luke = {}
const leia = {}
[luke, leia].forEach((jedi) => jedi.father = 'vader')

// хорошо
const luke = {};
const leia = {};
[luke, leia].forEach((jedi) => {
  jedi.father = 'vader';
});
```
####  Если блоки кода в условии if и else занимают несколько строк, расположите оператор else на той же строчке, где находится закрывающая фигурная скобка блока if.
 ```javascript
// плохо
if (test) {
  thing1();
  thing2();
}
else {
  thing3();
}

// хорошо
if (test) {
  thing1();
  thing2();
} else {
  thing3();
}
```
#### Объекты (в том числе и массивы) следует объявлять через фигурные скобки
 ```javascript
// плохо
const item = new Object();
const items = new Array();

// хорошо
const item = {};
const items = [];
```
#### Каждое новое свойство объекта следует писать с новой строки
 ```javascript
// плохо
const user = { firstName: "Zamira", age: 29 }

// хорошо
const user = { 
firstName: "Zamira",
age: 29,
}
```
#### Используйте одинарные кавычки '' для строк.
 ```javascript
// плохо
const name = "Capt. Janeway";

// плохо - литерал шаблонной строки должен содержать интерполяцию или переводы строк
const name = `Capt. Janeway`;

// хорошо
const name = 'Capt. Janeway';
```