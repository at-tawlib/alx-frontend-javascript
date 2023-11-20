# 0x02. ES6 classes

`OOP` -- `JavaScript` -- `ES6`

#### Install Jest, Babel, and ESLint
in your project directory:
-   Install Jest using:  `npm install --save-dev jest`
-   Install Babel using:  `npm install --save-dev babel-jest @babel/core @babel/preset-env`
-   Install ESLint using:  `npm install --save-dev eslint`

#### Configuration files
-  `package.json`
- `babel.config.js`
-  `.eslintrc.js`

Don’t forget to run  `$ npm install`  when you have the  `package.json`

### Tasks
---
[0-classroom.js](0-classroom.js) , [0-main.js](0-main.js)

Implement a class named  `ClassRoom`:
-   Prototype:  `export default class ClassRoom`
-   It should accept one attribute named  `maxStudentsSize`  (Number) and assigned to  `_maxStudentsSize`

```
bob@dylan:~$ 
bob@dylan:~$ npm run dev 0-main.js 
10
bob@dylan:~$ 
```
---
[1-make_classrooms.js](1-make_classrooms.js) , [1-main.js](1-main.js)

Import the  `ClassRoom`  class from  `0-classroom.js`.
Implement a function named  `initializeRooms`. It should return an array of 3  `ClassRoom`  objects with the sizes 19, 20, and 34 (in this order).

```
bob@dylan:~$ npm run dev 1-main.js 
[
  ClassRoom { _maxStudentsSize: 19 },
  ClassRoom { _maxStudentsSize: 20 },
  ClassRoom { _maxStudentsSize: 34 }
]
bob@dylan:~$ 
```
---

[2-hbtn_course.js](2-hbtn_course.js) ,  [2-main.js](2-main.js)
Implement a class named  `HolbertonCourse`:
-   Implement a getter and setter for each attribute.
```
bob@dylan:~$ npm run dev 2-main.js 
ES6
HolbertonCourse {
  _name: 'Python 101',
  _length: 1,
  _students: [ 'Bob', 'Jane' ]
}
TypeError: Name must be a string
    ...
TypeError: Length must be a number
    ...
bob@dylan:~$ 
```
---
**3. Methods, static methods, computed methods names..... MONEY**
[3-currency.js](3-currency.js) , [3-main.js](3-main.js)
Implement a class named  `Currency`:

-   - Constructor attributes:
    -   `code`  (String)
    -   `name`  (String)
-   Each attribute must be stored in an “underscore” attribute version (ex:  `name`  is stored in  `_name`)
-   Implement a getter and setter for each attribute.
-   Implement a method named  `displayFullCurrency`  that will return the attributes in the following format  `name (code)`.

```
bob@dylan:~$ npm run dev 3-main.js 
Dollars ($)
bob@dylan:~$ 
```
---
**4. Pricing**
[4-pricing.js](4-pricing.js) , [4-main.js](4-main.js)

Implement a class named  `Pricing`:
-   Constructor attributes:
    -   `amount`  (Number)
    -   `currency`  (Currency)
-   Each attribute must be stored in an “underscore” attribute version (ex:  `name`  is stored in  `_name`)
-   Implement a getter and setter for each attribute.
-   Implement a method named  `displayFullPrice`  that returns the attributes in the following format  `amount currency_name (currency_code)`.
-   Implement a static method named  `convertPrice`. It should accept two arguments:  `amount`  (Number),  `conversionRate`  (Number). The function should return the amount multiplied by the conversion rate.

```
bob@dylan:~$ npm run dev 4-main.js 
Pricing {
  _amount: 100,
  _currency: Currency { _code: 'EUR', _name: 'Euro' }
}
100 Euro (EUR)
bob@dylan:~$ 
```
---

**5. A Building**
[5-building.js](5-building.js), [5-main.js](5-main.js)

Implement a class named  `Building`:
-   Constructor attributes:
    -   `sqft`  (Number)
-   Each attribute must be stored in an “underscore” attribute version (ex:  `name`  is stored in  `_name`)
-   Implement a getter for each attribute.
-   Consider this class as an abstract class. And make sure that any class that extends from it should implement a method named  `evacuationWarningMessage`.
    -   If a class that extends from it does not have a  `evacuationWarningMessage`  method, throw an error with the message  `Class extending Building must override evacuationWarningMessage`

```
bob@dylan:~$ npm run dev 5-main.js 
Building { _sqft: 100 }
Error: Class extending Building must override evacuationWarningMessage
    ...
bob@dylan:~$ 
```
---
