# JavaScript Cheat Sheet (Expanded, W3Schools‑Style)

Structured reference divided into clear sections.

---

# 1. JavaScript Basics

## Embedding JavaScript

```
<script>
  console.log("Hello");
</script>
<script src="script.js"></script>
```

## Outputs

```
console.log()
document.write()
alert()
prompt()
confirm()
```

## Comments

```
// single line
/* multi line */
```

---

# 2. Variables

## Types

```
string, number, boolean, null, undefined, object, bigint, symbol
```

## Declarations

```
var a = 10;
let b = 20;
const c = 30;
```

## Operators

```
Arithmetic: + - * / % **
Comparison: == === != !== > < >= <=
Logical: && || !
Bitwise: & | ^ ~ << >> >>>
```

---

# 3. Control Flow

## If Else

```
if (age >= 18) { msg = "Adult"; }
else { msg = "Minor"; }
```

## Switch

```
switch(day){ case 0: break; default: }
```

---

# 4. Loops

## For

```
for (let i = 0; i < 5; i++){}
```

## While

```
while(i < 5){}
```

## Do While

```
do {} while()
```

## Control

```
break
continue
```

---

# 5. Functions

## Types

```
function fn(){}
const fn = function(){}
const fn = ()=>{}
```

---

# 6. Objects

```
const obj = { name:"Alex", age:18 };
obj.name;
obj.age = 20;
```

---

# 7. Arrays

```
const arr = [1,2,3];
arr.push(4);
arr.filter(x=>x>1);
arr.map(x=>x*2);
arr.reduce((a,b)=>a+b);
```

---

# 8. Strings

```
str.length
str.indexOf()
str.slice()
str.toUpperCase()
str.replace()
str.split()
```

---

# 9. Numbers & Math

```
Number("10")
parseInt("100px")
parseFloat("3.14")
Math.round()
Math.random()
Math.sqrt()
```

---

# 10. Dates

```
const d = new Date();
d.getFullYear();
d.setFullYear(2030);
```

---

# 11. DOM

## Selectors

```
document.getElementById()
document.querySelector()
document.querySelectorAll()
```

## Content

```
elem.innerHTML
elem.textContent
elem.value
```

## Styles

```
elem.style.color
elem.style.display
```

## Classes

```
elem.classList.add()
elem.classList.remove()
elem.classList.toggle()
```

## Create / Remove

```
const div = document.createElement("div");
document.body.appendChild(div);
elem.remove();
```

## Events

```
elem.addEventListener("click", fn);
```

---

# 12. Events Overview

```
Mouse: click, mouseenter, mouseleave
Keyboard: keydown, keyup
Form: submit, change, blur
```

---

# 13. JSON

```
const obj = JSON.parse('{"a":1}');
const json = JSON.stringify(obj);
localStorage.setItem("data", json);
JSON.parse(localStorage.getItem("data"));
```

---

# 14. Errors

```
try { throw "err"; }
catch(e){ console.log(e); }
finally{ console.log("done"); }
```

---

# 15. Regular Expressions

```
Patterns: digit, whitespace, boundary, +, ?, ^, $
Examples:
/abc/
```

---

# 16. Promises

```
const p = new Promise((res)=>res(10));
p.then(v=>console.log(v));
Promise.all([]);
Promise.race([]);
```

---

# 17. Advanced Functions

## Parameters & Defaults

```
function greet(name = "Guest"){
  return "Hello " + name;
}
```

## Rest Parameters

```
function sum(...nums){ return nums.reduce((a,b)=>a+b); }
```

## Call, Apply, Bind

```
fn.call(obj, a, b)
fn.apply(obj, [a, b])
const bound = fn.bind(obj)
```

---

# 18. Scopes & Closures

## Block / Function / Global Scope

```
let x = 10; // block
var y = 20; // function
```

## Closures

```
function outer(){
  let count = 0;
  return function(){ count++; return count; };
}
const counter = outer();
counter();
```

---

# 19. ES6+ Features

## Template Literals

```
`Hello ${name}`
```

## Destructuring

```
const {a, b} = obj;
const [x, y] = arr;
```

## Spread

```
const arr2 = [...arr, 4,5];
```

## Modules

```js
// export.js
export const x = 10;
export function fn(){}

// import
import { x, fn } from './export.js';
```

---

# 20. DOM Advanced

## Traversal

```
elem.parentNode
elem.children
elem.firstElementChild
elem.nextElementSibling
```

## Attributes

```
elem.getAttribute("src")
elem.setAttribute("href", "url")
elem.removeAttribute("disabled")
```

## Insert Adjacent

```
elem.insertAdjacentHTML("beforeend", "<p>Hi</p>")
```

## Event Object

```
elem.addEventListener("click", (e)=>{ console.log(e.target); })
```

---

# 21. Fetch API & AJAX

## Basic Fetch

```
fetch("/api")
  .then(res=>res.json())
  .then(data=>console.log(data))
  .catch(err=>console.error(err));
```

## Async/Await

```
async function getData(){
  try{
    const res = await fetch('/api');
    const data = await res.json();
    console.log(data);
  }catch(e){ console.error(e); }
}
```

## POST

```
fetch('/api',{
  method:'POST',
  headers:{'Content-Type':'application/json'},
  body:JSON.stringify({name:'Alex'})
})
```

---

# 22. Classes (ES6)

## Basic Class

```
class Person{
  constructor(name){ this.name = name; }
  speak(){ return this.name + ' speaks'; }
}
```

## Inheritance

```
class Student extends Person{
  constructor(name, grade){ super(name); this.grade = grade; }
}
```

---

# 23. Error Types

```
ReferenceError
SyntaxError
TypeError
RangeError
```

---

# 24. Storage APIs

## localStorage

```
localStorage.setItem('key','value')
localStorage.getItem('key')
```

## sessionStorage

```
sessionStorage.setItem('x',10)
```

## Cookies

```
document.cookie = "theme=dark; path=/; max-age=3600";
```

---

# 25. Timers

```
setTimeout(fn, 1000)
setInterval(fn, 500)
clearTimeout(id)
clearInterval(id)
```

---

# 26. Window & Browser APIs

```
window.location.href
window.history.back()
window.innerWidth
alert(), prompt(), confirm()
```

---

# 27. Modules & Bundling Concepts

```
ES Modules (import/export)
CommonJS (require/module.exports)
Bundlers: Webpack, Parcel, Vite
Transpiling: Babel
```

---

# 28. Advanced Array Methods

```
arr.find()
arr.findIndex()
arr.every()
arr.some()
arr.flat()
arr.flatMap()
```

---

# 29. Memory & Performance Basics

```
Avoid global variables
Prefer const & let over var
Use event delegation
Cache DOM selectors
```

---

# 30. Asynchronous Concepts

```
Event Loop
Call Stack
Task Queue
Microtasks (Promise)
```
