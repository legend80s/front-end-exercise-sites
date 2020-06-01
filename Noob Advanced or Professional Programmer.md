# Noob Advanced or Professional Programmer

## 测验你的级别

观看以下 YouTube 视频判断你是 Noob，Advanced 或 Professional 程序员

1. ![youtube favicon](https://www.youtube.com/favicon.ico) [Junior Vs Senior Code - How To Write Better Code - Part 1](https://www.youtube.com/watch?v=g2nMKzhkvxw)
2. ![youtube favicon](https://www.youtube.com/favicon.ico) [Junior Vs Senior Code - How To Write Better Code - Part 2](https://www.youtube.com/watch?v=5B587bQ-TNg)

摘取一些有启发性的留言：

> Being a pro is all about thinking that someone else will have to read and understand your code.
>
> and realizing that "someone else" could just be you, 6 months in the future
>
> The main problem with comments is that they have to be kept in sync with the actual code. So in practice it's usually best to have code that is as self-explanatory as possible. Comments should only be used to explain the overall intention of the code, i.e. meta-information that is not apparent from the code itself - because this (usually) does not change during refactoring or bugfixing. If you feel the need to explain your actual code in a comment, better invest the time into making the code more obvious.

如果无法观看视频以下是文字内容

首先是代码，目录结构如下

总结下就是：

- naming
- guard clause

## 测验题一

```
1-logic
  |__1-noob.js
  |__2-advanced.js
  |__3-pro.js
```

### 新手代码

1-noob.js

```js
function toAccounting(n) {
  if (n < 0) {
    return '(' + Math.abs(n) + ')';
  } else if (n >= 0) {
    return n
  }
}

// console.log(toAccounting(undefined))
console.log(toAccounting(0))
console.log(toAccounting(10))
console.log(toAccounting(-5))
```

### 高级前端工程师代码

2-advanced.js

```js
function numberToAccountingString(number) {
  if (number != null) {
    if (number < 0) {
      return `(${Math.abs(number)})`
    } else {
      return number.toString()
    }
  }
}

console.log(numberToAccountingString(undefined))
console.log(numberToAccountingString(0))
console.log(numberToAccountingString(10))
console.log(numberToAccountingString(-5))
```

### 资深前端工程师代码

3-pro.js

```js
function numberToAccountingString(number) {
  if (number == null) return
  if (number < 0) return `(${Math.abs(number)})`

  return number.toString()
}

console.log(numberToAccountingString(undefined))
console.log(numberToAccountingString(0))
console.log(numberToAccountingString(10))
console.log(numberToAccountingString(-5))
```

## 测验题二

```
2-variable-manipulation
  |__1-noob.js
  |__2-advanced.js
  |__3-pro.js
```

### 新手代码

1-noob.js

```js
function calculateTotal(items, options) {
  let t = 0
  items.forEach(i => {
    t += i.price * i.quan
  })
  t = t - t * (options.dis || 0)
  t = t * 1.1
  t = t + (options.ship || 5)
  return t
}

const testItems = [
  { price: 15, quan: 2 },
  { price: 20, quan: 1 },
  { price: 5, quan: 4 }
]

// console.log(calculateTotal())
// console.log(calculateTotal(testItems))
// console.log(calculateTotal(undefined, {}))
// console.log(calculateTotal([], {}))

console.log(calculateTotal(testItems, {}))
console.log(calculateTotal(testItems, { ship: 0}))
console.log(calculateTotal(testItems, { dis: .75 }))
console.log(calculateTotal(testItems, { ship: 12}))
```

### 高级前端工程师代码

2-advanced.js

```js
const TAX_RATE = 1.1
const SHIPPING_DEFAULT = 5

function calculateTotal(items, options = {}) {
  if (items == null || items.length === 0) return 0

  let total = 0;

  items.forEach(item => {
    total += item.price * item.quantity
  })

  total = total - total * (options.discount || 0)

  total = total * TAX_RATE

  if (options.shipping !== 0) {
    total = total + (options.shipping || SHIPPING_DEFAULT)
  }

  return total
}
```

### 资深前端工程师代码

3-pro.js

```js
const TAX_RATE = 1.1
const SHIPPING_DEFAULT = 5

function calculateTotal(items, { shipping = SHIPPING_DEFAULT, discount = 0 } = {}) {
  if (items == null || items.length === 0) return

  const itemCost = items.reduce((total, item) => {
    return total + item.price * item.quantity
  }, 0)

  const discountRate = 1 - discount

  return itemCost * discountRate * TAX_RATE + shipping
}
```

## 测验题三

目录结构：

```
3-async
    ├── 1-noob.js
    ├── 2-advanced.js
    ├── 3-pro.js
    └── pro
        └── askQuestion.js
```

### 新手代码

1-noob.js

```js
const readline = require('readline')

const readlineInterface = readline.createInterface({
  input: process.stdin,
  output: process. stdout,
})

readlineInterface.question('what is your name? ', name => {
  readlineInterface.question('What is your job? ', job => {
    readlineInterface.question('How old are you? ', age => {
      console.log('Hello ' + name + '. You are a ' + age + ' year old ' + job + '.')

      readlineInterface.close()
    })
  })
})
```

### 高级前端工程师代码

2-advanced.js

```js
const readline = require('readline')

const readlineInterface = readline.createInterface({
  input: process.stdin,
  output: process.stdout,
})

async function main() {
  const name = await askQuestion(readlineInterface, 'What is your name? ')
  const job = await askQuestion(readlineInterface, 'What is your job? ')
  const age = await askQuestion(readlineInterface, 'How old are you? ')

  console.log(`Hello ${name}. You are a ${age} years old ${job}`)

  readlineInterface.close()
}

main();

function askQuestion(readlineInterface, question) {
  return new Promise(resolve => {
    readlineInterface.question(question, answer => {
      resolve(answer);
    })
  })
}
```

### 资深前端工程师代码

3-pro.js

```js
const askQuestion = require('./pro/askQuestion');

async function main() {
  const name = await askQuestion('What is your name? ')
  const job = await askQuestion('What is your job? ')
  const age = await askQuestion('How old are you? ')

  console.log(`Hello ${name}. You are a ${age} years old ${job}`)
}

main();
```

阶段总结：

- **Callback Hell** resolve the nestling problem by converting callbacks to Promises
- Abstract away: break to 
- **Abstract Leaking** that is implementation details leaking out of our askQuestion function so that you need to understand those details in order to use the code.

## 测验题四

目录结构：

```
4-fat-functions
    ├── 1-noob.js
    ├── 2-advanced.js
    └── 3-pro.js
```

### 新手代码

1-noob.js

```js

```

### 高级前端工程师代码

2-advanced.js

```js

```

### 资深前端工程师代码

3-pro.js

```js

```

阶段总结：

- **SRP** the big takeway from this is that number one break up your big funtions into individual functions that have a single responsibility
- **DRY** 



