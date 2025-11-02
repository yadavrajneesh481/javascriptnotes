# 📚 Complete JavaScript Learning Guide: Notes, Examples & Interview Questions

## Table of Contents
1. [Week 1: JavaScript Fundamentals](#week-1)
2. [Week 2: Data Structures and Modern JavaScript](#week-2)
3. [Week 3: Advanced JavaScript Concepts](#week-3)
4. [Week 4: Advanced Concepts and Design Patterns](#week-4)
5. [Week 5: Modern Development and Project Work](#week-5)

---

# Week 1: JavaScript Fundamentals {#week-1}

## Day 1: Introduction to JavaScript

### What is JavaScript?

**Definition (Simple):** JavaScript is a programming language that makes websites interactive. It's like the "brain" of a website that makes things happen when you click buttons, type in forms, or move your mouse.

**Definition (Technical):** JavaScript is a lightweight, interpreted, dynamically-typed programming language that runs in web browsers and enables interactive web applications.

### Real-World Analogy
Think of a website like a restaurant:
- **HTML** = The menu (structure - what's available)
- **CSS** = The decoration (styling - how it looks)  
- **JavaScript** = The waiter (interactivity - makes things happen)

When you click a button, JavaScript is the waiter who takes your order and makes something happen!

### Why JavaScript?
```
┌─────────────────────────────────────┐
│     Why Learn JavaScript?           │
├─────────────────────────────────────┤
│ ✓ Runs in every web browser         │
│ ✓ Makes websites interactive        │
│ ✓ Can run on servers (Node.js)      │
│ ✓ Used for games, apps, websites    │
│ ✓ Easy to learn for beginners       │
└─────────────────────────────────────┘
```

### Setting Up Your Environment

**What You Need:**
1. **Code Editor** - Where you write code
   - VS Code (recommended)
   - Sublime Text
   - Atom

2. **Web Browser** - Where code runs
   - Chrome
   - Firefox
   - Safari

3. **Developer Tools** - Built into browsers
   - Press `F12` or `Ctrl+Shift+I` to open

### JavaScript in HTML

**Method 1: Inline Script (Inside HTML)**
```html
<!DOCTYPE html>
<html>
<head>
    <title>My First JavaScript</title>
</head>
<body>
    <h1>Hello World</h1>
    <script>
        console.log("I am inside HTML!");
    </script>
</body>
</html>
```

**Method 2: External File (Separate JS File)**
Create `script.js`:
```javascript
console.log("I am in a separate file!");
```

In HTML:
```html
<script src="script.js"></script>
```

### Your First JavaScript Code
```javascript
// This is a comment - computer ignores this
console.log("Hello, World!"); // Prints to console

// You can print anything
console.log(42);
console.log(true);
console.log("JavaScript is awesome!");
```

**What is `console.log()`?**
- It's like a printer for developers
- Prints messages to the browser console
- Helps you debug and see what's happening

### 🎯 Key Points
- JavaScript makes websites interactive
- It runs in your browser
- `console.log()` helps you see what's happening
- You can write JS inside HTML or in separate files

### 💡 Interview Questions (Hinglish)

**Q1: JavaScript kya hai aur HTML/CSS se kaise alag hai?**

**A:** JavaScript ek programming language hai jo websites ko interactive banata hai. HTML structure deta hai, CSS styling deta hai, lekin JavaScript action deta hai - jab aap kisi cheez par click karte ho to kuch hota hai. Yeh browser mein chalti hai.

**Q2: `console.log()` ka use kya hai?**

**A:** `console.log()` ek debugging tool hai. Isse aap apne code ka output dekh sakte ho. Jab aap browser mein F12 dabate ho aur console khol lete ho, to wahan aapka output dikh jaata hai.

---

## Day 2: Variables and Data Types

### What is a Variable?

**Definition:** A variable is like a labeled box where you store information. You give the box a name, and inside it you keep some value.

**Real-World Analogy:**
```
Imagine you have a shelf in your room:
┌──────────────────────┐
│  Box labeled "name"  │
│  Contains: "Raj"     │
└──────────────────────┘

In JavaScript:
let name = "Raj";  // Created a box, gave it a name, put value inside
```

### Variable Declaration Methods

**1. `let` - Modern way (Recommended)**
```javascript
let age = 25;
age = 26; // Can change the value
console.log(age); // Output: 26
```

**2. `const` - Constant (Cannot change)**
```javascript
const pi = 3.14;
pi = 3.15; // ❌ ERROR! Cannot change
```

**3. `var` - Old way (Don't use in new code)**
```javascript
var name = "Ali";
// Works but has confusing behavior - avoid it!
```

### Comparison Table
```
┌────────┬──────────────┬──────────────┬──────────────┐
│ Type   │ Can Change?  │ Scope        │ When to Use  │
├────────┼──────────────┼──────────────┼──────────────┤
│ let    │ Yes          │ Block scope  │ Most of time │
│ const  │ No           │ Block scope  │ Fixed values │
│ var    │ Yes          │ Function     │ Never (old)  │
└────────┴──────────────┴──────────────┴──────────────┘
```

### Primitive Data Types

**What are Primitives?**
Primitives are the basic building blocks of data. They're like LEGO pieces - simple, but you can build complex things with them.

#### 1. **String** - Text
```javascript
let name = "Priya";
let message = 'Hello World';
let empty = ""; // Empty string

console.log(name);     // Output: Priya
console.log(message);  // Output: Hello World
```

#### 2. **Number** - Whole numbers and decimals
```javascript
let age = 25;           // Whole number
let height = 5.8;       // Decimal
let temperature = -10;  // Negative

console.log(age + 5);   // Output: 30
console.log(height * 2); // Output: 11.6
```

#### 3. **Boolean** - True or False
```javascript
let isStudent = true;
let isRaining = false;

console.log(isStudent);  // Output: true
console.log(isRaining);  // Output: false
```

#### 4. **Null** - Intentional "nothing"
```javascript
let value = null; // Programmer said: "This is nothing"
console.log(value); // Output: null
```

#### 5. **Undefined** - Unintentional "nothing"
```javascript
let x;
console.log(x); // Output: undefined (not assigned yet)
```

#### 6. **Symbol** - Unique identifier (Advanced)
```javascript
let id = Symbol("unique");
// Each symbol is unique, even if created with same description
```

#### 7. **BigInt** - Very large numbers
```javascript
let bigNumber = 123456789012345678901234567890n;
console.log(bigNumber);
```

### Type Checking
```javascript
// Using typeof operator
console.log(typeof "hello");      // Output: "string"
console.log(typeof 42);           // Output: "number"
console.log(typeof true);         // Output: "boolean"
console.log(typeof undefined);    // Output: "undefined"
console.log(typeof null);         // Output: "object" (quirk!)
```

### Type Conversion

**String to Number:**
```javascript
let text = "42";
let number = Number(text);
console.log(number);        // Output: 42 (as number)
console.log(typeof number); // Output: "number"
```

**Number to String:**
```javascript
let num = 42;
let text = String(num);
console.log(text);        // Output: "42" (as text)
console.log(typeof text); // Output: "string"
```

**To Boolean:**
```javascript
let value = "hello";
let bool = Boolean(value);
console.log(bool); // Output: true
```

### 🎯 Key Points
- Variables store information
- Use `let` for most cases, `const` for fixed values
- 7 primitive types: string, number, boolean, null, undefined, symbol, bigint
- Use `typeof` to check data type
- You can convert between types

### 💡 Interview Questions (Hinglish)

**Q1: `let`, `const`, aur `var` mein kya difference hai?**

**A:** 
- `let` aur `const` modern hain, `var` purana hai
- `let` se value change kar sakte ho, `const` se nahi
- `let` aur `const` block scope follow karte hain, `var` nahi
- Naye code mein `let` aur `const` use karo, `var` kabhi nahi

**Q2: Null aur Undefined mein kya difference hai?**

**A:** 
- `null` = programmer ne khud likha "yeh nothing hai"
- `undefined` = variable create hua par value assign nahi ki
- Dono "nothing" hain lekin different reasons se

**Q3: Type conversion kya hota hai? Example do.**

**A:** Jab aap ek data type ko dusre mein convert karte ho. Jaise:
```javascript
let text = "42";
let num = Number(text); // String ko number mein convert kiya
```

---

## Day 3: Operators and Expressions

### What is an Operator?

**Definition:** An operator is a symbol that tells JavaScript to do something with values. Like `+` tells it to add, `-` tells it to subtract.

**Real-World Analogy:**
```
Operators are like kitchen tools:
+ is like a mixer (combines things)
- is like a knife (takes away)
* is like an oven (multiplies effort)
/ is like dividing a pizza
```

### Arithmetic Operators
```javascript
let a = 10;
let b = 3;

console.log(a + b);  // 13 (Addition)
console.log(a - b);  // 7  (Subtraction)
console.log(a * b);  // 30 (Multiplication)
console.log(a / b);  // 3.33... (Division)
console.log(a % b);  // 1 (Remainder/Modulo)
console.log(a ** 2); // 100 (Exponent/Power)
```

**Modulo Operator (%) - What is it?**
```javascript
// Modulo gives the REMAINDER after division
console.log(10 % 3);  // Output: 1 (10 ÷ 3 = 3 remainder 1)
console.log(20 % 5);  // Output: 0 (20 ÷ 5 = 4 remainder 0)

// Real use: Check if number is even or odd
let num = 7;
if (num % 2 === 0) {
    console.log("Even");
} else {
    console.log("Odd"); // Output: Odd
}
```

### Assignment Operators
```javascript
let x = 10;

x = x + 5;    // x is now 15
x += 5;       // Same as above, shorter way (x = 20)

x = x - 3;    // x is now 17
x -= 3;       // Same as above, shorter way (x = 14)

x *= 2;       // x = x * 2 (x = 28)
x /= 2;       // x = x / 2 (x = 14)
x %= 3;       // x = x % 3 (x = 2)
```

### Comparison Operators
These operators compare two values and return `true` or `false`.

```javascript
let a = 10;
let b = 5;

console.log(a > b);   // true (10 greater than 5?)
console.log(a < b);   // false (10 less than 5?)
console.log(a >= 10); // true (10 greater than or equal to 10?)
console.log(a <= 10); // true (10 less than or equal to 10?)
console.log(a == b);  // false (10 equal to 5?)
console.log(a != b);  // true (10 not equal to 5?)
```

### Equality: `==` vs `===`

**`==` (Loose Equality) - Converts types**
```javascript
console.log(5 == "5");   // true (converts "5" to 5, then compares)
console.log(0 == false); // true (converts false to 0)
```

**`===` (Strict Equality) - No conversion**
```javascript
console.log(5 === "5");   // false (different types)
console.log(0 === false); // false (different types)
```

**⚠️ Always use `===` in new code!**

### Logical Operators
```
┌──────────┬──────────────────────────────────────┐
│ Operator │ Meaning                              │
├──────────┼──────────────────────────────────────┤
│ &&       │ AND - Both must be true              │
│ ||       │ OR - At least one must be true       │
│ !        │ NOT - Flips true to false            │
└──────────┴──────────────────────────────────────┘
```

**AND Operator (&&)**
```javascript
let age = 25;
let hasLicense = true;

if (age >= 18 && hasLicense) {
    console.log("Can drive"); // Output: Can drive
}
// Both conditions must be true
```

**OR Operator (||)**
```javascript
let isWeekend = true;
let isHoliday = false;

if (isWeekend || isHoliday) {
    console.log("No school"); // Output: No school
}
// At least one must be true
```

**NOT Operator (!)**
```javascript
let isRaining = true;

if (!isRaining) {
    console.log("Go outside");
} else {
    console.log("Stay inside"); // Output: Stay inside
}
// ! flips the value
```

### Operator Precedence

**What is Precedence?**
Order in which operations happen. Like in math: multiplication before addition.

```javascript
// Math order: Multiply first, then add
let result = 2 + 3 * 4;
console.log(result); // Output: 14 (not 20)
// Because 3 * 4 = 12, then 2 + 12 = 14

// Use parentheses to change order
let result2 = (2 + 3) * 4;
console.log(result2); // Output: 20
```

**Precedence Order (High to Low):**
```
1. Parentheses ()
2. Exponentiation **
3. Multiplication, Division, Modulo (*, /, %)
4. Addition, Subtraction (+, -)
5. Comparison (>, <, >=, <=)
6. Equality (==, ===, !=, !==)
7. Logical AND (&&)
8. Logical OR (||)
```

### Type Coercion

**Definition:** JavaScript automatically converting one type to another.

```javascript
// String + Number = String (concatenation)
console.log("5" + 3);      // Output: "53" (not 8!)
console.log(5 + "3");      // Output: "53"

// String - Number = Number (subtraction)
console.log("10" - "3");   // Output: 7
console.log("10" - 3);     // Output: 7

// String * Number = Number
console.log("5" * 2);      // Output: 10
```

**⚠️ Coercion can be confusing! Use strict equality `===` to avoid issues.**

### 🎯 Key Points
- Operators perform actions on values
- Comparison operators return true/false
- Use `===` instead of `==`
- Operator precedence matters
- Type coercion can cause unexpected results

### 💡 Interview Questions (Hinglish)

**Q1: `==` aur `===` mein kya difference hai?**

**A:**
- `==` loose equality hai - type conversion karta hai
- `===` strict equality hai - type conversion nahi karta
- Example: `5 == "5"` true hai, lekin `5 === "5"` false hai
- Hamesha `===` use karo kyunki zyada safe hai

**Q2: Type coercion kya hai? Example do.**

**A:**
JavaScript automatically type convert karta hai. Jaise:
```javascript
console.log("5" + 3);  // "53" (string + number = string)
console.log("5" - 3);  // 2 (string - number = number)
```

**Q3: Operator precedence kya hota hai?**

**A:**
Jis order mein operations hote hain. Jaise math mein multiply pehle hota hai add se:
```javascript
2 + 3 * 4 = 14 (not 20)
// kyunki 3 * 4 = 12, phir 2 + 12 = 14
```

---

## Day 4: Control Flow

### What is Control Flow?

**Definition:** Control flow is deciding which code to run based on conditions. Like a decision tree.

**Real-World Analogy:**
```
Imagine you're deciding what to wear:
IF it's raining
    THEN wear raincoat
ELSE IF it's cold
    THEN wear sweater
ELSE
    THEN wear t-shirt
```

### If Statement

**Basic If:**
```javascript
let age = 18;

if (age >= 18) {
    console.log("You are an adult"); // Output: You are an adult
}
```

**If-Else:**
```javascript
let age = 15;

if (age >= 18) {
    console.log("You are an adult");
} else {
    console.log("You are a minor"); // Output: You are a minor
}
```

**If-Else If-Else:**
```javascript
let score = 75;

if (score >= 90) {
    console.log("Grade: A");
} else if (score >= 80) {
    console.log("Grade: B");
} else if (score >= 70) {
    console.log("Grade: C"); // Output: Grade: C
} else {
    console.log("Grade: F");
}
```

### Switch Statement

**When to use:** When you have many conditions checking the same variable.

```javascript
let day = 3;

switch (day) {
    case 1:
        console.log("Monday");
        break;
    case 2:
        console.log("Tuesday");
        break;
    case 3:
        console.log("Wednesday"); // Output: Wednesday
        break;
    default:
        console.log("Invalid day");
}
```

**Why `break`?**
```javascript
// Without break - falls through
let day = 1;
switch (day) {
    case 1:
        console.log("Monday");
        // No break! Falls through
    case 2:
        console.log("Tuesday");
        break;
}
// Output: Monday
//         Tuesday (unexpected!)

// With break - stops
let day = 1;
switch (day) {
    case 1:
        console.log("Monday");
        break; // Stops here
    case 2:
        console.log("Tuesday");
        break;
}
// Output: Monday (only)
```

### Ternary Operator

**Definition:** A shorthand way to write if-else in one line.

**Syntax:** `condition ? valueIfTrue : valueIfFalse`

```javascript
let age = 20;

// Traditional if-else
if (age >= 18) {
    console.log("Adult");
} else {
    console.log("Minor");
}

// Ternary operator (same thing, one line)
age >= 18 ? console.log("Adult") : console.log("Minor");

// Or assign to variable
let status = age >= 18 ? "Adult" : "Minor";
console.log(status); // Output: Adult
```

**Nested Ternary (Use carefully!):**
```javascript
let score = 75;
let grade = score >= 90 ? "A" : score >= 80 ? "B" : score >= 70 ? "C" : "F";
console.log(grade); // Output: C
```

### Truthy and Falsy Values

**Definition:** In JavaScript, some values are considered "true" and some "false" in boolean context.

**Falsy Values (Considered false):**
```javascript
if (false) { }     // false
if (0) { }         // zero
if ("") { }        // empty string
if (null) { }      // null
if (undefined) { } // undefined
if (NaN) { }       // Not a Number
// All above blocks won't execute
```

**Truthy Values (Considered true):**
```javascript
if (true) { console.log("true"); }           // Executes
if (1) { console.log("1"); }                 // Executes
if ("hello") { console.log("hello"); }       // Executes
if ([]) { console.log("array"); }            // Executes
if ({}) { console.log("object"); }           // Executes
if ("0") { console.log("string 0"); }        // Executes
```

**Practical Example:**
```javascript
let user = ""; // Empty string (falsy)

if (user) {
    console.log("User logged in");
} else {
    console.log("Please log in"); // Output: Please log in
}

let user2 = "Raj"; // Non-empty string (truthy)

if (user2) {
    console.log("Welcome " + user2); // Output: Welcome Raj
}
```

### Diagram: Control Flow
```
┌─────────────────┐
│  Start Program  │
└────────┬────────┘
         │
┌────────▼────────┐
│  Check Condition│
└────┬─────────┬──┘
     │         │
   True │         │ False
     │         │
┌────▼──┐  ┌───▼────┐
│Block 1│  │Block 2 │
└────┬──┘  └───┬────┘
     │         │
┌────▼─────────▼──┐
│  Continue Code  │
└─────────────────┘
```

### 🎯 Key Points
- If-else makes decisions based on conditions
- Switch is good for multiple conditions on same variable
- Ternary operator is shorthand for if-else
- Understand truthy and falsy values
- Control flow determines which code runs

### 💡 Interview Questions (Hinglish)

**Q1: If-else aur switch mein kya difference hai?**

**A:**
- If-else complex conditions ke liye zyada flexible hai
- Switch ek variable ke multiple values check karta hai
- Switch cleaner hota hai jab bohot saare cases hain
- Dono same kaam kar sakte hain, lekin different situations mein better hote hain

**Q2: Ternary operator kya hai? Kab use karte ho?**

**A:**
Ternary operator if-else ka shorthand hai:
```javascript
condition ? valueIfTrue : valueIfFalse
```
Use karte ho jab simple if-else hona ho, ek line mein likha ja sake.

**Q3: Truthy aur falsy kya hote hain?**

**A:**
- Falsy values: false, 0, "", null, undefined, NaN
- Truthy values: sab kuch aur (true, 1, "hello", [], {})
- Jab condition mein value daalte ho to JavaScript check karta hai truthy hai ya falsy

---

## Day 5: Loops and Iteration

### What is a Loop?

**Definition:** A loop repeats code multiple times without writing it again and again.

**Real-World Analogy:**
```
Imagine you need to say "Hello" 100 times.
Without loop: Hello, Hello, Hello, Hello... (write 100 times)
With loop: for (let i = 0; i < 100; i++) { console.log("Hello"); }
```

### For Loop

**Syntax:**
```javascript
for (initialization; condition; increment) {
    // Code to repeat
}
```

**Example:**
```javascript
for (let i = 0; i < 5; i++) {
    console.log(i);
}
// Output:
// 0
// 1
// 2
// 3
// 4
```

**Step-by-step:**
```
1. let i = 0        → Create variable i, set to 0
2. i < 5            → Check: is 0 < 5? Yes! Run code
3. console.log(0)   → Print 0
4. i++              → Increase i to 1
5. i < 5            → Check: is 1 < 5? Yes! Run code
6. console.log(1)   → Print 1
... (repeats until i = 5, then stops)
```

**Diagram:**
```
┌─────────────────────┐
│ Initialize: i = 0   │
└──────────┬──────────┘
           │
┌────▼─────────┐
│ Check i < 5? │
└────┬─────┬───┘
     │     │
   Yes│     │No → Exit Loop
     │     │
┌────▼──┐  └──────────────┐
│Run    │                 │
│Code   │                 │
└────┬──┘                 │
     │                    │
┌────▼──────┐             │
│ i++        │             │
└────┬───────┘             │
     │                    │
     └────────┬───────────┘
              │
┌─────▼─────┐
│ Next Loop  │
└────────────┘
```

### While Loop

**Syntax:**
```javascript
while (condition) {
    // Code to repeat
    // MUST change something to make condition false eventually
}
```

**Example:**
```javascript
let i = 0;
while (i < 5) {
    console.log(i);
    i++; // IMPORTANT: Must increase i, or loop runs forever!
}
// Output: 0, 1, 2, 3, 4
```

**⚠️ Infinite Loop (Don't do this!):**
```javascript
while (true) {
    console.log("Help! I'm stuck!");
    // No way to exit - runs forever!
}
```

### Do-While Loop

**Syntax:**
```javascript
do {
    // Code runs at least once
} while (condition);
```

**Example:**
```javascript
let i = 0;
do {
    console.log(i);
    i++;
} while (i < 5);
// Output: 0, 1, 2, 3, 4
```

**Difference from While:**
```javascript
// While - checks condition first
let i = 10;
while (i < 5) {
    console.log(i); // Never runs (10 is not < 5)
}

// Do-While - runs at least once
let i = 10;
do {
    console.log(i); // Runs once (10), then checks condition
} while (i < 5);
// Output: 10 (runs once even though condition is false)
```

### For...of Loop

**What is it?** Loops through values in an array or iterable.

```javascript
let fruits = ["Apple", "Banana", "Orange"];

for (let fruit of fruits) {
    console.log(fruit);
}
// Output:
// Apple
// Banana
// Orange
```

**Simpler than traditional for loop!**

### For...in Loop

**What is it?** Loops through keys/indexes of an object or array.

```javascript
let person = {
    name: "Raj",
    age: 25,
    city: "Delhi"
};

for (let key in person) {
    console.log(key + ": " + person[key]);
}
// Output:
// name: Raj
// age: 25
// city: Delhi
```

**For...of vs For...in:**
```
┌──────────┬─────────────────────┬──────────────────┐
│ Type     │ What it gives        │ Best for         │
├──────────┼─────────────────────┼──────────────────┤
│ for...of │ Values              │ Arrays           │
│ for...in │ Keys/Indexes        │ Objects          │
└──────────┴─────────────────────┴──────────────────┘
```

### Break and Continue

**Break - Exit loop completely:**
```javascript
for (let i = 0; i < 10; i++) {
    if (i === 5) {
        break; // Exit loop when i = 5
    }
    console.log(i);
}
// Output: 0, 1, 2, 3, 4
```

**Continue - Skip current iteration:**
```javascript
for (let i = 0; i < 5; i++) {
    if (i === 2) {
        continue; // Skip this iteration
    }
    console.log(i);
}
// Output: 0, 1, 3, 4 (2 is skipped)
```

### Labeled Statements

**Advanced feature - rarely used:**
```javascript
outerLoop: for (let i = 0; i < 3; i++) {
    for (let j = 0; j < 3; j++) {
        if (i === 1 && j === 1) {
            break outerLoop; // Breaks outer loop
        }
        console.log(i, j);
    }
}
```

### 🎯 Key Points
- Loops repeat code multiple times
- For loop: when you know how many times
- While loop: when you don't know how many times
- For...of: loop through array values
- For...in: loop through object keys
- Break exits loop, continue skips iteration

### 💡 Interview Questions (Hinglish)

**Q1: For, while, aur do-while loop mein kya difference hai?**

**A:**
- For loop: jab pata ho kitni baar chalana hai
- While loop: jab condition check karni ho
- Do-while: kam se kam ek baar chalega, phir condition check hoga
- Example: for (let i=0; i<5; i++) vs while(i<5) { i++; }

**Q2: For...of aur for...in mein kya difference hai?**

**A:**
- For...of array ke values deta hai
- For...in object ke keys deta hai
- Example:
```javascript
let arr = [1, 2, 3];
for (let val of arr) console.log(val); // 1, 2, 3
let obj = {a: 1};
for (let key in obj) console.log(key); // "a"
```

**Q3: Break aur continue kya karte hain?**

**A:**
- Break: loop ko completely exit kar deta hai
- Continue: current iteration ko skip kar deta hai, agle iteration par jaata hai
- Example: break se loop band ho jaata hai, continue se sirf ek iteration skip hota hai

---

## Day 6: Functions Fundamentals

### What is a Function?

**Definition:** A function is a reusable block of code that performs a specific task.

**Real-World Analogy:**
```
Function = Recipe
- Recipe name = Function name
- Ingredients = Parameters
- Instructions = Function body
- Result = Return value

You write recipe once, use it many times!
```

### Function Declaration

**Syntax:**
```javascript
function greet(name) {
    console.log("Hello, " + name);
}

greet("Raj");   // Output: Hello, Raj
greet("Priya"); // Output: Hello, Priya
```

**Parts of a function:**
```javascript
function greet(name) {
│        │      │
│        │      └─ Parameter (input)
│        └────── Function name
└───────────── Keyword
```

### Function Expression

**Alternative way to create function:**
```javascript
const add = function(a, b) {
    return a + b;
};

console.log(add(5, 3)); // Output: 8
```

### Arrow Functions

**Modern, shorter syntax:**
```javascript
// Traditional
function add(a, b) {
    return a + b;
}

// Arrow function
const add = (a, b) => {
    return a + b;
};

// Even shorter (one line)
const add = (a, b) => a + b;

console.log(add(5, 3)); // Output: 8
```

**Arrow function with one parameter:**
```javascript
const square = x => x * x;
console.log(square(5)); // Output: 25
```

**Arrow function with no parameters:**
```javascript
const greet = () => "Hello!";
console.log(greet()); // Output: Hello!
```

### Parameters vs Arguments

**Parameters:** Variables in function definition
**Arguments:** Values passed when calling function

```javascript
//           ↓ Parameters
function add(a, b) {
    return a + b;
}

//    ↓ Arguments
add(5, 3);
```

### Return Value

**What is return?** Sends value back from function.

```javascript
function multiply(a, b) {
    return a * b; // Sends result back
}

let result = multiply(4, 5);
console.log(result); // Output: 20

// Without return
function greet(name) {
    console.log("Hello, " + name);
    // No return, so returns undefined
}

let greeting = greet("Raj");
console.log(greeting); // Output: undefined
```

### Default Parameters

**What if user doesn't pass argument?**

```javascript
// Without default
function greet(name) {
    console.log("Hello, " + name);
}
greet(); // Output: Hello, undefined

// With default
function greet(name = "Guest") {
    console.log("Hello, " + name);
}

greet();      // Output: Hello, Guest
greet("Raj"); // Output: Hello, Raj
```

### Rest Parameters

**What if you don't know how many arguments?**

```javascript
function sum(...numbers) {
    let total = 0;
    for (let num of numbers) {
        total += num;
    }
    return total;
}

console.log(sum(1, 2, 3));       // Output: 6
console.log(sum(1, 2, 3, 4, 5)); // Output: 15
```

**How it works:**
```javascript
sum(1, 2, 3)
↓
numbers = [1, 2, 3]  (array of all arguments)
```

### Function Scope

**What is scope?** Where a variable is accessible.

```javascript
let global = "I'm global"; // Global scope

function myFunction() {
    let local = "I'm local"; // Local scope
    console.log(global); // Can access global
    console.log(local);  // Can access local
}

console.log(global); // Works
console.log(local);  // ERROR! Not accessible outside function
```

### Practical Example: Calculator
```javascript
function calculate(a, b, operation) {
    if (operation === "+") {
        return a + b;
    } else if (operation === "-") {
        return a - b;
    } else if (operation === "*") {
        return a * b;
    } else if (operation === "/") {
        return a / b;
    }
}

console.log(calculate(10, 5, "+"));  // Output: 15
console.log(calculate(10, 5, "-"));  // Output: 5
console.log(calculate(10, 5, "*"));  // Output: 50
console.log(calculate(10, 5, "/"));  // Output: 2
```

### 🎯 Key Points
- Functions are reusable blocks of code
- Parameters are inputs, return is output
- Arrow functions are modern syntax
- Default parameters provide fallback values
- Rest parameters accept multiple arguments
- Functions have their own scope

### 💡 Interview Questions (Hinglish)

**Q1: Function declaration aur arrow function mein kya difference hai?**

**A:**
- Function declaration: `function name() { }`
- Arrow function: `const name = () => { }`
- Arrow function shorter aur modern hai
- Arrow function mein `this` different hota hai (advanced topic)

**Q2: Parameters aur arguments kya hote hain?**

**A:**
- Parameters: function definition mein likhe jaate hain
- Arguments: function call karte time pass karte hain
```javascript
function add(a, b) { } // a, b = parameters
add(5, 3);             // 5, 3 = arguments
```

**Q3: Return kya karta hai?**

**A:**
Return function se value wapas bhejta hai:
```javascript
function add(a, b) {
    return a + b; // Value wapas bhej diya
}
let result = add(5, 3); // result = 8
```

---

## Day 7: Week 1 Review and Practice

### Week 1 Summary

This week we covered the fundamental building blocks of JavaScript:

**Day 1: Introduction**
- What JavaScript is and why it's important
- Setting up development environment
- Writing your first JavaScript code

**Day 2: Variables & Data Types**
- Storing information in variables (`let`, `const`, `var`)
- 7 primitive data types (string, number, boolean, etc.)
- Type checking and conversion

**Day 3: Operators**
- Arithmetic operations (+, -, *, /, %, **)
- Comparison and logical operators
- Understanding `===` vs `==`
- Operator precedence and type coercion

**Day 4: Control Flow**
- Making decisions with if-else statements
- Switch statements for multiple conditions
- Ternary operator for concise conditions
- Truthy and falsy values

**Day 5: Loops**
- Repeating code with for, while, do-while loops
- Iterating through arrays with for...of
- Iterating through objects with for...in
- Loop control with break and continue

**Day 6: Functions**
- Creating reusable code blocks
- Function declarations vs expressions vs arrow functions
- Parameters, arguments, and return values
- Default and rest parameters
- Function scope

### How Everything Connects

```
Variables store data → Operators manipulate data → Control flow decides what to do → Loops repeat actions → Functions organize everything
```

### Practice Exercises

**Exercise 1: Personal Information**
```javascript
// Create variables for personal info
const name = "Your Name";
let age = 25;
let isStudent = true;

// Use operators and control flow
if (age >= 18 && isStudent) {
    console.log(name + " is an adult student");
} else {
    console.log(name + " is either minor or not a student");
}
```

**Exercise 2: Grade Calculator**
```javascript
function calculateGrade(score) {
    if (score >= 90) return "A";
    else if (score >= 80) return "B";
    else if (score >= 70) return "C";
    else if (score >= 60) return "D";
    else return "F";
}

// Test with different scores
console.log(calculateGrade(95)); // A
console.log(calculateGrade(75)); // C
console.log(calculateGrade(55)); // F
```

**Exercise 3: Number Operations**
```javascript
function numberOperations(num) {
    console.log("Number:", num);
    console.log("Is even:", num % 2 === 0);
    console.log("Square:", num ** 2);
    console.log("Is positive:", num > 0);
}

numberOperations(7);
// Output:
// Number: 7
// Is even: false
// Square: 49
// Is positive: true
```

**Exercise 4: Array Processing**
```javascript
const numbers = [1, 2, 3, 4, 5];
let sum = 0;

// Calculate sum using loop
for (let num of numbers) {
    sum += num;
}

console.log("Sum:", sum);        // 15
console.log("Average:", sum / numbers.length); // 3
```

### Common Mistakes to Avoid

1. **Using `var` instead of `let`/`const`**
   ```javascript
   // ❌ Don't do this
   var name = "John";
   
   // ✅ Do this
   let name = "John";
   const PI = 3.14;
   ```

2. **Using `==` instead of `===`**
   ```javascript
   // ❌ Confusing
   if (5 == "5") // true (type coercion)
   
   // ✅ Clear
   if (5 === "5") // false (strict comparison)
   ```

3. **Forgetting to increment in while loops**
   ```javascript
   // ❌ Infinite loop
   let i = 0;
   while (i < 5) {
       console.log(i);
       // Forgot i++
   }
   
   // ✅ Proper loop
   let i = 0;
   while (i < 5) {
       console.log(i);
       i++; // Don't forget this!
   }
   ```

4. **Not using return in functions**
   ```javascript
   // ❌ Returns undefined
   function add(a, b) {
       a + b; // No return
   }
   
   // ✅ Returns the sum
   function add(a, b) {
       return a + b;
   }
   ```

### 💡 Week 1 Interview Questions (Hinglish)

**Q1: JavaScript mein variable declare karne ke kitne tarike hain?**

**A:** Teen tarike hain:
- `let` - modern way, value change kar sakte hain
- `const` - constant, value change nahi kar sakte
- `var` - purana way, avoid karna chahiye

**Q2: Truthy aur falsy values kya hain? Examples do.**

**A:** 
- Falsy: false, 0, "", null, undefined, NaN
- Truthy: baaki sab kuch (true, 1, "hello", [], {})
- If condition mein use hote hain

**Q3: Function banane ke kitne ways hain?**

**A:** Teen main ways:
```javascript
// Function declaration
function name() { }

// Function expression  
const name = function() { };

// Arrow function
const name = () => { };
```

**Q4: Loop kab use karte hain aur kitne types ke hote hain?**

**A:** Jab same code baar baar chalana ho:
- `for` - jab pata ho kitni baar
- `while` - jab condition check karni ho
- `do-while` - kam se kam ek baar chalana ho
- `for...of` - array values ke liye
- `for...in` - object keys ke liye

### Next Week Preview

Week 2 will cover:
- Arrays and their methods
- Objects and object manipulation
- Destructuring and spread operator
- Template literals and modern syntax
- Error handling basics

Keep practicing these fundamentals - they're the foundation for everything else!
---

# Week 2: Data Structures and Modern JavaScript {#week-2}

## Day 8: Arrays - Introduction and Basic Methods

### What is an Array?

**Definition:** An array is like a list that can hold multiple values in a specific order. Each item has a position (index) starting from 0.

**Real-World Analogy:**
```
Array = Shopping List
┌─────────────────┐
│ 0: Milk         │ ← Index 0
│ 1: Bread        │ ← Index 1  
│ 2: Eggs         │ ← Index 2
│ 3: Butter       │ ← Index 3
└─────────────────┘
```

### Creating Arrays

**Method 1: Array Literal (Recommended)**
```javascript
let fruits = ["Apple", "Banana", "Orange"];
let numbers = [1, 2, 3, 4, 5];
let mixed = ["Hello", 42, true, null];
let empty = [];
```

**Method 2: Array Constructor**
```javascript
let fruits = new Array("Apple", "Banana", "Orange");
let numbers = new Array(5); // Creates array with 5 empty slots
```

### Accessing Array Elements

```javascript
let fruits = ["Apple", "Banana", "Orange"];

console.log(fruits[0]);  // Output: Apple (first element)
console.log(fruits[1]);  // Output: Banana (second element)
console.log(fruits[2]);  // Output: Orange (third element)
console.log(fruits[3]);  // Output: undefined (doesn't exist)

// Get array length
console.log(fruits.length); // Output: 3
```

### Array Indexing Diagram
```
Index:    0        1         2
        ┌─────┬─────────┬────────┐
Array:  │Apple│ Banana  │ Orange │
        └─────┴─────────┴────────┘
Length: 3 (but last index is 2!)
```

### Basic Array Methods

#### Adding Elements

**`push()` - Add to end**
```javascript
let fruits = ["Apple", "Banana"];
fruits.push("Orange");
console.log(fruits); // Output: ["Apple", "Banana", "Orange"]

// Can add multiple elements
fruits.push("Mango", "Grapes");
console.log(fruits); // Output: ["Apple", "Banana", "Orange", "Mango", "Grapes"]
```

**`unshift()` - Add to beginning**
```javascript
let fruits = ["Banana", "Orange"];
fruits.unshift("Apple");
console.log(fruits); // Output: ["Apple", "Banana", "Orange"]
```

#### Removing Elements

**`pop()` - Remove from end**
```javascript
let fruits = ["Apple", "Banana", "Orange"];
let removed = fruits.pop();
console.log(removed); // Output: Orange
console.log(fruits);  // Output: ["Apple", "Banana"]
```

**`shift()` - Remove from beginning**
```javascript
let fruits = ["Apple", "Banana", "Orange"];
let removed = fruits.shift();
console.log(removed); // Output: Apple
console.log(fruits);  // Output: ["Banana", "Orange"]
```

#### Finding Elements

**`indexOf()` - Find position of element**
```javascript
let fruits = ["Apple", "Banana", "Orange"];
console.log(fruits.indexOf("Banana")); // Output: 1
console.log(fruits.indexOf("Mango"));  // Output: -1 (not found)
```

**`includes()` - Check if element exists**
```javascript
let fruits = ["Apple", "Banana", "Orange"];
console.log(fruits.includes("Banana")); // Output: true
console.log(fruits.includes("Mango"));  // Output: false
```

#### Other Useful Methods

**`slice()` - Get portion of array (doesn't modify original)**
```javascript
let fruits = ["Apple", "Banana", "Orange", "Mango"];
let portion = fruits.slice(1, 3);
console.log(portion); // Output: ["Banana", "Orange"]
console.log(fruits);  // Output: ["Apple", "Banana", "Orange", "Mango"] (unchanged)
```

**`splice()` - Remove/add elements at specific position**
```javascript
let fruits = ["Apple", "Banana", "Orange"];

// Remove 1 element at index 1
fruits.splice(1, 1);
console.log(fruits); // Output: ["Apple", "Orange"]

// Add elements at index 1
fruits.splice(1, 0, "Mango", "Grapes");
console.log(fruits); // Output: ["Apple", "Mango", "Grapes", "Orange"]
```

### Looping Through Arrays

**Traditional for loop:**
```javascript
let fruits = ["Apple", "Banana", "Orange"];

for (let i = 0; i < fruits.length; i++) {
    console.log(i + ": " + fruits[i]);
}
// Output:
// 0: Apple
// 1: Banana
// 2: Orange
```

**For...of loop (Recommended):**
```javascript
let fruits = ["Apple", "Banana", "Orange"];

for (let fruit of fruits) {
    console.log(fruit);
}
// Output:
// Apple
// Banana
// Orange
```

**For...in loop (Gets indexes):**
```javascript
let fruits = ["Apple", "Banana", "Orange"];

for (let index in fruits) {
    console.log(index + ": " + fruits[index]);
}
// Output:
// 0: Apple
// 1: Banana
// 2: Orange
```

### Multi-dimensional Arrays

**Array of arrays:**
```javascript
let matrix = [
    [1, 2, 3],
    [4, 5, 6],
    [7, 8, 9]
];

console.log(matrix[0]);    // Output: [1, 2, 3]
console.log(matrix[0][0]); // Output: 1
console.log(matrix[1][2]); // Output: 6
```

### 🎯 Key Points
- Arrays store multiple values in order
- Index starts from 0, not 1
- Use `push()/pop()` for end, `unshift()/shift()` for beginning
- `slice()` doesn't modify original, `splice()` does
- Use for...of to loop through values

### 💡 Interview Questions (Hinglish)

**Q1: Array mein element add aur remove kaise karte hain?**

**A:**
- Add: `push()` (end mein), `unshift()` (start mein)
- Remove: `pop()` (end se), `shift()` (start se)
- Example: `arr.push("new")` end mein add karega

**Q2: `slice()` aur `splice()` mein kya difference hai?**

**A:**
- `slice()`: original array change nahi karta, copy return karta hai
- `splice()`: original array modify karta hai, elements add/remove kar sakta hai
- Example: `arr.slice(1,3)` vs `arr.splice(1,1)`

**Q3: Array mein loop kaise chalate hain?**

**A:** Teen main ways:
```javascript
// Traditional for
for (let i = 0; i < arr.length; i++) { }

// For...of (values)
for (let item of arr) { }

// For...in (indexes)  
for (let index in arr) { }
```

---

## Day 9: Array Methods - Map, Filter, Reduce

### Higher-Order Functions

**Definition:** Functions that take other functions as arguments or return functions. Array methods like map, filter, reduce are higher-order functions.

**Why use them?** They make code more readable and functional programming style.

### Map Method

**What it does:** Creates a new array by transforming each element using a function.

**Real-World Analogy:**
```
Map = Photo Filter
Original photos → Apply filter → New filtered photos
[1, 2, 3] → multiply by 2 → [2, 4, 6]
```

**Syntax:**
```javascript
let newArray = array.map(function(element, index, array) {
    // Return transformed element
});
```

**Examples:**

**Double all numbers:**
```javascript
let numbers = [1, 2, 3, 4, 5];
let doubled = numbers.map(function(num) {
    return num * 2;
});
console.log(doubled); // Output: [2, 4, 6, 8, 10]
console.log(numbers); // Output: [1, 2, 3, 4, 5] (unchanged)
```

**With arrow function (shorter):**
```javascript
let numbers = [1, 2, 3, 4, 5];
let doubled = numbers.map(num => num * 2);
console.log(doubled); // Output: [2, 4, 6, 8, 10]
```

**Transform strings:**
```javascript
let names = ["raj", "priya", "amit"];
let capitalized = names.map(name => name.toUpperCase());
console.log(capitalized); // Output: ["RAJ", "PRIYA", "AMIT"]
```

**Extract properties from objects:**
```javascript
let users = [
    { name: "Raj", age: 25 },
    { name: "Priya", age: 30 },
    { name: "Amit", age: 28 }
];

let names = users.map(user => user.name);
console.log(names); // Output: ["Raj", "Priya", "Amit"]
```

### Filter Method

**What it does:** Creates a new array with elements that pass a test function.

**Real-World Analogy:**
```
Filter = Sieve/Strainer
All items → Pass through filter → Only matching items
[1,2,3,4,5] → keep even numbers → [2,4]
```

**Syntax:**
```javascript
let newArray = array.filter(function(element, index, array) {
    // Return true to keep, false to remove
});
```

**Examples:**

**Filter even numbers:**
```javascript
let numbers = [1, 2, 3, 4, 5, 6];
let evenNumbers = numbers.filter(num => num % 2 === 0);
console.log(evenNumbers); // Output: [2, 4, 6]
```

**Filter by age:**
```javascript
let users = [
    { name: "Raj", age: 17 },
    { name: "Priya", age: 25 },
    { name: "Amit", age: 16 }
];

let adults = users.filter(user => user.age >= 18);
console.log(adults); 
// Output: [{ name: "Priya", age: 25 }]
```

**Filter strings by length:**
```javascript
let words = ["hi", "hello", "javascript", "code"];
let longWords = words.filter(word => word.length > 4);
console.log(longWords); // Output: ["hello", "javascript"]
```

### Reduce Method

**What it does:** Reduces array to a single value by applying a function cumulatively.

**Real-World Analogy:**
```
Reduce = Blender
Multiple ingredients → Blend together → Single smoothie
[1,2,3,4] → add all → 10
```

**Syntax:**
```javascript
let result = array.reduce(function(accumulator, element, index, array) {
    // Return new accumulator value
}, initialValue);
```

**Examples:**

**Sum all numbers:**
```javascript
let numbers = [1, 2, 3, 4, 5];
let sum = numbers.reduce((total, num) => total + num, 0);
console.log(sum); // Output: 15

// Step by step:
// total=0, num=1 → return 0+1=1
// total=1, num=2 → return 1+2=3  
// total=3, num=3 → return 3+3=6
// total=6, num=4 → return 6+4=10
// total=10, num=5 → return 10+5=15
```

**Find maximum:**
```javascript
let numbers = [3, 7, 2, 9, 1];
let max = numbers.reduce((maximum, num) => {
    return num > maximum ? num : maximum;
});
console.log(max); // Output: 9
```

**Count occurrences:**
```javascript
let fruits = ["apple", "banana", "apple", "orange", "banana", "apple"];
let count = fruits.reduce((counter, fruit) => {
    counter[fruit] = (counter[fruit] || 0) + 1;
    return counter;
}, {});
console.log(count); 
// Output: { apple: 3, banana: 2, orange: 1 }
```

### Chaining Methods

**You can chain multiple array methods together:**

```javascript
let numbers = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];

let result = numbers
    .filter(num => num % 2 === 0)  // Keep even: [2,4,6,8,10]
    .map(num => num * 2)           // Double: [4,8,12,16,20]
    .reduce((sum, num) => sum + num, 0); // Sum: 60

console.log(result); // Output: 60
```

### Comparison with Traditional Loops

**Traditional way:**
```javascript
let numbers = [1, 2, 3, 4, 5];
let doubled = [];

for (let i = 0; i < numbers.length; i++) {
    doubled.push(numbers[i] * 2);
}
console.log(doubled); // [2, 4, 6, 8, 10]
```

**Modern way with map:**
```javascript
let numbers = [1, 2, 3, 4, 5];
let doubled = numbers.map(num => num * 2);
console.log(doubled); // [2, 4, 6, 8, 10]
```

### 🎯 Key Points
- Map: transforms each element, returns new array
- Filter: keeps elements that pass test, returns new array  
- Reduce: combines all elements into single value
- All methods don't modify original array
- Can chain methods together for powerful operations

### 💡 Interview Questions (Hinglish)

**Q1: Map, filter, aur reduce kya karte hain?**

**A:**
- Map: har element ko transform karta hai, naya array return karta hai
- Filter: condition pass karne wale elements rakhta hai
- Reduce: sab elements ko combine karke ek value banata hai
- Example: `[1,2,3].map(x=>x*2)` gives `[2,4,6]`

**Q2: Reduce method kaise kaam karta hai?**

**A:**
Reduce accumulator use karta hai:
```javascript
[1,2,3].reduce((total, num) => total + num, 0)
// Step 1: total=0, num=1 → return 1
// Step 2: total=1, num=2 → return 3  
// Step 3: total=3, num=3 → return 6
```

**Q3: Method chaining kya hai?**

**A:**
Multiple methods ko ek saath use karna:
```javascript
arr.filter(x => x > 0).map(x => x * 2).reduce((a,b) => a + b)
```
Har method naya array return karta hai, so chain kar sakte hain.

---

## Day 10: Objects - Creation and Manipulation

### What is an Object?

**Definition:** An object is a collection of key-value pairs. It's like a container that holds related information about something.

**Real-World Analogy:**
```
Object = ID Card
┌─────────────────────┐
│ Name: Raj Sharma    │ ← Property
│ Age: 25             │ ← Property  
│ City: Delhi         │ ← Property
│ isStudent: true     │ ← Property
└─────────────────────┘

In JavaScript:
let person = {
    name: "Raj Sharma",
    age: 25,
    city: "Delhi", 
    isStudent: true
};
```

### Creating Objects

**Method 1: Object Literal (Most Common)**
```javascript
let person = {
    name: "Raj",
    age: 25,
    city: "Delhi",
    isStudent: true
};
```

**Method 2: Object Constructor**
```javascript
let person = new Object();
person.name = "Raj";
person.age = 25;
person.city = "Delhi";
```

**Method 3: Constructor Function**
```javascript
function Person(name, age, city) {
    this.name = name;
    this.age = age;
    this.city = city;
}

let person = new Person("Raj", 25, "Delhi");
```

### Accessing Object Properties

**Dot Notation (Recommended):**
```javascript
let person = {
    name: "Raj",
    age: 25,
    city: "Delhi"
};

console.log(person.name); // Output: Raj
console.log(person.age);  // Output: 25
```

**Bracket Notation:**
```javascript
console.log(person["name"]); // Output: Raj
console.log(person["age"]);  // Output: 25

// Useful when property name has spaces or special characters
let obj = {
    "first name": "Raj",
    "phone-number": "123456789"
};

console.log(obj["first name"]);    // Output: Raj
console.log(obj["phone-number"]);  // Output: 123456789
```

**Dynamic Property Access:**
```javascript
let person = { name: "Raj", age: 25 };
let property = "name";

console.log(person[property]); // Output: Raj (same as person.name)
```

### Adding and Modifying Properties

```javascript
let person = {
    name: "Raj",
    age: 25
};

// Add new property
person.city = "Delhi";
person["country"] = "India";

// Modify existing property
person.age = 26;

console.log(person);
// Output: { name: "Raj", age: 26, city: "Delhi", country: "India" }
```

### Deleting Properties

```javascript
let person = {
    name: "Raj",
    age: 25,
    city: "Delhi"
};

delete person.city;
console.log(person); // Output: { name: "Raj", age: 25 }
```

### Methods in Objects

**Objects can contain functions (called methods):**

```javascript
let person = {
    name: "Raj",
    age: 25,
    
    // Method using function keyword
    greet: function() {
        return "Hello, I'm " + this.name;
    },
    
    // Method using arrow function (be careful with 'this')
    getAge: () => {
        return this.age; // 'this' doesn't work as expected in arrow functions
    },
    
    // ES6 shorthand method
    introduce() {
        return `Hi, I'm ${this.name} and I'm ${this.age} years old`;
    }
};

console.log(person.greet());     // Output: Hello, I'm Raj
console.log(person.introduce()); // Output: Hi, I'm Raj and I'm 25 years old
```

### The 'this' Keyword

**What is 'this'?** Refers to the object that the method belongs to.

```javascript
let person = {
    name: "Raj",
    age: 25,
    
    introduce: function() {
        // 'this' refers to the person object
        return "I'm " + this.name + ", age " + this.age;
    }
};

console.log(person.introduce()); // Output: I'm Raj, age 25
```

### Nested Objects

**Objects can contain other objects:**

```javascript
let person = {
    name: "Raj",
    age: 25,
    address: {
        street: "123 Main St",
        city: "Delhi",
        country: "India"
    },
    hobbies: ["reading", "coding", "gaming"]
};

// Accessing nested properties
console.log(person.address.city);     // Output: Delhi
console.log(person.hobbies[0]);       // Output: reading
```

### Object Methods and Properties

**Check if property exists:**
```javascript
let person = { name: "Raj", age: 25 };

console.log("name" in person);           // Output: true
console.log("city" in person);           // Output: false
console.log(person.hasOwnProperty("age")); // Output: true
```

**Get all keys:**
```javascript
let person = { name: "Raj", age: 25, city: "Delhi" };

let keys = Object.keys(person);
console.log(keys); // Output: ["name", "age", "city"]
```

**Get all values:**
```javascript
let values = Object.values(person);
console.log(values); // Output: ["Raj", 25, "Delhi"]
```

**Get key-value pairs:**
```javascript
let entries = Object.entries(person);
console.log(entries); 
// Output: [["name", "Raj"], ["age", 25], ["city", "Delhi"]]
```

### Looping Through Objects

**For...in loop:**
```javascript
let person = { name: "Raj", age: 25, city: "Delhi" };

for (let key in person) {
    console.log(key + ": " + person[key]);
}
// Output:
// name: Raj
// age: 25  
// city: Delhi
```

**Using Object.keys():**
```javascript
Object.keys(person).forEach(key => {
    console.log(key + ": " + person[key]);
});
```

### Object Comparison

**Objects are compared by reference, not value:**

```javascript
let obj1 = { name: "Raj" };
let obj2 = { name: "Raj" };
let obj3 = obj1;

console.log(obj1 === obj2); // Output: false (different objects)
console.log(obj1 === obj3); // Output: true (same reference)
```

### 🎯 Key Points
- Objects store key-value pairs
- Use dot notation for simple property names
- Use bracket notation for dynamic or special property names
- Objects can contain methods (functions)
- 'this' refers to the object in methods
- Objects are compared by reference, not value

### 💡 Interview Questions (Hinglish)

**Q1: Object mein property access karne ke kitne ways hain?**

**A:** Do main ways:
- Dot notation: `obj.property`
- Bracket notation: `obj["property"]`
- Bracket notation use karo jab property name mein space ho ya dynamic ho

**Q2: 'this' keyword kya hai objects mein?**

**A:**
'this' current object ko refer karta hai:
```javascript
let obj = {
    name: "Raj",
    greet() {
        return "Hello " + this.name; // this = obj
    }
};
```

**Q3: Object ki properties ko loop kaise karte hain?**

**A:** Multiple ways:
```javascript
// For...in
for (let key in obj) { }

// Object.keys()
Object.keys(obj).forEach(key => { });

// Object.entries()  
Object.entries(obj).forEach(([key, value]) => { });
```

---

## Day 11: Destructuring and Spread Operator

### What is Destructuring?

**Definition:** Destructuring is a way to extract values from arrays or properties from objects into separate variables.

**Real-World Analogy:**
```
Destructuring = Unpacking a suitcase
Suitcase contains: [shirt, pants, shoes]
Unpacking: shirt goes to closet, pants to drawer, shoes to rack

Array: [1, 2, 3]
Destructuring: let [a, b, c] = [1, 2, 3]
Result: a=1, b=2, c=3
```

### Array Destructuring

**Basic Array Destructuring:**
```javascript
let fruits = ["Apple", "Banana", "Orange"];

// Traditional way
let first = fruits[0];
let second = fruits[1];
let third = fruits[2];

// Destructuring way
let [first, second, third] = fruits;
console.log(first);  // Output: Apple
console.log(second); // Output: Banana
console.log(third);  // Output: Orange
```

**Skipping Elements:**
```javascript
let numbers = [1, 2, 3, 4, 5];

// Skip second element
let [first, , third] = numbers;
console.log(first); // Output: 1
console.log(third); // Output: 3
```

**Default Values:**
```javascript
let colors = ["red"];

let [primary, secondary = "blue"] = colors;
console.log(primary);   // Output: red
console.log(secondary); // Output: blue (default value)
```

**Rest in Destructuring:**
```javascript
let numbers = [1, 2, 3, 4, 5];

let [first, second, ...rest] = numbers;
console.log(first);  // Output: 1
console.log(second); // Output: 2
console.log(rest);   // Output: [3, 4, 5]
```

### Object Destructuring

**Basic Object Destructuring:**
```javascript
let person = {
    name: "Raj",
    age: 25,
    city: "Delhi"
};

// Traditional way
let name = person.name;
let age = person.age;
let city = person.city;

// Destructuring way
let {name, age, city} = person;
console.log(name); // Output: Raj
console.log(age);  // Output: 25
console.log(city); // Output: Delhi
```

**Renaming Variables:**
```javascript
let person = {name: "Raj", age: 25};

let {name: personName, age: personAge} = person;
console.log(personName); // Output: Raj
console.log(personAge);  // Output: 25
```

**Default Values:**
```javascript
let person = {name: "Raj"};

let {name, age = 30, city = "Unknown"} = person;
console.log(name); // Output: Raj
console.log(age);  // Output: 30 (default)
console.log(city); // Output: Unknown (default)
```

**Nested Destructuring:**
```javascript
let person = {
    name: "Raj",
    address: {
        city: "Delhi",
        country: "India"
    }
};

let {name, address: {city, country}} = person;
console.log(name);    // Output: Raj
console.log(city);    // Output: Delhi
console.log(country); // Output: India
```

### Function Parameter Destructuring

**Array Parameters:**
```javascript
function sum([a, b, c]) {
    return a + b + c;
}

console.log(sum([1, 2, 3])); // Output: 6
```

**Object Parameters:**
```javascript
function greet({name, age}) {
    return `Hello ${name}, you are ${age} years old`;
}

let person = {name: "Raj", age: 25};
console.log(greet(person)); // Output: Hello Raj, you are 25 years old
```

### Spread Operator (...)

**What is Spread?** Expands an array or object into individual elements.

**Array Spread:**
```javascript
let arr1 = [1, 2, 3];
let arr2 = [4, 5, 6];

// Combine arrays
let combined = [...arr1, ...arr2];
console.log(combined); // Output: [1, 2, 3, 4, 5, 6]

// Copy array
let copy = [...arr1];
console.log(copy); // Output: [1, 2, 3]
```

**Object Spread:**
```javascript
let person = {name: "Raj", age: 25};
let address = {city: "Delhi", country: "India"};

// Combine objects
let fullInfo = {...person, ...address};
console.log(fullInfo); 
// Output: {name: "Raj", age: 25, city: "Delhi", country: "India"}

// Copy object
let copy = {...person};
console.log(copy); // Output: {name: "Raj", age: 25}
```

**Function Arguments:**
```javascript
function sum(a, b, c) {
    return a + b + c;
}

let numbers = [1, 2, 3];
console.log(sum(...numbers)); // Output: 6 (same as sum(1, 2, 3))
```

### Rest vs Spread

```
┌─────────────────────────────────────────────────────────┐
│                Rest vs Spread                           │
├─────────────────────────────────────────────────────────┤
│ Rest (...)     │ Collects multiple elements into array  │
│ Spread (...)   │ Expands array into individual elements │
├─────────────────────────────────────────────────────────┤
│ Rest Example:   let [a, ...rest] = [1,2,3,4]          │
│                 // rest = [2,3,4]                      │
│                                                         │
│ Spread Example: let arr = [1,2,3]                      │
│                 console.log(...arr) // 1 2 3           │
└─────────────────────────────────────────────────────────┘
```

### Practical Examples

**Swapping Variables:**
```javascript
let a = 1;
let b = 2;

// Traditional way
let temp = a;
a = b;
b = temp;

// Destructuring way
[a, b] = [b, a];
console.log(a); // Output: 2
console.log(b); // Output: 1
```

**Function Returning Multiple Values:**
```javascript
function getNameAndAge() {
    return ["Raj", 25];
}

let [name, age] = getNameAndAge();
console.log(name); // Output: Raj
console.log(age);  // Output: 25
```

**Extracting from API Response:**
```javascript
let apiResponse = {
    data: {
        user: {
            name: "Raj",
            email: "raj@example.com"
        },
        posts: [1, 2, 3]
    },
    status: "success"
};

let {data: {user: {name, email}, posts}, status} = apiResponse;
console.log(name);   // Output: Raj
console.log(email);  // Output: raj@example.com
console.log(posts);  // Output: [1, 2, 3]
console.log(status); // Output: success
```

### 🎯 Key Points
- Destructuring extracts values from arrays/objects into variables
- Use [] for arrays, {} for objects
- Can provide default values and rename variables
- Spread operator (...) expands arrays/objects
- Rest operator (...) collects multiple elements
- Makes code cleaner and more readable

### 💡 Interview Questions (Hinglish)

**Q1: Destructuring kya hai aur kaise use karte hain?**

**A:**
Destructuring arrays ya objects se values extract karne ka modern way hai:
```javascript
// Array destructuring
let [a, b] = [1, 2];

// Object destructuring  
let {name, age} = {name: "Raj", age: 25};
```

**Q2: Spread aur Rest operator mein kya difference hai?**

**A:**
- Spread: array/object ko expand karta hai
- Rest: multiple values ko collect karta hai
```javascript
// Spread
let arr = [1, 2, 3];
console.log(...arr); // 1 2 3

// Rest
let [first, ...rest] = [1, 2, 3, 4]; // rest = [2, 3, 4]
```

**Q3: Object destructuring mein default values kaise set karte hain?**

**A:**
```javascript
let {name, age = 25, city = "Delhi"} = {name: "Raj"};
// age aur city ko default values mil jaayengi agar object mein nahi hain
```

---

## Day 12: Template Literals and Modern Syntax

### What are Template Literals?

**Definition:** Template literals are a modern way to create strings using backticks (`) instead of quotes. They allow embedded expressions and multi-line strings.

**Traditional Strings vs Template Literals:**
```javascript
// Traditional string concatenation
let name = "Raj";
let age = 25;
let message = "Hello, my name is " + name + " and I am " + age + " years old.";

// Template literal
let message = `Hello, my name is ${name} and I am ${age} years old.`;
```

### Basic Template Literal Syntax

**Using Backticks:**
```javascript
let greeting = `Hello World!`;
console.log(greeting); // Output: Hello World!
```

**Expression Interpolation:**
```javascript
let a = 5;
let b = 3;
let result = `${a} + ${b} = ${a + b}`;
console.log(result); // Output: 5 + 3 = 8
```

### Multi-line Strings

**Traditional Way (Difficult):**
```javascript
let html = "<div>" +
           "  <h1>Title</h1>" +
           "  <p>Content</p>" +
           "</div>";
```

**Template Literal Way (Easy):**
```javascript
let html = `
<div>
  <h1>Title</h1>
  <p>Content</p>
</div>
`;
```

### Expression Embedding

**Simple Expressions:**
```javascript
let price = 100;
let tax = 0.18;
let message = `Total price: ₹${price + (price * tax)}`;
console.log(message); // Output: Total price: ₹118
```

**Function Calls:**
```javascript
function formatName(name) {
    return name.toUpperCase();
}

let name = "raj";
let greeting = `Hello, ${formatName(name)}!`;
console.log(greeting); // Output: Hello, RAJ!
```

**Conditional Expressions:**
```javascript
let user = {name: "Raj", isAdmin: true};
let message = `Welcome ${user.name}! ${user.isAdmin ? "You have admin access" : "Regular user"}`;
console.log(message); // Output: Welcome Raj! You have admin access
```

### Tagged Template Literals

**Advanced Feature:**
```javascript
function highlight(strings, ...values) {
    return strings.reduce((result, string, i) => {
        return result + string + (values[i] ? `<mark>${values[i]}</mark>` : '');
    }, '');
}

let name = "Raj";
let age = 25;
let result = highlight`Hello ${name}, you are ${age} years old`;
console.log(result); 
// Output: Hello <mark>Raj</mark>, you are <mark>25</mark> years old
```

### Practical Examples

**HTML Generation:**
```javascript
function createCard(user) {
    return `
        <div class="card">
            <h2>${user.name}</h2>
            <p>Age: ${user.age}</p>
            <p>Email: ${user.email}</p>
            <button onclick="contact('${user.id}')">Contact</button>
        </div>
    `;
}

let user = {name: "Raj", age: 25, email: "raj@example.com", id: "123"};
console.log(createCard(user));
```

**SQL Query Building:**
```javascript
function buildQuery(table, conditions) {
    return `
        SELECT * 
        FROM ${table} 
        WHERE ${conditions.map(c => `${c.field} = '${c.value}'`).join(' AND ')}
    `;
}

let query = buildQuery('users', [
    {field: 'age', value: 25},
    {field: 'city', value: 'Delhi'}
]);
console.log(query);
// Output: SELECT * FROM users WHERE age = '25' AND city = 'Delhi'
```

### Modern JavaScript Syntax Features

#### Let and Const (Review)
```javascript
// Block scope
if (true) {
    let x = 1;
    const y = 2;
    // x and y only exist in this block
}
```

#### Arrow Functions (Review)
```javascript
// Traditional function
function add(a, b) {
    return a + b;
}

// Arrow function
const add = (a, b) => a + b;

// With single parameter
const square = x => x * x;

// With no parameters
const greet = () => "Hello!";
```

#### Default Parameters (Review)
```javascript
function greet(name = "Guest", greeting = "Hello") {
    return `${greeting}, ${name}!`;
}

console.log(greet());           // Output: Hello, Guest!
console.log(greet("Raj"));      // Output: Hello, Raj!
console.log(greet("Raj", "Hi")); // Output: Hi, Raj!
```

#### Enhanced Object Literals

**Property Shorthand:**
```javascript
let name = "Raj";
let age = 25;

// Traditional
let person = {
    name: name,
    age: age
};

// Shorthand
let person = {name, age};
```

**Method Shorthand:**
```javascript
// Traditional
let obj = {
    greet: function() {
        return "Hello!";
    }
};

// Shorthand
let obj = {
    greet() {
        return "Hello!";
    }
};
```

**Computed Property Names:**
```javascript
let propertyName = "dynamicKey";
let obj = {
    [propertyName]: "value",
    [`${propertyName}_2`]: "another value"
};
console.log(obj); // Output: {dynamicKey: "value", dynamicKey_2: "another value"}
```

### String Methods (Modern)

**`includes()`:**
```javascript
let text = "JavaScript is awesome";
console.log(text.includes("Script")); // Output: true
console.log(text.includes("Python")); // Output: false
```

**`startsWith()` and `endsWith()`:**
```javascript
let filename = "document.pdf";
console.log(filename.startsWith("doc"));  // Output: true
console.log(filename.endsWith(".pdf"));   // Output: true
```

**`repeat()`:**
```javascript
let star = "*";
console.log(star.repeat(5)); // Output: *****
```

**`padStart()` and `padEnd()`:**
```javascript
let num = "5";
console.log(num.padStart(3, "0")); // Output: 005
console.log(num.padEnd(3, "0"));   // Output: 500
```

### 🎯 Key Points
- Template literals use backticks (`) for strings
- ${expression} embeds JavaScript expressions
- Supports multi-line strings naturally
- Enhanced object literals provide shorthand syntax
- Modern string methods make text manipulation easier

### 💡 Interview Questions (Hinglish)

**Q1: Template literals kya hain aur kaise use karte hain?**

**A:**
Template literals backticks (`) use karte hain aur expressions embed kar sakte hain:
```javascript
let name = "Raj";
let message = `Hello ${name}!`; // Expression embedding
let multiline = `Line 1
Line 2`; // Multi-line support
```

**Q2: Template literals ke kya advantages hain?**

**A:**
- Expression embedding: ${variable}
- Multi-line strings easily
- No string concatenation needed
- More readable code
- Function calls bhi embed kar sakte hain

**Q3: Enhanced object literals kya features dete hain?**

**A:**
```javascript
let name = "Raj";
let obj = {
    name,           // Property shorthand
    greet() {},     // Method shorthand  
    [name]: "value" // Computed property names
};
```

---

## Day 13: Error Handling and Debugging

### What is Error Handling?

**Definition:** Error handling is the process of catching and managing errors that occur during code execution, preventing the program from crashing.

**Real-World Analogy:**
```
Error Handling = Safety Net
Trapeze artist (your code) performs dangerous stunts
Safety net (try-catch) catches them if they fall
Show continues instead of disaster
```

### Types of Errors

#### 1. Syntax Errors
**Code written incorrectly:**
```javascript
// Missing closing bracket
function greet() {
    console.log("Hello"
// SyntaxError: missing ) after argument list
```

#### 2. Runtime Errors
**Errors that occur while code is running:**
```javascript
let obj = null;
console.log(obj.name); // TypeError: Cannot read property 'name' of null
```

#### 3. Logical Errors
**Code runs but produces wrong results:**
```javascript
function calculateArea(length, width) {
    return length + width; // Should be length * width
}
// No error thrown, but wrong calculation
```

### Try-Catch Statement

**Basic Syntax:**
```javascript
try {
    // Code that might throw an error
} catch (error) {
    // Handle the error
} finally {
    // Always runs (optional)
}
```

**Simple Example:**
```javascript
try {
    let result = 10 / 0;
    console.log(result); // Infinity (not an error in JS)
    
    let obj = null;
    console.log(obj.name); // This will throw an error
} catch (error) {
    console.log("An error occurred:", error.message);
} finally {
    console.log("This always runs");
}

// Output:
// Infinity
// An error occurred: Cannot read property 'name' of null
// This always runs
```

### Error Object Properties

```javascript
try {
    let undefinedVariable;
    undefinedVariable.someMethod();
} catch (error) {
    console.log("Name:", error.name);         // TypeError
    console.log("Message:", error.message);   // Cannot read property 'someMethod' of undefined
    console.log("Stack:", error.stack);       // Full stack trace
}
```

### Throwing Custom Errors

**Using `throw` statement:**
```javascript
function divide(a, b) {
    if (b === 0) {
        throw new Error("Division by zero is not allowed");
    }
    return a / b;
}

try {
    let result = divide(10, 0);
    console.log(result);
} catch (error) {
    console.log("Error:", error.message); // Output: Error: Division by zero is not allowed
}
```

**Different Error Types:**
```javascript
// Generic Error
throw new Error("Something went wrong");

// Type Error
throw new TypeError("Expected a number");

// Range Error
throw new RangeError("Number out of range");

// Custom message
throw "Custom error message";
```

### Practical Error Handling Examples

**API Call Error Handling:**
```javascript
function fetchUserData(userId) {
    try {
        if (!userId) {
            throw new Error("User ID is required");
        }
        
        if (typeof userId !== 'number') {
            throw new TypeError("User ID must be a number");
        }
        
        if (userId < 1) {
            throw new RangeError("User ID must be positive");
        }
        
        // Simulate API call
        return `User data for ID: ${userId}`;
        
    } catch (error) {
        console.log(`Failed to fetch user data: ${error.message}`);
        return null;
    }
}

console.log(fetchUserData());      // Failed to fetch user data: User ID is required
console.log(fetchUserData("abc")); // Failed to fetch user data: User ID must be a number
console.log(fetchUserData(-1));    // Failed to fetch user data: User ID must be positive
console.log(fetchUserData(123));   // User data for ID: 123
```

**Form Validation:**
```javascript
function validateForm(formData) {
    let errors = [];
    
    try {
        if (!formData.name || formData.name.trim() === '') {
            throw new Error("Name is required");
        }
        
        if (!formData.email || !formData.email.includes('@')) {
            throw new Error("Valid email is required");
        }
        
        if (!formData.age || formData.age < 18) {
            throw new Error("Age must be 18 or above");
        }
        
        return { success: true, message: "Form is valid" };
        
    } catch (error) {
        return { success: false, message: error.message };
    }
}

// Test cases
console.log(validateForm({})); 
// Output: { success: false, message: "Name is required" }

console.log(validateForm({name: "Raj", email: "raj@example.com", age: 25})); 
// Output: { success: true, message: "Form is valid" }
```

### Debugging Techniques

#### 1. Console Methods
```javascript
let user = {name: "Raj", age: 25};

console.log("Basic log:", user);
console.error("This is an error");
console.warn("This is a warning");
console.info("This is info");
console.table(user); // Shows data in table format
console.group("User Details");
console.log("Name:", user.name);
console.log("Age:", user.age);
console.groupEnd();
```

#### 2. Debugger Statement
```javascript
function calculateTotal(items) {
    let total = 0;
    
    debugger; // Execution will pause here in browser dev tools
    
    for (let item of items) {
        total += item.price;
    }
    
    return total;
}
```

#### 3. Conditional Logging
```javascript
function processData(data, debug = false) {
    if (debug) console.log("Processing data:", data);
    
    // Process data
    let result = data.map(item => item * 2);
    
    if (debug) console.log("Result:", result);
    
    return result;
}

processData([1, 2, 3], true); // Will show debug logs
```

### Error Handling Best Practices

#### 1. Be Specific with Errors
```javascript
// ❌ Generic error
if (age < 0) {
    throw new Error("Invalid input");
}

// ✅ Specific error
if (age < 0) {
    throw new RangeError("Age cannot be negative");
}
```

#### 2. Don't Ignore Errors
```javascript
// ❌ Silent failure
try {
    riskyOperation();
} catch (error) {
    // Ignoring error
}

// ✅ Handle appropriately
try {
    riskyOperation();
} catch (error) {
    console.error("Operation failed:", error.message);
    // Maybe show user-friendly message
    // Maybe retry
    // Maybe use fallback
}
```

#### 3. Use Finally for Cleanup
```javascript
function processFile(filename) {
    let file = null;
    
    try {
        file = openFile(filename);
        return processData(file);
    } catch (error) {
        console.error("Failed to process file:", error.message);
        return null;
    } finally {
        // Always cleanup, even if error occurred
        if (file) {
            closeFile(file);
        }
    }
}
```

### 🎯 Key Points
- Use try-catch to handle runtime errors
- throw creates custom errors
- finally block always executes
- Be specific with error types and messages
- Use console methods for debugging
- Don't ignore errors silently

### 💡 Interview Questions (Hinglish)

**Q1: Error handling kya hai aur kaise karte hain?**

**A:**
Error handling code ko crash hone se bachata hai:
```javascript
try {
    // Risky code
    let result = someOperation();
} catch (error) {
    // Handle error
    console.log("Error:", error.message);
} finally {
    // Cleanup (optional)
}
```

**Q2: Try-catch-finally mein finally ka kya role hai?**

**A:**
Finally block hamesha chalti hai, chahe error aaye ya na aaye:
```javascript
try {
    // Code
} catch (error) {
    // Error handling
} finally {
    // Cleanup - always runs
    console.log("This always executes");
}
```

**Q3: Custom error kaise throw karte hain?**

**A:**
```javascript
function validateAge(age) {
    if (age < 0) {
        throw new Error("Age cannot be negative");
    }
    if (age > 150) {
        throw new RangeError("Age seems unrealistic");
    }
}
```

---

## Day 14: Week 2 Review and Practice

### Week 2 Summary

This week we explored JavaScript's data structures and modern syntax:

**Day 8: Arrays Basics**
- Creating and accessing arrays
- Basic methods: push, pop, shift, unshift
- Finding elements: indexOf, includes
- Array manipulation: slice, splice

**Day 9: Array Methods**
- Higher-order functions: map, filter, reduce
- Method chaining for powerful operations
- Functional programming concepts

**Day 10: Objects**
- Object creation and property access
- Methods and 'this' keyword
- Object iteration and manipulation
- Nested objects and comparison

**Day 11: Destructuring & Spread**
- Array and object destructuring
- Default values and renaming
- Spread operator for arrays and objects
- Rest parameters in functions

**Day 12: Template Literals**
- Modern string creation with backticks
- Expression embedding with ${}
- Multi-line strings
- Enhanced object literals

**Day 13: Error Handling**
- Try-catch-finally blocks
- Throwing custom errors
- Debugging techniques
- Error handling best practices

### How Everything Connects

```
Arrays & Objects (data storage) → Methods (data manipulation) → 
Destructuring (data extraction) → Template Literals (data presentation) → 
Error Handling (robust code)
```

### Comprehensive Practice Exercises

**Exercise 1: Student Management System**
```javascript
class StudentManager {
    constructor() {
        this.students = [];
    }
    
    addStudent(student) {
        try {
            // Validate student data
            if (!student.name || !student.age || !student.subjects) {
                throw new Error("Missing required student information");
            }
            
            if (student.age < 16 || student.age > 25) {
                throw new RangeError("Student age must be between 16 and 25");
            }
            
            this.students.push({
                id: Date.now(),
                ...student,
                createdAt: new Date().toISOString()
            });
            
            return { success: true, message: "Student added successfully" };
            
        } catch (error) {
            return { success: false, message: error.message };
        }
    }
    
    getStudentsBySubject(subject) {
        return this.students.filter(student => 
            student.subjects.includes(subject)
        );
    }
    
    getAverageAge() {
        if (this.students.length === 0) return 0;
        
        const totalAge = this.students.reduce((sum, student) => 
            sum + student.age, 0
        );
        
        return totalAge / this.students.length;
    }
    
    generateReport() {
        const report = this.students.map(({name, age, subjects}) => ({
            name,
            age,
            subjectCount: subjects.length,
            subjects: subjects.join(', ')
        }));
        
        return `
            Student Report
            ==============
            Total Students: ${this.students.length}
            Average Age: ${this.getAverageAge().toFixed(1)}
            
            Students:
            ${report.map(s => `- ${s.name} (${s.age}): ${s.subjects}`).join('\n')}
        `;
    }
}

// Usage
const manager = new StudentManager();

// Add students
console.log(manager.addStudent({
    name: "Raj",
    age: 20,
    subjects: ["Math", "Physics", "Chemistry"]
}));

console.log(manager.addStudent({
    name: "Priya", 
    age: 19,
    subjects: ["Biology", "Chemistry", "English"]
}));

// Get students by subject
console.log("Chemistry students:", manager.getStudentsBySubject("Chemistry"));

// Generate report
console.log(manager.generateReport());
```

**Exercise 2: E-commerce Cart System**
```javascript
const cart = {
    items: [],
    
    addItem(product, quantity = 1) {
        try {
            const {id, name, price} = product;
            
            if (!id || !name || !price) {
                throw new Error("Invalid product data");
            }
            
            if (price <= 0) {
                throw new RangeError("Price must be positive");
            }
            
            const existingItem = this.items.find(item => item.id === id);
            
            if (existingItem) {
                existingItem.quantity += quantity;
            } else {
                this.items.push({id, name, price, quantity});
            }
            
            return `Added ${quantity} ${name}(s) to cart`;
            
        } catch (error) {
            return `Error: ${error.message}`;
        }
    },
    
    removeItem(productId) {
        const index = this.items.findIndex(item => item.id === productId);
        
        if (index === -1) {
            return "Item not found in cart";
        }
        
        const removedItem = this.items.splice(index, 1)[0];
        return `Removed ${removedItem.name} from cart`;
    },
    
    updateQuantity(productId, newQuantity) {
        const item = this.items.find(item => item.id === productId);
        
        if (!item) {
            return "Item not found in cart";
        }
        
        if (newQuantity <= 0) {
            return this.removeItem(productId);
        }
        
        item.quantity = newQuantity;
        return `Updated ${item.name} quantity to ${newQuantity}`;
    },
    
    getTotal() {
        return this.items.reduce((total, item) => 
            total + (item.price * item.quantity), 0
        );
    },
    
    getItemCount() {
        return this.items.reduce((count, item) => 
            count + item.quantity, 0
        );
    },
    
    generateInvoice() {
        if (this.items.length === 0) {
            return "Cart is empty";
        }
        
        const itemList = this.items.map(({name, price, quantity}) => {
            const total = price * quantity;
            return `${name} x${quantity} - ₹${price} each = ₹${total}`;
        }).join('\n');
        
        return `
            INVOICE
            =======
            ${itemList}
            
            Total Items: ${this.getItemCount()}
            Total Amount: ₹${this.getTotal()}
        `;
    },
    
    applyDiscount(percentage) {
        if (percentage < 0 || percentage > 100) {
            throw new RangeError("Discount must be between 0 and 100");
        }
        
        const discount = this.getTotal() * (percentage / 100);
        const finalAmount = this.getTotal() - discount;
        
        return {
            originalAmount: this.getTotal(),
            discount: discount,
            finalAmount: finalAmount,
            message: `${percentage}% discount applied`
        };
    }
};

// Usage
console.log(cart.addItem({id: 1, name: "Laptop", price: 50000}, 1));
console.log(cart.addItem({id: 2, name: "Mouse", price: 500}, 2));
console.log(cart.addItem({id: 3, name: "Keyboard", price: 1500}, 1));

console.log(cart.generateInvoice());
console.log(cart.applyDiscount(10));
```

**Exercise 3: Data Processing Pipeline**
```javascript
const dataProcessor = {
    // Sample data
    rawData: [
        {name: "raj sharma", age: 25, salary: 50000, department: "IT"},
        {name: "priya patel", age: 28, salary: 60000, department: "HR"},
        {name: "amit kumar", age: 22, salary: 45000, department: "IT"},
        {name: "sneha singh", age: 30, salary: 70000, department: "Finance"},
        {name: "rohit gupta", age: 26, salary: 55000, department: "IT"}
    ],
    
    // Clean and normalize data
    cleanData(data = this.rawData) {
        return data.map(person => ({
            ...person,
            name: person.name
                .split(' ')
                .map(word => word.charAt(0).toUpperCase() + word.slice(1))
                .join(' '),
            department: person.department.toUpperCase()
        }));
    },
    
    // Filter by criteria
    filterBy(criteria) {
        const cleanedData = this.cleanData();
        
        return cleanedData.filter(person => {
            return Object.entries(criteria).every(([key, value]) => {
                if (typeof value === 'object' && value.min !== undefined) {
                    return person[key] >= value.min && person[key] <= value.max;
                }
                return person[key] === value;
            });
        });
    },
    
    // Group by department
    groupByDepartment(data = this.cleanData()) {
        return data.reduce((groups, person) => {
            const dept = person.department;
            if (!groups[dept]) {
                groups[dept] = [];
            }
            groups[dept].push(person);
            return groups;
        }, {});
    },
    
    // Calculate statistics
    getStatistics(data = this.cleanData()) {
        const salaries = data.map(person => person.salary);
        const ages = data.map(person => person.age);
        
        return {
            totalEmployees: data.length,
            averageSalary: salaries.reduce((a, b) => a + b, 0) / salaries.length,
            averageAge: ages.reduce((a, b) => a + b, 0) / ages.length,
            maxSalary: Math.max(...salaries),
            minSalary: Math.min(...salaries),
            departmentCount: Object.keys(this.groupByDepartment(data)).length
        };
    },
    
    // Generate comprehensive report
    generateReport() {
        try {
            const cleanedData = this.cleanData();
            const stats = this.getStatistics(cleanedData);
            const groupedData = this.groupByDepartment(cleanedData);
            
            let report = `
                EMPLOYEE REPORT
                ===============
                Total Employees: ${stats.totalEmployees}
                Average Salary: ₹${stats.averageSalary.toFixed(0)}
                Average Age: ${stats.averageAge.toFixed(1)} years
                Salary Range: ₹${stats.minSalary} - ₹${stats.maxSalary}
                
                DEPARTMENT BREAKDOWN:
            `;
            
            Object.entries(groupedData).forEach(([dept, employees]) => {
                const deptAvgSalary = employees.reduce((sum, emp) => sum + emp.salary, 0) / employees.length;
                report += `
                ${dept}: ${employees.length} employees (Avg Salary: ₹${deptAvgSalary.toFixed(0)})`;
                employees.forEach(emp => {
                    report += `
                  - ${emp.name} (${emp.age}): ₹${emp.salary}`;
                });
            });
            
            return report;
            
        } catch (error) {
            return `Error generating report: ${error.message}`;
        }
    }
};

// Usage
console.log(dataProcessor.generateReport());

// Filter IT employees with salary > 50000
const itHighEarners = dataProcessor.filterBy({
    department: "IT",
    salary: {min: 50000, max: Infinity}
});
console.log("IT High Earners:", itHighEarners);
```

### Common Patterns and Best Practices

**1. Error Handling Pattern:**
```javascript
function safeOperation(data) {
    try {
        // Validate input
        if (!data) throw new Error("Data is required");
        
        // Process data
        const result = processData(data);
        
        // Return success
        return {success: true, data: result};
        
    } catch (error) {
        // Log error for debugging
        console.error("Operation failed:", error);
        
        // Return user-friendly error
        return {success: false, error: error.message};
    }
}
```

**2. Data Transformation Pattern:**
```javascript
const transformData = (rawData) => {
    return rawData
        .filter(item => item.isValid)           // Remove invalid items
        .map(item => ({                         // Transform structure
            ...item,
            processedAt: new Date().toISOString()
        }))
        .sort((a, b) => a.priority - b.priority); // Sort by priority
};
```

**3. Configuration Object Pattern:**
```javascript
function createUser({
    name,
    email,
    age = 18,
    role = 'user',
    isActive = true
} = {}) {
    // Validate required fields
    if (!name || !email) {
        throw new Error("Name and email are required");
    }
    
    return {
        id: Date.now(),
        name,
        email,
        age,
        role,
        isActive,
        createdAt: new Date().toISOString()
    };
}
```

### 💡 Week 2 Interview Questions (Hinglish)

**Q1: Array methods map, filter, reduce ka real-world use case batao.**

**A:**
E-commerce cart example:
```javascript
const cart = [{name: "Laptop", price: 50000, qty: 1}];

// Map - calculate totals
const totals = cart.map(item => item.price * item.qty);

// Filter - expensive items
const expensive = cart.filter(item => item.price > 10000);

// Reduce - grand total
const grandTotal = cart.reduce((sum, item) => sum + (item.price * item.qty), 0);
```

**Q2: Destructuring ka practical use kya hai?**

**A:**
API response handling:
```javascript
const {data: {user: {name, email}, posts}, status} = apiResponse;
// Ek line mein nested data extract kar liya
```

**Q3: Error handling kab aur kaise karte hain?**

**A:**
User input validation, API calls, file operations mein:
```javascript
try {
    const result = await apiCall();
    return {success: true, data: result};
} catch (error) {
    console.error(error);
    return {success: false, message: "Something went wrong"};
}
```

### Next Week Preview

Week 3 will cover:
- Advanced functions (closures, higher-order functions)
- Scope and hoisting concepts
- Asynchronous JavaScript (callbacks, promises)
- Event handling and DOM manipulation
- Object-oriented programming basics

The foundation you've built with data structures and modern syntax will be crucial for these advanced topics!

---

# Week 3: Advanced JavaScript Concepts {#week-3}

## Day 15: Advanced Functions and Scope

### Function Declarations vs Expressions vs Arrow Functions

**Function Declaration:**
```javascript
// Hoisted - can be called before declaration
console.log(add(2, 3)); // Works! Output: 5

function add(a, b) {
    return a + b;
}
```

**Function Expression:**
```javascript
// Not hoisted - cannot be called before declaration
console.log(multiply(2, 3)); // Error! Cannot access before initialization

const multiply = function(a, b) {
    return a * b;
};
```

**Arrow Function:**
```javascript
// Not hoisted, shorter syntax, different 'this' behavior
const divide = (a, b) => {
    if (b === 0) throw new Error("Division by zero");
    return a / b;
};

// Even shorter for single expressions
const square = x => x * x;
const greet = () => "Hello!";
```

### Scope in JavaScript

**What is Scope?** Scope determines where variables can be accessed in your code.

#### Global Scope
```javascript
let globalVar = "I'm global";

function someFunction() {
    console.log(globalVar); // Can access global variable
}

console.log(globalVar); // Can access from anywhere
```

#### Function Scope
```javascript
function myFunction() {
    let functionScoped = "I'm function scoped";
    
    if (true) {
        var varVariable = "I'm var"; // Function scoped
        let letVariable = "I'm let"; // Block scoped
    }
    
    console.log(varVariable); // Works - var is function scoped
    console.log(letVariable); // Error - let is block scoped
}
```

#### Block Scope
```javascript
if (true) {
    let blockScoped = "I'm block scoped";
    const alsoBlockScoped = "Me too";
    var notBlockScoped = "I'm not block scoped";
}

console.log(notBlockScoped); // Works - var ignores block scope
console.log(blockScoped);    // Error - let respects block scope
```

#### Scope Chain
```javascript
let global = "global";

function outer() {
    let outerVar = "outer";
    
    function inner() {
        let innerVar = "inner";
        
        // Can access all three variables
        console.log(innerVar);  // "inner"
        console.log(outerVar);  // "outer" 
        console.log(global);    // "global"
    }
    
    inner();
    // console.log(innerVar); // Error - can't access inner scope
}

outer();
```

### Hoisting

**What is Hoisting?** JavaScript moves variable and function declarations to the top of their scope during compilation.

**Variable Hoisting:**
```javascript
console.log(x); // undefined (not error!)
var x = 5;

// Above code is interpreted as:
var x; // Declaration hoisted
console.log(x); // undefined
x = 5; // Assignment stays in place
```

**Let and Const Hoisting:**
```javascript
console.log(y); // ReferenceError: Cannot access 'y' before initialization
let y = 10;

console.log(z); // ReferenceError: Cannot access 'z' before initialization  
const z = 20;
```

**Function Hoisting:**
```javascript
// Function declarations are fully hoisted
console.log(sayHello()); // "Hello!" - Works!

function sayHello() {
    return "Hello!";
}

// Function expressions are not hoisted
console.log(sayBye()); // TypeError: sayBye is not a function

var sayBye = function() {
    return "Bye!";
};
```

### Closures

**What is a Closure?** A closure is when an inner function has access to variables from its outer function, even after the outer function has finished executing.

**Basic Closure:**
```javascript
function outerFunction(x) {
    // Outer function's variable
    
    function innerFunction(y) {
        // Inner function can access outer function's variable
        return x + y;
    }
    
    return innerFunction;
}

const addFive = outerFunction(5);
console.log(addFive(3)); // Output: 8

// Even though outerFunction finished, innerFunction still remembers x = 5
```

**Real-World Example - Counter:**
```javascript
function createCounter() {
    let count = 0; // Private variable
    
    return {
        increment: function() {
            count++;
            return count;
        },
        decrement: function() {
            count--;
            return count;
        },
        getCount: function() {
            return count;
        }
    };
}

const counter = createCounter();
console.log(counter.increment()); // 1
console.log(counter.increment()); // 2
console.log(counter.getCount());  // 2
console.log(counter.decrement()); // 1

// count variable is private - cannot be accessed directly
console.log(counter.count); // undefined
```

**Closure in Loops (Common Interview Question):**
```javascript
// Problem - all functions log 3
for (var i = 0; i < 3; i++) {
    setTimeout(function() {
        console.log(i); // 3, 3, 3 (not 0, 1, 2)
    }, 100);
}

// Solution 1 - Use let (block scope)
for (let i = 0; i < 3; i++) {
    setTimeout(function() {
        console.log(i); // 0, 1, 2
    }, 100);
}

// Solution 2 - Use closure
for (var i = 0; i < 3; i++) {
    (function(j) {
        setTimeout(function() {
            console.log(j); // 0, 1, 2
        }, 100);
    })(i);
}
```

### Higher-Order Functions

**Definition:** Functions that take other functions as arguments or return functions.

**Function as Argument:**
```javascript
function calculate(operation, a, b) {
    return operation(a, b);
}

const add = (x, y) => x + y;
const multiply = (x, y) => x * y;

console.log(calculate(add, 5, 3));      // 8
console.log(calculate(multiply, 5, 3)); // 15
```

**Function Returning Function:**
```javascript
function createMultiplier(multiplier) {
    return function(number) {
        return number * multiplier;
    };
}

const double = createMultiplier(2);
const triple = createMultiplier(3);

console.log(double(5)); // 10
console.log(triple(5)); // 15
```

**Practical Example - Event Handler Factory:**
```javascript
function createEventHandler(eventType, message) {
    return function(element) {
        element.addEventListener(eventType, function() {
            console.log(message);
        });
    };
}

const createClickHandler = createEventHandler('click', 'Button clicked!');
const createHoverHandler = createEventHandler('mouseenter', 'Mouse entered!');

// Usage (in browser)
// createClickHandler(document.getElementById('myButton'));
```

### IIFE (Immediately Invoked Function Expression)

**What is IIFE?** A function that runs immediately after it's defined.

**Basic IIFE:**
```javascript
(function() {
    console.log("I run immediately!");
})();

// With parameters
(function(name) {
    console.log("Hello, " + name);
})("Raj");
```

**Why use IIFE?**
```javascript
// Avoid polluting global scope
(function() {
    let privateVariable = "I'm private";
    
    // This code runs but doesn't create global variables
    function privateFunction() {
        return "I'm also private";
    }
})();

// privateVariable and privateFunction are not accessible here
```

**Module Pattern with IIFE:**
```javascript
const Calculator = (function() {
    // Private variables and functions
    let result = 0;
    
    function log(operation, value) {
        console.log(`${operation}: ${value}`);
    }
    
    // Public API
    return {
        add: function(value) {
            result += value;
            log("Added", value);
            return this;
        },
        
        subtract: function(value) {
            result -= value;
            log("Subtracted", value);
            return this;
        },
        
        getResult: function() {
            return result;
        },
        
        reset: function() {
            result = 0;
            log("Reset", 0);
            return this;
        }
    };
})();

// Usage - method chaining
Calculator.add(10).subtract(3).add(5);
console.log(Calculator.getResult()); // 12
```

### 🎯 Key Points
- Function declarations are hoisted, expressions are not
- Scope determines variable accessibility
- Closures allow inner functions to access outer variables
- Higher-order functions work with other functions
- IIFE creates private scope immediately

### 💡 Interview Questions (Hinglish)

**Q1: Hoisting kya hai? Example do.**

**A:**
Hoisting means declarations top par move ho jaate hain:
```javascript
console.log(x); // undefined (not error)
var x = 5;

// Interpreted as:
var x; // Declaration hoisted
console.log(x); // undefined
x = 5; // Assignment stays
```

**Q2: Closure kya hai aur kab use karte hain?**

**A:**
Closure inner function ko outer function ke variables access karne deta hai:
```javascript
function outer(x) {
    return function inner(y) {
        return x + y; // x still accessible
    };
}
const addFive = outer(5);
console.log(addFive(3)); // 8
```
Use cases: Private variables, module pattern, callbacks

**Q3: Let, const, aur var mein scope difference kya hai?**

**A:**
- `var`: Function scoped, hoisted with undefined
- `let`: Block scoped, hoisted but not accessible (TDZ)
- `const`: Block scoped, hoisted but not accessible, cannot reassign

---## Day 16:
 Asynchronous JavaScript - Callbacks and Promises

### What is Asynchronous Programming?

**Definition:** Asynchronous programming allows code to run without blocking other operations. Instead of waiting for one task to complete, JavaScript can start other tasks.

**Real-World Analogy:**
```
Synchronous = Standing in line at bank
- Wait for person ahead to finish
- Then your turn
- Everyone waits

Asynchronous = Restaurant ordering
- Place order (start task)
- Get buzzer (callback/promise)
- Do other things while food cooks
- Buzzer rings when ready (task complete)
```

### The Problem with Synchronous Code

```javascript
// Synchronous - blocks everything
function slowOperation() {
    // Simulate slow operation (don't actually do this!)
    let start = Date.now();
    while (Date.now() - start < 3000) {
        // Block for 3 seconds
    }
    return "Operation complete";
}

console.log("Start");
console.log(slowOperation()); // Blocks for 3 seconds
console.log("End");

// Output (after 3 second delay):
// Start
// Operation complete  
// End
```

### Callbacks

**What is a Callback?** A function passed to another function to be called later when an operation completes.

**Basic Callback Example:**
```javascript
function greetUser(name, callback) {
    console.log("Processing greeting for " + name);
    
    // Simulate async operation
    setTimeout(() => {
        const greeting = "Hello, " + name + "!";
        callback(greeting); // Call the callback with result
    }, 1000);
}

function displayGreeting(message) {
    console.log("Received: " + message);
}

console.log("Start");
greetUser("Raj", displayGreeting);
console.log("End");

// Output:
// Start
// Processing greeting for Raj
// End
// (1 second later) Received: Hello, Raj!
```

**Real-World Example - File Reading:**
```javascript
// Simulated file reading with callback
function readFile(filename, callback) {
    console.log("Reading file: " + filename);
    
    setTimeout(() => {
        if (filename.endsWith('.txt')) {
            callback(null, "File content: Hello World!");
        } else {
            callback(new Error("Invalid file type"), null);
        }
    }, 1500);
}

// Usage
readFile("document.txt", (error, data) => {
    if (error) {
        console.log("Error:", error.message);
    } else {
        console.log("Success:", data);
    }
});
```

### Callback Hell

**The Problem:**
```javascript
// Nested callbacks become hard to read and maintain
getData(function(a) {
    getMoreData(a, function(b) {
        getEvenMoreData(b, function(c) {
            getFinalData(c, function(d) {
                // Finally do something with d
                console.log("Final result:", d);
            });
        });
    });
});

// This creates a "pyramid of doom" or "callback hell"
```

### Promises

**What is a Promise?** A Promise represents a value that may be available now, later, or never. It's a cleaner way to handle asynchronous operations.

**Promise States:**
```
┌─────────────────────────────────────┐
│            Promise States           │
├─────────────────────────────────────┤
│ Pending   → Operation in progress   │
│ Fulfilled → Operation successful    │
│ Rejected  → Operation failed        │
└─────────────────────────────────────┘
```

**Creating a Promise:**
```javascript
const myPromise = new Promise((resolve, reject) => {
    // Async operation
    setTimeout(() => {
        const success = true;
        
        if (success) {
            resolve("Operation successful!"); // Fulfill the promise
        } else {
            reject(new Error("Operation failed!")); // Reject the promise
        }
    }, 1000);
});
```

**Using Promises with .then() and .catch():**
```javascript
myPromise
    .then(result => {
        console.log("Success:", result);
    })
    .catch(error => {
        console.log("Error:", error.message);
    });
```

**Promise Example - API Call Simulation:**
```javascript
function fetchUserData(userId) {
    return new Promise((resolve, reject) => {
        console.log("Fetching user data...");
        
        setTimeout(() => {
            if (userId > 0) {
                resolve({
                    id: userId,
                    name: "Raj Sharma",
                    email: "raj@example.com"
                });
            } else {
                reject(new Error("Invalid user ID"));
            }
        }, 2000);
    });
}

// Usage
fetchUserData(123)
    .then(user => {
        console.log("User found:", user);
        return user.id; // Return value for next .then()
    })
    .then(userId => {
        console.log("User ID is:", userId);
    })
    .catch(error => {
        console.log("Failed to fetch user:", error.message);
    });
```

### Promise Chaining

**Sequential Operations:**
```javascript
function step1() {
    return new Promise(resolve => {
        setTimeout(() => resolve("Step 1 complete"), 1000);
    });
}

function step2(data) {
    return new Promise(resolve => {
        setTimeout(() => resolve(data + " → Step 2 complete"), 1000);
    });
}

function step3(data) {
    return new Promise(resolve => {
        setTimeout(() => resolve(data + " → Step 3 complete"), 1000);
    });
}

// Chain promises
step1()
    .then(result1 => {
        console.log(result1);
        return step2(result1);
    })
    .then(result2 => {
        console.log(result2);
        return step3(result2);
    })
    .then(result3 => {
        console.log("Final result:", result3);
    })
    .catch(error => {
        console.log("Error in chain:", error.message);
    });
```

### Promise.all() and Promise.race()

**Promise.all() - Wait for all promises:**
```javascript
const promise1 = new Promise(resolve => setTimeout(() => resolve("First"), 1000));
const promise2 = new Promise(resolve => setTimeout(() => resolve("Second"), 2000));
const promise3 = new Promise(resolve => setTimeout(() => resolve("Third"), 1500));

Promise.all([promise1, promise2, promise3])
    .then(results => {
        console.log("All completed:", results);
        // Output: ["First", "Second", "Third"]
    })
    .catch(error => {
        console.log("One failed:", error.message);
    });
```

**Promise.race() - First to complete wins:**
```javascript
const fast = new Promise(resolve => setTimeout(() => resolve("Fast"), 1000));
const slow = new Promise(resolve => setTimeout(() => resolve("Slow"), 3000));

Promise.race([fast, slow])
    .then(result => {
        console.log("Winner:", result); // Output: "Fast"
    });
```

### Converting Callbacks to Promises

**Callback Version:**
```javascript
function readFileCallback(filename, callback) {
    setTimeout(() => {
        if (filename.endsWith('.txt')) {
            callback(null, "File content");
        } else {
            callback(new Error("Invalid file"), null);
        }
    }, 1000);
}
```

**Promise Version:**
```javascript
function readFilePromise(filename) {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            if (filename.endsWith('.txt')) {
                resolve("File content");
            } else {
                reject(new Error("Invalid file"));
            }
        }, 1000);
    });
}

// Usage
readFilePromise("document.txt")
    .then(content => console.log(content))
    .catch(error => console.log(error.message));
```

### 🎯 Key Points
- Asynchronous code doesn't block execution
- Callbacks are functions passed to be called later
- Callback hell makes code hard to read
- Promises provide cleaner async handling
- Promise chaining allows sequential operations
- Promise.all() waits for all, Promise.race() takes first

### 💡 Interview Questions (Hinglish)

**Q1: Synchronous aur Asynchronous code mein kya difference hai?**

**A:**
- Synchronous: Ek ke baad ek execute hota hai, blocking hota hai
- Asynchronous: Parallel mein execute hota hai, non-blocking
```javascript
// Sync - blocks
console.log("1");
blockingOperation(); // Waits here
console.log("2");

// Async - doesn't block  
console.log("1");
setTimeout(() => console.log("2"), 1000); // Doesn't wait
console.log("3"); // Runs immediately
```

**Q2: Promise kya hai aur callback se kaise better hai?**

**A:**
Promise async operations ko handle karne ka modern way hai:
- Callback hell avoid karta hai
- Better error handling
- Chaining possible hai
```javascript
// Callback hell
getData(function(a) {
    getMoreData(a, function(b) {
        // Nested callbacks
    });
});

// Promise chain
getData()
    .then(a => getMoreData(a))
    .then(b => console.log(b))
    .catch(error => console.log(error));
```

**Q3: Promise.all() aur Promise.race() kya karte hain?**

**A:**
- Promise.all(): Sab promises complete hone ka wait karta hai
- Promise.race(): Jo pehle complete ho jaaye, uska result deta hai
```javascript
Promise.all([p1, p2, p3]).then(results => {
    // All three completed
});

Promise.race([p1, p2, p3]).then(result => {
    // First one completed
});
```

---## Day 
17: Async/Await and Modern Asynchronous Patterns

### What is Async/Await?

**Definition:** Async/await is a modern syntax that makes asynchronous code look and behave more like synchronous code, making it easier to read and write.

**Promise vs Async/Await:**
```javascript
// Using Promises
function fetchUserWithPromises(userId) {
    return fetchUser(userId)
        .then(user => {
            console.log("User:", user);
            return fetchUserPosts(user.id);
        })
        .then(posts => {
            console.log("Posts:", posts);
            return posts;
        })
        .catch(error => {
            console.log("Error:", error.message);
        });
}

// Using Async/Await (cleaner!)
async function fetchUserWithAsync(userId) {
    try {
        const user = await fetchUser(userId);
        console.log("User:", user);
        
        const posts = await fetchUserPosts(user.id);
        console.log("Posts:", posts);
        
        return posts;
    } catch (error) {
        console.log("Error:", error.message);
    }
}
```

### Async Functions

**Creating Async Functions:**
```javascript
// Function declaration
async function getData() {
    return "Hello World";
}

// Function expression
const getData = async function() {
    return "Hello World";
};

// Arrow function
const getData = async () => {
    return "Hello World";
};

// All async functions return a Promise
console.log(getData()); // Promise {<fulfilled>: "Hello World"}
```

**Async Function Always Returns Promise:**
```javascript
async function example() {
    return "Hello"; // Automatically wrapped in Promise.resolve()
}

// Equivalent to:
function example() {
    return Promise.resolve("Hello");
}

// Usage
example().then(result => console.log(result)); // "Hello"
```

### Await Keyword

**Basic Await Usage:**
```javascript
function delay(ms) {
    return new Promise(resolve => setTimeout(resolve, ms));
}

async function example() {
    console.log("Start");
    
    await delay(2000); // Wait for 2 seconds
    console.log("After 2 seconds");
    
    await delay(1000); // Wait for 1 more second
    console.log("After 3 seconds total");
}

example();
```

**Await with Real Promises:**
```javascript
function fetchData() {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            const success = Math.random() > 0.3;
            if (success) {
                resolve({data: "Important information"});
            } else {
                reject(new Error("Network error"));
            }
        }, 1000);
    });
}

async function handleData() {
    try {
        console.log("Fetching data...");
        const result = await fetchData(); // Wait for promise to resolve
        console.log("Received:", result.data);
    } catch (error) {
        console.log("Failed:", error.message);
    }
}

handleData();
```

### Error Handling with Try-Catch

**Multiple Async Operations:**
```javascript
async function processUserData(userId) {
    try {
        // Sequential operations
        const user = await fetchUser(userId);
        const profile = await fetchProfile(user.id);
        const preferences = await fetchPreferences(user.id);
        
        return {
            user,
            profile,
            preferences
        };
        
    } catch (error) {
        // Catches any error from any await
        console.log("Error processing user data:", error.message);
        throw error; // Re-throw if needed
    }
}
```

**Handling Specific Errors:**
```javascript
async function robustDataFetch(userId) {
    let user, profile, preferences;
    
    try {
        user = await fetchUser(userId);
    } catch (error) {
        console.log("User fetch failed:", error.message);
        return null;
    }
    
    try {
        profile = await fetchProfile(user.id);
    } catch (error) {
        console.log("Profile fetch failed, using default");
        profile = {name: "Unknown", avatar: "default.jpg"};
    }
    
    try {
        preferences = await fetchPreferences(user.id);
    } catch (error) {
        console.log("Preferences fetch failed, using default");
        preferences = {theme: "light", language: "en"};
    }
    
    return {user, profile, preferences};
}
```

### Parallel vs Sequential Execution

**Sequential (One after another):**
```javascript
async function sequential() {
    console.time("Sequential");
    
    const result1 = await operation1(); // Wait 1 second
    const result2 = await operation2(); // Wait 1 second  
    const result3 = await operation3(); // Wait 1 second
    
    console.timeEnd("Sequential"); // ~3 seconds total
    return [result1, result2, result3];
}
```

**Parallel (All at once):**
```javascript
async function parallel() {
    console.time("Parallel");
    
    // Start all operations simultaneously
    const promise1 = operation1();
    const promise2 = operation2();
    const promise3 = operation3();
    
    // Wait for all to complete
    const results = await Promise.all([promise1, promise2, promise3]);
    
    console.timeEnd("Parallel"); // ~1 second total
    return results;
}

// Alternative syntax
async function parallelAlternative() {
    const results = await Promise.all([
        operation1(),
        operation2(),
        operation3()
    ]);
    return results;
}
```

### Real-World Examples

**API Data Fetching:**
```javascript
class UserService {
    async getUserDashboard(userId) {
        try {
            // Fetch user basic info first
            const user = await this.fetchUser(userId);
            
            // Then fetch additional data in parallel
            const [posts, friends, notifications] = await Promise.all([
                this.fetchUserPosts(userId),
                this.fetchUserFriends(userId),
                this.fetchUserNotifications(userId)
            ]);
            
            return {
                user,
                posts,
                friends,
                notifications,
                lastUpdated: new Date().toISOString()
            };
            
        } catch (error) {
            console.error("Dashboard fetch failed:", error);
            throw new Error("Unable to load dashboard");
        }
    }
    
    async fetchUser(userId) {
        // Simulate API call
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                if (userId > 0) {
                    resolve({id: userId, name: "Raj", email: "raj@example.com"});
                } else {
                    reject(new Error("Invalid user ID"));
                }
            }, 500);
        });
    }
    
    async fetchUserPosts(userId) {
        return new Promise(resolve => {
            setTimeout(() => {
                resolve([
                    {id: 1, title: "My first post", content: "Hello world!"},
                    {id: 2, title: "Learning JavaScript", content: "Async/await is cool!"}
                ]);
            }, 800);
        });
    }
    
    async fetchUserFriends(userId) {
        return new Promise(resolve => {
            setTimeout(() => {
                resolve([
                    {id: 2, name: "Priya"},
                    {id: 3, name: "Amit"}
                ]);
            }, 600);
        });
    }
    
    async fetchUserNotifications(userId) {
        return new Promise(resolve => {
            setTimeout(() => {
                resolve([
                    {id: 1, message: "Priya liked your post", read: false},
                    {id: 2, message: "Amit commented on your photo", read: true}
                ]);
            }, 400);
        });
    }
}

// Usage
const userService = new UserService();

async function loadDashboard() {
    try {
        console.log("Loading dashboard...");
        const dashboard = await userService.getUserDashboard(123);
        console.log("Dashboard loaded:", dashboard);
    } catch (error) {
        console.log("Failed to load dashboard:", error.message);
    }
}

loadDashboard();
```

**File Processing with Async/Await:**
```javascript
class FileProcessor {
    async processFiles(filenames) {
        const results = [];
        
        for (const filename of filenames) {
            try {
                console.log(`Processing ${filename}...`);
                
                const content = await this.readFile(filename);
                const processed = await this.processContent(content);
                const saved = await this.saveResult(filename, processed);
                
                results.push({
                    filename,
                    success: true,
                    size: processed.length
                });
                
            } catch (error) {
                console.log(`Failed to process ${filename}:`, error.message);
                results.push({
                    filename,
                    success: false,
                    error: error.message
                });
            }
        }
        
        return results;
    }
    
    async readFile(filename) {
        return new Promise((resolve, reject) => {
            setTimeout(() => {
                if (filename.endsWith('.txt')) {
                    resolve(`Content of ${filename}`);
                } else {
                    reject(new Error("Unsupported file type"));
                }
            }, Math.random() * 1000);
        });
    }
    
    async processContent(content) {
        return new Promise(resolve => {
            setTimeout(() => {
                resolve(content.toUpperCase() + " [PROCESSED]");
            }, 500);
        });
    }
    
    async saveResult(filename, content) {
        return new Promise(resolve => {
            setTimeout(() => {
                resolve(`Saved processed ${filename}`);
            }, 300);
        });
    }
}

// Usage
const processor = new FileProcessor();

async function batchProcess() {
    const files = ["doc1.txt", "doc2.txt", "image.jpg", "doc3.txt"];
    
    console.log("Starting batch processing...");
    const results = await processor.processFiles(files);
    
    console.log("Batch processing complete:");
    results.forEach(result => {
        if (result.success) {
            console.log(`✓ ${result.filename} (${result.size} chars)`);
        } else {
            console.log(`✗ ${result.filename}: ${result.error}`);
        }
    });
}

batchProcess();
```

### Common Async/Await Patterns

**Retry Pattern:**
```javascript
async function retryOperation(operation, maxRetries = 3) {
    for (let attempt = 1; attempt <= maxRetries; attempt++) {
        try {
            return await operation();
        } catch (error) {
            console.log(`Attempt ${attempt} failed:`, error.message);
            
            if (attempt === maxRetries) {
                throw new Error(`Operation failed after ${maxRetries} attempts`);
            }
            
            // Wait before retry (exponential backoff)
            await new Promise(resolve => setTimeout(resolve, attempt * 1000));
        }
    }
}

// Usage
async function unreliableAPI() {
    if (Math.random() < 0.7) {
        throw new Error("Network error");
    }
    return "Success!";
}

retryOperation(unreliableAPI)
    .then(result => console.log("Final result:", result))
    .catch(error => console.log("All attempts failed:", error.message));
```

**Timeout Pattern:**
```javascript
function withTimeout(promise, timeoutMs) {
    const timeout = new Promise((_, reject) => {
        setTimeout(() => reject(new Error("Operation timed out")), timeoutMs);
    });
    
    return Promise.race([promise, timeout]);
}

async function fetchWithTimeout(url, timeoutMs = 5000) {
    try {
        const result = await withTimeout(fetch(url), timeoutMs);
        return result;
    } catch (error) {
        if (error.message === "Operation timed out") {
            console.log("Request timed out");
        }
        throw error;
    }
}
```

### 🎯 Key Points
- Async/await makes asynchronous code look synchronous
- Always use try-catch for error handling
- Understand sequential vs parallel execution
- Use Promise.all() for parallel operations
- Async functions always return promises
- Await can only be used inside async functions

### 💡 Interview Questions (Hinglish)

**Q1: Async/await kya hai aur Promise se kaise different hai?**

**A:**
Async/await Promise ka syntactic sugar hai, code ko synchronous jaisa dikhata hai:
```javascript
// Promise
fetchData().then(data => console.log(data)).catch(err => console.log(err));

// Async/await  
try {
    const data = await fetchData();
    console.log(data);
} catch (err) {
    console.log(err);
}
```

**Q2: Sequential aur parallel execution mein kya difference hai?**

**A:**
```javascript
// Sequential - ek ke baad ek (slow)
const a = await operation1(); // 1 sec
const b = await operation2(); // 1 sec  
// Total: 2 seconds

// Parallel - saath mein (fast)
const [a, b] = await Promise.all([
    operation1(), // 1 sec
    operation2()  // 1 sec  
]);
// Total: 1 second
```

**Q3: Async function mein error handling kaise karte hain?**

**A:**
Try-catch use karte hain:
```javascript
async function example() {
    try {
        const result = await riskyOperation();
        return result;
    } catch (error) {
        console.log("Error:", error.message);
        throw error; // Re-throw if needed
    }
}
```

---#
# Day 18: DOM Manipulation and Events

### What is the DOM?

**Definition:** DOM (Document Object Model) is a programming interface that represents HTML documents as a tree of objects that JavaScript can manipulate.

**Real-World Analogy:**
```
DOM = Building Blueprint
- HTML = Building structure  
- DOM = Interactive blueprint you can modify
- JavaScript = Architect who can change the blueprint
- Changes appear in real building (webpage)
```

**DOM Tree Structure:**
```
document
└── html
    ├── head
    │   ├── title
    │   └── meta
    └── body
        ├── h1
        ├── div
        │   ├── p
        │   └── button
        └── script
```

### Selecting DOM Elements

**Basic Selectors:**
```javascript
// By ID
const element = document.getElementById('myId');

// By Class Name (returns HTMLCollection)
const elements = document.getElementsByClassName('myClass');

// By Tag Name (returns HTMLCollection)
const paragraphs = document.getElementsByTagName('p');

// Query Selector (returns first match)
const element = document.querySelector('.myClass');
const element = document.querySelector('#myId');
const element = document.querySelector('div p'); // CSS selector

// Query Selector All (returns NodeList)
const elements = document.querySelectorAll('.myClass');
const elements = document.querySelectorAll('div p');
```

**Modern Approach (Recommended):**
```javascript
// Single element
const button = document.querySelector('#submitBtn');
const firstParagraph = document.querySelector('p');
const navItem = document.querySelector('.nav-item');

// Multiple elements
const allButtons = document.querySelectorAll('button');
const menuItems = document.querySelectorAll('.menu-item');

// Advanced selectors
const activeLinks = document.querySelectorAll('a.active');
const inputFields = document.querySelectorAll('input[type="text"]');
```

### Manipulating Element Content

**Text Content:**
```javascript
const heading = document.querySelector('h1');

// Get text content
console.log(heading.textContent); // Gets text only
console.log(heading.innerText);   // Gets visible text only

// Set text content
heading.textContent = "New Heading";
heading.innerText = "Another Heading";
```

**HTML Content:**
```javascript
const container = document.querySelector('.container');

// Get HTML content
console.log(container.innerHTML);

// Set HTML content
container.innerHTML = '<p>New <strong>HTML</strong> content</p>';

// Safer alternative (prevents XSS)
container.textContent = '<p>This will show as text, not HTML</p>';
```

**Attributes:**
```javascript
const image = document.querySelector('img');

// Get attributes
console.log(image.getAttribute('src'));
console.log(image.src); // Direct property access

// Set attributes
image.setAttribute('src', 'new-image.jpg');
image.src = 'another-image.jpg'; // Direct property

// Remove attributes
image.removeAttribute('alt');

// Check if attribute exists
if (image.hasAttribute('data-id')) {
    console.log('Has data-id attribute');
}
```

### Styling Elements

**CSS Classes:**
```javascript
const element = document.querySelector('.box');

// Add class
element.classList.add('active');
element.classList.add('highlight', 'important'); // Multiple classes

// Remove class
element.classList.remove('inactive');

// Toggle class
element.classList.toggle('visible'); // Add if not present, remove if present

// Check if class exists
if (element.classList.contains('active')) {
    console.log('Element is active');
}

// Replace class
element.classList.replace('old-class', 'new-class');
```

**Direct Styling:**
```javascript
const box = document.querySelector('.box');

// Set individual styles
box.style.backgroundColor = 'blue';
box.style.width = '200px';
box.style.height = '100px';
box.style.border = '2px solid red';

// Set multiple styles
Object.assign(box.style, {
    backgroundColor: 'green',
    color: 'white',
    padding: '20px',
    borderRadius: '10px'
});

// Get computed styles
const styles = window.getComputedStyle(box);
console.log(styles.backgroundColor);
console.log(styles.width);
```

### Creating and Modifying Elements

**Creating Elements:**
```javascript
// Create new element
const newDiv = document.createElement('div');
const newParagraph = document.createElement('p');
const newButton = document.createElement('button');

// Set content and attributes
newDiv.textContent = 'This is a new div';
newDiv.className = 'dynamic-content';
newDiv.id = 'newDiv';

newButton.textContent = 'Click Me';
newButton.setAttribute('type', 'button');
newButton.classList.add('btn', 'btn-primary');
```

**Adding Elements to DOM:**
```javascript
const container = document.querySelector('.container');
const newElement = document.createElement('p');
newElement.textContent = 'New paragraph';

// Append to end
container.appendChild(newElement);

// Prepend to beginning
container.prepend(newElement);

// Insert before specific element
const existingElement = document.querySelector('.existing');
container.insertBefore(newElement, existingElement);

// Modern methods
container.append(newElement); // Can append multiple elements
container.prepend(newElement);

// Insert adjacent
existingElement.insertAdjacentElement('beforebegin', newElement);
existingElement.insertAdjacentElement('afterend', newElement);
```

**Removing Elements:**
```javascript
const elementToRemove = document.querySelector('.remove-me');

// Modern way
elementToRemove.remove();

// Old way (still works)
elementToRemove.parentNode.removeChild(elementToRemove);

// Remove all children
const container = document.querySelector('.container');
container.innerHTML = ''; // Quick but not ideal for event listeners

// Better way to remove all children
while (container.firstChild) {
    container.removeChild(container.firstChild);
}
```

### Event Handling

**Adding Event Listeners:**
```javascript
const button = document.querySelector('#myButton');

// Basic event listener
button.addEventListener('click', function() {
    console.log('Button clicked!');
});

// Arrow function
button.addEventListener('click', () => {
    console.log('Button clicked with arrow function!');
});

// Named function (can be removed later)
function handleClick() {
    console.log('Button clicked with named function!');
}
button.addEventListener('click', handleClick);

// Remove event listener
button.removeEventListener('click', handleClick);
```

**Event Object:**
```javascript
button.addEventListener('click', function(event) {
    console.log('Event type:', event.type);
    console.log('Target element:', event.target);
    console.log('Current target:', event.currentTarget);
    console.log('Mouse position:', event.clientX, event.clientY);
    
    // Prevent default behavior
    event.preventDefault();
    
    // Stop event propagation
    event.stopPropagation();
});
```

**Common Events:**
```javascript
const input = document.querySelector('#textInput');
const form = document.querySelector('#myForm');
const div = document.querySelector('#myDiv');

// Input events
input.addEventListener('input', (e) => {
    console.log('Input value:', e.target.value);
});

input.addEventListener('focus', () => {
    console.log('Input focused');
});

input.addEventListener('blur', () => {
    console.log('Input lost focus');
});

// Form events
form.addEventListener('submit', (e) => {
    e.preventDefault(); // Prevent form submission
    console.log('Form submitted');
});

// Mouse events
div.addEventListener('mouseenter', () => {
    console.log('Mouse entered');
});

div.addEventListener('mouseleave', () => {
    console.log('Mouse left');
});

// Keyboard events
document.addEventListener('keydown', (e) => {
    console.log('Key pressed:', e.key);
    if (e.key === 'Escape') {
        console.log('Escape key pressed');
    }
});
```

### Event Delegation

**Problem with Multiple Elements:**
```javascript
// Inefficient - adding listener to each button
const buttons = document.querySelectorAll('.btn');
buttons.forEach(button => {
    button.addEventListener('click', handleButtonClick);
});
```

**Solution - Event Delegation:**
```javascript
// Efficient - single listener on parent
const container = document.querySelector('.button-container');

container.addEventListener('click', function(e) {
    // Check if clicked element is a button
    if (e.target.classList.contains('btn')) {
        console.log('Button clicked:', e.target.textContent);
        
        // Handle different button types
        if (e.target.classList.contains('delete-btn')) {
            handleDelete(e.target);
        } else if (e.target.classList.contains('edit-btn')) {
            handleEdit(e.target);
        }
    }
});

function handleDelete(button) {
    const item = button.closest('.item');
    item.remove();
}

function handleEdit(button) {
    const item = button.closest('.item');
    // Edit logic here
}
```

### Practical Examples

**Todo List Application:**
```javascript
class TodoApp {
    constructor() {
        this.todos = [];
        this.todoContainer = document.querySelector('#todoContainer');
        this.todoInput = document.querySelector('#todoInput');
        this.addButton = document.querySelector('#addButton');
        
        this.init();
    }
    
    init() {
        // Add event listeners
        this.addButton.addEventListener('click', () => this.addTodo());
        this.todoInput.addEventListener('keypress', (e) => {
            if (e.key === 'Enter') {
                this.addTodo();
            }
        });
        
        // Event delegation for todo actions
        this.todoContainer.addEventListener('click', (e) => {
            if (e.target.classList.contains('delete-btn')) {
                this.deleteTodo(e.target.dataset.id);
            } else if (e.target.classList.contains('toggle-btn')) {
                this.toggleTodo(e.target.dataset.id);
            }
        });
    }
    
    addTodo() {
        const text = this.todoInput.value.trim();
        if (!text) return;
        
        const todo = {
            id: Date.now(),
            text: text,
            completed: false
        };
        
        this.todos.push(todo);
        this.renderTodo(todo);
        this.todoInput.value = '';
    }
    
    renderTodo(todo) {
        const todoElement = document.createElement('div');
        todoElement.className = `todo-item ${todo.completed ? 'completed' : ''}`;
        todoElement.innerHTML = `
            <span class="todo-text">${todo.text}</span>
            <button class="toggle-btn" data-id="${todo.id}">
                ${todo.completed ? 'Undo' : 'Complete'}
            </button>
            <button class="delete-btn" data-id="${todo.id}">Delete</button>
        `;
        
        this.todoContainer.appendChild(todoElement);
    }
    
    deleteTodo(id) {
        this.todos = this.todos.filter(todo => todo.id != id);
        this.renderAllTodos();
    }
    
    toggleTodo(id) {
        const todo = this.todos.find(todo => todo.id == id);
        if (todo) {
            todo.completed = !todo.completed;
            this.renderAllTodos();
        }
    }
    
    renderAllTodos() {
        this.todoContainer.innerHTML = '';
        this.todos.forEach(todo => this.renderTodo(todo));
    }
}

// Initialize the app
// const todoApp = new TodoApp();
```

**Dynamic Form Validation:**
```javascript
class FormValidator {
    constructor(formSelector) {
        this.form = document.querySelector(formSelector);
        this.init();
    }
    
    init() {
        // Real-time validation
        this.form.addEventListener('input', (e) => {
            this.validateField(e.target);
        });
        
        // Form submission
        this.form.addEventListener('submit', (e) => {
            e.preventDefault();
            this.validateForm();
        });
    }
    
    validateField(field) {
        const value = field.value.trim();
        const fieldName = field.name;
        let isValid = true;
        let message = '';
        
        // Remove existing error
        this.clearFieldError(field);
        
        // Validation rules
        switch (fieldName) {
            case 'email':
                isValid = /^[^\s@]+@[^\s@]+\.[^\s@]+$/.test(value);
                message = 'Please enter a valid email address';
                break;
                
            case 'password':
                isValid = value.length >= 8;
                message = 'Password must be at least 8 characters';
                break;
                
            case 'name':
                isValid = value.length >= 2;
                message = 'Name must be at least 2 characters';
                break;
        }
        
        if (!isValid && value !== '') {
            this.showFieldError(field, message);
        }
        
        return isValid;
    }
    
    showFieldError(field, message) {
        field.classList.add('error');
        
        const errorElement = document.createElement('div');
        errorElement.className = 'error-message';
        errorElement.textContent = message;
        
        field.parentNode.appendChild(errorElement);
    }
    
    clearFieldError(field) {
        field.classList.remove('error');
        const errorMessage = field.parentNode.querySelector('.error-message');
        if (errorMessage) {
            errorMessage.remove();
        }
    }
    
    validateForm() {
        const fields = this.form.querySelectorAll('input[required]');
        let isFormValid = true;
        
        fields.forEach(field => {
            if (!this.validateField(field)) {
                isFormValid = false;
            }
        });
        
        if (isFormValid) {
            console.log('Form is valid! Submitting...');
            // Submit form logic here
        } else {
            console.log('Form has errors');
        }
    }
}

// Usage
// const validator = new FormValidator('#myForm');
```

### 🎯 Key Points
- DOM represents HTML as manipulable objects
- Use querySelector/querySelectorAll for modern element selection
- Manipulate content with textContent/innerHTML
- Use classList for CSS class management
- Event delegation is efficient for multiple similar elements
- Always prevent default behavior when needed

### 💡 Interview Questions (Hinglish)

**Q1: DOM kya hai aur JavaScript isse kaise interact karta hai?**

**A:**
DOM (Document Object Model) HTML ko object tree ke form mein represent karta hai:
```javascript
// HTML: <div id="myDiv">Hello</div>
const div = document.querySelector('#myDiv');
div.textContent = 'New content'; // Changes HTML
```

**Q2: Event delegation kya hai aur kab use karte hain?**

**A:**
Event delegation parent element par ek listener lagana hai multiple children ke liye:
```javascript
// Instead of this (inefficient)
buttons.forEach(btn => btn.addEventListener('click', handler));

// Do this (efficient)
container.addEventListener('click', (e) => {
    if (e.target.matches('button')) {
        handler(e);
    }
});
```

**Q3: Element create aur DOM mein add kaise karte hain?**

**A:**
```javascript
// Create element
const div = document.createElement('div');
div.textContent = 'New element';
div.classList.add('my-class');

// Add to DOM
document.body.appendChild(div);
// or
document.querySelector('.container').append(div);
```

---##
 Day 19: Object-Oriented Programming Basics

### What is Object-Oriented Programming?

**Definition:** OOP is a programming paradigm that organizes code into objects that contain both data (properties) and functions (methods) that work with that data.

**Real-World Analogy:**
```
OOP = Car Manufacturing
- Class = Car Blueprint (design/template)
- Object = Actual Car (instance made from blueprint)
- Properties = Car features (color, model, engine)
- Methods = Car actions (start, stop, accelerate)
```

### Classes in JavaScript

**Basic Class Syntax:**
```javascript
class Car {
    // Constructor - runs when new object is created
    constructor(make, model, year) {
        this.make = make;     // Property
        this.model = model;   // Property
        this.year = year;     // Property
        this.isRunning = false; // Default property
    }
    
    // Method - function inside class
    start() {
        this.isRunning = true;
        return `${this.make} ${this.model} is now running`;
    }
    
    stop() {
        this.isRunning = false;
        return `${this.make} ${this.model} has stopped`;
    }
    
    getInfo() {
        return `${this.year} ${this.make} ${this.model}`;
    }
}

// Creating objects (instances)
const car1 = new Car("Toyota", "Camry", 2022);
const car2 = new Car("Honda", "Civic", 2021);

console.log(car1.getInfo()); // "2022 Toyota Camry"
console.log(car1.start());   // "Toyota Camry is now running"
console.log(car2.getInfo()); // "2021 Honda Civic"
```

### Constructor Function (Old Way)

**Before ES6 Classes:**
```javascript
// Constructor function
function Car(make, model, year) {
    this.make = make;
    this.model = model;
    this.year = year;
    this.isRunning = false;
}

// Adding methods to prototype
Car.prototype.start = function() {
    this.isRunning = true;
    return `${this.make} ${this.model} is now running`;
};

Car.prototype.stop = function() {
    this.isRunning = false;
    return `${this.make} ${this.model} has stopped`;
};

// Usage (same as class)
const car = new Car("Toyota", "Camry", 2022);
```

### Instance vs Static Methods

**Instance Methods (work on specific object):**
```javascript
class Calculator {
    constructor() {
        this.result = 0;
    }
    
    // Instance method - works on specific calculator object
    add(number) {
        this.result += number;
        return this;
    }
    
    subtract(number) {
        this.result -= number;
        return this;
    }
    
    getResult() {
        return this.result;
    }
}

const calc1 = new Calculator();
const calc2 = new Calculator();

calc1.add(10).subtract(3); // calc1.result = 7
calc2.add(5);              // calc2.result = 5
```

**Static Methods (work on class itself):**
```javascript
class MathUtils {
    // Static method - called on class, not instance
    static add(a, b) {
        return a + b;
    }
    
    static multiply(a, b) {
        return a * b;
    }
    
    static PI = 3.14159; // Static property
}

// Call static methods on class
console.log(MathUtils.add(5, 3));      // 8
console.log(MathUtils.multiply(4, 2)); // 8
console.log(MathUtils.PI);             // 3.14159

// Cannot call on instance
const math = new MathUtils();
// math.add(1, 2); // Error! add is not a function
```

### Getters and Setters

**Controlling Property Access:**
```javascript
class Person {
    constructor(firstName, lastName, age) {
        this.firstName = firstName;
        this.lastName = lastName;
        this._age = age; // Private convention (underscore)
    }
    
    // Getter - access like property
    get fullName() {
        return `${this.firstName} ${this.lastName}`;
    }
    
    get age() {
        return this._age;
    }
    
    // Setter - set like property
    set age(newAge) {
        if (newAge < 0 || newAge > 150) {
            throw new Error("Invalid age");
        }
        this._age = newAge;
    }
    
    set fullName(name) {
        const parts = name.split(' ');
        this.firstName = parts[0];
        this.lastName = parts[1];
    }
}

const person = new Person("Raj", "Sharma", 25);

// Using getters (like properties)
console.log(person.fullName); // "Raj Sharma"
console.log(person.age);       // 25

// Using setters (like properties)
person.age = 26;              // Calls setter
person.fullName = "Amit Kumar"; // Calls setter

console.log(person.firstName); // "Amit"
console.log(person.lastName);  // "Kumar"
```

### Inheritance

**Extending Classes:**
```javascript
// Parent class (Base class)
class Animal {
    constructor(name, species) {
        this.name = name;
        this.species = species;
    }
    
    makeSound() {
        return `${this.name} makes a sound`;
    }
    
    eat() {
        return `${this.name} is eating`;
    }
}

// Child class (Derived class)
class Dog extends Animal {
    constructor(name, breed) {
        super(name, "Canine"); // Call parent constructor
        this.breed = breed;
    }
    
    // Override parent method
    makeSound() {
        return `${this.name} barks: Woof! Woof!`;
    }
    
    // New method specific to Dog
    wagTail() {
        return `${this.name} is wagging tail`;
    }
}

class Cat extends Animal {
    constructor(name, breed) {
        super(name, "Feline");
        this.breed = breed;
    }
    
    makeSound() {
        return `${this.name} meows: Meow!`;
    }
    
    purr() {
        return `${this.name} is purring`;
    }
}

// Usage
const dog = new Dog("Buddy", "Golden Retriever");
const cat = new Cat("Whiskers", "Persian");

console.log(dog.makeSound()); // "Buddy barks: Woof! Woof!"
console.log(cat.makeSound()); // "Whiskers meows: Meow!"
console.log(dog.eat());       // "Buddy is eating" (inherited)
console.log(dog.wagTail());   // "Buddy is wagging tail"
```

### Method Overriding and Super

**Using Super to Call Parent Methods:**
```javascript
class Vehicle {
    constructor(make, model) {
        this.make = make;
        this.model = model;
    }
    
    start() {
        return `${this.make} ${this.model} engine started`;
    }
    
    getInfo() {
        return `Vehicle: ${this.make} ${this.model}`;
    }
}

class ElectricCar extends Vehicle {
    constructor(make, model, batteryCapacity) {
        super(make, model); // Call parent constructor
        this.batteryCapacity = batteryCapacity;
    }
    
    start() {
        // Call parent method and extend it
        const parentResult = super.start();
        return `${parentResult} (Electric motor activated)`;
    }
    
    getInfo() {
        // Call parent method and extend it
        const parentInfo = super.getInfo();
        return `${parentInfo}, Battery: ${this.batteryCapacity}kWh`;
    }
    
    charge() {
        return `Charging ${this.make} ${this.model}`;
    }
}

const tesla = new ElectricCar("Tesla", "Model 3", 75);
console.log(tesla.start());   // "Tesla Model 3 engine started (Electric motor activated)"
console.log(tesla.getInfo()); // "Vehicle: Tesla Model 3, Battery: 75kWh"
console.log(tesla.charge());  // "Charging Tesla Model 3"
```

### Private Fields and Methods (Modern JavaScript)

**True Private Members:**
```javascript
class BankAccount {
    // Private fields (start with #)
    #balance = 0;
    #accountNumber;
    
    constructor(accountNumber, initialBalance = 0) {
        this.#accountNumber = accountNumber;
        this.#balance = initialBalance;
    }
    
    // Private method
    #validateAmount(amount) {
        return amount > 0 && typeof amount === 'number';
    }
    
    // Public methods
    deposit(amount) {
        if (this.#validateAmount(amount)) {
            this.#balance += amount;
            return `Deposited ₹${amount}. New balance: ₹${this.#balance}`;
        }
        throw new Error("Invalid amount");
    }
    
    withdraw(amount) {
        if (!this.#validateAmount(amount)) {
            throw new Error("Invalid amount");
        }
        
        if (amount > this.#balance) {
            throw new Error("Insufficient funds");
        }
        
        this.#balance -= amount;
        return `Withdrawn ₹${amount}. New balance: ₹${this.#balance}`;
    }
    
    getBalance() {
        return this.#balance;
    }
    
    getAccountInfo() {
        return {
            accountNumber: this.#accountNumber,
            balance: this.#balance
        };
    }
}

const account = new BankAccount("ACC123", 1000);
console.log(account.deposit(500));  // "Deposited ₹500. New balance: ₹1500"
console.log(account.withdraw(200)); // "Withdrawn ₹200. New balance: ₹1300"
console.log(account.getBalance());  // 1300

// These will cause errors:
// console.log(account.#balance);      // SyntaxError
// account.#validateAmount(100);       // SyntaxError
```

### Practical Example: Library Management System

```javascript
class Book {
    constructor(title, author, isbn, copies = 1) {
        this.title = title;
        this.author = author;
        this.isbn = isbn;
        this.totalCopies = copies;
        this.availableCopies = copies;
        this.borrowedBy = [];
    }
    
    isAvailable() {
        return this.availableCopies > 0;
    }
    
    borrow(memberId) {
        if (!this.isAvailable()) {
            throw new Error(`No copies of "${this.title}" available`);
        }
        
        this.availableCopies--;
        this.borrowedBy.push({
            memberId,
            borrowDate: new Date()
        });
        
        return `"${this.title}" borrowed successfully`;
    }
    
    return(memberId) {
        const borrowIndex = this.borrowedBy.findIndex(
            record => record.memberId === memberId
        );
        
        if (borrowIndex === -1) {
            throw new Error(`Member ${memberId} hasn't borrowed this book`);
        }
        
        this.borrowedBy.splice(borrowIndex, 1);
        this.availableCopies++;
        
        return `"${this.title}" returned successfully`;
    }
    
    getInfo() {
        return {
            title: this.title,
            author: this.author,
            isbn: this.isbn,
            available: this.availableCopies,
            total: this.totalCopies
        };
    }
}

class Member {
    constructor(id, name, email) {
        this.id = id;
        this.name = name;
        this.email = email;
        this.borrowedBooks = [];
        this.joinDate = new Date();
    }
    
    borrowBook(book) {
        try {
            const result = book.borrow(this.id);
            this.borrowedBooks.push(book.isbn);
            return result;
        } catch (error) {
            throw error;
        }
    }
    
    returnBook(book) {
        try {
            const result = book.return(this.id);
            const bookIndex = this.borrowedBooks.indexOf(book.isbn);
            if (bookIndex > -1) {
                this.borrowedBooks.splice(bookIndex, 1);
            }
            return result;
        } catch (error) {
            throw error;
        }
    }
    
    getBorrowedBooks() {
        return this.borrowedBooks;
    }
}

class Library {
    constructor(name) {
        this.name = name;
        this.books = new Map(); // ISBN -> Book
        this.members = new Map(); // ID -> Member
    }
    
    addBook(book) {
        if (this.books.has(book.isbn)) {
            // Book already exists, increase copies
            const existingBook = this.books.get(book.isbn);
            existingBook.totalCopies += book.totalCopies;
            existingBook.availableCopies += book.availableCopies;
        } else {
            this.books.set(book.isbn, book);
        }
        return `Book "${book.title}" added to library`;
    }
    
    addMember(member) {
        if (this.members.has(member.id)) {
            throw new Error(`Member with ID ${member.id} already exists`);
        }
        this.members.set(member.id, member);
        return `Member "${member.name}" added to library`;
    }
    
    borrowBook(memberId, isbn) {
        const member = this.members.get(memberId);
        const book = this.books.get(isbn);
        
        if (!member) {
            throw new Error(`Member with ID ${memberId} not found`);
        }
        
        if (!book) {
            throw new Error(`Book with ISBN ${isbn} not found`);
        }
        
        return member.borrowBook(book);
    }
    
    returnBook(memberId, isbn) {
        const member = this.members.get(memberId);
        const book = this.books.get(isbn);
        
        if (!member) {
            throw new Error(`Member with ID ${memberId} not found`);
        }
        
        if (!book) {
            throw new Error(`Book with ISBN ${isbn} not found`);
        }
        
        return member.returnBook(book);
    }
    
    searchBooks(query) {
        const results = [];
        for (const book of this.books.values()) {
            if (book.title.toLowerCase().includes(query.toLowerCase()) ||
                book.author.toLowerCase().includes(query.toLowerCase())) {
                results.push(book.getInfo());
            }
        }
        return results;
    }
    
    getLibraryStats() {
        const totalBooks = Array.from(this.books.values())
            .reduce((sum, book) => sum + book.totalCopies, 0);
        
        const availableBooks = Array.from(this.books.values())
            .reduce((sum, book) => sum + book.availableCopies, 0);
        
        return {
            name: this.name,
            totalMembers: this.members.size,
            totalBooks: totalBooks,
            availableBooks: availableBooks,
            borrowedBooks: totalBooks - availableBooks
        };
    }
}

// Usage Example
const library = new Library("City Central Library");

// Add books
const book1 = new Book("JavaScript: The Good Parts", "Douglas Crockford", "978-0596517748", 3);
const book2 = new Book("Clean Code", "Robert Martin", "978-0132350884", 2);

console.log(library.addBook(book1));
console.log(library.addBook(book2));

// Add members
const member1 = new Member("M001", "Raj Sharma", "raj@example.com");
const member2 = new Member("M002", "Priya Patel", "priya@example.com");

console.log(library.addMember(member1));
console.log(library.addMember(member2));

// Borrow books
console.log(library.borrowBook("M001", "978-0596517748"));
console.log(library.borrowBook("M002", "978-0132350884"));

// Library stats
console.log(library.getLibraryStats());

// Search books
console.log(library.searchBooks("JavaScript"));
```

### 🎯 Key Points
- Classes are blueprints for creating objects
- Constructor initializes object properties
- Methods are functions inside classes
- Inheritance allows classes to extend other classes
- Use super() to call parent constructor/methods
- Private fields (#) provide true encapsulation
- Static methods belong to class, not instances

### 💡 Interview Questions (Hinglish)

**Q1: Class aur Object mein kya difference hai?**

**A:**
- Class: Blueprint/template hai objects banane ke liye
- Object: Class ka instance hai, actual data ke saath
```javascript
class Car { } // Class (blueprint)
const myCar = new Car(); // Object (instance)
```

**Q2: Inheritance kya hai aur kaise implement karte hain?**

**A:**
Inheritance ek class ko dusri class se properties aur methods inherit karne deta hai:
```javascript
class Animal {
    eat() { return "eating"; }
}

class Dog extends Animal {
    bark() { return "barking"; }
}

const dog = new Dog();
dog.eat(); // Inherited method
dog.bark(); // Own method
```

**Q3: Static methods kya hote hain?**

**A:**
Static methods class par call hote hain, instance par nahi:
```javascript
class MathUtils {
    static add(a, b) { return a + b; }
}

MathUtils.add(2, 3); // ✓ Correct
const math = new MathUtils();
math.add(2, 3); // ✗ Error
```

---## Day 20
: Modules and Modern JavaScript Features

### What are Modules?

**Definition:** Modules are separate files that contain reusable code. They help organize code, avoid naming conflicts, and make code more maintainable.

**Real-World Analogy:**
```
Modules = Kitchen Appliances
- Each appliance (module) has specific function
- Microwave (module) heats food
- Blender (module) makes smoothies  
- You import what you need for cooking
- Each works independently but can work together
```

### ES6 Modules (Import/Export)

**Named Exports:**
```javascript
// math.js - Exporting multiple functions
export function add(a, b) {
    return a + b;
}

export function subtract(a, b) {
    return a - b;
}

export const PI = 3.14159;

export class Calculator {
    multiply(a, b) {
        return a * b;
    }
}

// Alternative syntax - export at end
function divide(a, b) {
    if (b === 0) throw new Error("Division by zero");
    return a / b;
}

const E = 2.71828;

export { divide, E };
```

**Default Exports:**
```javascript
// user.js - One main export per file
class User {
    constructor(name, email) {
        this.name = name;
        this.email = email;
    }
    
    getInfo() {
        return `${this.name} (${this.email})`;
    }
}

export default User;

// Or inline default export
export default class User {
    // class definition
}

// Or with functions
export default function createUser(name, email) {
    return new User(name, email);
}
```

**Importing Modules:**
```javascript
// main.js - Importing from other modules

// Named imports
import { add, subtract, PI } from './math.js';
import { Calculator } from './math.js';

// Import with alias
import { add as sum, subtract as minus } from './math.js';

// Import all named exports
import * as MathUtils from './math.js';

// Default import
import User from './user.js';

// Mixed imports
import User, { add, PI } from './utils.js';

// Usage
console.log(add(5, 3));           // 8
console.log(sum(5, 3));           // 8 (alias)
console.log(MathUtils.add(5, 3)); // 8 (namespace)

const user = new User("Raj", "raj@example.com");
console.log(user.getInfo());
```

### Module Patterns

**Utility Module:**
```javascript
// utils.js
export const formatCurrency = (amount, currency = 'INR') => {
    return new Intl.NumberFormat('en-IN', {
        style: 'currency',
        currency: currency
    }).format(amount);
};

export const formatDate = (date, locale = 'en-IN') => {
    return new Intl.DateTimeFormat(locale).format(date);
};

export const debounce = (func, delay) => {
    let timeoutId;
    return function (...args) {
        clearTimeout(timeoutId);
        timeoutId = setTimeout(() => func.apply(this, args), delay);
    };
};

export const throttle = (func, limit) => {
    let inThrottle;
    return function (...args) {
        if (!inThrottle) {
            func.apply(this, args);
            inThrottle = true;
            setTimeout(() => inThrottle = false, limit);
        }
    };
};

// Usage in another file
import { formatCurrency, debounce } from './utils.js';

console.log(formatCurrency(1000)); // ₹1,000.00
const debouncedSearch = debounce(searchFunction, 300);
```

**API Module:**
```javascript
// api.js
const BASE_URL = 'https://jsonplaceholder.typicode.com';

class ApiClient {
    async get(endpoint) {
        try {
            const response = await fetch(`${BASE_URL}${endpoint}`);
            if (!response.ok) {
                throw new Error(`HTTP error! status: ${response.status}`);
            }
            return await response.json();
        } catch (error) {
            console.error('API GET error:', error);
            throw error;
        }
    }
    
    async post(endpoint, data) {
        try {
            const response = await fetch(`${BASE_URL}${endpoint}`, {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify(data)
            });
            
            if (!response.ok) {
                throw new Error(`HTTP error! status: ${response.status}`);
            }
            
            return await response.json();
        } catch (error) {
            console.error('API POST error:', error);
            throw error;
        }
    }
}

// Specific API functions
export const getUsers = () => {
    const api = new ApiClient();
    return api.get('/users');
};

export const getUser = (id) => {
    const api = new ApiClient();
    return api.get(`/users/${id}`);
};

export const createUser = (userData) => {
    const api = new ApiClient();
    return api.post('/users', userData);
};

export default ApiClient;
```

### Modern JavaScript Features

#### Optional Chaining (?.)
```javascript
// Problem: Accessing nested properties safely
const user = {
    name: "Raj",
    address: {
        street: "123 Main St",
        city: "Delhi"
    }
};

// Old way - lots of checking
if (user && user.address && user.address.street) {
    console.log(user.address.street);
}

// Modern way - optional chaining
console.log(user?.address?.street); // "123 Main St"
console.log(user?.phone?.number);   // undefined (no error)

// With arrays
const users = [
    { name: "Raj", posts: [{ title: "Hello" }] }
];

console.log(users[0]?.posts?.[0]?.title); // "Hello"
console.log(users[1]?.posts?.[0]?.title); // undefined

// With methods
user?.getName?.(); // Calls method only if it exists
```

#### Nullish Coalescing (??)
```javascript
// Problem: Default values with falsy values
let username = "";
let displayName = username || "Guest"; // "Guest" (but "" might be valid)

// Solution: Nullish coalescing (only null/undefined)
let displayName = username ?? "Guest"; // "" (keeps empty string)

// Examples
console.log(null ?? "default");      // "default"
console.log(undefined ?? "default"); // "default"
console.log("" ?? "default");        // "" (empty string is kept)
console.log(0 ?? "default");         // 0 (zero is kept)
console.log(false ?? "default");     // false (false is kept)

// Practical example
function createUser(options = {}) {
    return {
        name: options.name ?? "Anonymous",
        age: options.age ?? 0,
        isActive: options.isActive ?? true
    };
}

console.log(createUser({ name: "", age: 0, isActive: false }));
// { name: "", age: 0, isActive: false } - preserves falsy values
```

#### Logical Assignment Operators
```javascript
// ||= (OR assignment)
let name = "";
name ||= "Default Name"; // Assigns if name is falsy
console.log(name); // "Default Name"

// &&= (AND assignment)  
let user = { name: "Raj" };
user.name &&= user.name.toUpperCase(); // Assigns if name is truthy
console.log(user.name); // "RAJ"

// ??= (Nullish assignment)
let config = { theme: null };
config.theme ??= "light"; // Assigns if theme is null/undefined
console.log(config.theme); // "light"

// Practical example
class Settings {
    constructor(options = {}) {
        this.theme = options.theme;
        this.language = options.language;
        this.notifications = options.notifications;
        
        // Set defaults only if null/undefined
        this.theme ??= "light";
        this.language ??= "en";
        this.notifications ??= true;
    }
}
```

#### Numeric Separators
```javascript
// Large numbers are hard to read
const million = 1000000;
const billion = 1000000000;

// Use underscores for readability
const million = 1_000_000;
const billion = 1_000_000_000;
const decimal = 123.456_789;
const binary = 0b1010_0001;
const hex = 0xFF_EC_DE_5E;

console.log(million); // 1000000 (underscores ignored at runtime)
```

#### String Methods
```javascript
// replaceAll()
const text = "Hello world, world is beautiful";
console.log(text.replaceAll("world", "universe"));
// "Hello universe, universe is beautiful"

// at() - negative indexing
const str = "JavaScript";
console.log(str.at(-1));  // "t" (last character)
console.log(str.at(-2));  // "p" (second last)

// Array at() method
const arr = [1, 2, 3, 4, 5];
console.log(arr.at(-1)); // 5 (last element)
console.log(arr.at(-2)); // 4 (second last)
```

### Practical Module Example: Task Manager

**models/task.js:**
```javascript
export class Task {
    constructor(title, description = "", priority = "medium") {
        this.id = Date.now() + Math.random();
        this.title = title;
        this.description = description;
        this.priority = priority;
        this.completed = false;
        this.createdAt = new Date();
        this.updatedAt = new Date();
    }
    
    complete() {
        this.completed = true;
        this.updatedAt = new Date();
    }
    
    update(updates) {
        Object.assign(this, updates);
        this.updatedAt = new Date();
    }
    
    toJSON() {
        return {
            id: this.id,
            title: this.title,
            description: this.description,
            priority: this.priority,
            completed: this.completed,
            createdAt: this.createdAt.toISOString(),
            updatedAt: this.updatedAt.toISOString()
        };
    }
}
```

**services/taskService.js:**
```javascript
import { Task } from '../models/task.js';

class TaskService {
    constructor() {
        this.tasks = this.loadTasks();
    }
    
    createTask(title, description, priority) {
        const task = new Task(title, description, priority);
        this.tasks.push(task);
        this.saveTasks();
        return task;
    }
    
    getTasks(filter = {}) {
        let filteredTasks = [...this.tasks];
        
        if (filter.completed !== undefined) {
            filteredTasks = filteredTasks.filter(
                task => task.completed === filter.completed
            );
        }
        
        if (filter.priority) {
            filteredTasks = filteredTasks.filter(
                task => task.priority === filter.priority
            );
        }
        
        return filteredTasks;
    }
    
    getTask(id) {
        return this.tasks.find(task => task.id === id);
    }
    
    updateTask(id, updates) {
        const task = this.getTask(id);
        if (task) {
            task.update(updates);
            this.saveTasks();
            return task;
        }
        throw new Error(`Task with id ${id} not found`);
    }
    
    deleteTask(id) {
        const index = this.tasks.findIndex(task => task.id === id);
        if (index > -1) {
            const deletedTask = this.tasks.splice(index, 1)[0];
            this.saveTasks();
            return deletedTask;
        }
        throw new Error(`Task with id ${id} not found`);
    }
    
    completeTask(id) {
        const task = this.getTask(id);
        if (task) {
            task.complete();
            this.saveTasks();
            return task;
        }
        throw new Error(`Task with id ${id} not found`);
    }
    
    getStats() {
        const total = this.tasks.length;
        const completed = this.tasks.filter(task => task.completed).length;
        const pending = total - completed;
        
        const byPriority = this.tasks.reduce((acc, task) => {
            acc[task.priority] = (acc[task.priority] || 0) + 1;
            return acc;
        }, {});
        
        return {
            total,
            completed,
            pending,
            byPriority
        };
    }
    
    loadTasks() {
        try {
            const saved = localStorage.getItem('tasks');
            if (saved) {
                const taskData = JSON.parse(saved);
                return taskData.map(data => {
                    const task = new Task(data.title, data.description, data.priority);
                    Object.assign(task, data);
                    task.createdAt = new Date(data.createdAt);
                    task.updatedAt = new Date(data.updatedAt);
                    return task;
                });
            }
        } catch (error) {
            console.error('Error loading tasks:', error);
        }
        return [];
    }
    
    saveTasks() {
        try {
            const taskData = this.tasks.map(task => task.toJSON());
            localStorage.setItem('tasks', JSON.stringify(taskData));
        } catch (error) {
            console.error('Error saving tasks:', error);
        }
    }
}

export default new TaskService(); // Singleton instance
```

**utils/validators.js:**
```javascript
export const validateTask = (taskData) => {
    const errors = [];
    
    if (!taskData?.title?.trim()) {
        errors.push("Title is required");
    }
    
    if (taskData.title && taskData.title.length > 100) {
        errors.push("Title must be less than 100 characters");
    }
    
    const validPriorities = ["low", "medium", "high"];
    if (taskData.priority && !validPriorities.includes(taskData.priority)) {
        errors.push("Priority must be low, medium, or high");
    }
    
    return {
        isValid: errors.length === 0,
        errors
    };
};

export const sanitizeInput = (input) => {
    return input?.toString().trim().replace(/[<>]/g, '') ?? '';
};
```

**main.js:**
```javascript
import taskService from './services/taskService.js';
import { validateTask, sanitizeInput } from './utils/validators.js';

class TaskManager {
    constructor() {
        this.init();
    }
    
    init() {
        this.renderTasks();
        this.setupEventListeners();
    }
    
    setupEventListeners() {
        const form = document.querySelector('#taskForm');
        form?.addEventListener('submit', (e) => {
            e.preventDefault();
            this.handleAddTask(e);
        });
        
        const taskList = document.querySelector('#taskList');
        taskList?.addEventListener('click', (e) => {
            if (e.target.classList.contains('complete-btn')) {
                this.handleCompleteTask(e.target.dataset.id);
            } else if (e.target.classList.contains('delete-btn')) {
                this.handleDeleteTask(e.target.dataset.id);
            }
        });
    }
    
    handleAddTask(event) {
        const formData = new FormData(event.target);
        const taskData = {
            title: sanitizeInput(formData.get('title')),
            description: sanitizeInput(formData.get('description')),
            priority: formData.get('priority')
        };
        
        const validation = validateTask(taskData);
        if (!validation.isValid) {
            this.showErrors(validation.errors);
            return;
        }
        
        try {
            taskService.createTask(
                taskData.title,
                taskData.description,
                taskData.priority
            );
            
            event.target.reset();
            this.renderTasks();
            this.showSuccess("Task created successfully!");
            
        } catch (error) {
            this.showError("Failed to create task: " + error.message);
        }
    }
    
    handleCompleteTask(taskId) {
        try {
            taskService.completeTask(Number(taskId));
            this.renderTasks();
            this.showSuccess("Task completed!");
        } catch (error) {
            this.showError("Failed to complete task: " + error.message);
        }
    }
    
    handleDeleteTask(taskId) {
        if (confirm("Are you sure you want to delete this task?")) {
            try {
                taskService.deleteTask(Number(taskId));
                this.renderTasks();
                this.showSuccess("Task deleted!");
            } catch (error) {
                this.showError("Failed to delete task: " + error.message);
            }
        }
    }
    
    renderTasks() {
        const tasks = taskService.getTasks();
        const taskList = document.querySelector('#taskList');
        
        if (!taskList) return;
        
        taskList.innerHTML = tasks.map(task => `
            <div class="task-item ${task.completed ? 'completed' : ''}">
                <h3>${task.title}</h3>
                <p>${task.description}</p>
                <span class="priority priority-${task.priority}">${task.priority}</span>
                <div class="task-actions">
                    ${!task.completed ? 
                        `<button class="complete-btn" data-id="${task.id}">Complete</button>` : 
                        '<span class="completed-badge">✓ Completed</span>'
                    }
                    <button class="delete-btn" data-id="${task.id}">Delete</button>
                </div>
            </div>
        `).join('');
        
        this.renderStats();
    }
    
    renderStats() {
        const stats = taskService.getStats();
        const statsElement = document.querySelector('#stats');
        
        if (statsElement) {
            statsElement.innerHTML = `
                <div class="stat">Total: ${stats.total}</div>
                <div class="stat">Completed: ${stats.completed}</div>
                <div class="stat">Pending: ${stats.pending}</div>
            `;
        }
    }
    
    showSuccess(message) {
        this.showMessage(message, 'success');
    }
    
    showError(message) {
        this.showMessage(message, 'error');
    }
    
    showErrors(errors) {
        this.showMessage(errors.join(', '), 'error');
    }
    
    showMessage(message, type) {
        // Implementation for showing toast messages
        console.log(`${type.toUpperCase()}: ${message}`);
    }
}

// Initialize the application
document.addEventListener('DOMContentLoaded', () => {
    new TaskManager();
});
```

### 🎯 Key Points
- Modules organize code into reusable files
- Use named exports for multiple exports, default for single main export
- Import only what you need to keep bundle size small
- Optional chaining (?.) safely accesses nested properties
- Nullish coalescing (??) provides better default value handling
- Modern features make code more readable and maintainable

### 💡 Interview Questions (Hinglish)

**Q1: ES6 modules kya hain aur kaise use karte hain?**

**A:**
Modules code ko separate files mein organize karne ka way hai:
```javascript
// math.js
export const add = (a, b) => a + b;
export default class Calculator { }

// main.js  
import Calculator, { add } from './math.js';
```

**Q2: Optional chaining (?.) kya hai?**

**A:**
Safely nested properties access karne ka modern way:
```javascript
// Old way
if (user && user.address && user.address.street) { }

// New way
console.log(user?.address?.street); // No error if any part is null/undefined
```

**Q3: Nullish coalescing (??) aur OR (||) mein kya difference hai?**

**A:**
```javascript
// || treats all falsy values as "no value"
"" || "default"    // "default"
0 || "default"     // "default"

// ?? only treats null/undefined as "no value"  
"" ?? "default"    // ""
0 ?? "default"     // 0
null ?? "default"  // "default"
```

---##
 Day 21: Week 3 Review and Advanced Practice

### Week 3 Summary

This week we explored advanced JavaScript concepts that are crucial for modern development:

**Day 15: Advanced Functions and Scope**
- Function declarations vs expressions vs arrow functions
- Scope chain and hoisting behavior
- Closures and their practical applications
- Higher-order functions and IIFE patterns

**Day 16: Asynchronous JavaScript - Callbacks and Promises**
- Understanding asynchronous programming
- Callback functions and callback hell
- Promises and promise chaining
- Promise.all() and Promise.race()

**Day 17: Async/Await and Modern Patterns**
- Async/await syntax for cleaner code
- Error handling with try-catch
- Sequential vs parallel execution
- Real-world async patterns

**Day 18: DOM Manipulation and Events**
- Selecting and manipulating DOM elements
- Event handling and event delegation
- Creating dynamic user interfaces
- Best practices for DOM interaction

**Day 19: Object-Oriented Programming**
- Classes and constructors
- Inheritance and method overriding
- Private fields and static methods
- Real-world OOP applications

**Day 20: Modules and Modern Features**
- ES6 import/export system
- Module organization patterns
- Optional chaining and nullish coalescing
- Modern JavaScript syntax features

### Advanced Practice Projects

**Project 1: Advanced Todo Application with Local Storage**
```javascript
// models/todo.js
export class Todo {
    constructor(text, category = 'general', priority = 'medium') {
        this.id = crypto.randomUUID();
        this.text = text;
        this.category = category;
        this.priority = priority;
        this.completed = false;
        this.createdAt = new Date();
        this.updatedAt = new Date();
        this.dueDate = null;
        this.tags = [];
    }
    
    toggle() {
        this.completed = !this.completed;
        this.updatedAt = new Date();
        return this;
    }
    
    update(updates) {
        Object.assign(this, updates);
        this.updatedAt = new Date();
        return this;
    }
    
    addTag(tag) {
        if (!this.tags.includes(tag)) {
            this.tags.push(tag);
            this.updatedAt = new Date();
        }
        return this;
    }
    
    removeTag(tag) {
        this.tags = this.tags.filter(t => t !== tag);
        this.updatedAt = new Date();
        return this;
    }
    
    isOverdue() {
        return this.dueDate && new Date() > new Date(this.dueDate) && !this.completed;
    }
    
    toJSON() {
        return {
            id: this.id,
            text: this.text,
            category: this.category,
            priority: this.priority,
            completed: this.completed,
            createdAt: this.createdAt.toISOString(),
            updatedAt: this.updatedAt.toISOString(),
            dueDate: this.dueDate,
            tags: [...this.tags]
        };
    }
    
    static fromJSON(data) {
        const todo = new Todo(data.text, data.category, data.priority);
        Object.assign(todo, {
            id: data.id,
            completed: data.completed,
            createdAt: new Date(data.createdAt),
            updatedAt: new Date(data.updatedAt),
            dueDate: data.dueDate,
            tags: data.tags || []
        });
        return todo;
    }
}
```

```javascript
// services/todoService.js
import { Todo } from '../models/todo.js';

class TodoService {
    #todos = [];
    #storageKey = 'advanced-todos';
    
    constructor() {
        this.loadTodos();
    }
    
    async createTodo(text, options = {}) {
        try {
            const todo = new Todo(text, options.category, options.priority);
            
            if (options.dueDate) {
                todo.dueDate = options.dueDate;
            }
            
            if (options.tags) {
                todo.tags = [...options.tags];
            }
            
            this.#todos.push(todo);
            await this.saveTodos();
            
            return { success: true, todo };
        } catch (error) {
            return { success: false, error: error.message };
        }
    }
    
    async updateTodo(id, updates) {
        try {
            const todo = this.#todos.find(t => t.id === id);
            if (!todo) {
                throw new Error('Todo not found');
            }
            
            todo.update(updates);
            await this.saveTodos();
            
            return { success: true, todo };
        } catch (error) {
            return { success: false, error: error.message };
        }
    }
    
    async deleteTodo(id) {
        try {
            const index = this.#todos.findIndex(t => t.id === id);
            if (index === -1) {
                throw new Error('Todo not found');
            }
            
            const deletedTodo = this.#todos.splice(index, 1)[0];
            await this.saveTodos();
            
            return { success: true, todo: deletedTodo };
        } catch (error) {
            return { success: false, error: error.message };
        }
    }
    
    async toggleTodo(id) {
        try {
            const todo = this.#todos.find(t => t.id === id);
            if (!todo) {
                throw new Error('Todo not found');
            }
            
            todo.toggle();
            await this.saveTodos();
            
            return { success: true, todo };
        } catch (error) {
            return { success: false, error: error.message };
        }
    }
    
    getTodos(filters = {}) {
        let filtered = [...this.#todos];
        
        // Filter by completion status
        if (filters.completed !== undefined) {
            filtered = filtered.filter(todo => todo.completed === filters.completed);
        }
        
        // Filter by category
        if (filters.category) {
            filtered = filtered.filter(todo => todo.category === filters.category);
        }
        
        // Filter by priority
        if (filters.priority) {
            filtered = filtered.filter(todo => todo.priority === filters.priority);
        }
        
        // Filter by tags
        if (filters.tags?.length) {
            filtered = filtered.filter(todo => 
                filters.tags.some(tag => todo.tags.includes(tag))
            );
        }
        
        // Filter by search text
        if (filters.search) {
            const searchLower = filters.search.toLowerCase();
            filtered = filtered.filter(todo => 
                todo.text.toLowerCase().includes(searchLower) ||
                todo.tags.some(tag => tag.toLowerCase().includes(searchLower))
            );
        }
        
        // Filter overdue
        if (filters.overdue) {
            filtered = filtered.filter(todo => todo.isOverdue());
        }
        
        // Sort
        const sortBy = filters.sortBy || 'createdAt';
        const sortOrder = filters.sortOrder || 'desc';
        
        filtered.sort((a, b) => {
            let aVal = a[sortBy];
            let bVal = b[sortBy];
            
            if (sortBy.includes('Date')) {
                aVal = new Date(aVal);
                bVal = new Date(bVal);
            }
            
            if (sortOrder === 'asc') {
                return aVal > bVal ? 1 : -1;
            } else {
                return aVal < bVal ? 1 : -1;
            }
        });
        
        return filtered;
    }
    
    getStats() {
        const total = this.#todos.length;
        const completed = this.#todos.filter(t => t.completed).length;
        const pending = total - completed;
        const overdue = this.#todos.filter(t => t.isOverdue()).length;
        
        const byCategory = this.#todos.reduce((acc, todo) => {
            acc[todo.category] = (acc[todo.category] || 0) + 1;
            return acc;
        }, {});
        
        const byPriority = this.#todos.reduce((acc, todo) => {
            acc[todo.priority] = (acc[todo.priority] || 0) + 1;
            return acc;
        }, {});
        
        const allTags = [...new Set(this.#todos.flatMap(t => t.tags))];
        
        return {
            total,
            completed,
            pending,
            overdue,
            byCategory,
            byPriority,
            allTags
        };
    }
    
    async bulkUpdate(ids, updates) {
        try {
            const results = await Promise.all(
                ids.map(id => this.updateTodo(id, updates))
            );
            
            const successful = results.filter(r => r.success);
            const failed = results.filter(r => !r.success);
            
            return {
                success: failed.length === 0,
                updated: successful.length,
                failed: failed.length,
                errors: failed.map(f => f.error)
            };
        } catch (error) {
            return { success: false, error: error.message };
        }
    }
    
    async exportTodos() {
        try {
            const data = {
                todos: this.#todos.map(todo => todo.toJSON()),
                exportDate: new Date().toISOString(),
                version: '1.0'
            };
            
            return { success: true, data };
        } catch (error) {
            return { success: false, error: error.message };
        }
    }
    
    async importTodos(data) {
        try {
            if (!data.todos || !Array.isArray(data.todos)) {
                throw new Error('Invalid import data format');
            }
            
            const importedTodos = data.todos.map(todoData => Todo.fromJSON(todoData));
            
            // Merge with existing todos (avoid duplicates by ID)
            const existingIds = new Set(this.#todos.map(t => t.id));
            const newTodos = importedTodos.filter(t => !existingIds.has(t.id));
            
            this.#todos.push(...newTodos);
            await this.saveTodos();
            
            return { 
                success: true, 
                imported: newTodos.length,
                skipped: importedTodos.length - newTodos.length
            };
        } catch (error) {
            return { success: false, error: error.message };
        }
    }
    
    async saveTodos() {
        try {
            const data = this.#todos.map(todo => todo.toJSON());
            localStorage.setItem(this.#storageKey, JSON.stringify(data));
        } catch (error) {
            console.error('Failed to save todos:', error);
            throw new Error('Failed to save todos to storage');
        }
    }
    
    loadTodos() {
        try {
            const data = localStorage.getItem(this.#storageKey);
            if (data) {
                const todoData = JSON.parse(data);
                this.#todos = todoData.map(data => Todo.fromJSON(data));
            }
        } catch (error) {
            console.error('Failed to load todos:', error);
            this.#todos = [];
        }
    }
}

export default new TodoService();
```

**Project 2: Real-time Data Dashboard**
```javascript
// services/dataService.js
class DataService {
    #apiBase = 'https://jsonplaceholder.typicode.com';
    #cache = new Map();
    #cacheTimeout = 5 * 60 * 1000; // 5 minutes
    
    async fetchWithCache(url, options = {}) {
        const cacheKey = `${url}_${JSON.stringify(options)}`;
        const cached = this.#cache.get(cacheKey);
        
        if (cached && Date.now() - cached.timestamp < this.#cacheTimeout) {
            return cached.data;
        }
        
        try {
            const response = await fetch(url, {
                ...options,
                headers: {
                    'Content-Type': 'application/json',
                    ...options.headers
                }
            });
            
            if (!response.ok) {
                throw new Error(`HTTP ${response.status}: ${response.statusText}`);
            }
            
            const data = await response.json();
            
            // Cache the result
            this.#cache.set(cacheKey, {
                data,
                timestamp: Date.now()
            });
            
            return data;
        } catch (error) {
            console.error('Fetch error:', error);
            throw error;
        }
    }
    
    async getUsers() {
        return this.fetchWithCache(`${this.#apiBase}/users`);
    }
    
    async getPosts() {
        return this.fetchWithCache(`${this.#apiBase}/posts`);
    }
    
    async getComments() {
        return this.fetchWithCache(`${this.#apiBase}/comments`);
    }
    
    async getUserPosts(userId) {
        return this.fetchWithCache(`${this.#apiBase}/users/${userId}/posts`);
    }
    
    async getPostComments(postId) {
        return this.fetchWithCache(`${this.#apiBase}/posts/${postId}/comments`);
    }
    
    // Simulate real-time data updates
    startRealTimeUpdates(callback, interval = 30000) {
        const updateData = async () => {
            try {
                const [users, posts, comments] = await Promise.all([
                    this.getUsers(),
                    this.getPosts(),
                    this.getComments()
                ]);
                
                const stats = this.calculateStats(users, posts, comments);
                callback({ success: true, data: stats });
            } catch (error) {
                callback({ success: false, error: error.message });
            }
        };
        
        // Initial update
        updateData();
        
        // Set up interval
        const intervalId = setInterval(updateData, interval);
        
        // Return cleanup function
        return () => clearInterval(intervalId);
    }
    
    calculateStats(users, posts, comments) {
        const userStats = users.map(user => {
            const userPosts = posts.filter(post => post.userId === user.id);
            const userComments = comments.filter(comment => 
                userPosts.some(post => post.id === comment.postId)
            );
            
            return {
                ...user,
                postsCount: userPosts.length,
                commentsReceived: userComments.length,
                avgCommentsPerPost: userPosts.length > 0 ? 
                    (userComments.length / userPosts.length).toFixed(2) : 0
            };
        });
        
        const topUsers = userStats
            .sort((a, b) => b.postsCount - a.postsCount)
            .slice(0, 5);
        
        const totalStats = {
            totalUsers: users.length,
            totalPosts: posts.length,
            totalComments: comments.length,
            avgPostsPerUser: (posts.length / users.length).toFixed(2),
            avgCommentsPerPost: (comments.length / posts.length).toFixed(2)
        };
        
        return {
            userStats,
            topUsers,
            totalStats,
            lastUpdated: new Date().toISOString()
        };
    }
    
    clearCache() {
        this.#cache.clear();
    }
}

export default new DataService();
```

```javascript
// components/dashboard.js
import dataService from '../services/dataService.js';

export class Dashboard {
    #container;
    #updateInterval;
    #isLoading = false;
    
    constructor(containerId) {
        this.#container = document.getElementById(containerId);
        if (!this.#container) {
            throw new Error(`Container with id '${containerId}' not found`);
        }
        
        this.init();
    }
    
    init() {
        this.render();
        this.startRealTimeUpdates();
        this.setupEventListeners();
    }
    
    render() {
        this.#container.innerHTML = `
            <div class="dashboard">
                <header class="dashboard-header">
                    <h1>Real-time Data Dashboard</h1>
                    <div class="dashboard-controls">
                        <button id="refreshBtn" class="btn btn-primary">Refresh</button>
                        <button id="exportBtn" class="btn btn-secondary">Export</button>
                        <span id="lastUpdated" class="last-updated"></span>
                    </div>
                </header>
                
                <div id="loadingIndicator" class="loading hidden">
                    <div class="spinner"></div>
                    <span>Loading data...</span>
                </div>
                
                <div class="dashboard-grid">
                    <div class="stats-overview">
                        <h2>Overview</h2>
                        <div id="totalStats" class="stats-cards"></div>
                    </div>
                    
                    <div class="top-users">
                        <h2>Top Contributors</h2>
                        <div id="topUsersList" class="users-list"></div>
                    </div>
                    
                    <div class="user-details">
                        <h2>User Details</h2>
                        <div id="userTable" class="data-table"></div>
                    </div>
                </div>
            </div>
        `;
    }
    
    setupEventListeners() {
        const refreshBtn = this.#container.querySelector('#refreshBtn');
        const exportBtn = this.#container.querySelector('#exportBtn');
        
        refreshBtn?.addEventListener('click', () => this.forceRefresh());
        exportBtn?.addEventListener('click', () => this.exportData());
    }
    
    startRealTimeUpdates() {
        this.showLoading(true);
        
        this.#updateInterval = dataService.startRealTimeUpdates(
            (result) => this.handleDataUpdate(result),
            30000 // Update every 30 seconds
        );
    }
    
    handleDataUpdate(result) {
        this.showLoading(false);
        
        if (result.success) {
            this.updateUI(result.data);
        } else {
            this.showError(result.error);
        }
    }
    
    updateUI(data) {
        this.updateTotalStats(data.totalStats);
        this.updateTopUsers(data.topUsers);
        this.updateUserTable(data.userStats);
        this.updateLastUpdated(data.lastUpdated);
    }
    
    updateTotalStats(stats) {
        const container = this.#container.querySelector('#totalStats');
        if (!container) return;
        
        container.innerHTML = `
            <div class="stat-card">
                <h3>Total Users</h3>
                <span class="stat-value">${stats.totalUsers}</span>
            </div>
            <div class="stat-card">
                <h3>Total Posts</h3>
                <span class="stat-value">${stats.totalPosts}</span>
            </div>
            <div class="stat-card">
                <h3>Total Comments</h3>
                <span class="stat-value">${stats.totalComments}</span>
            </div>
            <div class="stat-card">
                <h3>Avg Posts/User</h3>
                <span class="stat-value">${stats.avgPostsPerUser}</span>
            </div>
        `;
    }
    
    updateTopUsers(topUsers) {
        const container = this.#container.querySelector('#topUsersList');
        if (!container) return;
        
        container.innerHTML = topUsers.map((user, index) => `
            <div class="user-card">
                <div class="user-rank">#${index + 1}</div>
                <div class="user-info">
                    <h4>${user.name}</h4>
                    <p>${user.email}</p>
                </div>
                <div class="user-stats">
                    <span class="posts-count">${user.postsCount} posts</span>
                    <span class="comments-count">${user.commentsReceived} comments</span>
                </div>
            </div>
        `).join('');
    }
    
    updateUserTable(userStats) {
        const container = this.#container.querySelector('#userTable');
        if (!container) return;
        
        const tableHTML = `
            <table>
                <thead>
                    <tr>
                        <th>Name</th>
                        <th>Email</th>
                        <th>Posts</th>
                        <th>Comments Received</th>
                        <th>Avg Comments/Post</th>
                    </tr>
                </thead>
                <tbody>
                    ${userStats.map(user => `
                        <tr>
                            <td>${user.name}</td>
                            <td>${user.email}</td>
                            <td>${user.postsCount}</td>
                            <td>${user.commentsReceived}</td>
                            <td>${user.avgCommentsPerPost}</td>
                        </tr>
                    `).join('')}
                </tbody>
            </table>
        `;
        
        container.innerHTML = tableHTML;
    }
    
    updateLastUpdated(timestamp) {
        const element = this.#container.querySelector('#lastUpdated');
        if (element) {
            const date = new Date(timestamp);
            element.textContent = `Last updated: ${date.toLocaleTimeString()}`;
        }
    }
    
    showLoading(show) {
        const indicator = this.#container.querySelector('#loadingIndicator');
        if (indicator) {
            indicator.classList.toggle('hidden', !show);
        }
        this.#isLoading = show;
    }
    
    showError(message) {
        // Create or update error message
        let errorElement = this.#container.querySelector('.error-message');
        if (!errorElement) {
            errorElement = document.createElement('div');
            errorElement.className = 'error-message';
            this.#container.insertBefore(errorElement, this.#container.firstChild);
        }
        
        errorElement.innerHTML = `
            <div class="alert alert-error">
                <span>Error: ${message}</span>
                <button onclick="this.parentElement.remove()">×</button>
            </div>
        `;
        
        // Auto-hide after 5 seconds
        setTimeout(() => {
            errorElement.remove();
        }, 5000);
    }
    
    async forceRefresh() {
        if (this.#isLoading) return;
        
        dataService.clearCache();
        this.showLoading(true);
        
        try {
            const [users, posts, comments] = await Promise.all([
                dataService.getUsers(),
                dataService.getPosts(),
                dataService.getComments()
            ]);
            
            const stats = dataService.calculateStats(users, posts, comments);
            this.updateUI(stats);
        } catch (error) {
            this.showError(error.message);
        } finally {
            this.showLoading(false);
        }
    }
    
    async exportData() {
        try {
            const [users, posts, comments] = await Promise.all([
                dataService.getUsers(),
                dataService.getPosts(),
                dataService.getComments()
            ]);
            
            const exportData = {
                users,
                posts,
                comments,
                stats: dataService.calculateStats(users, posts, comments),
                exportDate: new Date().toISOString()
            };
            
            const blob = new Blob([JSON.stringify(exportData, null, 2)], {
                type: 'application/json'
            });
            
            const url = URL.createObjectURL(blob);
            const a = document.createElement('a');
            a.href = url;
            a.download = `dashboard-data-${new Date().toISOString().split('T')[0]}.json`;
            document.body.appendChild(a);
            a.click();
            document.body.removeChild(a);
            URL.revokeObjectURL(url);
            
        } catch (error) {
            this.showError('Failed to export data: ' + error.message);
        }
    }
    
    destroy() {
        if (this.#updateInterval) {
            this.#updateInterval();
        }
    }
}
```

### Advanced Concepts Integration

**Combining Multiple Concepts:**
```javascript
// Advanced utility class combining closures, async/await, and modern features
class AdvancedUtilities {
    // Private fields
    #cache = new Map();
    #observers = new Set();
    
    // Static method for creating singleton instances
    static #instances = new Map();
    
    static getInstance(key = 'default') {
        if (!this.#instances.has(key)) {
            this.#instances.set(key, new AdvancedUtilities());
        }
        return this.#instances.get(key);
    }
    
    // Closure-based rate limiter
    createRateLimiter(maxCalls, timeWindow) {
        const calls = [];
        
        return function(fn) {
            return async function(...args) {
                const now = Date.now();
                
                // Remove old calls outside time window
                while (calls.length > 0 && calls[0] <= now - timeWindow) {
                    calls.shift();
                }
                
                if (calls.length >= maxCalls) {
                    throw new Error('Rate limit exceeded');
                }
                
                calls.push(now);
                return await fn.apply(this, args);
            };
        };
    }
    
    // Advanced memoization with TTL
    memoize(fn, ttl = 60000) {
        const cache = new Map();
        
        return async function(...args) {
            const key = JSON.stringify(args);
            const cached = cache.get(key);
            
            if (cached && Date.now() - cached.timestamp < ttl) {
                return cached.value;
            }
            
            const result = await fn.apply(this, args);
            cache.set(key, {
                value: result,
                timestamp: Date.now()
            });
            
            return result;
        };
    }
    
    // Observer pattern implementation
    subscribe(event, callback) {
        if (!this.#observers.has(event)) {
            this.#observers.set(event, new Set());
        }
        
        this.#observers.get(event).add(callback);
        
        // Return unsubscribe function
        return () => {
            this.#observers.get(event)?.delete(callback);
        };
    }
    
    emit(event, data) {
        const callbacks = this.#observers.get(event);
        if (callbacks) {
            callbacks.forEach(callback => {
                try {
                    callback(data);
                } catch (error) {
                    console.error('Observer callback error:', error);
                }
            });
        }
    }
    
    // Async retry with exponential backoff
    async retry(fn, maxAttempts = 3, baseDelay = 1000) {
        let lastError;
        
        for (let attempt = 1; attempt <= maxAttempts; attempt++) {
            try {
                return await fn();
            } catch (error) {
                lastError = error;
                
                if (attempt === maxAttempts) {
                    break;
                }
                
                const delay = baseDelay * Math.pow(2, attempt - 1);
                await new Promise(resolve => setTimeout(resolve, delay));
            }
        }
        
        throw lastError;
    }
    
    // Batch processing with concurrency control
    async processBatch(items, processor, concurrency = 3) {
        const results = [];
        const errors = [];
        
        for (let i = 0; i < items.length; i += concurrency) {
            const batch = items.slice(i, i + concurrency);
            
      ## batch.map(async (item, index) =
                const
                batcconst result hPawait processrod Aem, i +dvadex)nced e
             success: truesult, index: i  };
            } ca{
                 return { successe, errindex: i + ind
         ### Week 3 SumPrThis week we exploanced JavaScepts that areial for moment:
          
**D: Ad     
          vanonst batchcedults = await Functse.all(batchProione**
           
-           batcFunction derEach(resuclans {
    vs exp      if (result.resehavio{
        r          resulult.index] = lt.result;
    } else {
            errors.ex: result.i: result.err });
           }
        });
  
        
      rn { results, er
    }
}

// Usa- Closmple
cures ansis = AdvancedUtilities.grow stance();

// Rafunctctica API calll applicationionshain and hoistingr-order functions andE patterns
ateLimitils.createRateLim000)(f

// Memoized eve operati
- Bet memoizedCast praion = utils.mectices fync (n) => {
    //or DODate expensay erationstion
    await neromise(r=> setTimeout(r 1000));
urn n * n;
}, 30000)

**D16:nt system
con Asyncjbscribe = utilecsubscribe('dataUpdated',td meth => {
    consolod overData updated:ri-Orta);
});

utiiented ProhtaUpdated', { ronoSci** Date.now() });
- P

### 🎯 Kerivatorldtion Points
 Oscrsures provide private ipte and factory f
//Async/aw modeOP eClies promise-baso.js
explasses organize relored functionalityt ce Projec St
    conststeparate orage** cate enable reusabilitygory = 'geral', iority = 'me') {
        tsyntax featurehiscryove code readabipto.randomUUID(
`` th manipulaison creates .tteractive experienceext = text

### 💡 Week 3 Advanhis.categoiew Questionry = telish)

**Q1: goryure ka practica;atao aur example do.**
        this.prioritAt = new Date();
 y;:**
Closure    thte variables ais.tags = [functions];ane ke liye use hi:
```pt
function create
   t count = 0; //  variable
    retu {
     ment: () => ++cou
 }  decrement: t,
      () => count
  
    toggle() {

const counter     }nter();
counteent(); // private hai, dis nahi kar sae
```

**Q2sync/await mein error hling kaise karte hainiple operations ke liy

**A:**
```javasc    es(tag)) {ate();
  function processMOperations() {
  {
      // Sequential
const user = hUser();
const profile wait fetchProfile(user
        
        // P  updatedAt = new Da
        const [p    , friends]     ret Promise.all([
      turn  fetchPosts(user.id),thi  rem     return {
           returhFriends(user.idn
        ]);
    thi      s;
  D     return ate();ile, piends };
    } cat
        consoOperation fail:', error);
row error;
    }
   {
    }

**Q3: Module   tem mein circulcy kaise handte hain?
     his.N() {oISOString(),
**A:**
Cir   ar depende      .tags,karne ke ways:
- Ste: thiities ss.deparate moduueDaten rakho
- Dependency injection e karo
- Evedriven architure use 
  `javascript
// In  }d of A imporg B and B importing
    e shared mod both A and B i
```

### k Preview
atedAt),
   over at:edAnew Date(da),
    s: data.t,
         iqu   dueDate:ta.dueDate
    men });on
-todo; patterns anIs
- Testbugging strategies
    }
}anced concepts fromrm the foundatio these professiona topics!

 Advance
        ret and gesarba
-``jek 4: Advancedrvices/toavnd Design Paervins {#week-4}

##ce.sc22: Design Patter MevaScript

###sign Patterns
- Port { Todo } froerf../models/todo.or ;
odDefini      t Design pattehis.loa reusable solutdFro to commonly occurrSeg problemrviage()tware design. They;present best nd proven solutions.
    }
**Real-World Analo ce {os = [];
  i
Design Patterns.s Architectural BlObseubss
- House Bc pattern  Pattern tfor ate
-statrerent hibeesifferent implementati
    se blueprint, ubfferent materialsscribe(c
  Proven struc   e that wor    this.subscricl  coush(callback);nstructor(   optimizatio   
-``

### Si e     retutern

**Purpose:rn (nsure a class ha) =>    th instance ais.sign pe global access to itattebserver, Factory, Sin= callback)
We      };        this.escribers = this.subter(sub
    plementation:*
    nvascript
clasoti  s) {eConnection {
s.forEach(cainstancllback allback(this.t
    #isCon     pri false;
    
   or}ity);tor() 
  this  if (DatabaseConne.th(todinstance) {
  o)        return Dat;ction.#innce;
        }
     
        Da  thseConnectiis.    retur = this;
 n todo;ohis.#connect( a
    }
   dd todo: ${erre}`);
   onnect() {
    }   // Simabase connection
onso'Connectto database...')
        this.#isConne      await this    ge();
    }
          return     ;
    }uery(sql) {
        i(!this.#isConnecte
            throw new   'Database no);
        }
  e.log(`Executing${sql}`);
       rn `Result for: 
    }
    
    static g tnotify()() {
       ;odo(idatabaseConnecti) {nce) {
       Databason.#instance = new baseConion();
    
        return Datab   Connection.#instance;
      
        return todo    his.ntoify(););

// Usage
        t = new DatabaseChis.notif();
const d DatabaseC;
const db3 = DaeConnection.ge);

consb1 === db2); /same instance
le.log(db2 === db3true - same in
 ``

**Modern Sin   } id);h Module:**
``
// da
lass DatabaseC {
    #ido => todsColso.ce;s.complete
        }
 omp    
        l#connectrs.category) {();eted
            filte{filtered.filter(todo =o.category === frs.category
        }
           t
    #connf (filters.prect()     constr          f= {}) d = filtered.fil{eted !== undefined) {
               tered = fl   red.filter(todoconsole..priority === filters.plogif y);
        }
(fi     
      ltif (filteteng to database..red;
            f    red = filter  .filter(todo =>  tho.tags.includes(i = [...tag));
        .os];ted = true;
        
        if (fil }rch) {
            conower = filters.setoLowerCase();
     ered = filted.filter(
                ry(sqlext.toLowerCa) {);cludes(wer) ||
             todo.tags. tag.toLowerCaseincludes(searchLow
            );
      re}
        
     t   sulort by priority t f date
        retorn filte: ${sql}((a, b) => {
      `;  const priorityOrder 3, medium: 2, low: 
           const prityDiff = prityOrder[b.priority] - prtyOrder[a.prior
         
      iorityDiff 0) return p;
            rew Date(b.createdAtnew Date(a.createdAt);
  });
    }
   
// Exp Stats() {
        const   tal = this.todo  if (instance
e       consxpormpleted = th!thefaulisilter(todo => to.#i  mpleted).length; nneaseCo';
d       const ove`` this.todos.r(todo => todo.isOv)).length;
     
     const byCegory = thidos.reduce((acc,do) => {
            actodo.category] = (actegory] |
            ret;
        }, {}
###     
        const byPFb.quey Pathis.todos.reduce((actern => {
   cc[todo.pri(acc[todo.priori| 0) + 1;
 return acc;
      }, {});
     
        ret
*           total,
 *Purpornn'S ompleted,
 Crea       pending:te ELj - completed,
        ects wECdue,
            comT *t snRate: totalpeci FROM h.round((uectreted / total) * exact  0,
           clasategory,
         ses.ion();ty
       
 F  }
    
    actocteditToStorage() {
        dry {
        :**onst data = this.ts.map(todo .toJSON());
    ocalStorage.setItem JSON.stringif
        } catch (er`b fromscriptname;
            co   .emairor('Failed tl = ole;dos:', e);
          new Erled to save data'
    }}
    }
    
   romStorage() 
} = rol try {e;
 emai       const data = lol;thisrage.getItem('todo.permi
            if (data) min extends 
clascons        const patructorJSON.parse(nata);
         me,s ' this.todos = par.il.map(todoData ) {do.fro(todoData
            }
     /datn othe,(error) {
   emai     console.error('Fal, 'ado load todosmir'delete'
       , 'm this.todos =fian
          }
    }
    
    as exportData() {
  nst data = {
      todos: this.tap(to=> todo.toJSON()),
       exportDaew Date().toISOStr
            version:    ma  geUsers() {      this.p{le;
        };
          }
} const blo= new Blob([JSONtringify(data, null{
          typetion/json'
       
mai     
    lr  const url = UR(na) {teObjectURL(blob);me, email, ditor');
        c       thircument.createElemissio=');
     ['ra.href = url;
 ead'   a.down, 'write'];os-${te().toISOSt('T')[0]}.jn`;
  ick();
    URL.revokeObjectU(url
    }
    
    async impoata(file) {
    return nomise((resolve, re
           reader = new FileRea();
        
        reader.o= (e) => {
      try 
    e               c   {ta = JSON.parse(e.esult
          eturn     
     'Editinconte   if (datant...';Array.isArodos)) {
              s.todos = d.map(todota => TodoN(todoDat
                is.saveToStora
}                this.notif;
                  esolve(thlength);
        } else {
                 reor('Invalid format'));
           }
          } catch 
           reject(new Erroo parse file')
 email)          {
            };
     a      
    me, e   reader.onermar = () => rejeil,new Error('Favieweto read file'));r');d'];
  }        readerext(file);
   
    }
}

ault new Toce();
```

```jpt
// compontodoApp.js
imp todoSer '../services/todos';
import bounce } fromutils/helpers.js';

ess TodoApp {
    con() {
}     this.curren{};
        this.init(

    
    init() {
          is.setupEventListe  'e();
       ditor'setupSubscrip, 'view;
     er'];render();
    }

    setupEvent {
        // d todo form
nst addForm = docut.querySelector('#oForm');
      addEventL('submit', thisdo.bind(this));
      
      Search inpuncing
        csearchInpuument.querySeleearchInput');
   (searnput) {
         const deearch = d(this.handleSearnd(this), 300);
        searchInput.addEsten('input', debouncedch);
       
        
   }lter buttons
   documentstener('click', (e){
          if (e.target.hes('[data-lter]')) {
     this.(e.target.dataset.f, e.targettaset.value
           
        
       arget.matches(on]')) {
       is.handlerget.dataset.rget.datid);
      
        });
     ); // Ma// Usagemple.com');naging us
conso   // Klonoard shst eFac
        dtor.edry.cdEventListener(ntent())', this.handleKeyb; /rebind(thisaser('e content...
        
      condiExport/Importor'', 'prwer.permissiiya@ex  // ['read']
```    cxportBtn = docuuerySelector('#eBtn');
 portBtn?.adListener('click', ()Service());
   
        cortInput = documelector('#importInput'
       importInpuistener('c.handleImpornd(this)

    
  criptions() {
      ce.subscrib => {
         .render
**Imple });
    }
 mentatam#:**
```j Oync handleAddTodbseripttter {
        e.preve     this();
        .# #evenevents.set(eMap();[]);
        const formData = new }mData(e.targe
          ent(event) formDa.puset('text')?.trh(cal
        conlback= formData.geory') || 'genera
         priority = formpriority') || 'medium
        
        if (!t       
            this.show / Retur'Please enter n unsu text', 'error'bsc.off(event,ribe    th;
            ret}in;
        s.
        
               retur#events.)) {turn;
            await  co  nsvice.addTodo(text, cat c     priority); s = this.#events.get(ev
            e. const index();
   = dexOf(cthis.showMessage('Tallbacd successfully!'succes
        } c  ch (error) {
              ca.showMessage(error.ndllbac, 'errkex >
        }
     -1e(index, 1);
       ) {
    handleSearch(e      
   t    this.currentFhis.#ev arch = e.t       (ene;
        tts.deletcall;
    }
    
backs0) {ilter(filterType, va
      === 'all') {
        delete urrentFilter[f
        } e{
            this.cuer[filterType] = value= 'true' ? true : == 'false' ? false ;
        }
    s.render()
            }pdateFilterU
    }

    asynndleAction(acti id) {
        
            switch) {
            case 'le':
          aService.togTodo(id);
               break;
          case 'del
            })) ret if (confirm('urn;u sure you want to deleteodo?')) {
                await toService.odo(id);
                   thisssage('Tted', 'succe
              ;
                    break;
         }      case 'edi tch (error) {        callback(data);        
                       s.startEdit(i      console   callba.server calforEach(cal:', error);l
                    break;
               });       t   const callbacs.h= this.#events.get(as(e
nt, } } catch or) {
      this.showMessagor.message,or');
   }
    }

    handleKeybe) {
  // Ctrl/ + N: New todo
   if ((ctrlKey ||y) && e.key ) {
            e.prult();
 document.querySelector(oText')?.focus()
        }
       {
    su  // Escape: Clebscribeers
       = thisvkey === 'Escape') ent, (d
            this. cak(data);er = {};
         em.price, nder();
      0)his.updateFilte
        }
              unsubscribe()his.getState(sum, item) =>
    
    async handlet(e) {
        constrget.files[0];
  (!file) return
        
    getStat  
            const cou  l()await todoServic {tmportData(file);otal = this.#items.
            this.sh    ssag rettported ${count}emsur: successful[.!`, 'success'..
        } catthn {#ror) {
items       th.lemhowMessags],message,rror');
    }
    
        e.target.valu   };Reset file input

    
    stit(id) {
   st todo =rvice.findid);
        if odo) return
        
       }odoElement = documuerySelector("${id}"];
        constement = todoquerySelectorxt');
     
        input = documentnt('input');
}put.ty= 'text
        input.value = todo. l s
        input.className class CartDit';
  splay { itemCount: : this.#total,
        const saveEd   = async () => {
co          constnstrText = input.value.ts.m();
     cart = ca (newText &urnewText t;= todo.text) {
 rs()           t;
                    awai    }ce.updateTodo(id{ text: newText });
cto             } catch (error)r    this.setup    ) {
     e              ttupLisowMessage(error.teners() { rror');    
                 this.upd hisisplay(state).cart.odated', (state) =>
            }      });
     #c     this.renderal   }y: ${state.emCount} items, Total: ₹al}`);
    }  };

  .addEventListener('bEdit);
      input.addEvekeydown', (e)
}          if (e.ke 'Enter') saEdit();
        f (e.key === 'Esrender();
        }
        
    textElement.With(input);
 .focus();
       .select();
    }
    
artNotider() {
        thficatioerTodos();
 ns {s.renderStats()
 truc   this.updatetor(cUI();
    }
  
      nderTodos()   thi o     Listeners();
        const t this.ctodoService.gart = s(this.currentFiltcansole.log(`Ca
        const container =  e} addt.querySelector('#ed tort`);
        
       !containern;
        
  odos.l) {
   ontainer.iTML = `
             <div clempty-state">
        <p>No t found<
                 });{Object.keys(Filter).leh > 0 ? 
              '<buck="this.clea)">Clear Filters 
                  p>Add your first o above!</p>'
              }
         div>
    
            retu
   o    }
     g(`Noti
        c   }r.innerHTML = tod> `
       iv class="ttodo.completed ? 'compted' : ''} ${tue() ? 'ove: ''}" 
         data-id="${todid}">
    <div class=tent">
            <button class=tn" data-actio"toggle" da${todo.id}">
              ${todo.completed ? '✓'
                 /button>
        <div clasdo-text">${thieHtml(todo.)}</div>
            <div class=-meta">
              <span class="">${todo.category
                <span cl"priority priority-${tority}"iority>
                ${todo.tag => `<"tagpan>`).join('')
}               todo.dueDate ? `<an class="due-datenew DatDate).toLocaleDatepan>` : ''}
              </div>
       </div>
      <div clo-actions">
                 <button datadit" data-id="${todotle="Edit">✏️</button
             on data-actionte" data-id=d}"lete">🗑️<ton>
           /div>
     /div>
   .join('');
    }
   
    renderStclass f
       icanst stats = ttnalytics {ietStats();
    {i  const containerte document.qm.naSelector('#statsme;
        
        } r fromtainer) return;
    c   
        containar.innerHTML = `t`);
             div class=" ruts-grid">
      ct        <div claor(crt;t-card">
        <div class=er">${st.total
                    class="stat-labe>Total</di
                    this.setListeners(
             }div class="stat-c
                  <div class=r">${stats.compled}</div>
              s="stat-label"ed</div>
            </div>
    <div class="stat-
               v class="st${stats.pending}</div
                    setup  ass="sta   this">Pending</div>
 .) {', (       </{ item, car=> {
                <div class      -card">
    itemNam         <d   itass="stat-em.ner">${stats.compamtionRate}%</de,
                      iv class="stat-la    >Completion Rate</d  artTo        ittotal
               em/div>
             }  ${stats.);0 ? `
                  <div class="verdue"
                e       <div class="nt, dalytic">${stats.ovs:due}</div>
         ${eata) {ve    <div class="stat-nt}el">Overdue`,tav>
  );      </div>
      ` : ''}
   </div>
        
    }
    
lterUI() {
     te active filter but
        documen    }ectorAll('[datlter]').forEa(btn => {
        ilterTybtn.dataset.filter;
}    const ue = btnalue;
            
  if (this.er[filterTy=== filtelue || 
      ilterValue ===l' && !this.currentlter[filte])) {
           ssList.add('active')
           onstlse {
          cart =btn.classList.r nert();ive');
          }
        });
c       
     onst nopdate search tificatst diCarew CartNotifications(ctDisplay(c
co      consnstearchInput = d ana// UwuerySelector('#se CartAnals(;
        ifcartarchInput &);rentFilter.se searchInput.value{
            searchI = this.currentFilterch || '';
        }
  
 'La
    cleaptop',00 });
        this.currentFiuse', pric
        this.rene: 100
Itr }
    
    st.rMessage(message, typeemoveItem(e{
     m(ontainer.querySelect('#messages');
```  if (!containe
attern      co${type.toase()}: ${message}`
          r
*       }
  *P    urpose:** Encapsed functionalirovide plic/prace.
Pvascripconst messageEl = dtent.createElement('
        meconstEl.className = CalcuattorMssage-${td fu`;
        menctionsodextContent = ule =ge;
         (f
        container.a  let uern:messageEl);** {
        
       lsetTimeouet histoo
            mw new Er.remove(yrror('Inva um)) {ber');
        }, 30   ;
    }
    
      }apeHtml(text)
        const     cumentateElement
        div.textCont    = te return {
        (num)  div.in    res;
    }
}
ul`

```javascriptng
        /helpers.js
exp num;onst debounce = (func, dT', num);{
    let t
    return function (.{
        clea(timeoutId);
    timeou= setTimeout> func.apply(this, aay);
    };
};

st throttle = (, limit) => {
Throttle;
  n function (.
             inThrottle) {  this;
    func.aly(this, args);
            inThr   m  = true;
            setTimeout(validateNurottle = falsmbeultip);
        }
    };
        ly(num)ult *= num;
  {      log('s;
    rt const form    },ate, options = {}) => 
  MUn new Intl.Damat('en-US', {
        meric',
        mshort',
        d 'numeric',
      tions
    }).format(n Date(date));
}

export const        eId = () => {
  divide(n Date.now().toStri    6) + Math{.toString(36)
};

exporeepClone = (obj)> {
    if (obj =ull || typeof objject') return obj;
    if (obj       ceof Date) return new    i(obj);
 f (num obj instanceof Arr=== 0 turn obj.map(item =   reumlone(item));
    ifberypeof obj === 'obj(nt') {
        const cloum);
        Object.keys(ob           key => {
         thr Eoned[key] =rror(Clone(obj[k'Div;
        })ision byo');
        return clon      }
    }
};
           DE', n   num;um);
      n this;
    avascript
//   in.js
import { TodoApp },m './conents/todp.js';

doent.addEventListener(ontentLoed', () => {
doApp();
});
`

### Advance   cepts Integr

**Projec     Real-time Chat   lt() {ion Simulation*
 ``javascript
/        ed async psult; with WebSocket s
class ChatApp {        },
      etuructor() {
   rn t reis.messages = []set(his;
        ohis.users = nry() {y]; // Return cop
        this.       } = new Event;
        nectionStat'disconnected';
     this.recons = 0;
       onnectpts = 5;
    }

    async conneername) {
       
            this.tionStatus = 'c;
            this.eminge', { status: ng' });
   
            //nnection delay
    }       awai;elay(10
}           
 )()    ;Simulate random conlure
   if (Math.random()  {
        row new Error('Cfailed');
           }
     
            th// UsagectionStatus = e  urn [...;
          this.reconnepts = 0;
     emit('statusChange'{ status: 'connected'
                 emit('u orModued', { username, timlemp: new Date()
            
        .mubtract(rt receiving me5)
            .startMessageR
          
    .   } catcdiviltiply(
            t2)   g  ectionS  ) ul= 'disconnectt ';
  = 0;his.emiange', {  'disconnecter: error.m
            
    / Auto-reconn exponential ba
;           if (this.rec// 5getHtempts < this.istory(nnectAttempts) {
`              `` Est delay = Math.powS6:**reconnectAtte * 1000;
```javastsu     setTimeoulat0;
                    eratireconnectAvalupts++;
    }             t(username);
            }, delay);
        }
      
 
    
    async ssage(text, type =) {
     is.connectitus !== 'connted') {
        throw new Errorconnected to chat');
}
        
   st messag
        #valida crypto.randoer(num) 
            {er');
            type     }
            times  }w Date(),
          sender: this.cuser,
            status: 'sending'
        };
        
        this.messages.push(message);
        this.emit('messageAdded', { message });
        
        try {
            // Simulate network delay
            await this.delay(Math.random() * 1000);
            
            // Simulate message failure
            if (Math.random() < 0.1) {
                throw new Error('Message failed to send');
            }
            
            message.status = 'sent';
            this.emit('messageUpdated', { message });
            
        } catch (error) {
            message.status = 'failed';
            this.emit('messageUpdated', { message });
            throw error;
        }
    }
    
    startMessageReceiver() {
        // Simulate receiving messages from other users
        const receiveMessage = async () => {
            if (this.connectionStatus !== 'connected') return;
            
            // Random delay between messages
            await this.delay(Math.random() * 5000 + 2000);
            
            const sampleMessages = [
                "Hello everyone!",
                "How's everyone doing?",
                "Great weather today!",
                "Anyone working on interesting projects?",
                "JavaScript is awesome! 🚀"
            ];
            
            const message = {
                id: crypto.randomUUID(),
                text: sampleMessages[Math.floor(Math.random() * sampleMessages.length)],
                type: 'text',
                timestamp: new Date(),
                sender: `User${Math.floor(Math.random() * 100)}`,
                status: 'received'
            };
            
            this.messages.push(message);
            this.emit('messageAdded', { message });
            
            // Continue receiving
            receiveMessage();
        };
        
        receiveMessage();
    }
    
    // Event emitter methods
    on(event, callback) {
        this.eventEmitter.addEventListener(event, callback);
    }
    
    off(event, callback) {
        this.eventEmitter.removeEventListener(event, callback);
    }
    
    emit(event, data) {
        this.eventEmitter.dispatchEvent(new CustomEvent(event, { detail: data }));
    }
    
    delay(ms) {
        return new Promise(resolve => setTimeout(resolve, ms));
    }
    
    // Message history with pagination
    async getMessageHistory(page = 1, limit = 20) {
        const start = (page - 1) * limit;
        const end = start + limit;
        
        // Simulate API delay
        await this.delay(500);
        
        return {
            messages: this.messages.slice(start, end),
            hasMore: end < this.messages.length,
            total: this.messages.length
        };
    }
    
    // Search messages
    searchMessages(query) {
        return this.messages.filter(message => 
            message.text.toLowerCase().includes(query.toLowerCase())
        );
    }
    
    // Get online users
    getOnlineUsers() {
        return Array.from(this.users.values()).filter(user => user.online);
    }
    
    disconnect() {
        this.connectionStatus = 'disconnected';
        this.emit('statusChange', { status: 'disconnected' });
        this.emit('userLeft', { username: this.currentUser, timestamp: new Date() });
    }
}
```

### Performance Optimization Patterns

```javascript
// Memoization for expensive calculations
const memoize = (fn) => {
    const cache = new Map();
    
    return function (...args) {
        const key = JSON.stringify(args);
        
        if (cache.has(key)) {
            return cache.get(key);
        }
        
        const result = fn.apply(this, args);
        cache.set(key, result);
        return result;
    };
};

// Example usage
const expensiveCalculation = memoize((n) => {
    console.log(`Calculating for ${n}`);
    let result = 0;
    for (let i = 0; i < n * 1000000; i++) {
        result += i;
    }
    return result;
});

// Lazy loading pattern
class LazyLoader {
    constructor() {
        this.cache = new Map();
    }
    
    async load(key, loader) {
        if (this.cache.has(key)) {
            return this.cache.get(key);
        }
        
        const promise = loader();
        this.cache.set(key, promise);
        
        try {
            const result = await promise;
            this.cache.set(key, result);
            return result;
        } catch (error) {
            this.cache.delete(key);
            throw error;
        }
    }
}

// Virtual scrolling for large lists
class VirtualList {
    constructor(container, itemHeight, renderItem) {
        this.container = container;
        this.itemHeight = itemHeight;
        this.renderItem = renderItem;
        this.items = [];
        this.visibleStart = 0;
        this.visibleEnd = 0;
        this.scrollTop = 0;
        
        this.setupScrollListener();
    }
    
    setItems(items) {
        this.items = items;
        this.updateVisibleRange();
        this.render();
    }
    
    setupScrollListener() {
        this.container.addEventListener('scroll', () => {
            this.scrollTop = this.container.scrollTop;
            this.updateVisibleRange();
            this.render();
        });
    }
    
    updateVisibleRange() {
        const containerHeight = this.container.clientHeight;
        const totalHeight = this.items.length * this.itemHeight;
        
        this.visibleStart = Math.floor(this.scrollTop / this.itemHeight);
        this.visibleEnd = Math.min(
            this.visibleStart + Math.ceil(containerHeight / this.itemHeight) + 1,
            this.items.length
        );
    }
    
    render() {
        const visibleItems = this.items.slice(this.visibleStart, this.visibleEnd);
        
        this.container.innerHTML = `
            <div style="height: ${this.visibleStart * this.itemHeight}px;"></div>
            ${visibleItems.map((item, index) => 
                this.renderItem(item, this.visibleStart + index)
            ).join('')}
            <div style="height: ${(this.items.length - this.visibleEnd) * this.itemHeight}px;"></div>
        `;
    }
}
```

### 💡 Week 3 Advanced Interview Questions (Hinglish)

**Q1: Closure ka practical use case batao aur memory leak kaise avoid karte hain?**

**A:**
Closure ka use private variables aur module pattern mein:
```javascript
function createCounter() {
    let count = 0; // Private variable
    
    return {
        increment: () => ++count,
        decrement: () => --count,
        getCount: () => count
    };
}

// Memory leak avoid karne ke liye references clear karo:
let counter = createCounter();
// Use counter...
counter = null; // Clear reference
```

**Q2: Event delegation kya hai aur performance benefits kya hain?**

**A:**
Event delegation parent element par ek listener lagana hai multiple children ke liye:
```javascript
// Inefficient - har button par listener
buttons.forEach(btn => btn.addEventListener('click', handler));

// Efficient - ek listener parent par
container.addEventListener('click', (e) => {
    if (e.target.matches('button')) {
        handler(e);
    }
});
```
Benefits: Kam memory usage, dynamic elements automatically handle hote hain.

**Q3: Promise chaining vs async/await mein performance difference hai?**

**A:**
Performance same hai, sirf syntax different hai:
```javascript
// Promise chaining
fetchUser()
    .then(user => fetchPosts(user.id))
    .then(posts => console.log(posts));

// Async/await (same performance, better readability)
async function getData() {
    const user = await fetchUser();
    const posts = await fetchPosts(user.id);
    console.log(posts);
}
```
Async/await debugging aur error handling mein better hai.

---
   ereturn this;
    }
 btract(num) {
     .#vahis.#rT', nuesult -= num);
       m;liurn this;
    dateum);
  this.#log('SU
    mult     this.dateNumber(num);#
        teturn this;his.#result rTIPLY', num);
e num
    
    divide(n;
        this.#validatumber(num);
        this.#log('DIVis.#re  m);
        return t t /
    
    get  }= nu) {
        returnm;esult;
    }
    reset() {
   is.#result = 0;
   this.#history = 
     i  return thisf (num ===  throw newvision by zero
    }
    
    get     ry()thi  'ADD', num);  aof(thm;
        return [...th    this.#i];
    }
}

```
v = cvv;
 .expiryDate = er.sliceexpiry(-
        re  succes: 'Credit Card'
     s: true,' + Dat
    }
    
       idate() {
             me  is.carturn {r && thisansactionIds.expiryDate;
  : 'C

class        ayment {
      (strucg PayPal ptor(em = email;swoaymenr
        returdo{
            succesf ₹$rue,
            method: ' {amount}`)actionId: 'PP_' +;ate.now()
 ;      };
   le.log(`Account: ${this.email}
    validate().ema     il && throcesssword;sin
    }
}

class       upiId) {
        t   t piId = {iId;
    ) {
        consoleProcessing D: ${this.upiId}`);
  of ₹${amourn { true,
           sacthod: 'UPI'
 ti     };
    onId: 'UPI_' + D
    
    val () {d && this.upiId.i;
    }
}

// Conlass
class rocessor {
    constructor() {   rn this.up
        this.paymentStr   null;
    }
 
    }
  processPymentStraayme  nt(ategm {
        ifthrow new Error('Npayment et');
     
        
     
}

// U !sult = processthis.payme.aymentv;

// PayPal pa = new Patrategy(pyPaal);
result lPalSeessor.processPaymnt('user);
console.log@exple.com',sult:', res 'pas
ent
const upiw UPIPymentStrategy(upresult);
aym

###  Pattern

**Implementation:*meterize cliendifferent requestsperations, and suppo
Purposascript
e:** Encver - the ate a rehat performs s ant,tual work
class TextE allowing you to p
    constructor() {result .log('Paengtymen= processor.ent('utm');nt;
        this.cu(500 = position;
    );h);deletedText;
  
    ontent;
    }
    getConte   his.conten.content.slice(0, poion) + this.content.ice(positi
c   setCursor(o      r) {ath.min(positiotent.length));

   etu  this.cursor = Marnn  ositi this.contenton, positio
    }
// Commandand {
    execute( in   ;siet be implemented');
  t be implemented');
    ndo() {new Error('Und
 

// Concre       ts);
    }
    
clasindo() {
 sertTesonss.edittructor(eText(te Irxtot.length, r,is.texition);
t,  }
}
 this.po text, po;mmand {
   ructor(editor, lenh, position) {
r();
        this.tor;
      this.length =ngth;sition;
        thdeletedText = '';
   
    execute(ext) {leteText(thihis.position);, thiion);
    }
}e commte();(command);
      this.curon++;
    }
   
       o() {
            return
        }lse;
 }
    
    ndo() {
      urn this.currenn >= 0;
    }
    canRedo() {his.higth - 1;
    }
console.log(editoent()); // "H
eleteTextCmand(edi
invoker.undtor;
console.,itor.getContent()o World!"
do();
e.log(editor.g()); // "Hello "

invdo(); // ""

/``objects without speciexact class
pattmmand encapsulaern pr makions for undo/redo es ctionality
algorioIntete hrvvryinsestionserHinglish)ain?**
n kyab use 
**Q1**
S: Singln pattern ek hrchnstance ensangekartaable
-vejavascript
classtatic insta ides null;
    c getInstance( {ew Datase();
        }this.instance;
     
}
```
Us   re.insDatabaseern ka real-world e ctanc do.**

**A:**
ctions, logg jaise DOMing,e s ya custom ev=:
```javascript
ctEmitter {
 on(event, callback) add liste */ }
    emit(evendata) { /* noall li */ }
}
 sakte hain
proceor.setPaymentStraCreditCard()
 / Usage:  as  on', name('ype create, emai kari hai?**tacide hota hai  
Us`

---e hai.createUse
```Factory - usejavi method change
// Strategy - pay
- Fry: Object creatir type decid
ategy: Runtimealgorithm chang
**A:**
- temAdded', upd  iUI);
```ory pattern se di
pattern
**Q3: f (!this.ie {
**Q2: Obse  encapsr enablesnd pri loostcope
- Sts in creatbetween objectsestass application

- Sieton ensures sing
### 🎯 Key/  operationslo "// "Hello Worl
.log(editor.getCo
covoker.redo();
nsole.log(ediinvokertent()); // "H
consoletor.getCon
e/ Undo opditor, 'xecuteCommanWor// Usagello Worl); // "Hello "ld!', d!"

consolor.getContent(
conoker.executeCost inenew InsertTextComditovoker.r = new Edoker(editor, 0));
console.
const edit   = new TextEdito     return this.c      tositiohis.currentPositi  --;
   Execute cuteCommand(new Insertcommandsand(editor, 'Hello
i     th(thisturn true;s.history[this.ntPosi
            mmand.execute(
            const com    istoe;tPosition++;
            this    }story.length - 1)
    () {rrentPosition < 
        if (
        retury[this..curis.hand >= 0) curre{sition];
           ommand.undo();
 const command =
 and.ex

- manageshis.history = this.h co an.slice(0, thid unrrentPosition + 1);
   dooredo functionality)
    e   // Execute andnt position
    executeCemove any commands aftomman}clommand) {
        //ass EditorInvok
    constructcurrentPosition = -or undo() {
        this.edit   = editor;
        this.editory = [];
  otText(t
            .dele   this.phis.editor.
    DeletCommand e
            execute()}
sitiotTextCommand exteComman
        sup  ;on = pos
        thisext = text
cla     this.editor = editsst  throw newionror('Execute method m = this) {ion);
        thi= positionength; this.content.
    }   const deletedition = this.curso
    deleteText(lengt 
     his.contes.content.slice(0, sition+ text + this.content.s
    insertText(text,     this.curso
processo
// UPsword');
const par.setPaymetrategy(creditCard)id');
prnsole.log('Pocesnt result:sor.setPatementProcessor();()) {
    t process    }ment
const trategy.pd = neay(amountardPayment('123)23456', '123', '1
// Credit ca        return t    setPa   throw new EymentS      d payment detacrategy = straostrategy) {nsol   }
        this.paymentcons  co
    pay(}
 amo    this.passwunt)} word) {
        this{
        //  ole.log(`  redit car{this.d payment
        console.log(`Proce #ing credit ## Straymentaes.#${amount}`);
   validatncardNumbe
ne a family of gorithms, encapsul one, and make theerchang
ion:**ate) s.ca{
       
    construor(cardNumber, cv
```javascri
**Ims CreditCardPayment pyment strateglement**Purpose:ult new CalcueNune ium); // Single) { instannstance
explator }; // Classreating 
       num !== 'number' || )) {alid n
          throw ne
og      this.#history.pu(operation, va
    #historyor {
    #r
clas
// calculato
ttern wi
ern Mo
consalculatorModul
console.log(Ca      orModule.getRes  histor, 0);y =;
      
            lo
          
           
        log('SU
            resul         }validateNumb,t(num) {
        
   tm;
            num);
     urn this; // Enable 
    //      validateN Publ  };
    
         t
        if (t perationp!== 'number' eration}, Result}`);
    }
    functiopern   /teNumber(n/ Privtioation}: ${n, value) {atebles 
    function v       ` onsole.log(  history
**Clas
### Mo{ id: 2, name: 
ca.addItem({ id:
    ole.lo
    tracId: i});
    }
    .trackEvedded',
 cart        cart.on('itemA  console        this.cart.     temRemoved', ({ item } s consetupListenotification:   s() {}) => {
   
        thi  uprt.on('itemAddedateDispla
        }   this.emit);rtUpdated
  daegetState() });
     
}     this.emit('iRemovem: removedItem, cart: 
    ;
          alculateTotal();
 
 exten      const remodsdItem = t f (index .splice(index,> -1) {
Ete= itemId)r {;
     
    [] 0;
    (item) {
        thieTotal();});tems.findIndex(it => item.id 
       'cartUpdat, this.getState()
    }
    , cart: this.getSta
    rem const indoveItem    thi) {
     s.emit(    #Addeditems.push
    ;
    #t
// ss ShoppinReal-v  reent,mple: Shopping C unsubscribe;
 callbac
      if (!this.#
    off(event, cs.#events.als(event)) lbac   {
        if (!
       if (!this.#ev
clasrvervent, callback) {
 Patple.c');ple.com'); are notified.
Purpose:*a one-to-mandency between objects sone object chang state, all dep
conlog(adanageUse
const viewer =tory.create('viewer', 'Amit'
/o  t admin = User     rn ['adteUser('admin', 'Rajmin'
    }() {
    
  ryr(ttic getUseype,ew new Error(`Unknown we na Vie: ${type}`);
  ewer(nmerCasr':ame, ema
e()) {);     retu
           
            ': new Editor(name, em
              case 'admi       switch mail);
            
    sta         return tiw Admin(nac
  sss UserFacto.permissions 
    constructor
class ss wer extends User ss Editor extends Us= ['
    construcread', 'w
        return 'Managing user  th
 construct(name, email
            t  or('Database  connecte
    getTodo
    fic   turn this.todos.fin    d) => todo.id  {
       return deletedT     if (indthrow new Error('Tot found');
it this.sa  letedTodoveT = this.todosdex, 1)[0];

        co
  st index =  }Todo(i this.td) {indIndex(todo => to
  
    
    dotoggl = this.fin Error('Todo not 
        await this.saveToSt   if();
       (!todo) thro
        todo.update(upd    if) throw n('Todo not 
    c updateTods) {
        cothis.fi
       awanotifch (error) {
 y();throw new Erro
it thiStorage();

     sync addTodo(tedo = new Todo(text    catego thic frosiy) {
        try {gn(tomJSON(ddo, {te(data
               ata(da id: data.idta.tetegory, data.pry);
            completeObompleted,
       createdAt
        const todo = new T         tags: t    t: this.updatedISOString
     dueDatnew D,t: this.c
            i     completed: ority:ompletedcategory this.priori: thisy,
      
            id: tate()e) new Date(thisre false;& !this.complete
            text: t        ret
    isOverdu
 this   bjec.updat.assign(thates);
 
     thisthipdates) {ss = this.tags.filter(t; t !== tag);
    
  
    this.tagthis.updatedAt = news.p
             ddTag((!this.tatag) {
         ret      this.ct = new Dateompletemp()leted;
   his.updat
 his.completed =tedAt = new Da
        this.up    this**assds ansAdvancedplication with 
s and Modern apFeaturplications features (oes** chaining, nullis)

### Advanced P- Building mo
**ES6 imporvaScrit/expDay d patterns stat
- Module organizatiies athods
- Rend consng delegation
 dInheritanynamic user i
g aript - Cbacks and end Pronderstanding)

**Day 17:andlnd manipulating DOing w ents
- EvAsynry-catch
- Se asynial async pvents*atterns*
- Sele
y 18: DOM Manipulati
 vs parallel exchrtion
- and Modner code
ern Patternono programmingallback functio and callback 
- - onc/await syntax for clmise.all() and PrPromises and mise # W
eek 4: Advanced Concepts and Design Patterns {#week-4}

## Day 22: Advanced Object-Oriented Programming

### Prototypes and Prototype Chain

**What is Prototype?** Every JavaScript object has a prototype - another object from which it inherits properties and methods.

**Understanding the Prototype Chain:**
```javascript
// Every function has a prototype property
function Person(name) {
    this.name = name;
}

// Add method to prototype
Person.prototype.greet = function() {
    return `Hello, I'm ${this.name}`;
};

Person.prototype.species = "Homo sapiens";

const person1 = new Person("Raj");
const person2 = new Person("Priya");

console.log(person1.greet()); // "Hello, I'm Raj"
console.log(person1.species); // "Homo sapiens"

// Both instances share the same prototype
console.log(person1.__proto__ === Person.prototype); // true
console.log(person1.__proto__ === person2.__proto__); // true
```

**Prototype Chain Visualization:**
```
person1 → Person.prototype → Object.prototype → null
   ↓           ↓                    ↓
 {name: "Raj"} {greet: function}  {toString: function}
```

**Checking Prototype Chain:**
```javascript
function Animal(name) {
    this.name = name;
}

Animal.prototype.eat = function() {
    return `${this.name} is eating`;
};

function Dog(name, breed) {
    Animal.call(this, name); // Call parent constructor
    this.breed = breed;
}

// Set up inheritance
Dog.prototype = Object.create(Animal.prototype);
Dog.prototype.constructor = Dog;

Dog.prototype.bark = function() {
    return `${this.name} is barking`;
};

const dog = new Dog("Buddy", "Golden Retriever");

// Prototype chain methods
console.log(dog.hasOwnProperty('name'));    // true (own property)
console.log(dog.hasOwnProperty('eat'));     // false (inherited)
console.log('eat' in dog);                  // true (in prototype chain)
console.log(dog instanceof Dog);           // true
console.log(dog instanceof Animal);        // true
console.log(dog instanceof Object);        // true

// Get prototype
console.log(Object.getPrototypeOf(dog) === Dog.prototype); // true
```

### Advanced Inheritance Patterns

**Mixin Pattern:**
```javascript
// Mixin - reusable functionality
const CanFly = {
    fly() {
        return `${this.name} is flying`;
    },
    
    land() {
        return `${this.name} has landed`;
    }
};

const CanSwim = {
    swim() {
        return `${this.name} is swimming`;
    },
    
    dive() {
        return `${this.name} is diving`;
    }
};

// Base class
class Animal {
    constructor(name) {
        this.name = name;
    }
    
    eat() {
        return `${this.name} is eating`;
    }
}

// Mix in capabilities
class Bird extends Animal {
    constructor(name, wingspan) {
        super(name);
        this.wingspan = wingspan;
    }
}

class Duck extends Animal {
    constructor(name) {
        super(name);
    }
}

// Apply mixins
Object.assign(Bird.prototype, CanFly);
Object.assign(Duck.prototype, CanFly, CanSwim);

const eagle = new Bird("Eagle", "2m");
const duck = new Duck("Donald");

console.log(eagle.fly());  // "Eagle is flying"
console.log(duck.swim());  // "Donald is swimming"
console.log(duck.fly());   // "Donald is flying"
```

**Factory Pattern:**
```javascript
class VehicleFactory {
    static createVehicle(type, options) {
        switch (type.toLowerCase()) {
            case 'car':
                return new Car(options);
            case 'motorcycle':
                return new Motorcycle(options);
            case 'truck':
                return new Truck(options);
            default:
                throw new Error(`Unknown vehicle type: ${type}`);
        }
    }
}

class Vehicle {
    constructor({ make, model, year }) {
        this.make = make;
        this.model = model;
        this.year = year;
    }
    
    getInfo() {
        return `${this.year} ${this.make} ${this.model}`;
    }
}

class Car extends Vehicle {
    constructor(options) {
        super(options);
        this.type = 'car';
        this.doors = options.doors || 4;
    }
    
    start() {
        return `${this.getInfo()} car started`;
    }
}

class Motorcycle extends Vehicle {
    constructor(options) {
        super(options);
        this.type = 'motorcycle';
        this.engineSize = options.engineSize;
    }
    
    start() {
        return `${this.getInfo()} motorcycle started`;
    }
}

class Truck extends Vehicle {
    constructor(options) {
        super(options);
        this.type = 'truck';
        this.loadCapacity = options.loadCapacity;
    }
    
    start() {
        return `${this.getInfo()} truck started`;
    }
}

// Usage
const car = VehicleFactory.createVehicle('car', {
    make: 'Toyota',
    model: 'Camry',
    year: 2022,
    doors: 4
});

const bike = VehicleFactory.createVehicle('motorcycle', {
    make: 'Honda',
    model: 'CBR',
    year: 2021,
    engineSize: '600cc'
});

console.log(car.start());  // "2022 Toyota Camry car started"
console.log(bike.start()); // "2021 Honda CBR motorcycle started"
```

### Composition over Inheritance

**Problem with Deep Inheritance:**
```javascript
// Deep inheritance hierarchy - hard to maintain
class Animal {}
class Mammal extends Animal {}
class Carnivore extends Mammal {}
class Feline extends Carnivore {}
class BigCat extends Feline {}
class Lion extends BigCat {}

// What if we need a flying mammal? Or swimming carnivore?
// Inheritance becomes complex and rigid
```

**Solution with Composition:**
```javascript
// Behavior objects
const canEat = (state) => ({
    eat(food) {
        return `${state.name} is eating ${food}`;
    }
});

const canWalk = (state) => ({
    walk() {
        return `${state.name} is walking`;
    }
});

const canSwim = (state) => ({
    swim() {
        return `${state.name} is swimming`;
    }
});

const canFly = (state) => ({
    fly() {
        return `${state.name} is flying`;
    }
});

// Factory functions using composition
const createAnimal = (name) => {
    const state = { name };
    return Object.assign({}, canEat(state));
};

const createDog = (name) => {
    const state = { name };
    return Object.assign(
        {},
        canEat(state),
        canWalk(state),
        canSwim(state),
        {
            bark() {
                return `${state.name} is barking`;
            }
        }
    );
};

const createBird = (name) => {
    const state = { name };
    return Object.assign(
        {},
        canEat(state),
        canWalk(state),
        canFly(state),
        {
            chirp() {
                return `${state.name} is chirping`;
            }
        }
    );
};

const createDuck = (name) => {
    const state = { name };
    return Object.assign(
        {},
        canEat(state),
        canWalk(state),
        canSwim(state),
        canFly(state),
        {
            quack() {
                return `${state.name} is quacking`;
            }
        }
    );
};

// Usage
const dog = createDog("Buddy");
const bird = createBird("Tweety");
const duck = createDuck("Donald");

console.log(dog.walk());   // "Buddy is walking"
console.log(dog.swim());   // "Buddy is swimming"
// console.log(dog.fly()); // Error - dogs can't fly

console.log(duck.swim());  // "Donald is swimming"
console.log(duck.fly());   // "Donald is flying"
console.log(duck.quack()); // "Donald is quacking"
```

### Advanced Class Features

**Private Fields and Methods:**
```javascript
class BankAccount {
    // Private fields
    #balance = 0;
    #accountNumber;
    #transactions = [];
    
    constructor(accountNumber, initialBalance = 0) {
        this.#accountNumber = accountNumber;
        this.#balance = initialBalance;
        this.#addTransaction('initial', initialBalance);
    }
    
    // Private method
    #addTransaction(type, amount) {
        this.#transactions.push({
            type,
            amount,
            timestamp: new Date(),
            balance: this.#balance
        });
    }
    
    #validateAmount(amount) {
        if (typeof amount !== 'number' || amount <= 0) {
            throw new Error('Amount must be a positive number');
        }
    }
    
    // Public methods
    deposit(amount) {
        this.#validateAmount(amount);
        this.#balance += amount;
        this.#addTransaction('deposit', amount);
        return this.#balance;
    }
    
    withdraw(amount) {
        this.#validateAmount(amount);
        
        if (amount > this.#balance) {
            throw new Error('Insufficient funds');
        }
        
        this.#balance -= amount;
        this.#addTransaction('withdrawal', -amount);
        return this.#balance;
    }
    
    getBalance() {
        return this.#balance;
    }
    
    getStatement() {
        return {
            accountNumber: this.#accountNumber,
            currentBalance: this.#balance,
            transactions: [...this.#transactions] // Return copy
        };
    }
    
    // Static method
    static validateAccountNumber(accountNumber) {
        return /^\d{10}$/.test(accountNumber);
    }
}

const account = new BankAccount('1234567890', 1000);
console.log(account.deposit(500));   // 1500
console.log(account.withdraw(200));  // 1300
console.log(account.getBalance());   // 1300

// These will cause errors:
// console.log(account.#balance);      // SyntaxError
// account.#addTransaction('test', 0); // SyntaxError
```

**Abstract Classes (Simulation):**
```javascript
class AbstractShape {
    constructor() {
        if (new.target === AbstractShape) {
            throw new Error('Cannot instantiate abstract class');
        }
    }
    
    // Abstract method - must be implemented by subclasses
    calculateArea() {
        throw new Error('calculateArea method must be implemented');
    }
    
    calculatePerimeter() {
        throw new Error('calculatePerimeter method must be implemented');
    }
    
    // Concrete method - can be used by all subclasses
    getInfo() {
        return `${this.constructor.name}: Area = ${this.calculateArea()}, Perimeter = ${this.calculatePerimeter()}`;
    }
}

class Rectangle extends AbstractShape {
    constructor(width, height) {
        super();
        this.width = width;
        this.height = height;
    }
    
    calculateArea() {
        return this.width * this.height;
    }
    
    calculatePerimeter() {
        return 2 * (this.width + this.height);
    }
}

class Circle extends AbstractShape {
    constructor(radius) {
        super();
        this.radius = radius;
    }
    
    calculateArea() {
        return Math.PI * this.radius * this.radius;
    }
    
    calculatePerimeter() {
        return 2 * Math.PI * this.radius;
    }
}

// Usage
const rectangle = new Rectangle(5, 3);
const circle = new Circle(4);

console.log(rectangle.getInfo()); // "Rectangle: Area = 15, Perimeter = 16"
console.log(circle.getInfo());    // "Circle: Area = 50.27, Perimeter = 25.13"

// This will throw an error:
// const shape = new AbstractShape(); // Error: Cannot instantiate abstract class
```

### Decorator Pattern

**Method Decorators:**
```javascript
// Decorator functions
function logMethod(target, propertyName, descriptor) {
    const originalMethod = descriptor.value;
    
    descriptor.value = function (...args) {
        console.log(`Calling ${propertyName} with arguments:`, args);
        const result = originalMethod.apply(this, args);
        console.log(`${propertyName} returned:`, result);
        return result;
    };
    
    return descriptor;
}

function measureTime(target, propertyName, descriptor) {
    const originalMethod = descriptor.value;
    
    descriptor.value = function (...args) {
        const start = performance.now();
        const result = originalMethod.apply(this, args);
        const end = performance.now();
        console.log(`${propertyName} took ${end - start} milliseconds`);
        return result;
    };
    
    return descriptor;
}

// Manual decorator application (since decorators aren't fully supported yet)
class Calculator {
    add(a, b) {
        return a + b;
    }
    
    multiply(a, b) {
        // Simulate expensive operation
        let result = 0;
        for (let i = 0; i < b; i++) {
            result += a;
        }
        return result;
    }
}

// Apply decorators manually
const originalAdd = Calculator.prototype.add;
Calculator.prototype.add = logMethod(Calculator.prototype, 'add', {
    value: originalAdd
}).value;

const originalMultiply = Calculator.prototype.multiply;
Calculator.prototype.multiply = measureTime(Calculator.prototype, 'multiply', {
    value: originalMultiply
}).value;

const calc = new Calculator();
console.log(calc.add(5, 3));      // Logs method call and result
console.log(calc.multiply(4, 1000)); // Logs execution time
```

**Function Decorators:**
```javascript
// Higher-order function decorators
const withLogging = (fn) => {
    return function (...args) {
        console.log(`Calling function with args:`, args);
        const result = fn.apply(this, args);
        console.log(`Function returned:`, result);
        return result;
    };
};

const withRetry = (maxAttempts = 3) => (fn) => {
    return async function (...args) {
        let lastError;
        
        for (let attempt = 1; attempt <= maxAttempts; attempt++) {
            try {
                return await fn.apply(this, args);
            } catch (error) {
                lastError = error;
                console.log(`Attempt ${attempt} failed:`, error.message);
                
                if (attempt < maxAttempts) {
                    await new Promise(resolve => setTimeout(resolve, 1000 * attempt));
                }
            }
        }
        
        throw lastError;
    };
};

const withCache = (fn) => {
    const cache = new Map();
    
    return function (...args) {
        const key = JSON.stringify(args);
        
        if (cache.has(key)) {
            console.log('Cache hit');
            return cache.get(key);
        }
        
        console.log('Cache miss');
        const result = fn.apply(this, args);
        cache.set(key, result);
        return result;
    };
};

// Usage
const expensiveFunction = withCache(withLogging((n) => {
    console.log(`Computing expensive operation for ${n}`);
    return n * n * n;
}));

const unreliableFunction = withRetry(3)(async (data) => {
    if (Math.random() < 0.7) {
        throw new Error('Random failure');
    }
    return `Processed: ${data}`;
});

// Test decorated functions
console.log(expensiveFunction(5)); // Cache miss, computes
console.log(expensiveFunction(5)); // Cache hit, returns cached

unreliableFunction('test data')
    .then(result => console.log(result))
    .catch(error => console.log('Final error:', error.message));
```

### 🎯 Key Points
- Prototype chain enables inheritance in JavaScript
- Composition is often more flexible than inheritance
- Private fields (#) provide true encapsulation
- Abstract classes can be simulated for better design
- Decorators add functionality without modifying original code
- Factory pattern centralizes object creation logic

### 💡 Interview Questions (Hinglish)

**Q1: Prototype chain kya hai aur inheritance kaise kaam karta hai?**

**A:**
Prototype chain objects ke beech inheritance establish karta hai:
```javascript
function Animal(name) { this.name = name; }
Animal.prototype.eat = function() { return "eating"; };

function Dog(name) { Animal.call(this, name); }
Dog.prototype = Object.create(Animal.prototype);

const dog = new Dog("Buddy");
dog.eat(); // Prototype chain se inherit hua
```

**Q2: Composition over inheritance kya hai?**

**A:**
Inheritance ke bajaye objects ko combine karna:
```javascript
// Inheritance (rigid)
class FlyingBird extends Bird extends Animal {}

// Composition (flexible)
const duck = Object.assign({}, canSwim, canFly, canWalk);
```
Composition zyada flexible hai aur multiple behaviors easily combine kar sakte hain.

**Q3: Private fields (#) aur regular properties mein kya difference hai?**

**A:**
```javascript
class Example {
    publicField = "accessible";
    #privateField = "not accessible";
    
    getPrivate() {
        return this.#privateField; // Only accessible inside class
    }
}

const obj = new Example();
console.log(obj.publicField);  // Works
console.log(obj.#privateField); // SyntaxError
```

---## Day 23: D
esign Patterns in JavaScript

### What are Design Patterns?

**Definition:** Design patterns are reusable solutions to commonly occurring problems in software design. They represent best practices and proven solutions.

**Real-World Analogy:**
```
Design Patterns = Architectural Blueprints
- House blueprint (pattern) can be used to build many houses
- Each house (implementation) is unique but follows same structure
- Patterns solve common problems (how to organize rooms, plumbing, etc.)
```

### Creational Patterns

#### Singleton Pattern
**Problem:** Ensure only one instance of a class exists.

```javascript
class DatabaseConnection {
    constructor() {
        if (DatabaseConnection.instance) {
            return DatabaseConnection.instance;
        }
        
        this.connection = null;
        this.isConnected = false;
        DatabaseConnection.instance = this;
    }
    
    connect() {
        if (!this.isConnected) {
            this.connection = "Connected to database";
            this.isConnected = true;
            console.log("Database connected");
        }
        return this.connection;
    }
    
    disconnect() {
        if (this.isConnected) {
            this.connection = null;
            this.isConnected = false;
            console.log("Database disconnected");
        }
    }
    
    query(sql) {
        if (!this.isConnected) {
            throw new Error("Database not connected");
        }
        return `Executing: ${sql}`;
    }
}

// Usage
const db1 = new DatabaseConnection();
const db2 = new DatabaseConnection();

console.log(db1 === db2); // true - same instance
db1.connect();
console.log(db2.query("SELECT * FROM users")); // Works because same instance
```

**Modern Singleton with Module:**
```javascript
// databaseService.js
class DatabaseService {
    constructor() {
        this.connection = null;
        this.isConnected = false;
    }
    
    async connect(config) {
        if (this.isConnected) return this.connection;
        
        try {
            // Simulate connection
            await new Promise(resolve => setTimeout(resolve, 1000));
            this.connection = `Connected to ${config.host}:${config.port}`;
            this.isConnected = true;
            console.log("Database connected");
            return this.connection;
        } catch (error) {
            throw new Error(`Connection failed: ${error.message}`);
        }
    }
    
    async query(sql) {
        if (!this.isConnected) {
            throw new Error("Database not connected");
        }
        
        // Simulate query
        await new Promise(resolve => setTimeout(resolve, 100));
        return { sql, results: [], timestamp: new Date() };
    }
    
    disconnect() {
        this.connection = null;
        this.isConnected = false;
        console.log("Database disconnected");
    }
}

// Export single instance
export default new DatabaseService();
```

#### Factory Pattern
**Problem:** Create objects without specifying exact classes.

```javascript
// Product classes
class Car {
    constructor(options) {
        this.type = 'car';
        this.make = options.make;
        this.model = options.model;
        this.doors = options.doors || 4;
    }
    
    getInfo() {
        return `${this.make} ${this.model} (${this.doors} doors)`;
    }
    
    start() {
        return `${this.getInfo()} car started`;
    }
}

class Truck {
    constructor(options) {
        this.type = 'truck';
        this.make = options.make;
        this.model = options.model;
        this.loadCapacity = options.loadCapacity;
    }
    
    getInfo() {
        return `${this.make} ${this.model} (${this.loadCapacity}kg capacity)`;
    }
    
    start() {
        return `${this.getInfo()} truck started`;
    }
}

class Motorcycle {
    constructor(options) {
        this.type = 'motorcycle';
        this.make = options.make;
        this.model = options.model;
        this.engineSize = options.engineSize;
    }
    
    getInfo() {
        return `${this.make} ${this.model} (${this.engineSize})`;
    }
    
    start() {
        return `${this.getInfo()} motorcycle started`;
    }
}

// Factory
class VehicleFactory {
    static vehicleTypes = {
        car: Car,
        truck: Truck,
        motorcycle: Motorcycle
    };
    
    static createVehicle(type, options) {
        const VehicleClass = this.vehicleTypes[type.toLowerCase()];
        
        if (!VehicleClass) {
            throw new Error(`Unknown vehicle type: ${type}`);
        }
        
        return new VehicleClass(options);
    }
    
    static registerVehicleType(type, vehicleClass) {
        this.vehicleTypes[type.toLowerCase()] = vehicleClass;
    }
    
    static getAvailableTypes() {
        return Object.keys(this.vehicleTypes);
    }
}

// Usage
const car = VehicleFactory.createVehicle('car', {
    make: 'Toyota',
    model: 'Camry',
    doors: 4
});

const truck = VehicleFactory.createVehicle('truck', {
    make: 'Ford',
    model: 'F-150',
    loadCapacity: 1000
});

console.log(car.start());   // "Toyota Camry (4 doors) car started"
console.log(truck.start()); // "Ford F-150 (1000kg capacity) truck started"

// Add new vehicle type
class ElectricCar extends Car {
    constructor(options) {
        super(options);
        this.batteryCapacity = options.batteryCapacity;
        this.type = 'electric-car';
    }
    
    getInfo() {
        return `${this.make} ${this.model} (${this.batteryCapacity}kWh battery)`;
    }
}

VehicleFactory.registerVehicleType('electric-car', ElectricCar);

const tesla = VehicleFactory.createVehicle('electric-car', {
    make: 'Tesla',
    model: 'Model 3',
    batteryCapacity: 75
});

console.log(tesla.start()); // "Tesla Model 3 (75kWh battery) car started"
```

#### Builder Pattern
**Problem:** Construct complex objects step by step.

```javascript
class QueryBuilder {
    constructor() {
        this.reset();
    }
    
    reset() {
        this.query = {
            select: [],
            from: '',
            joins: [],
            where: [],
            groupBy: [],
            having: [],
            orderBy: [],
            limit: null,
            offset: null
        };
        return this;
    }
    
    select(...columns) {
        this.query.select.push(...columns);
        return this;
    }
    
    from(table) {
        this.query.from = table;
        return this;
    }
    
    join(table, condition) {
        this.query.joins.push(`JOIN ${table} ON ${condition}`);
        return this;
    }
    
    leftJoin(table, condition) {
        this.query.joins.push(`LEFT JOIN ${table} ON ${condition}`);
        return this;
    }
    
    where(condition) {
        this.query.where.push(condition);
        return this;
    }
    
    groupBy(...columns) {
        this.query.groupBy.push(...columns);
        return this;
    }
    
    having(condition) {
        this.query.having.push(condition);
        return this;
    }
    
    orderBy(column, direction = 'ASC') {
        this.query.orderBy.push(`${column} ${direction}`);
        return this;
    }
    
    limit(count) {
        this.query.limit = count;
        return this;
    }
    
    offset(count) {
        this.query.offset = count;
        return this;
    }
    
    build() {
        let sql = '';
        
        // SELECT
        if (this.query.select.length > 0) {
            sql += `SELECT ${this.query.select.join(', ')}`;
        } else {
            sql += 'SELECT *';
        }
        
        // FROM
        if (this.query.from) {
            sql += ` FROM ${this.query.from}`;
        }
        
        // JOINS
        if (this.query.joins.length > 0) {
            sql += ` ${this.query.joins.join(' ')}`;
        }
        
        // WHERE
        if (this.query.where.length > 0) {
            sql += ` WHERE ${this.query.where.join(' AND ')}`;
        }
        
        // GROUP BY
        if (this.query.groupBy.length > 0) {
            sql += ` GROUP BY ${this.query.groupBy.join(', ')}`;
        }
        
        // HAVING
        if (this.query.having.length > 0) {
            sql += ` HAVING ${this.query.having.join(' AND ')}`;
        }
        
        // ORDER BY
        if (this.query.orderBy.length > 0) {
            sql += ` ORDER BY ${this.query.orderBy.join(', ')}`;
        }
        
        // LIMIT
        if (this.query.limit !== null) {
            sql += ` LIMIT ${this.query.limit}`;
        }
        
        // OFFSET
        if (this.query.offset !== null) {
            sql += ` OFFSET ${this.query.offset}`;
        }
        
        return sql;
    }
}

// Usage
const query = new QueryBuilder()
    .select('u.name', 'u.email', 'p.title')
    .from('users u')
    .leftJoin('posts p', 'u.id = p.user_id')
    .where('u.active = 1')
    .where('u.created_at > "2023-01-01"')
    .groupBy('u.id')
    .having('COUNT(p.id) > 0')
    .orderBy('u.name', 'ASC')
    .limit(10)
    .offset(20)
    .build();

console.log(query);
// SELECT u.name, u.email, p.title FROM users u LEFT JOIN posts p ON u.id = p.user_id WHERE u.active = 1 AND u.created_at > "2023-01-01" GROUP BY u.id HAVING COUNT(p.id) > 0 ORDER BY u.name ASC LIMIT 10 OFFSET 20
```

### Structural Patterns

#### Adapter Pattern
**Problem:** Make incompatible interfaces work together.

```javascript
// Old API (legacy system)
class OldPaymentGateway {
    makePayment(amount) {
        return {
            status: amount > 0 ? 'success' : 'failed',
            transactionId: Math.random().toString(36).substr(2, 9),
            amount: amount
        };
    }
}

// New API (modern system)
class NewPaymentGateway {
    processPayment(paymentData) {
        return {
            success: paymentData.amount > 0,
            id: crypto.randomUUID(),
            total: paymentData.amount,
            timestamp: new Date().toISOString()
        };
    }
}

// Adapter to make old API compatible with new interface
class PaymentAdapter {
    constructor(oldGateway) {
        this.oldGateway = oldGateway;
    }
    
    processPayment(paymentData) {
        // Convert new interface to old interface
        const result = this.oldGateway.makePayment(paymentData.amount);
        
        // Convert old response to new format
        return {
            success: result.status === 'success',
            id: result.transactionId,
            total: result.amount,
            timestamp: new Date().toISOString()
        };
    }
}

// Usage
const oldGateway = new OldPaymentGateway();
const newGateway = new NewPaymentGateway();
const adaptedOldGateway = new PaymentAdapter(oldGateway);

// Both gateways now have the same interface
const paymentData = { amount: 100 };

console.log('New Gateway:', newGateway.processPayment(paymentData));
console.log('Adapted Old Gateway:', adaptedOldGateway.processPayment(paymentData));
```

#### Decorator Pattern
**Problem:** Add new functionality to objects without altering their structure.

```javascript
// Base component
class Coffee {
    constructor() {
        this.description = "Simple coffee";
        this.cost = 2.00;
    }
    
    getDescription() {
        return this.description;
    }
    
    getCost() {
        return this.cost;
    }
}

// Decorator base class
class CoffeeDecorator {
    constructor(coffee) {
        this.coffee = coffee;
    }
    
    getDescription() {
        return this.coffee.getDescription();
    }
    
    getCost() {
        return this.coffee.getCost();
    }
}

// Concrete decorators
class MilkDecorator extends CoffeeDecorator {
    constructor(coffee) {
        super(coffee);
    }
    
    getDescription() {
        return this.coffee.getDescription() + ", Milk";
    }
    
    getCost() {
        return this.coffee.getCost() + 0.50;
    }
}

class SugarDecorator extends CoffeeDecorator {
    constructor(coffee) {
        super(coffee);
    }
    
    getDescription() {
        return this.coffee.getDescription() + ", Sugar";
    }
    
    getCost() {
        return this.coffee.getCost() + 0.25;
    }
}

class WhipDecorator extends CoffeeDecorator {
    constructor(coffee) {
        super(coffee);
    }
    
    getDescription() {
        return this.coffee.getDescription() + ", Whipped Cream";
    }
    
    getCost() {
        return this.coffee.getCost() + 0.75;
    }
}

// Usage
let coffee = new Coffee();
console.log(`${coffee.getDescription()}: $${coffee.getCost()}`);

// Add milk
coffee = new MilkDecorator(coffee);
console.log(`${coffee.getDescription()}: $${coffee.getCost()}`);

// Add sugar
coffee = new SugarDecorator(coffee);
console.log(`${coffee.getDescription()}: $${coffee.getCost()}`);

// Add whipped cream
coffee = new WhipDecorator(coffee);
console.log(`${coffee.getDescription()}: $${coffee.getCost()}`);

// Output:
// Simple coffee: $2
// Simple coffee, Milk: $2.5
// Simple coffee, Milk, Sugar: $2.75
// Simple coffee, Milk, Sugar, Whipped Cream: $3.5
```

### Behavioral Patterns

#### Observer Pattern
**Problem:** Notify multiple objects about state changes.

```javascript
class EventEmitter {
    constructor() {
        this.events = {};
    }
    
    on(event, callback) {
        if (!this.events[event]) {
            this.events[event] = [];
        }
        this.events[event].push(callback);
        
        // Return unsubscribe function
        return () => {
            this.events[event] = this.events[event].filter(cb => cb !== callback);
        };
    }
    
    emit(event, data) {
        if (this.events[event]) {
            this.events[event].forEach(callback => {
                try {
                    callback(data);
                } catch (error) {
                    console.error(`Error in event handler for ${event}:`, error);
                }
            });
        }
    }
    
    once(event, callback) {
        const unsubscribe = this.on(event, (data) => {
            callback(data);
            unsubscribe();
        });
        return unsubscribe;
    }
    
    removeAllListeners(event) {
        if (event) {
            delete this.events[event];
        } else {
            this.events = {};
        }
    }
}

// Subject (Observable)
class ShoppingCart extends EventEmitter {
    constructor() {
        super();
        this.items = [];
        this.total = 0;
    }
    
    addItem(item) {
        this.items.push(item);
        this.total += item.price;
        
        this.emit('itemAdded', { item, total: this.total, items: [...this.items] });
        this.emit('cartChanged', { action: 'add', item, total: this.total });
    }
    
    removeItem(itemId) {
        const itemIndex = this.items.findIndex(item => item.id === itemId);
        
        if (itemIndex > -1) {
            const removedItem = this.items.splice(itemIndex, 1)[0];
            this.total -= removedItem.price;
            
            this.emit('itemRemoved', { item: removedItem, total: this.total, items: [...this.items] });
            this.emit('cartChanged', { action: 'remove', item: removedItem, total: this.total });
        }
    }
    
    clear() {
        const oldItems = [...this.items];
        this.items = [];
        this.total = 0;
        
        this.emit('cartCleared', { oldItems });
        this.emit('cartChanged', { action: 'clear', total: 0 });
    }
}

// Observers
class CartDisplay {
    constructor(cart) {
        this.cart = cart;
        this.setupListeners();
    }
    
    setupListeners() {
        this.cart.on('cartChanged', (data) => {
            this.updateDisplay(data);
        });
    }
    
    updateDisplay(data) {
        console.log(`Cart Display: ${data.action} - Total: $${data.total}`);
    }
}

class InventoryManager {
    constructor(cart) {
        this.cart = cart;
        this.inventory = new Map();
        this.setupListeners();
    }
    
    setupListeners() {
        this.cart.on('itemAdded', (data) => {
            this.updateInventory(data.item, -1);
        });
        
        this.cart.on('itemRemoved', (data) => {
            this.updateInventory(data.item, 1);
        });
    }
    
    updateInventory(item, change) {
        const currentStock = this.inventory.get(item.id) || 100;
        const newStock = currentStock + change;
        this.inventory.set(item.id, newStock);
        
        console.log(`Inventory: ${item.name} stock updated to ${newStock}`);
        
        if (newStock < 10) {
            console.log(`⚠️ Low stock alert for ${item.name}`);
        }
    }
}

class EmailNotifier {
    constructor(cart) {
        this.cart = cart;
        this.setupListeners();
    }
    
    setupListeners() {
        this.cart.on('itemAdded', (data) => {
            if (data.total > 100) {
                this.sendPromotionEmail(data);
            }
        });
    }
    
    sendPromotionEmail(data) {
        console.log(`📧 Sending promotion email - Cart total: $${data.total}`);
    }
}

// Usage
const cart = new ShoppingCart();
const display = new CartDisplay(cart);
const inventory = new InventoryManager(cart);
const emailNotifier = new EmailNotifier(cart);

// Add items to cart
cart.addItem({ id: 1, name: "Laptop", price: 999 });
cart.addItem({ id: 2, name: "Mouse", price: 25 });
cart.addItem({ id: 3, name: "Keyboard", price: 75 });

// Remove item
cart.removeItem(2);

// Clear cart
cart.clear();
```

#### Strategy Pattern
**Problem:** Select algorithm at runtime.

```javascript
// Strategy interface
class PaymentStrategy {
    pay(amount) {
        throw new Error("pay method must be implemented");
    }
    
    validate(paymentData) {
        throw new Error("validate method must be implemented");
    }
}

// Concrete strategies
class CreditCardStrategy extends PaymentStrategy {
    constructor(cardNumber, cvv, expiryDate) {
        super();
        this.cardNumber = cardNumber;
        this.cvv = cvv;
        this.expiryDate = expiryDate;
    }
    
    validate(paymentData) {
        // Validate credit card data
        if (!this.cardNumber || this.cardNumber.length !== 16) {
            throw new Error("Invalid card number");
        }
        
        if (!this.cvv || this.cvv.length !== 3) {
            throw new Error("Invalid CVV");
        }
        
        return true;
    }
    
    pay(amount) {
        this.validate();
        
        // Simulate payment processing
        return {
            success: true,
            transactionId: `CC_${Date.now()}`,
            amount: amount,
            method: 'Credit Card',
            last4: this.cardNumber.slice(-4)
        };
    }
}

class PayPalStrategy extends PaymentStrategy {
    constructor(email, password) {
        super();
        this.email = email;
        this.password = password;
    }
    
    validate(paymentData) {
        if (!this.email || !this.email.includes('@')) {
            throw new Error("Invalid email");
        }
        
        if (!this.password || this.password.length < 6) {
            throw new Error("Invalid password");
        }
        
        return true;
    }
    
    pay(amount) {
        this.validate();
        
        return {
            success: true,
            transactionId: `PP_${Date.now()}`,
            amount: amount,
            method: 'PayPal',
            email: this.email
        };
    }
}

class CryptoStrategy extends PaymentStrategy {
    constructor(walletAddress, privateKey) {
        super();
        this.walletAddress = walletAddress;
        this.privateKey = privateKey;
    }
    
    validate(paymentData) {
        if (!this.walletAddress || this.walletAddress.length !== 42) {
            throw new Error("Invalid wallet address");
        }
        
        return true;
    }
    
    pay(amount) {
        this.validate();
        
        return {
            success: true,
            transactionId: `CRYPTO_${Date.now()}`,
            amount: amount,
            method: 'Cryptocurrency',
            wallet: this.walletAddress.slice(0, 6) + '...' + this.walletAddress.slice(-4)
        };
    }
}

// Context
class PaymentProcessor {
    constructor() {
        this.strategy = null;
    }
    
    setStrategy(strategy) {
        this.strategy = strategy;
    }
    
    processPayment(amount) {
        if (!this.strategy) {
            throw new Error("Payment strategy not set");
        }
        
        try {
            const result = this.strategy.pay(amount);
            console.log(`Payment processed: ${JSON.stringify(result, null, 2)}`);
            return result;
        } catch (error) {
            console.error(`Payment failed: ${error.message}`);
            throw error;
        }
    }
}

// Usage
const processor = new PaymentProcessor();

// Pay with credit card
const creditCard = new CreditCardStrategy("1234567890123456", "123", "12/25");
processor.setStrategy(creditCard);
processor.processPayment(100);

// Pay with PayPal
const paypal = new PayPalStrategy("user@example.com", "password123");
processor.setStrategy(paypal);
processor.processPayment(50);

// Pay with crypto
const crypto = new CryptoStrategy("0x1234567890123456789012345678901234567890", "private_key");
processor.setStrategy(crypto);
processor.processPayment(75);
```

### 🎯 Key Points
- Design patterns solve common programming problems
- Creational patterns handle object creation
- Structural patterns deal with object composition
- Behavioral patterns focus on communication between objects
- Patterns improve code reusability and maintainability
- Choose patterns based on specific problems, not just because they exist

### 💡 Interview Questions (Hinglish)

**Q1: Singleton pattern kya hai aur kab use karte hain?**

**A:**
Singleton pattern ensure karta hai ki class ka sirf ek instance ho:
```javascript
class Database {
    constructor() {
        if (Database.instance) {
            return Database.instance;
        }
        Database.instance = this;
    }
}

const db1 = new Database();
const db2 = new Database();
console.log(db1 === db2); // true
```
Use cases: Database connections, logging, configuration settings.

**Q2: Observer pattern ka real-world example do.**

**A:**
Event-driven systems mein use hota hai:
```javascript
class Newsletter {
    constructor() {
        this.subscribers = [];
    }
    
    subscribe(email) {
        this.subscribers.push(email);
    }
    
    notify(news) {
        this.subscribers.forEach(email => {
            console.log(`Sending to ${email}: ${news}`);
        });
    }
}
```
Examples: Event listeners, MVC architecture, pub-sub systems.

**Q3: Strategy pattern kab aur kaise use karte hain?**

**A:**
Jab runtime par algorithm change karna ho:
```javascript
class Calculator {
    setStrategy(strategy) {
        this.strategy = strategy;
    }
    
    calculate(a, b) {
        return this.strategy.execute(a, b);
    }
}

const addStrategy = { execute: (a, b) => a + b };
const multiplyStrategy = { execute: (a, b) => a * b };
```
Use cases: Payment methods, sorting algorithms, validation rules.

---## D
ay 24: Performance Optimization and Best Practices

### JavaScript Performance Fundamentals

**Understanding Performance Bottlenecks:**
```javascript
// Performance measurement
function measurePerformance(fn, label) {
    const start = performance.now();
    const result = fn();
    const end = performance.now();
    console.log(`${label}: ${end - start} milliseconds`);
    return result;
}

// Example usage
const slowFunction = () => {
    let sum = 0;
    for (let i = 0; i < 1000000; i++) {
        sum += i;
    }
    return sum;
};

measurePerformance(slowFunction, "Slow Loop");
```

### Memory Management and Optimization

#### Memory Leaks Prevention
```javascript
// ❌ Memory leak - event listeners not removed
class BadComponent {
    constructor() {
        this.data = new Array(1000000).fill('data');
        
        // Event listener never removed
        document.addEventListener('click', this.handleClick.bind(this));
    }
    
    handleClick() {
        console.log('Clicked');
    }
}

// ✅ Proper cleanup
class GoodComponent {
    constructor() {
        this.data = new Array(1000000).fill('data');
        this.handleClick = this.handleClick.bind(this);
        
        document.addEventListener('click', this.handleClick);
    }
    
    handleClick() {
        console.log('Clicked');
    }
    
    destroy() {
        // Clean up event listeners
        document.removeEventListener('click', this.handleClick);
        
        // Clear references
        this.data = null;
    }
}

// ❌ Memory leak - closures holding references
function createLeakyFunction() {
    const largeData = new Array(1000000).fill('data');
    
    return function() {
        // This closure keeps largeData in memory even if not used
        console.log('Function called');
    };
}

// ✅ Avoid unnecessary closures
function createEfficientFunction() {
    // Don't capture unnecessary variables
    return function() {
        console.log('Function called');
    };
}

// ❌ Memory leak - detached DOM nodes
class DOMLeakExample {
    constructor() {
        this.elements = [];
    }
    
    addElement() {
        const div = document.createElement('div');
        div.innerHTML = 'Some content';
        document.body.appendChild(div);
        
        // Keeping reference to DOM element
        this.elements.push(div);
    }
    
    removeElement() {
        const div = this.elements.pop();
        if (div && div.parentNode) {
            div.parentNode.removeChild(div);
            // div is still referenced in this.elements array!
        }
    }
}

// ✅ Proper DOM cleanup
class DOMCleanExample {
    constructor() {
        this.elements = new Set();
    }
    
    addElement() {
        const div = document.createElement('div');
        div.innerHTML = 'Some content';
        document.body.appendChild(div);
        
        this.elements.add(div);
    }
    
    removeElement(element) {
        if (element && element.parentNode) {
            element.parentNode.removeChild(element);
            this.elements.delete(element); // Remove reference
        }
    }
    
    cleanup() {
        this.elements.forEach(element => {
            if (element.parentNode) {
                element.parentNode.removeChild(element);
            }
        });
        this.elements.clear();
    }
}
```

#### Efficient Data Structures
```javascript
// ❌ Inefficient array operations
class SlowList {
    constructor() {
        this.items = [];
    }
    
    // O(n) - slow for large arrays
    contains(item) {
        return this.items.indexOf(item) !== -1;
    }
    
    // O(n) - slow removal
    remove(item) {
        const index = this.items.indexOf(item);
        if (index > -1) {
            this.items.splice(index, 1);
        }
    }
}

// ✅ Efficient with Set
class FastList {
    constructor() {
        this.items = new Set();
    }
    
    // O(1) - fast lookup
    contains(item) {
        return this.items.has(item);
    }
    
    // O(1) - fast removal
    remove(item) {
        return this.items.delete(item);
    }
    
    add(item) {
        this.items.add(item);
    }
    
    toArray() {
        return Array.from(this.items);
    }
}

// Map vs Object for key-value storage
class PerformanceComparison {
    static compareMapVsObject() {
        const iterations = 100000;
        
        // Object performance
        console.time('Object operations');
        const obj = {};
        for (let i = 0; i < iterations; i++) {
            obj[`key${i}`] = i;
        }
        for (let i = 0; i < iterations; i++) {
            const value = obj[`key${i}`];
        }
        console.timeEnd('Object operations');
        
        // Map performance
        console.time('Map operations');
        const map = new Map();
        for (let i = 0; i < iterations; i++) {
            map.set(`key${i}`, i);
        }
        for (let i = 0; i < iterations; i++) {
            const value = map.get(`key${i}`);
        }
        console.timeEnd('Map operations');
    }
}

// PerformanceComparison.compareMapVsObject();
```

### Algorithm Optimization

#### Memoization for Expensive Calculations
```javascript
// ❌ Expensive recursive function
function slowFibonacci(n) {
    if (n <= 1) return n;
    return slowFibonacci(n - 1) + slowFibonacci(n - 2);
}

// ✅ Memoized version
function createMemoizedFibonacci() {
    const cache = new Map();
    
    function fibonacci(n) {
        if (n <= 1) return n;
        
        if (cache.has(n)) {
            return cache.get(n);
        }
        
        const result = fibonacci(n - 1) + fibonacci(n - 2);
        cache.set(n, result);
        return result;
    }
    
    return fibonacci;
}

const fastFibonacci = createMemoizedFibonacci();

// Performance comparison
console.time('Slow Fibonacci');
console.log(slowFibonacci(35));
console.timeEnd('Slow Fibonacci');

console.time('Fast Fibonacci');
console.log(fastFibonacci(35));
console.timeEnd('Fast Fibonacci');

// Generic memoization utility
function memoize(fn, keyGenerator = (...args) => JSON.stringify(args)) {
    const cache = new Map();
    
    return function memoized(...args) {
        const key = keyGenerator(...args);
        
        if (cache.has(key)) {
            return cache.get(key);
        }
        
        const result = fn.apply(this, args);
        cache.set(key, result);
        return result;
    };
}

// Usage
const expensiveCalculation = memoize((x, y) => {
    console.log(`Computing ${x} * ${y}`);
    return x * y;
});

console.log(expensiveCalculation(5, 3)); // Computing 5 * 3, returns 15
console.log(expensiveCalculation(5, 3)); // Returns 15 (from cache)
```

#### Debouncing and Throttling
```javascript
// Debouncing - delay execution until after calls have stopped
function debounce(func, delay) {
    let timeoutId;
    
    return function debounced(...args) {
        // Clear previous timeout
        clearTimeout(timeoutId);
        
        // Set new timeout
        timeoutId = setTimeout(() => {
            func.apply(this, args);
        }, delay);
    };
}

// Throttling - limit execution to once per time period
function throttle(func, limit) {
    let inThrottle;
    
    return function throttled(...args) {
        if (!inThrottle) {
            func.apply(this, args);
            inThrottle = true;
            
            setTimeout(() => {
                inThrottle = false;
            }, limit);
        }
    };
}

// Advanced throttling with leading and trailing options
function advancedThrottle(func, limit, options = {}) {
    let timeout;
    let previous = 0;
    
    const { leading = true, trailing = true } = options;
    
    return function throttled(...args) {
        const now = Date.now();
        
        if (!previous && !leading) {
            previous = now;
        }
        
        const remaining = limit - (now - previous);
        
        if (remaining <= 0 || remaining > limit) {
            if (timeout) {
                clearTimeout(timeout);
                timeout = null;
            }
            
            previous = now;
            func.apply(this, args);
        } else if (!timeout && trailing) {
            timeout = setTimeout(() => {
                previous = leading ? Date.now() : 0;
                timeout = null;
                func.apply(this, args);
            }, remaining);
        }
    };
}

// Usage examples
const searchInput = document.querySelector('#search');
const scrollContainer = document.querySelector('#container');

// Debounced search - wait for user to stop typing
const debouncedSearch = debounce((query) => {
    console.log(`Searching for: ${query}`);
    // Perform search API call
}, 300);

searchInput?.addEventListener('input', (e) => {
    debouncedSearch(e.target.value);
});

// Throttled scroll - limit scroll event handling
const throttledScroll = throttle(() => {
    console.log('Scroll event handled');
    // Update scroll position, lazy load images, etc.
}, 100);

scrollContainer?.addEventListener('scroll', throttledScroll);
```

### DOM Performance Optimization

#### Efficient DOM Manipulation
```javascript
// ❌ Inefficient DOM updates
function inefficientDOMUpdate(items) {
    const container = document.querySelector('#container');
    
    // Causes multiple reflows and repaints
    items.forEach(item => {
        const div = document.createElement('div');
        div.textContent = item.name;
        div.style.color = item.color;
        container.appendChild(div); // Each append causes reflow
    });
}

// ✅ Efficient DOM updates
function efficientDOMUpdate(items) {
    const container = document.querySelector('#container');
    
    // Create document fragment to batch DOM operations
    const fragment = document.createDocumentFragment();
    
    items.forEach(item => {
        const div = document.createElement('div');
        div.textContent = item.name;
        div.style.color = item.color;
        fragment.appendChild(div); // No reflow until fragment is appended
    });
    
    // Single reflow
    container.appendChild(fragment);
}

// ✅ Even more efficient with innerHTML (for simple content)
function veryEfficientDOMUpdate(items) {
    const container = document.querySelector('#container');
    
    const html = items.map(item => 
        `<div style="color: ${item.color}">${item.name}</div>`
    ).join('');
    
    container.innerHTML = html; // Single DOM operation
}

// Virtual scrolling for large lists
class VirtualScrollList {
    constructor(container, itemHeight, renderItem) {
        this.container = container;
        this.itemHeight = itemHeight;
        this.renderItem = renderItem;
        this.items = [];
        this.visibleStart = 0;
        this.visibleEnd = 0;
        this.scrollTop = 0;
        this.containerHeight = container.clientHeight;
        
        this.setupScrollListener();
    }
    
    setItems(items) {
        this.items = items;
        this.updateVisibleRange();
        this.render();
    }
    
    setupScrollListener() {
        const throttledScroll = throttle(() => {
            this.scrollTop = this.container.scrollTop;
            this.updateVisibleRange();
            this.render();
        }, 16); // ~60fps
        
        this.container.addEventListener('scroll', throttledScroll);
    }
    
    updateVisibleRange() {
        const buffer = 5; // Render extra items for smooth scrolling
        
        this.visibleStart = Math.max(0, 
            Math.floor(this.scrollTop / this.itemHeight) - buffer
        );
        
        this.visibleEnd = Math.min(this.items.length,
            this.visibleStart + Math.ceil(this.containerHeight / this.itemHeight) + buffer * 2
        );
    }
    
    render() {
        const visibleItems = this.items.slice(this.visibleStart, this.visibleEnd);
        
        // Create spacers to maintain scroll position
        const topSpacer = this.visibleStart * this.itemHeight;
        const bottomSpacer = (this.items.length - this.visibleEnd) * this.itemHeight;
        
        const html = `
            <div style="height: ${topSpacer}px;"></div>
            ${visibleItems.map((item, index) => 
                this.renderItem(item, this.visibleStart + index)
            ).join('')}
            <div style="height: ${bottomSpacer}px;"></div>
        `;
        
        this.container.innerHTML = html;
    }
}
```

### Asynchronous Performance

#### Efficient Promise Handling
```javascript
// ❌ Sequential processing (slow)
async function slowProcessing(urls) {
    const results = [];
    
    for (const url of urls) {
        const response = await fetch(url);
        const data = await response.json();
        results.push(data);
    }
    
    return results;
}

// ✅ Parallel processing (fast)
async function fastProcessing(urls) {
    const promises = urls.map(async (url) => {
        const response = await fetch(url);
        return response.json();
    });
    
    return Promise.all(promises);
}

// ✅ Controlled concurrency
async function controlledProcessing(urls, concurrency = 3) {
    const results = [];
    
    for (let i = 0; i < urls.length; i += concurrency) {
        const batch = urls.slice(i, i + concurrency);
        const batchPromises = batch.map(async (url) => {
            const response = await fetch(url);
            return response.json();
        });
        
        const batchResults = await Promise.all(batchPromises);
        results.push(...batchResults);
    }
    
    return results;
}

// Promise pool for managing concurrent operations
class PromisePool {
    constructor(concurrency = 3) {
        this.concurrency = concurrency;
        this.running = 0;
        this.queue = [];
    }
    
    async add(promiseFunction) {
        return new Promise((resolve, reject) => {
            this.queue.push({
                promiseFunction,
                resolve,
                reject
            });
            
            this.process();
        });
    }
    
    async process() {
        if (this.running >= this.concurrency || this.queue.length === 0) {
            return;
        }
        
        this.running++;
        const { promiseFunction, resolve, reject } = this.queue.shift();
        
        try {
            const result = await promiseFunction();
            resolve(result);
        } catch (error) {
            reject(error);
        } finally {
            this.running--;
            this.process(); // Process next item in queue
        }
    }
}

// Usage
const pool = new PromisePool(3);

const urls = ['url1', 'url2', 'url3', 'url4', 'url5'];
const promises = urls.map(url => 
    pool.add(() => fetch(url).then(r => r.json()))
);

Promise.all(promises).then(results => {
    console.log('All requests completed:', results);
});
```

### Code Splitting and Lazy Loading

```javascript
// Dynamic imports for code splitting
class ModuleLoader {
    constructor() {
        this.cache = new Map();
    }
    
    async loadModule(moduleName) {
        if (this.cache.has(moduleName)) {
            return this.cache.get(moduleName);
        }
        
        try {
            let module;
            
            switch (moduleName) {
                case 'chart':
                    module = await import('./modules/chart.js');
                    break;
                case 'calendar':
                    module = await import('./modules/calendar.js');
                    break;
                case 'editor':
                    module = await import('./modules/editor.js');
                    break;
                default:
                    throw new Error(`Unknown module: ${moduleName}`);
            }
            
            this.cache.set(moduleName, module);
            return module;
            
        } catch (error) {
            console.error(`Failed to load module ${moduleName}:`, error);
            throw error;
        }
    }
    
    async loadComponent(componentName, container) {
        try {
            const module = await this.loadModule(componentName);
            const component = new module.default(container);
            return component;
        } catch (error) {
            console.error(`Failed to load component ${componentName}:`, error);
            throw error;
        }
    }
}

// Lazy loading with Intersection Observer
class LazyLoader {
    constructor() {
        this.observer = new IntersectionObserver(
            this.handleIntersection.bind(this),
            {
                rootMargin: '50px',
                threshold: 0.1
            }
        );
    }
    
    observe(element, loadFunction) {
        element.dataset.loadFunction = loadFunction.toString();
        this.observer.observe(element);
    }
    
    handleIntersection(entries) {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                const element = entry.target;
                const loadFunctionStr = element.dataset.loadFunction;
                
                if (loadFunctionStr) {
                    try {
                        const loadFunction = new Function('return ' + loadFunctionStr)();
                        loadFunction(element);
                        this.observer.unobserve(element);
                    } catch (error) {
                        console.error('Error executing load function:', error);
                    }
                }
            }
        });
    }
    
    disconnect() {
        this.observer.disconnect();
    }
}

// Usage
const moduleLoader = new ModuleLoader();
const lazyLoader = new LazyLoader();

// Lazy load chart when section becomes visible
const chartSection = document.querySelector('#chart-section');
lazyLoader.observe(chartSection, async (element) => {
    const chartModule = await moduleLoader.loadModule('chart');
    const chart = new chartModule.default(element);
    chart.render();
});
```

### Performance Monitoring

```javascript
class PerformanceMonitor {
    constructor() {
        this.metrics = new Map();
        this.observers = [];
        
        this.setupObservers();
    }
    
    setupObservers() {
        // Performance Observer for various metrics
        if ('PerformanceObserver' in window) {
            // Long tasks (blocking main thread)
            const longTaskObserver = new PerformanceObserver((list) => {
                list.getEntries().forEach(entry => {
                    console.warn(`Long task detected: ${entry.duration}ms`);
                    this.recordMetric('longTask', entry.duration);
                });
            });
            
            try {
                longTaskObserver.observe({ entryTypes: ['longtask'] });
                this.observers.push(longTaskObserver);
            } catch (e) {
                console.log('Long task observer not supported');
            }
            
            // Layout shifts
            const layoutShiftObserver = new PerformanceObserver((list) => {
                let cumulativeScore = 0;
                
                list.getEntries().forEach(entry => {
                    if (!entry.hadRecentInput) {
                        cumulativeScore += entry.value;
                    }
                });
                
                if (cumulativeScore > 0) {
                    console.warn(`Layout shift detected: ${cumulativeScore}`);
                    this.recordMetric('layoutShift', cumulativeScore);
                }
            });
            
            try {
                layoutShiftObserver.observe({ entryTypes: ['layout-shift'] });
                this.observers.push(layoutShiftObserver);
            } catch (e) {
                console.log('Layout shift observer not supported');
            }
        }
    }
    
    recordMetric(name, value) {
        if (!this.metrics.has(name)) {
            this.metrics.set(name, []);
        }
        
        this.metrics.get(name).push({
            value,
            timestamp: Date.now()
        });
    }
    
    measureFunction(fn, name) {
        const start = performance.now();
        const result = fn();
        const duration = performance.now() - start;
        
        this.recordMetric(name, duration);
        
        if (duration > 16) { // More than one frame at 60fps
            console.warn(`Slow function ${name}: ${duration}ms`);
        }
        
        return result;
    }
    
    async measureAsyncFunction(fn, name) {
        const start = performance.now();
        const result = await fn();
        const duration = performance.now() - start;
        
        this.recordMetric(name, duration);
        
        return result;
    }
    
    getMetrics() {
        const summary = {};
        
        this.metrics.forEach((values, name) => {
            const durations = values.map(v => v.value);
            summary[name] = {
                count: durations.length,
                average: durations.reduce((a, b) => a + b, 0) / durations.length,
                min: Math.min(...durations),
                max: Math.max(...durations),
                recent: durations.slice(-10) // Last 10 measurements
            };
        });
        
        return summary;
    }
    
    getVitalMetrics() {
        return new Promise((resolve) => {
            // Core Web Vitals
            const vitals = {};
            
            // Largest Contentful Paint (LCP)
            new PerformanceObserver((list) => {
                const entries = list.getEntries();
                const lastEntry = entries[entries.length - 1];
                vitals.lcp = lastEntry.startTime;
            }).observe({ entryTypes: ['largest-contentful-paint'] });
            
            // First Input Delay (FID)
            new PerformanceObserver((list) => {
                list.getEntries().forEach(entry => {
                    vitals.fid = entry.processingStart - entry.startTime;
                });
            }).observe({ entryTypes: ['first-input'] });
            
            // Cumulative Layout Shift (CLS)
            let clsScore = 0;
            new PerformanceObserver((list) => {
                list.getEntries().forEach(entry => {
                    if (!entry.hadRecentInput) {
                        clsScore += entry.value;
                    }
                });
                vitals.cls = clsScore;
            }).observe({ entryTypes: ['layout-shift'] });
            
            setTimeout(() => resolve(vitals), 1000);
        });
    }
    
    disconnect() {
        this.observers.forEach(observer => observer.disconnect());
        this.observers = [];
    }
}

// Usage
const monitor = new PerformanceMonitor();

// Measure function performance
const result = monitor.measureFunction(() => {
    // Some expensive operation
    return Array.from({ length: 100000 }, (_, i) => i * i);
}, 'arrayGeneration');

// Get performance summary
setTimeout(() => {
    console.log('Performance Metrics:', monitor.getMetrics());
    
    monitor.getVitalMetrics().then(vitals => {
        console.log('Core Web Vitals:', vitals);
    });
}, 5000);
```

### 🎯 Key Points
- Measure performance before optimizing
- Avoid memory leaks by cleaning up references
- Use efficient data structures (Set, Map)
- Implement memoization for expensive calculations
- Debounce/throttle frequent operations
- Batch DOM operations to minimize reflows
- Use Promise.all() for parallel async operations
- Implement lazy loading for better initial load times
- Monitor performance metrics in production

### 💡 Interview Questions (Hinglish)

**Q1: Memory leaks kaise avoid karte hain JavaScript mein?**

**A:**
```javascript
// Event listeners remove karo
element.removeEventListener('click', handler);

// References clear karo
this.data = null;

// Closures mein unnecessary variables capture na karo
function createHandler() {
    // const largeData = ...; // Avoid if not needed
    return () => console.log('handled');
}
```

**Q2: Debouncing aur throttling mein kya difference hai?**

**A:**
- Debouncing: Function call delay karta hai jab tak calls stop na ho jaayein
- Throttling: Function ko fixed interval par limit karta hai
```javascript
// Debounce - search input ke liye
const debouncedSearch = debounce(search, 300);

// Throttle - scroll events ke liye  
const throttledScroll = throttle(handleScroll, 100);
```

**Q3: DOM performance kaise optimize karte hain?**

**A:**
```javascript
// Batch DOM operations
const fragment = document.createDocumentFragment();
items.forEach(item => {
    const div = document.createElement('div');
    fragment.appendChild(div);
});
container.appendChild(fragment); // Single reflow

// Virtual scrolling for large lists
// Lazy loading with Intersection Observer
```

---#
# Day 25: Testing and Debugging

### Testing Fundamentals

**Why Test JavaScript Code?**
- Catch bugs early in development
- Ensure code works as expected
- Make refactoring safer
- Document how code should behave
- Improve code quality and maintainability

### Types of Testing

#### Unit Testing
**Testing individual functions or components in isolation.**

```javascript
// Example function to test
function calculateTax(price, taxRate) {
    if (typeof price !== 'number' || typeof taxRate !== 'number') {
        throw new Error('Price and tax rate must be numbers');
    }
    
    if (price < 0 || taxRate < 0) {
        throw new Error('Price and tax rate must be positive');
    }
    
    return price * (taxRate / 100);
}

// Manual testing (basic approach)
function testCalculateTax() {
    // Test normal case
    const result1 = calculateTax(100, 10);
    console.assert(result1 === 10, 'Expected 10, got ' + result1);
    
    // Test edge cases
    const result2 = calculateTax(0, 10);
    console.assert(result2 === 0, 'Expected 0, got ' + result2);
    
    // Test error cases
    try {
        calculateTax('100', 10);
        console.assert(false, 'Should have thrown error for string price');
    } catch (error) {
        console.assert(error.message.includes('numbers'), 'Wrong error message');
    }
    
    console.log('All tests passed!');
}

// testCalculateTax();
```

**Simple Test Framework:**
```javascript
class SimpleTestFramework {
    constructor() {
        this.tests = [];
        this.passed = 0;
        this.failed = 0;
    }
    
    describe(description, testFunction) {
        console.log(`\n📝 ${description}`);
        testFunction();
    }
    
    it(description, testFunction) {
        try {
            testFunction();
            this.passed++;
            console.log(`  ✅ ${description}`);
        } catch (error) {
            this.failed++;
            console.log(`  ❌ ${description}`);
            console.log(`     Error: ${error.message}`);
        }
    }
    
    expect(actual) {
        return {
            toBe: (expected) => {
                if (actual !== expected) {
                    throw new Error(`Expected ${expected}, but got ${actual}`);
                }
            },
            
            toEqual: (expected) => {
                if (JSON.stringify(actual) !== JSON.stringify(expected)) {
                    throw new Error(`Expected ${JSON.stringify(expected)}, but got ${JSON.stringify(actual)}`);
                }
            },
            
            toThrow: (expectedError) => {
                if (typeof actual !== 'function') {
                    throw new Error('Expected a function that throws');
                }
                
                try {
                    actual();
                    throw new Error('Expected function to throw an error');
                } catch (error) {
                    if (expectedError && !error.message.includes(expectedError)) {
                        throw new Error(`Expected error containing "${expectedError}", but got "${error.message}"`);
                    }
                }
            },
            
            toBeGreaterThan: (expected) => {
                if (actual <= expected) {
                    throw new Error(`Expected ${actual} to be greater than ${expected}`);
                }
            },
            
            toContain: (expected) => {
                if (!actual.includes(expected)) {
                    throw new Error(`Expected ${actual} to contain ${expected}`);
                }
            }
        };
    }
    
    summary() {
        console.log(`\n📊 Test Summary:`);
        console.log(`   Passed: ${this.passed}`);
        console.log(`   Failed: ${this.failed}`);
        console.log(`   Total: ${this.passed + this.failed}`);
        
        if (this.failed === 0) {
            console.log('   🎉 All tests passed!');
        }
    }
}

// Usage
const test = new SimpleTestFramework();

test.describe('calculateTax function', () => {
    test.it('should calculate tax correctly for positive numbers', () => {
        test.expect(calculateTax(100, 10)).toBe(10);
        test.expect(calculateTax(200, 5)).toBe(10);
    });
    
    test.it('should handle zero values', () => {
        test.expect(calculateTax(0, 10)).toBe(0);
        test.expect(calculateTax(100, 0)).toBe(0);
    });
    
    test.it('should throw error for invalid inputs', () => {
        test.expect(() => calculateTax('100', 10)).toThrow('numbers');
        test.expect(() => calculateTax(100, '10')).toThrow('numbers');
        test.expect(() => calculateTax(-100, 10)).toThrow('positive');
    });
});

test.summary();
```

#### Integration Testing
**Testing how multiple components work together.**

```javascript
// Example: Testing a shopping cart system
class ShoppingCart {
    constructor() {
        this.items = [];
        this.discounts = [];
    }
    
    addItem(product, quantity = 1) {
        const existingItem = this.items.find(item => item.product.id === product.id);
        
        if (existingItem) {
            existingItem.quantity += quantity;
        } else {
            this.items.push({ product, quantity });
        }
    }
    
    removeItem(productId) {
        this.items = this.items.filter(item => item.product.id !== productId);
    }
    
    applyDiscount(discount) {
        this.discounts.push(discount);
    }
    
    getTotal() {
        const subtotal = this.items.reduce((total, item) => {
            return total + (item.product.price * item.quantity);
        }, 0);
        
        const discountAmount = this.discounts.reduce((total, discount) => {
            return total + (subtotal * discount.percentage / 100);
        }, 0);
        
        return Math.max(0, subtotal - discountAmount);
    }
    
    getItemCount() {
        return this.items.reduce((count, item) => count + item.quantity, 0);
    }
}

class Product {
    constructor(id, name, price) {
        this.id = id;
        this.name = name;
        this.price = price;
    }
}

// Integration tests
test.describe('Shopping Cart Integration', () => {
    let cart, product1, product2;
    
    // Setup before each test
    function setup() {
        cart = new ShoppingCart();
        product1 = new Product(1, 'Laptop', 1000);
        product2 = new Product(2, 'Mouse', 50);
    }
    
    test.it('should add items and calculate total correctly', () => {
        setup();
        
        cart.addItem(product1, 1);
        cart.addItem(product2, 2);
        
        test.expect(cart.getItemCount()).toBe(3);
        test.expect(cart.getTotal()).toBe(1100);
    });
    
    test.it('should apply discounts correctly', () => {
        setup();
        
        cart.addItem(product1, 1);
        cart.applyDiscount({ percentage: 10 });
        
        test.expect(cart.getTotal()).toBe(900);
    });
    
    test.it('should handle item removal', () => {
        setup();
        
        cart.addItem(product1, 1);
        cart.addItem(product2, 1);
        cart.removeItem(product2.id);
        
        test.expect(cart.getItemCount()).toBe(1);
        test.expect(cart.getTotal()).toBe(1000);
    });
});

test.summary();
```

### Test-Driven Development (TDD)

**TDD Process: Red → Green → Refactor**

```javascript
// Step 1: Write failing test (Red)
test.describe('User Authentication', () => {
    test.it('should validate email format', () => {
        test.expect(validateEmail('user@example.com')).toBe(true);
        test.expect(validateEmail('invalid-email')).toBe(false);
    });
});

// Step 2: Write minimal code to pass test (Green)
function validateEmail(email) {
    return email.includes('@') && email.includes('.');
}

// Step 3: Refactor (improve code while keeping tests passing)
function validateEmail(email) {
    const emailRegex = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
    return emailRegex.test(email);
}

// Add more tests
test.describe('User Authentication - Extended', () => {
    test.it('should validate password strength', () => {
        test.expect(validatePassword('weak')).toBe(false);
        test.expect(validatePassword('StrongPass123!')).toBe(true);
    });
    
    test.it('should authenticate user with valid credentials', () => {
        const user = authenticateUser('user@example.com', 'StrongPass123!');
        test.expect(user).toEqual({ email: 'user@example.com', authenticated: true });
    });
});

// Implement functions to pass tests
function validatePassword(password) {
    return password.length >= 8 && 
           /[A-Z]/.test(password) && 
           /[a-z]/.test(password) && 
           /\d/.test(password) && 
           /[!@#$%^&*]/.test(password);
}

function authenticateUser(email, password) {
    if (validateEmail(email) && validatePassword(password)) {
        return { email, authenticated: true };
    }
    return { authenticated: false };
}
```

### Mocking and Stubbing

**Mocking external dependencies for isolated testing.**

```javascript
// Mock implementation
class MockFetch {
    constructor() {
        this.calls = [];
        this.responses = new Map();
    }
    
    // Set up mock response
    mockResponse(url, response) {
        this.responses.set(url, response);
    }
    
    // Mock fetch function
    fetch(url, options = {}) {
        this.calls.push({ url, options });
        
        const response = this.responses.get(url);
        
        if (response) {
            return Promise.resolve({
                ok: response.ok !== false,
                status: response.status || 200,
                json: () => Promise.resolve(response.data),
                text: () => Promise.resolve(JSON.stringify(response.data))
            });
        }
        
        return Promise.reject(new Error(`No mock response for ${url}`));
    }
    
    // Verify calls
    wasCalledWith(url, options) {
        return this.calls.some(call => 
            call.url === url && 
            JSON.stringify(call.options) === JSON.stringify(options)
        );
    }
    
    getCallCount() {
        return this.calls.length;
    }
    
    reset() {
        this.calls = [];
        this.responses.clear();
    }
}

// Service to test
class UserService {
    constructor(fetchFunction = fetch) {
        this.fetch = fetchFunction;
    }
    
    async getUser(id) {
        const response = await this.fetch(`/api/users/${id}`);
        
        if (!response.ok) {
            throw new Error(`Failed to fetch user: ${response.status}`);
        }
        
        return response.json();
    }
    
    async createUser(userData) {
        const response = await this.fetch('/api/users', {
            method: 'POST',
            headers: { 'Content-Type': 'application/json' },
            body: JSON.stringify(userData)
        });
        
        if (!response.ok) {
            throw new Error(`Failed to create user: ${response.status}`);
        }
        
        return response.json();
    }
}

// Tests with mocks
test.describe('UserService with Mocks', () => {
    let mockFetch, userService;
    
    function setup() {
        mockFetch = new MockFetch();
        userService = new UserService(mockFetch.fetch.bind(mockFetch));
    }
    
    test.it('should fetch user successfully', async () => {
        setup();
        
        const userData = { id: 1, name: 'John Doe', email: 'john@example.com' };
        mockFetch.mockResponse('/api/users/1', { data: userData });
        
        const user = await userService.getUser(1);
        
        test.expect(user).toEqual(userData);
        test.expect(mockFetch.wasCalledWith('/api/users/1', {})).toBe(true);
    });
    
    test.it('should handle fetch errors', async () => {
        setup();
        
        mockFetch.mockResponse('/api/users/999', { 
            ok: false, 
            status: 404, 
            data: { error: 'User not found' } 
        });
        
        try {
            await userService.getUser(999);
            test.expect(false).toBe(true); // Should not reach here
        } catch (error) {
            test.expect(error.message).toContain('Failed to fetch user: 404');
        }
    });
    
    test.it('should create user with correct data', async () => {
        setup();
        
        const newUser = { name: 'Jane Doe', email: 'jane@example.com' };
        const createdUser = { id: 2, ...newUser };
        
        mockFetch.mockResponse('/api/users', { data: createdUser });
        
        const result = await userService.createUser(newUser);
        
        test.expect(result).toEqual(createdUser);
        test.expect(mockFetch.wasCalledWith('/api/users', {
            method: 'POST',
            headers: { 'Content-Type': 'application/json' },
            body: JSON.stringify(newUser)
        })).toBe(true);
    });
});

test.summary();
```

### Advanced Debugging Techniques

#### Console Debugging
```javascript
// Advanced console methods
class DebugHelper {
    static logWithStyle(message, style = 'color: blue; font-weight: bold') {
        console.log(`%c${message}`, style);
    }
    
    static logObject(obj, label = 'Object') {
        console.group(label);
        console.table(obj);
        console.log('JSON:', JSON.stringify(obj, null, 2));
        console.groupEnd();
    }
    
    static logPerformance(fn, label) {
        console.time(label);
        const result = fn();
        console.timeEnd(label);
        return result;
    }
    
    static logCallStack() {
        console.trace('Call stack:');
    }
    
    static logConditional(condition, message) {
        console.assert(condition, message);
    }
    
    static logCount(label) {
        console.count(label);
    }
    
    static createLogger(namespace) {
        return {
            log: (message) => console.log(`[${namespace}] ${message}`),
            warn: (message) => console.warn(`[${namespace}] ${message}`),
            error: (message) => console.error(`[${namespace}] ${message}`),
            debug: (message) => console.debug(`[${namespace}] ${message}`)
        };
    }
}

// Usage examples
const logger = DebugHelper.createLogger('UserService');

class DebuggableUserService {
    constructor() {
        this.users = [];
        this.logger = DebugHelper.createLogger('UserService');
    }
    
    addUser(user) {
        this.logger.log(`Adding user: ${user.name}`);
        
        // Conditional logging
        DebugHelper.logConditional(user.email, 'User must have email');
        
        // Performance logging
        const result = DebugHelper.logPerformance(() => {
            this.users.push(user);
            return user;
        }, 'Add User Operation');
        
        // Count logging
        DebugHelper.logCount('Users Added');
        
        // Object logging
        DebugHelper.logObject(user, 'Added User');
        
        return result;
    }
    
    findUser(id) {
        this.logger.log(`Finding user with ID: ${id}`);
        
        const user = this.users.find(u => u.id === id);
        
        if (!user) {
            this.logger.warn(`User not found: ${id}`);
            DebugHelper.logCallStack();
        }
        
        return user;
    }
}
```

#### Error Handling and Logging
```javascript
class ErrorHandler {
    constructor() {
        this.errors = [];
        this.setupGlobalErrorHandling();
    }
    
    setupGlobalErrorHandling() {
        // Handle uncaught errors
        window.addEventListener('error', (event) => {
            this.logError({
                type: 'JavaScript Error',
                message: event.message,
                filename: event.filename,
                line: event.lineno,
                column: event.colno,
                stack: event.error?.stack,
                timestamp: new Date().toISOString()
            });
        });
        
        // Handle unhandled promise rejections
        window.addEventListener('unhandledrejection', (event) => {
            this.logError({
                type: 'Unhandled Promise Rejection',
                message: event.reason?.message || event.reason,
                stack: event.reason?.stack,
                timestamp: new Date().toISOString()
            });
        });
    }
    
    logError(error) {
        this.errors.push(error);
        
        // Log to console with styling
        console.group(`🚨 ${error.type}`);
        console.error('Message:', error.message);
        if (error.filename) {
            console.error('File:', `${error.filename}:${error.line}:${error.column}`);
        }
        if (error.stack) {
            console.error('Stack:', error.stack);
        }
        console.error('Time:', error.timestamp);
        console.groupEnd();
        
        // Send to error reporting service (in production)
        this.reportError(error);
    }
    
    reportError(error) {
        // In production, send to error reporting service
        // fetch('/api/errors', { method: 'POST', body: JSON.stringify(error) });
        console.log('Error reported to service:', error.type);
    }
    
    getErrorSummary() {
        const summary = this.errors.reduce((acc, error) => {
            acc[error.type] = (acc[error.type] || 0) + 1;
            return acc;
        }, {});
        
        return {
            total: this.errors.length,
            byType: summary,
            recent: this.errors.slice(-5)
        };
    }
    
    clearErrors() {
        this.errors = [];
    }
}

// Custom error classes
class ValidationError extends Error {
    constructor(message, field) {
        super(message);
        this.name = 'ValidationError';
        this.field = field;
    }
}

class NetworkError extends Error {
    constructor(message, status, url) {
        super(message);
        this.name = 'NetworkError';
        this.status = status;
        this.url = url;
    }
}

// Usage
const errorHandler = new ErrorHandler();

function validateUser(user) {
    if (!user.email) {
        throw new ValidationError('Email is required', 'email');
    }
    
    if (!user.name) {
        throw new ValidationError('Name is required', 'name');
    }
    
    return true;
}

async function fetchUserData(id) {
    try {
        const response = await fetch(`/api/users/${id}`);
        
        if (!response.ok) {
            throw new NetworkError(
                `Failed to fetch user data`,
                response.status,
                response.url
            );
        }
        
        return await response.json();
    } catch (error) {
        if (error instanceof NetworkError) {
            console.error('Network error occurred:', error.message);
        }
        throw error;
    }
}

// Test error handling
try {
    validateUser({ name: 'John' }); // Missing email
} catch (error) {
    if (error instanceof ValidationError) {
        console.error(`Validation failed for ${error.field}: ${error.message}`);
    }
}

// Check error summary
setTimeout(() => {
    console.log('Error Summary:', errorHandler.getErrorSummary());
}, 2000);
```

### 🎯 Key Points
- Write tests before or alongside code development
- Use unit tests for individual functions
- Use integration tests for component interactions
- Mock external dependencies for isolated testing
- Implement proper error handling and logging
- Use console methods effectively for debugging
- Set up global error handling for production apps

### 💡 Interview Questions (Hinglish)

**Q1: Unit testing aur integration testing mein kya difference hai?**

**A:**
- Unit testing: Individual functions ko isolate mein test karna
- Integration testing: Multiple components ke interaction ko test karna
```javascript
// Unit test
test('add function', () => {
    expect(add(2, 3)).toBe(5);
});

// Integration test  
test('shopping cart with products', () => {
    cart.addItem(product);
    expect(cart.getTotal()).toBe(product.price);
});
```

**Q2: Mocking kya hai aur kab use karte hain?**

**A:**
External dependencies ko fake implementation se replace karna:
```javascript
// Mock API calls for testing
const mockFetch = jest.fn().mockResolvedValue({
    json: () => Promise.resolve({ id: 1, name: 'Test' })
});

// Test without actual API call
const user = await getUserData(1);
expect(mockFetch).toHaveBeenCalledWith('/api/users/1');
```

**Q3: JavaScript mein error handling best practices kya hain?**

**A:**
```javascript
// Try-catch for sync code
try {
    riskyOperation();
} catch (error) {
    console.error('Error:', error.message);
    // Handle or re-throw
}

// Async error handling
async function fetchData() {
    try {
        const data = await apiCall();
        return data;
    } catch (error) {
        logger.error('API call failed:', error);
        throw new CustomError('Data fetch failed');
    }
}

// Global error handlers
window.addEventListener('error', handleError);
window.addEventListener('unhandledrejection', handlePromiseError);
```

---##
 Day 26: Security Best Practices

### JavaScript Security Fundamentals

**Common Security Vulnerabilities:**
1. Cross-Site Scripting (XSS)
2. Cross-Site Request Forgery (CSRF)
3. Code Injection
4. Insecure Data Storage
5. Authentication/Authorization Issues

### Cross-Site Scripting (XSS) Prevention

#### Understanding XSS
```javascript
// ❌ Vulnerable to XSS
function displayUserComment(comment) {
    document.getElementById('comments').innerHTML = comment;
    // If comment contains: <script>alert('XSS')</script>
    // It will execute malicious code
}

// ❌ Another XSS vulnerability
function searchResults(query) {
    document.getElementById('results').innerHTML = 
        `<h2>Results for: ${query}</h2>`;
    // If query contains: <img src=x onerror=alert('XSS')>
    // Malicious code executes
}
```

#### XSS Prevention Techniques
```javascript
// ✅ Safe HTML escaping
class SecurityUtils {
    static escapeHtml(unsafe) {
        return unsafe
            .replace(/&/g, "&amp;")
            .replace(/</g, "&lt;")
            .replace(/>/g, "&gt;")
            .replace(/"/g, "&quot;")
            .replace(/'/g, "&#039;");
    }
    
    static sanitizeInput(input) {
        // Remove potentially dangerous characters
        return input.replace(/<script\b[^<]*(?:(?!<\/script>)<[^<]*)*<\/script>/gi, '');
    }
    
    static createSafeElement(tagName, textContent, attributes = {}) {
        const element = document.createElement(tagName);
        element.textContent = textContent; // Safe - no HTML parsing
        
        Object.entries(attributes).forEach(([key, value]) => {
            // Validate attribute names and values
            if (this.isValidAttribute(key, value)) {
                element.setAttribute(key, value);
            }
        });
        
        return element;
    }
    
    static isValidAttribute(name, value) {
        // Whitelist safe attributes
        const safeAttributes = ['class', 'id', 'data-*', 'aria-*'];
        const dangerousAttributes = ['onclick', 'onload', 'onerror', 'javascript:'];
        
        if (dangerousAttributes.some(attr => 
            name.toLowerCase().includes(attr) || 
            value.toLowerCase().includes(attr)
        )) {
            return false;
        }
        
        return safeAttributes.some(attr => 
            name === attr || (attr.endsWith('*') && name.startsWith(attr.slice(0, -1)))
        );
    }
}

// ✅ Safe comment display
function displayUserCommentSafe(comment) {
    const commentsContainer = document.getElementById('comments');
    const commentElement = SecurityUtils.createSafeElement('div', comment, {
        class: 'user-comment'
    });
    commentsContainer.appendChild(commentElement);
}

// ✅ Safe search results
function searchResultsSafe(query) {
    const resultsContainer = document.getElementById('results');
    const headerElement = SecurityUtils.createSafeElement('h2', `Results for: ${query}`);
    resultsContainer.appendChild(headerElement);
}

// ✅ Content Security Policy (CSP) helper
class CSPHelper {
    static generateNonce() {
        const array = new Uint8Array(16);
        crypto.getRandomValues(array);
        return btoa(String.fromCharCode.apply(null, array));
    }
    
    static createSecureScript(code, nonce) {
        const script = document.createElement('script');
        script.nonce = nonce;
        script.textContent = code;
        return script;
    }
    
    static setCSPHeaders() {
        // This would typically be set on the server
        const meta = document.createElement('meta');
        meta.httpEquiv = 'Content-Security-Policy';
        meta.content = `
            default-src 'self';
            script-src 'self' 'nonce-${this.generateNonce()}';
            style-src 'self' 'unsafe-inline';
            img-src 'self' data: https:;
            connect-src 'self';
            font-src 'self';
            object-src 'none';
            base-uri 'self';
            form-action 'self';
        `.replace(/\s+/g, ' ').trim();
        
        document.head.appendChild(meta);
    }
}
```

### Input Validation and Sanitization

```javascript
class InputValidator {
    static patterns = {
        email: /^[^\s@]+@[^\s@]+\.[^\s@]+$/,
        phone: /^\+?[\d\s\-\(\)]+$/,
        alphanumeric: /^[a-zA-Z0-9]+$/,
        safeString: /^[a-zA-Z0-9\s\-_.,!?]+$/,
        url: /^https?:\/\/(www\.)?[-a-zA-Z0-9@:%._\+~#=]{1,256}\.[a-zA-Z0-9()]{1,6}\b([-a-zA-Z0-9()@:%_\+.~#?&//=]*)$/
    };
    
    static validate(input, type, options = {}) {
        const result = {
            isValid: false,
            sanitized: '',
            errors: []
        };
        
        // Basic sanitization
        let sanitized = this.basicSanitize(input);
        
        // Type-specific validation
        switch (type) {
            case 'email':
                result.isValid = this.patterns.email.test(sanitized);
                if (!result.isValid) {
                    result.errors.push('Invalid email format');
                }
                break;
                
            case 'password':
                result.isValid = this.validatePassword(sanitized, options);
                if (!result.isValid) {
                    result.errors.push('Password does not meet requirements');
                }
                break;
                
            case 'username':
                sanitized = sanitized.toLowerCase().trim();
                result.isValid = this.patterns.alphanumeric.test(sanitized) && 
                                sanitized.length >= 3 && 
                                sanitized.length <= 20;
                if (!result.isValid) {
                    result.errors.push('Username must be 3-20 alphanumeric characters');
                }
                break;
                
            case 'url':
                result.isValid = this.patterns.url.test(sanitized);
                if (!result.isValid) {
                    result.errors.push('Invalid URL format');
                }
                break;
                
            case 'safeText':
                result.isValid = this.patterns.safeString.test(sanitized);
                if (!result.isValid) {
                    result.errors.push('Text contains invalid characters');
                }
                break;
                
            default:
                result.errors.push('Unknown validation type');
        }
        
        result.sanitized = sanitized;
        return result;
    }
    
    static basicSanitize(input) {
        if (typeof input !== 'string') {
            return '';
        }
        
        return input
            .trim()
            .replace(/[\x00-\x1F\x7F]/g, '') // Remove control characters
            .replace(/\s+/g, ' '); // Normalize whitespace
    }
    
    static validatePassword(password, options = {}) {
        const {
            minLength = 8,
            requireUppercase = true,
            requireLowercase = true,
            requireNumbers = true,
            requireSpecialChars = true
        } = options;
        
        if (password.length < minLength) return false;
        if (requireUppercase && !/[A-Z]/.test(password)) return false;
        if (requireLowercase && !/[a-z]/.test(password)) return false;
        if (requireNumbers && !/\d/.test(password)) return false;
        if (requireSpecialChars && !/[!@#$%^&*()_+\-=\[\]{};':"\\|,.<>\/?]/.test(password)) return false;
        
        return true;
    }
    
    static sanitizeForSQL(input) {
        // Basic SQL injection prevention (use parameterized queries instead)
        return input.replace(/['";\\]/g, '\\$&');
    }
    
    static sanitizeFileName(filename) {
        return filename
            .replace(/[^a-zA-Z0-9._-]/g, '_')
            .replace(/_{2,}/g, '_')
            .substring(0, 255);
    }
}

// Usage examples
const emailValidation = InputValidator.validate('user@example.com', 'email');
console.log(emailValidation); // { isValid: true, sanitized: 'user@example.com', errors: [] }

const passwordValidation = InputValidator.validate('weak', 'password');
console.log(passwordValidation); // { isValid: false, sanitized: 'weak', errors: [...] }
```

### Secure Authentication and Authorization

```javascript
class SecureAuth {
    constructor() {
        this.tokenKey = 'auth_token';
        this.refreshTokenKey = 'refresh_token';
        this.tokenExpiry = 15 * 60 * 1000; // 15 minutes
        this.refreshTokenExpiry = 7 * 24 * 60 * 60 * 1000; // 7 days
    }
    
    // Secure password hashing (client-side pre-hashing)
    async hashPassword(password, salt) {
        const encoder = new TextEncoder();
        const data = encoder.encode(password + salt);
        const hashBuffer = await crypto.subtle.digest('SHA-256', data);
        const hashArray = Array.from(new Uint8Array(hashBuffer));
        return hashArray.map(b => b.toString(16).padStart(2, '0')).join('');
    }
    
    // Generate secure random salt
    generateSalt() {
        const array = new Uint8Array(32);
        crypto.getRandomValues(array);
        return Array.from(array, byte => byte.toString(16).padStart(2, '0')).join('');
    }
    
    // Secure token storage
    storeToken(token, isRefreshToken = false) {
        const key = isRefreshToken ? this.refreshTokenKey : this.tokenKey;
        const expiry = Date.now() + (isRefreshToken ? this.refreshTokenExpiry : this.tokenExpiry);
        
        const tokenData = {
            token,
            expiry,
            timestamp: Date.now()
        };
        
        // Use sessionStorage for access tokens, localStorage for refresh tokens
        const storage = isRefreshToken ? localStorage : sessionStorage;
        storage.setItem(key, JSON.stringify(tokenData));
    }
    
    getToken(isRefreshToken = false) {
        const key = isRefreshToken ? this.refreshTokenKey : this.tokenKey;
        const storage = isRefreshToken ? localStorage : sessionStorage;
        
        try {
            const tokenData = JSON.parse(storage.getItem(key));
            
            if (!tokenData || Date.now() > tokenData.expiry) {
                this.clearToken(isRefreshToken);
                return null;
            }
            
            return tokenData.token;
        } catch (error) {
            this.clearToken(isRefreshToken);
            return null;
        }
    }
    
    clearToken(isRefreshToken = false) {
        const key = isRefreshToken ? this.refreshTokenKey : this.tokenKey;
        const storage = isRefreshToken ? localStorage : sessionStorage;
        storage.removeItem(key);
    }
    
    // Secure API request with automatic token refresh
    async secureRequest(url, options = {}) {
        let token = this.getToken();
        
        // Try to refresh token if expired
        if (!token) {
            token = await this.refreshAccessToken();
        }
        
        if (!token) {
            throw new Error('Authentication required');
        }
        
        const secureOptions = {
            ...options,
            headers: {
                ...options.headers,
                'Authorization': `Bearer ${token}`,
                'Content-Type': 'application/json',
                'X-Requested-With': 'XMLHttpRequest' // CSRF protection
            }
        };
        
        try {
            const response = await fetch(url, secureOptions);
            
            if (response.status === 401) {
                // Token expired, try refresh
                const newToken = await this.refreshAccessToken();
                if (newToken) {
                    secureOptions.headers.Authorization = `Bearer ${newToken}`;
                    return fetch(url, secureOptions);
                }
            }
            
            return response;
        } catch (error) {
            console.error('Secure request failed:', error);
            throw error;
        }
    }
    
    async refreshAccessToken() {
        const refreshToken = this.getToken(true);
        
        if (!refreshToken) {
            return null;
        }
        
        try {
            const response = await fetch('/api/auth/refresh', {
                method: 'POST',
                headers: {
                    'Content-Type': 'application/json',
                },
                body: JSON.stringify({ refreshToken })
            });
            
            if (response.ok) {
                const data = await response.json();
                this.storeToken(data.accessToken);
                
                if (data.refreshToken) {
                    this.storeToken(data.refreshToken, true);
                }
                
                return data.accessToken;
            }
        } catch (error) {
            console.error('Token refresh failed:', error);
        }
        
        // Refresh failed, clear all tokens
        this.clearToken();
        this.clearToken(true);
        return null;
    }
    
    // Secure logout
    async logout() {
        const refreshToken = this.getToken(true);
        
        if (refreshToken) {
            try {
                await fetch('/api/auth/logout', {
                    method: 'POST',
                    headers: {
                        'Content-Type': 'application/json',
                    },
                    body: JSON.stringify({ refreshToken })
                });
            } catch (error) {
                console.error('Logout request failed:', error);
            }
        }
        
        // Clear all tokens
        this.clearToken();
        this.clearToken(true);
        
        // Clear other sensitive data
        sessionStorage.clear();
        
        // Redirect to login
        window.location.href = '/login';
    }
    
    // Check if user is authenticated
    isAuthenticated() {
        return this.getToken() !== null || this.getToken(true) !== null;
    }
}

// Usage
const auth = new SecureAuth();

// Login example
async function login(email, password) {
    try {
        const salt = auth.generateSalt();
        const hashedPassword = await auth.hashPassword(password, salt);
        
        const response = await fetch('/api/auth/login', {
            method: 'POST',
            headers: {
                'Content-Type': 'application/json',
            },
            body: JSON.stringify({
                email,
                password: hashedPassword,
                salt
            })
        });
        
        if (response.ok) {
            const data = await response.json();
            auth.storeToken(data.accessToken);
            auth.storeToken(data.refreshToken, true);
            return true;
        }
        
        return false;
    } catch (error) {
        console.error('Login failed:', error);
        return false;
    }
}

// Protected API call example
async function getUserProfile() {
    try {
        const response = await auth.secureRequest('/api/user/profile');
        
        if (response.ok) {
            return await response.json();
        }
        
        throw new Error('Failed to fetch profile');
    } catch (error) {
        console.error('Profile fetch failed:', error);
        throw error;
    }
}
```

### Data Protection and Privacy

```javascript
class DataProtection {
    // Encrypt sensitive data before storing
    static async encryptData(data, password) {
        const encoder = new TextEncoder();
        const dataBuffer = encoder.encode(JSON.stringify(data));
        
        // Generate salt
        const salt = crypto.getRandomValues(new Uint8Array(16));
        
        // Derive key from password
        const keyMaterial = await crypto.subtle.importKey(
            'raw',
            encoder.encode(password),
            'PBKDF2',
            false,
            ['deriveKey']
        );
        
        const key = await crypto.subtle.deriveKey(
            {
                name: 'PBKDF2',
                salt: salt,
                iterations: 100000,
                hash: 'SHA-256'
            },
            keyMaterial,
            { name: 'AES-GCM', length: 256 },
            false,
            ['encrypt']
        );
        
        // Generate IV
        const iv = crypto.getRandomValues(new Uint8Array(12));
        
        // Encrypt data
        const encryptedData = await crypto.subtle.encrypt(
            { name: 'AES-GCM', iv: iv },
            key,
            dataBuffer
        );
        
        // Combine salt, iv, and encrypted data
        const result = new Uint8Array(salt.length + iv.length + encryptedData.byteLength);
        result.set(salt, 0);
        result.set(iv, salt.length);
        result.set(new Uint8Array(encryptedData), salt.length + iv.length);
        
        return btoa(String.fromCharCode.apply(null, result));
    }
    
    static async decryptData(encryptedData, password) {
        const encoder = new TextEncoder();
        const data = new Uint8Array(atob(encryptedData).split('').map(c => c.charCodeAt(0)));
        
        // Extract salt, iv, and encrypted data
        const salt = data.slice(0, 16);
        const iv = data.slice(16, 28);
        const encrypted = data.slice(28);
        
        // Derive key from password
        const keyMaterial = await crypto.subtle.importKey(
            'raw',
            encoder.encode(password),
            'PBKDF2',
            false,
            ['deriveKey']
        );
        
        const key = await crypto.subtle.deriveKey(
            {
                name: 'PBKDF2',
                salt: salt,
                iterations: 100000,
                hash: 'SHA-256'
            },
            keyMaterial,
            { name: 'AES-GCM', length: 256 },
            false,
            ['decrypt']
        );
        
        // Decrypt data
        const decryptedData = await crypto.subtle.decrypt(
            { name: 'AES-GCM', iv: iv },
            key,
            encrypted
        );
        
        const decoder = new TextDecoder();
        return JSON.parse(decoder.decode(decryptedData));
    }
    
    // Secure data storage with encryption
    static async storeSecureData(key, data, password) {
        try {
            const encryptedData = await this.encryptData(data, password);
            localStorage.setItem(key, encryptedData);
            return true;
        } catch (error) {
            console.error('Failed to store secure data:', error);
            return false;
        }
    }
    
    static async getSecureData(key, password) {
        try {
            const encryptedData = localStorage.getItem(key);
            if (!encryptedData) return null;
            
            return await this.decryptData(encryptedData, password);
        } catch (error) {
            console.error('Failed to retrieve secure data:', error);
            return null;
        }
    }
    
    // Data anonymization
    static anonymizeData(data, fieldsToAnonymize = []) {
        const anonymized = { ...data };
        
        fieldsToAnonymize.forEach(field => {
            if (anonymized[field]) {
                if (field === 'email') {
                    const [local, domain] = anonymized[field].split('@');
                    anonymized[field] = `${local.charAt(0)}***@${domain}`;
                } else if (field === 'phone') {
                    anonymized[field] = anonymized[field].replace(/\d(?=\d{4})/g, '*');
                } else if (field === 'name') {
                    anonymized[field] = anonymized[field].charAt(0) + '***';
                } else {
                    anonymized[field] = '***';
                }
            }
        });
        
        return anonymized;
    }
    
    // PII detection and masking
    static maskPII(text) {
        return text
            .replace(/\b\d{4}[\s-]?\d{4}[\s-]?\d{4}[\s-]?\d{4}\b/g, '**** **** **** ****') // Credit cards
            .replace(/\b\d{3}-\d{2}-\d{4}\b/g, '***-**-****') // SSN
            .replace(/\b[A-Za-z0-9._%+-]+@[A-Za-z0-9.-]+\.[A-Z|a-z]{2,}\b/g, '***@***.***') // Email
            .replace(/\b\d{3}[\s-]?\d{3}[\s-]?\d{4}\b/g, '***-***-****'); // Phone
    }
    
    // Secure data deletion
    static secureDelete(key) {
        if (localStorage.getItem(key)) {
            // Overwrite with random data multiple times
            for (let i = 0; i < 3; i++) {
                const randomData = crypto.getRandomValues(new Uint8Array(1024));
                localStorage.setItem(key, btoa(String.fromCharCode.apply(null, randomData)));
            }
            localStorage.removeItem(key);
        }
        
        if (sessionStorage.getItem(key)) {
            for (let i = 0; i < 3; i++) {
                const randomData = crypto.getRandomValues(new Uint8Array(1024));
                sessionStorage.setItem(key, btoa(String.fromCharCode.apply(null, randomData)));
            }
            sessionStorage.removeItem(key);
        }
    }
}

// Usage examples
async function demonstrateDataProtection() {
    const sensitiveData = {
        name: 'John Doe',
        email: 'john@example.com',
        phone: '123-456-7890',
        creditCard: '1234-5678-9012-3456'
    };
    
    const password = 'user-master-password';
    
    // Store encrypted data
    await DataProtection.storeSecureData('user-profile', sensitiveData, password);
    
    // Retrieve and decrypt data
    const retrievedData = await DataProtection.getSecureData('user-profile', password);
    console.log('Retrieved data:', retrievedData);
    
    // Anonymize data for analytics
    const anonymizedData = DataProtection.anonymizeData(sensitiveData, ['email', 'phone', 'name']);
    console.log('Anonymized data:', anonymizedData);
    
    // Mask PII in text
    const textWithPII = 'Contact John at john@example.com or 123-456-7890. His card is 1234-5678-9012-3456.';
    const maskedText = DataProtection.maskPII(textWithPII);
    console.log('Masked text:', maskedText);
    
    // Secure deletion
    DataProtection.secureDelete('user-profile');
}

// demonstrateDataProtection();
```

### Security Headers and Configuration

```javascript
class SecurityConfig {
    // Set security headers (typically done on server, but can be enforced client-side)
    static setSecurityHeaders() {
        // Content Security Policy
        const cspMeta = document.createElement('meta');
        cspMeta.httpEquiv = 'Content-Security-Policy';
        cspMeta.content = `
            default-src 'self';
            script-src 'self' 'unsafe-inline' https://trusted-cdn.com;
            style-src 'self' 'unsafe-inline';
            img-src 'self' data: https:;
            connect-src 'self' https://api.example.com;
            font-src 'self' https://fonts.googleapis.com;
            object-src 'none';
            base-uri 'self';
            form-action 'self';
            frame-ancestors 'none';
            upgrade-insecure-requests;
        `.replace(/\s+/g, ' ').trim();
        document.head.appendChild(cspMeta);
        
        // X-Frame-Options
        const frameMeta = document.createElement('meta');
        frameMeta.httpEquiv = 'X-Frame-Options';
        frameMeta.content = 'DENY';
        document.head.appendChild(frameMeta);
        
        // X-Content-Type-Options
        const contentTypeMeta = document.createElement('meta');
        contentTypeMeta.httpEquiv = 'X-Content-Type-Options';
        contentTypeMeta.content = 'nosniff';
        document.head.appendChild(contentTypeMeta);
    }
    
    // Secure cookie settings
    static setSecureCookie(name, value, options = {}) {
        const {
            maxAge = 86400, // 1 day
            secure = true,
            httpOnly = false, // Can't be set from JavaScript
            sameSite = 'Strict',
            path = '/'
        } = options;
        
        let cookieString = `${name}=${encodeURIComponent(value)}`;
        cookieString += `; Max-Age=${maxAge}`;
        cookieString += `; Path=${path}`;
        cookieString += `; SameSite=${sameSite}`;
        
        if (secure) {
            cookieString += '; Secure';
        }
        
        // Note: HttpOnly can only be set server-side
        document.cookie = cookieString;
    }
    
    // CSRF token management
    static getCSRFToken() {
        const meta = document.querySelector('meta[name="csrf-token"]');
        return meta ? meta.getAttribute('content') : null;
    }
    
    static addCSRFToken(formData) {
        const token = this.getCSRFToken();
        if (token) {
            formData.append('_token', token);
        }
        return formData;
    }
    
    // Secure random number generation
    static generateSecureRandom(length = 32) {
        const array = new Uint8Array(length);
        crypto.getRandomValues(array);
        return Array.from(array, byte => byte.toString(16).padStart(2, '0')).join('');
    }
    
    // Rate limiting (client-side)
    static createRateLimiter(maxRequests, timeWindow) {
        const requests = [];
        
        return function rateLimiter() {
            const now = Date.now();
            
            // Remove old requests outside time window
            while (requests.length > 0 && requests[0] < now - timeWindow) {
                requests.shift();
            }
            
            // Check if limit exceeded
            if (requests.length >= maxRequests) {
                throw new Error('Rate limit exceeded');
            }
            
            // Add current request
            requests.push(now);
            return true;
        };
    }
}

// Usage
SecurityConfig.setSecurityHeaders();

// Rate limiting example
const apiRateLimiter = SecurityConfig.createRateLimiter(10, 60000); // 10 requests per minute

async function makeAPICall(url, data) {
    try {
        apiRateLimiter(); // Check rate limit
        
        const formData = new FormData();
        Object.entries(data).forEach(([key, value]) => {
            formData.append(key, value);
        });
        
        // Add CSRF token
        SecurityConfig.addCSRFToken(formData);
        
        const response = await fetch(url, {
            method: 'POST',
            body: formData,
            headers: {
                'X-Requested-With': 'XMLHttpRequest'
            }
        });
        
        return response;
    } catch (error) {
        console.error('API call failed:', error);
        throw error;
    }
}
```

### 🎯 Key Points
- Always validate and sanitize user input
- Use Content Security Policy (CSP) to prevent XSS
- Implement proper authentication and authorization
- Encrypt sensitive data before storage
- Use secure communication (HTTPS)
- Implement rate limiting and CSRF protection
- Follow principle of least privilege
- Keep dependencies updated and scan for vulnerabilities

### 💡 Interview Questions (Hinglish)

**Q1: XSS attack kya hai aur kaise prevent karte hain?**

**A:**
XSS (Cross-Site Scripting) malicious script inject karna hai:
```javascript
// ❌ Vulnerable
element.innerHTML = userInput; // Can execute scripts

// ✅ Safe
element.textContent = userInput; // No script execution
// Or escape HTML
const safe = userInput.replace(/</g, '&lt;').replace(/>/g, '&gt;');
```

**Q2: Secure authentication kaise implement karte hain?**

**A:**
```javascript
// JWT tokens with refresh mechanism
// Hash passwords before sending
const hashedPassword = await crypto.subtle.digest('SHA-256', password);

// Store tokens securely
sessionStorage.setItem('accessToken', token); // Short-lived
localStorage.setItem('refreshToken', refreshToken); // Long-lived

// Add authorization headers
headers: { 'Authorization': `Bearer ${token}` }
```

**Q3: Client-side data encryption kaise karte hain?**

**A:**
```javascript
// Use Web Crypto API
const key = await crypto.subtle.generateKey(
    { name: 'AES-GCM', length: 256 },
    false,
    ['encrypt', 'decrypt']
);

const encrypted = await crypto.subtle.encrypt(
    { name: 'AES-GCM', iv: iv },
    key,
    data
);
```

---## Day 2
7: Week 4 Review and Advanced Projects

### Week 4 Summary

This week we explored advanced JavaScript concepts and professional development practices:

**Day 22: Advanced Object-Oriented Programming**
- Prototypes and prototype chain
- Advanced inheritance patterns (mixins, composition)
- Private fields and abstract classes
- Decorator pattern implementation

**Day 23: Design Patterns**
- Creational patterns (Singleton, Factory, Builder)
- Structural patterns (Adapter, Decorator)
- Behavioral patterns (Observer, Strategy)
- Real-world pattern applications

**Day 24: Performance Optimization**
- Memory management and leak prevention
- Algorithm optimization and memoization
- DOM performance and virtual scrolling
- Asynchronous performance patterns

**Day 25: Testing and Debugging**
- Unit and integration testing
- Test-driven development (TDD)
- Mocking and stubbing techniques
- Advanced debugging strategies

**Day 26: Security Best Practices**
- XSS and injection prevention
- Secure authentication and authorization
- Data encryption and privacy protection
- Security headers and configuration

### Advanced Project: Enterprise Task Management System

Let's build a comprehensive task management system that incorporates all the concepts from Week 4:

```javascript
// models/Task.js - Advanced Task Model with Security
class Task {
    #id;
    #createdBy;
    #assignedTo;
    #encryptedData;
    
    constructor(data, createdBy) {
        this.#id = this.generateSecureId();
        this.#createdBy = createdBy;
        this.#assignedTo = data.assignedTo || createdBy;
        
        // Public properties
        this.title = this.sanitizeInput(data.title);
        this.description = this.sanitizeInput(data.description);
        this.priority = this.validatePriority(data.priority);
        this.status = 'pending';
        this.tags = this.sanitizeTags(data.tags || []);
        this.dueDate = data.dueDate ? new Date(data.dueDate) : null;
        this.createdAt = new Date();
        this.updatedAt = new Date();
        this.version = 1;
        
        // Audit trail
        this.auditLog = [{
            action: 'created',
            userId: createdBy,
            timestamp: this.createdAt,
            changes: { status: 'pending' }
        }];
    }
    
    // Private methods
    generateSecureId() {
        const array = new Uint8Array(16);
        crypto.getRandomValues(array);
        return Array.from(array, byte => byte.toString(16).padStart(2, '0')).join('');
    }
    
    sanitizeInput(input) {
        if (typeof input !== 'string') return '';
        return input
            .trim()
            .replace(/[<>]/g, '')
            .substring(0, 1000); // Limit length
    }
    
    validatePriority(priority) {
        const validPriorities = ['low', 'medium', 'high', 'critical'];
        return validPriorities.includes(priority) ? priority : 'medium';
    }
    
    sanitizeTags(tags) {
        return tags
            .filter(tag => typeof tag === 'string')
            .map(tag => tag.trim().toLowerCase())
            .filter(tag => tag.length > 0 && tag.length <= 50)
            .slice(0, 10); // Limit number of tags
    }
    
    // Public methods
    getId() {
        return this.#id;
    }
    
    getCreatedBy() {
        return this.#createdBy;
    }
    
    getAssignedTo() {
        return this.#assignedTo;
    }
    
    update(changes, userId) {
        if (!this.canEdit(userId)) {
            throw new Error('Unauthorized: Cannot edit this task');
        }
        
        const oldValues = {};
        const newValues = {};
        
        // Track changes for audit
        Object.keys(changes).forEach(key => {
            if (this.hasOwnProperty(key) && this[key] !== changes[key]) {
                oldValues[key] = this[key];
                newValues[key] = changes[key];
                
                // Apply sanitization based on field
                switch (key) {
                    case 'title':
                    case 'description':
                        this[key] = this.sanitizeInput(changes[key]);
                        break;
                    case 'priority':
                        this[key] = this.validatePriority(changes[key]);
                        break;
                    case 'tags':
                        this[key] = this.sanitizeTags(changes[key]);
                        break;
                    case 'status':
                        this[key] = this.validateStatus(changes[key]);
                        break;
                    default:
                        this[key] = changes[key];
                }
            }
        });
        
        if (Object.keys(newValues).length > 0) {
            this.updatedAt = new Date();
            this.version++;
            
            // Add to audit log
            this.auditLog.push({
                action: 'updated',
                userId,
                timestamp: this.updatedAt,
                changes: newValues,
                oldValues
            });
        }
        
        return this;
    }
    
    validateStatus(status) {
        const validStatuses = ['pending', 'in-progress', 'completed', 'cancelled'];
        return validStatuses.includes(status) ? status : this.status;
    }
    
    canEdit(userId) {
        return userId === this.#createdBy || userId === this.#assignedTo;
    }
    
    canView(userId) {
        // For now, anyone can view. In real app, check permissions
        return true;
    }
    
    assign(newAssignee, userId) {
        if (!this.canEdit(userId)) {
            throw new Error('Unauthorized: Cannot assign this task');
        }
        
        const oldAssignee = this.#assignedTo;
        this.#assignedTo = newAssignee;
        this.updatedAt = new Date();
        this.version++;
        
        this.auditLog.push({
            action: 'assigned',
            userId,
            timestamp: this.updatedAt,
            changes: { assignedTo: newAssignee },
            oldValues: { assignedTo: oldAssignee }
        });
        
        return this;
    }
    
    complete(userId) {
        return this.update({ status: 'completed' }, userId);
    }
    
    isOverdue() {
        return this.dueDate && new Date() > this.dueDate && this.status !== 'completed';
    }
    
    getDaysUntilDue() {
        if (!this.dueDate) return null;
        const diffTime = this.dueDate - new Date();
        return Math.ceil(diffTime / (1000 * 60 * 60 * 24));
    }
    
    // Serialization with security
    toJSON(userId) {
        if (!this.canView(userId)) {
            throw new Error('Unauthorized: Cannot view this task');
        }
        
        return {
            id: this.#id,
            title: this.title,
            description: this.description,
            priority: this.priority,
            status: this.status,
            tags: [...this.tags],
            dueDate: this.dueDate?.toISOString(),
            createdAt: this.createdAt.toISOString(),
            updatedAt: this.updatedAt.toISOString(),
            createdBy: this.#createdBy,
            assignedTo: this.#assignedTo,
            version: this.version,
            isOverdue: this.isOverdue(),
            daysUntilDue: this.getDaysUntilDue()
        };
    }
    
    // Factory method
    static fromJSON(data, userId) {
        const task = Object.create(Task.prototype);
        task.#id = data.id;
        task.#createdBy = data.createdBy;
        task.#assignedTo = data.assignedTo;
        
        Object.assign(task, {
            title: data.title,
            description: data.description,
            priority: data.priority,
            status: data.status,
            tags: data.tags,
            dueDate: data.dueDate ? new Date(data.dueDate) : null,
            createdAt: new Date(data.createdAt),
            updatedAt: new Date(data.updatedAt),
            version: data.version,
            auditLog: data.auditLog || []
        });
        
        return task;
    }
}
```

```javascript
// services/TaskService.js - Service with Design Patterns
class TaskService {
    constructor() {
        this.tasks = new Map();
        this.observers = new Set();
        this.cache = new Map();
        this.rateLimiter = this.createRateLimiter(100, 60000); // 100 ops per minute
        this.encryptionKey = null;
        
        this.loadTasks();
    }
    
    // Singleton pattern
    static getInstance() {
        if (!TaskService.instance) {
            TaskService.instance = new TaskService();
        }
        return TaskService.instance;
    }
    
    // Observer pattern
    subscribe(observer) {
        this.observers.add(observer);
        return () => this.observers.delete(observer);
    }
    
    notify(event, data) {
        this.observers.forEach(observer => {
            try {
                observer(event, data);
            } catch (error) {
                console.error('Observer error:', error);
            }
        });
    }
    
    // Rate limiting
    createRateLimiter(maxOps, timeWindow) {
        const operations = [];
        
        return () => {
            const now = Date.now();
            
            // Remove old operations
            while (operations.length > 0 && operations[0] < now - timeWindow) {
                operations.shift();
            }
            
            if (operations.length >= maxOps) {
                throw new Error('Rate limit exceeded');
            }
            
            operations.push(now);
        };
    }
    
    // Memoized search
    search = this.memoize((query, filters = {}) => {
        const tasks = Array.from(this.tasks.values());
        
        return tasks.filter(task => {
            // Text search
            if (query) {
                const searchText = `${task.title} ${task.description} ${task.tags.join(' ')}`.toLowerCase();
                if (!searchText.includes(query.toLowerCase())) {
                    return false;
                }
            }
            
            // Filters
            if (filters.status && task.status !== filters.status) return false;
            if (filters.priority && task.priority !== filters.priority) return false;
            if (filters.assignedTo && task.getAssignedTo() !== filters.assignedTo) return false;
            if (filters.createdBy && task.getCreatedBy() !== filters.createdBy) return false;
            if (filters.overdue && !task.isOverdue()) return false;
            
            return true;
        });
    });
    
    memoize(fn, keyGenerator = (...args) => JSON.stringify(args)) {
        const cache = new Map();
        
        return (...args) => {
            const key = keyGenerator(...args);
            
            if (cache.has(key)) {
                return cache.get(key);
            }
            
            const result = fn.apply(this, args);
            cache.set(key, result);
            
            // Clear cache after 5 minutes
            setTimeout(() => cache.delete(key), 300000);
            
            return result;
        };
    }
    
    // CRUD operations with security
    async createTask(taskData, userId) {
        this.rateLimiter();
        
        if (!userId) {
            throw new Error('Authentication required');
        }
        
        const task = new Task(taskData, userId);
        this.tasks.set(task.getId(), task);
        
        await this.saveTasks();
        this.notify('taskCreated', { task: task.toJSON(userId), userId });
        
        return task;
    }
    
    async getTask(taskId, userId) {
        const task = this.tasks.get(taskId);
        
        if (!task) {
            throw new Error('Task not found');
        }
        
        if (!task.canView(userId)) {
            throw new Error('Unauthorized');
        }
        
        return task;
    }
    
    async updateTask(taskId, changes, userId) {
        this.rateLimiter();
        
        const task = await this.getTask(taskId, userId);
        const oldData = task.toJSON(userId);
        
        task.update(changes, userId);
        
        await this.saveTasks();
        this.notify('taskUpdated', { 
            task: task.toJSON(userId), 
            oldData, 
            userId 
        });
        
        return task;
    }
    
    async deleteTask(taskId, userId) {
        this.rateLimiter();
        
        const task = await this.getTask(taskId, userId);
        
        if (!task.canEdit(userId)) {
            throw new Error('Unauthorized');
        }
        
        this.tasks.delete(taskId);
        
        await this.saveTasks();
        this.notify('taskDeleted', { taskId, userId });
        
        return true;
    }
    
    async getTasks(userId, filters = {}) {
        const tasks = Array.from(this.tasks.values())
            .filter(task => task.canView(userId))
            .map(task => task.toJSON(userId));
        
        // Apply filters
        return tasks.filter(task => {
            if (filters.status && task.status !== filters.status) return false;
            if (filters.priority && task.priority !== filters.priority) return false;
            if (filters.assignedTo && task.assignedTo !== filters.assignedTo) return false;
            return true;
        });
    }
    
    // Analytics
    getAnalytics(userId) {
        const tasks = Array.from(this.tasks.values())
            .filter(task => task.canView(userId));
        
        const analytics = {
            total: tasks.length,
            byStatus: {},
            byPriority: {},
            overdue: 0,
            completedThisWeek: 0,
            averageCompletionTime: 0
        };
        
        const weekAgo = new Date(Date.now() - 7 * 24 * 60 * 60 * 1000);
        let completionTimes = [];
        
        tasks.forEach(task => {
            // Status distribution
            analytics.byStatus[task.status] = (analytics.byStatus[task.status] || 0) + 1;
            
            // Priority distribution
            analytics.byPriority[task.priority] = (analytics.byPriority[task.priority] || 0) + 1;
            
            // Overdue tasks
            if (task.isOverdue()) {
                analytics.overdue++;
            }
            
            // Completed this week
            if (task.status === 'completed' && task.updatedAt > weekAgo) {
                analytics.completedThisWeek++;
                
                // Calculate completion time
                const completionTime = task.updatedAt - task.createdAt;
                completionTimes.push(completionTime);
            }
        });
        
        // Average completion time
        if (completionTimes.length > 0) {
            const avgMs = completionTimes.reduce((a, b) => a + b, 0) / completionTimes.length;
            analytics.averageCompletionTime = Math.round(avgMs / (1000 * 60 * 60 * 24)); // Days
        }
        
        return analytics;
    }
    
    // Persistence with encryption
    async saveTasks() {
        try {
            const tasksData = Array.from(this.tasks.entries()).map(([id, task]) => [
                id,
                task.toJSON(task.getCreatedBy()) // Use creator's permissions for serialization
            ]);
            
            const dataToSave = {
                tasks: tasksData,
                timestamp: new Date().toISOString(),
                version: '1.0'
            };
            
            // In a real app, encrypt sensitive data
            localStorage.setItem('tasks', JSON.stringify(dataToSave));
        } catch (error) {
            console.error('Failed to save tasks:', error);
            throw new Error('Failed to save tasks');
        }
    }
    
    loadTasks() {
        try {
            const saved = localStorage.getItem('tasks');
            if (!saved) return;
            
            const data = JSON.parse(saved);
            
            if (data.tasks) {
                data.tasks.forEach(([id, taskData]) => {
                    const task = Task.fromJSON(taskData, taskData.createdBy);
                    this.tasks.set(id, task);
                });
            }
        } catch (error) {
            console.error('Failed to load tasks:', error);
        }
    }
    
    // Bulk operations
    async bulkUpdate(taskIds, changes, userId) {
        const results = [];
        
        for (const taskId of taskIds) {
            try {
                const task = await this.updateTask(taskId, changes, userId);
                results.push({ taskId, success: true, task: task.toJSON(userId) });
            } catch (error) {
                results.push({ taskId, success: false, error: error.message });
            }
        }
        
        return results;
    }
    
    async exportTasks(userId, format = 'json') {
        const tasks = await this.getTasks(userId);
        
        switch (format) {
            case 'json':
                return JSON.stringify(tasks, null, 2);
            
            case 'csv':
                const headers = ['ID', 'Title', 'Description', 'Status', 'Priority', 'Due Date', 'Created'];
                const rows = tasks.map(task => [
                    task.id,
                    task.title,
                    task.description,
                    task.status,
                    task.priority,
                    task.dueDate || '',
                    task.createdAt
                ]);
                
                return [headers, ...rows].map(row => 
                    row.map(cell => `"${cell}"`).join(',')
                ).join('\n');
            
            default:
                throw new Error('Unsupported export format');
        }
    }
}
```

```javascript
// components/TaskManager.js - Advanced UI Component
class TaskManager {
    constructor(containerId, userId) {
        this.container = document.getElementById(containerId);
        this.userId = userId;
        this.taskService = TaskService.getInstance();
        this.currentFilter = {};
        this.sortBy = 'createdAt';
        this.sortOrder = 'desc';
        
        this.init();
    }
    
    init() {
        this.setupEventListeners();
        this.setupSubscriptions();
        this.render();
        this.loadAnalytics();
    }
    
    setupEventListeners() {
        // Debounced search
        const searchInput = this.container.querySelector('#search');
        if (searchInput) {
            const debouncedSearch = this.debounce((e) => {
                this.handleSearch(e.target.value);
            }, 300);
            
            searchInput.addEventListener('input', debouncedSearch);
        }
        
        // Event delegation for task actions
        this.container.addEventListener('click', (e) => {
            const action = e.target.dataset.action;
            const taskId = e.target.dataset.taskId;
            
            switch (action) {
                case 'complete':
                    this.completeTask(taskId);
                    break;
                case 'edit':
                    this.editTask(taskId);
                    break;
                case 'delete':
                    this.deleteTask(taskId);
                    break;
                case 'assign':
                    this.assignTask(taskId);
                    break;
            }
        });
        
        // Form submission
        const taskForm = this.container.querySelector('#task-form');
        if (taskForm) {
            taskForm.addEventListener('submit', (e) => {
                e.preventDefault();
                this.handleTaskSubmission(e);
            });
        }
        
        // Filter changes
        this.container.addEventListener('change', (e) => {
            if (e.target.matches('[data-filter]')) {
                this.handleFilterChange(e.target.dataset.filter, e.target.value);
            }
        });
        
        // Keyboard shortcuts
        document.addEventListener('keydown', (e) => {
            if (e.ctrlKey || e.metaKey) {
                switch (e.key) {
                    case 'n':
                        e.preventDefault();
                        this.showCreateTaskModal();
                        break;
                    case 'f':
                        e.preventDefault();
                        searchInput?.focus();
                        break;
                }
            }
        });
    }
    
    setupSubscriptions() {
        this.taskService.subscribe((event, data) => {
            switch (event) {
                case 'taskCreated':
                case 'taskUpdated':
                case 'taskDeleted':
                    this.render();
                    this.loadAnalytics();
                    this.showNotification(`Task ${event.replace('task', '').toLowerCase()}`, 'success');
                    break;
            }
        });
    }
    
    debounce(func, delay) {
        let timeoutId;
        return (...args) => {
            clearTimeout(timeoutId);
            timeoutId = setTimeout(() => func.apply(this, args), delay);
        };
    }
    
    async handleSearch(query) {
        try {
            const results = this.taskService.search(query, this.currentFilter);
            this.renderTasks(results);
        } catch (error) {
            this.showNotification('Search failed: ' + error.message, 'error');
        }
    }
    
    async handleTaskSubmission(e) {
        const formData = new FormData(e.target);
        const taskData = {
            title: formData.get('title'),
            description: formData.get('description'),
            priority: formData.get('priority'),
            dueDate: formData.get('dueDate'),
            tags: formData.get('tags')?.split(',').map(tag => tag.trim()) || []
        };
        
        try {
            await this.taskService.createTask(taskData, this.userId);
            e.target.reset();
            this.hideCreateTaskModal();
        } catch (error) {
            this.showNotification('Failed to create task: ' + error.message, 'error');
        }
    }
    
    async completeTask(taskId) {
        try {
            await this.taskService.updateTask(taskId, { status: 'completed' }, this.userId);
        } catch (error) {
            this.showNotification('Failed to complete task: ' + error.message, 'error');
        }
    }
    
    async deleteTask(taskId) {
        if (!confirm('Are you sure you want to delete this task?')) return;
        
        try {
            await this.taskService.deleteTask(taskId, this.userId);
        } catch (error) {
            this.showNotification('Failed to delete task: ' + error.message, 'error');
        }
    }
    
    async render() {
        try {
            const tasks = await this.taskService.getTasks(this.userId, this.currentFilter);
            this.renderTasks(tasks);
        } catch (error) {
            this.showNotification('Failed to load tasks: ' + error.message, 'error');
        }
    }
    
    renderTasks(tasks) {
        const tasksContainer = this.container.querySelector('#tasks-container');
        if (!tasksContainer) return;
        
        if (tasks.length === 0) {
            tasksContainer.innerHTML = `
                <div class="empty-state">
                    <h3>No tasks found</h3>
                    <p>Create your first task to get started!</p>
                    <button onclick="this.showCreateTaskModal()" class="btn btn-primary">
                        Create Task
                    </button>
                </div>
            `;
            return;
        }
        
        // Sort tasks
        const sortedTasks = this.sortTasks(tasks);
        
        tasksContainer.innerHTML = sortedTasks.map(task => `
            <div class="task-card ${task.status} ${task.priority}" data-task-id="${task.id}">
                <div class="task-header">
                    <h3 class="task-title">${this.escapeHtml(task.title)}</h3>
                    <div class="task-actions">
                        ${task.status !== 'completed' ? `
                            <button data-action="complete" data-task-id="${task.id}" 
                                    class="btn btn-sm btn-success" title="Complete">
                                ✓
                            </button>
                        ` : ''}
                        <button data-action="edit" data-task-id="${task.id}" 
                                class="btn btn-sm btn-secondary" title="Edit">
                            ✏️
                        </button>
                        <button data-action="delete" data-task-id="${task.id}" 
                                class="btn btn-sm btn-danger" title="Delete">
                            🗑️
                        </button>
                    </div>
                </div>
                
                <div class="task-body">
                    <p class="task-description">${this.escapeHtml(task.description)}</p>
                    
                    <div class="task-meta">
                        <span class="priority priority-${task.priority}">${task.priority}</span>
                        <span class="status status-${task.status}">${task.status}</span>
                        
                        ${task.dueDate ? `
                            <span class="due-date ${task.isOverdue ? 'overdue' : ''}">
                                Due: ${new Date(task.dueDate).toLocaleDateString()}
                                ${task.isOverdue ? '(Overdue)' : ''}
                            </span>
                        ` : ''}
                    </div>
                    
                    ${task.tags.length > 0 ? `
                        <div class="task-tags">
                            ${task.tags.map(tag => `<span class="tag">#${tag}</span>`).join('')}
                        </div>
                    ` : ''}
                </div>
                
                <div class="task-footer">
                    <small class="text-muted">
                        Created: ${new Date(task.createdAt).toLocaleDateString()}
                        ${task.createdAt !== task.updatedAt ? 
                            `• Updated: ${new Date(task.updatedAt).toLocaleDateString()}` : ''
                        }
                    </small>
                </div>
            </div>
        `).join('');
    }
    
    sortTasks(tasks) {
        return tasks.sort((a, b) => {
            let aValue = a[this.sortBy];
            let bValue = b[this.sortBy];
            
            // Handle dates
            if (this.sortBy.includes('At') || this.sortBy === 'dueDate') {
                aValue = new Date(aValue);
                bValue = new Date(bValue);
            }
            
            // Handle priority
            if (this.sortBy === 'priority') {
                const priorityOrder = { low: 1, medium: 2, high: 3, critical: 4 };
                aValue = priorityOrder[aValue];
                bValue = priorityOrder[bValue];
            }
            
            if (this.sortOrder === 'asc') {
                return aValue > bValue ? 1 : -1;
            } else {
                return aValue < bValue ? 1 : -1;
            }
        });
    }
    
    async loadAnalytics() {
        try {
            const analytics = this.taskService.getAnalytics(this.userId);
            this.renderAnalytics(analytics);
        } catch (error) {
            console.error('Failed to load analytics:', error);
        }
    }
    
    renderAnalytics(analytics) {
        const analyticsContainer = this.container.querySelector('#analytics');
        if (!analyticsContainer) return;
        
        analyticsContainer.innerHTML = `
            <div class="analytics-grid">
                <div class="metric-card">
                    <h4>Total Tasks</h4>
                    <div class="metric-value">${analytics.total}</div>
                </div>
                
                <div class="metric-card">
                    <h4>Completed This Week</h4>
                    <div class="metric-value">${analytics.completedThisWeek}</div>
                </div>
                
                <div class="metric-card ${analytics.overdue > 0 ? 'warning' : ''}">
                    <h4>Overdue</h4>
                    <div class="metric-value">${analytics.overdue}</div>
                </div>
                
                <div class="metric-card">
                    <h4>Avg. Completion Time</h4>
                    <div class="metric-value">${analytics.averageCompletionTime} days</div>
                </div>
            </div>
            
            <div class="charts-container">
                <div class="chart">
                    <h5>By Status</h5>
                    ${this.renderChart(analytics.byStatus)}
                </div>
                
                <div class="chart">
                    <h5>By Priority</h5>
                    ${this.renderChart(analytics.byPriority)}
                </div>
            </div>
        `;
    }
    
    renderChart(data) {
        const total = Object.values(data).reduce((sum, count) => sum + count, 0);
        
        return `
            <div class="simple-chart">
                ${Object.entries(data).map(([key, count]) => {
                    const percentage = total > 0 ? (count / total * 100).toFixed(1) : 0;
                    return `
                        <div class="chart-item">
                            <span class="chart-label">${key}</span>
                            <div class="chart-bar">
                                <div class="chart-fill" style="width: ${percentage}%"></div>
                            </div>
                            <span class="chart-value">${count} (${percentage}%)</span>
                        </div>
                    `;
                }).join('')}
            </div>
        `;
    }
    
    escapeHtml(text) {
        const div = document.createElement('div');
        div.textContent = text;
        return div.innerHTML;
    }
    
    showNotification(message, type = 'info') {
        const notification = document.createElement('div');
        notification.className = `notification notification-${type}`;
        notification.textContent = message;
        
        document.body.appendChild(notification);
        
        setTimeout(() => {
            notification.remove();
        }, 3000);
    }
    
    showCreateTaskModal() {
        // Implementation for modal
        console.log('Show create task modal');
    }
    
    hideCreateTaskModal() {
        // Implementation for modal
        console.log('Hide create task modal');
    }
}

// Initialize the application
document.addEventListener('DOMContentLoaded', () => {
    // In a real app, get user ID from authentication
    const userId = 'user-123';
    const taskManager = new TaskManager('task-manager-container', userId);
});
```

### Performance Testing and Optimization

```javascript
// performance/PerformanceTest.js
class PerformanceTest {
    static async runTaskServiceBenchmarks() {
        const taskService = TaskService.getInstance();
        const userId = 'test-user';
        
        console.log('🚀 Running Task Service Performance Tests...\n');
        
        // Test 1: Task Creation Performance
        console.time('Create 1000 tasks');
        const taskIds = [];
        
        for (let i = 0; i < 1000; i++) {
            const task = await taskService.createTask({
                title: `Task ${i}`,
                description: `Description for task ${i}`,
                priority: ['low', 'medium', 'high'][i % 3],
                tags: [`tag${i % 10}`, `category${i % 5}`]
            }, userId);
            
            taskIds.push(task.getId());
        }
        
        console.timeEnd('Create 1000 tasks');
        
        // Test 2: Search Performance
        console.time('Search in 1000 tasks');
        const searchResults = taskService.search('Task', { priority: 'high' });
        console.timeEnd('Search in 1000 tasks');
        console.log(`Found ${searchResults.length} results\n`);
        
        // Test 3: Bulk Update Performance
        console.time('Bulk update 100 tasks');
        const bulkResults = await taskService.bulkUpdate(
            taskIds.slice(0, 100),
            { status: 'completed' },
            userId
        );
        console.timeEnd('Bulk update 100 tasks');
        console.log(`Updated ${bulkResults.filter(r => r.success).length} tasks\n`);
        
        // Test 4: Analytics Performance
        console.time('Generate analytics');
        const analytics = taskService.getAnalytics(userId);
        console.timeEnd('Generate analytics');
        console.log('Analytics:', analytics, '\n');
        
        // Test 5: Memory Usage
        const memoryBefore = performance.memory?.usedJSHeapSize || 0;
        
        // Create and destroy many tasks
        for (let i = 0; i < 500; i++) {
            const task = await taskService.createTask({
                title: `Temp Task ${i}`,
                description: 'Temporary task for memory test'
            }, userId);
            
            await taskService.deleteTask(task.getId(), userId);
        }
        
        const memoryAfter = performance.memory?.usedJSHeapSize || 0;
        console.log(`Memory usage change: ${((memoryAfter - memoryBefore) / 1024 / 1024).toFixed(2)} MB\n`);
        
        // Cleanup
        for (const taskId of taskIds) {
            try {
                await taskService.deleteTask(taskId, userId);
            } catch (error) {
                // Task might already be deleted
            }
        }
        
        console.log('✅ Performance tests completed!');
    }
    
    static measureRenderPerformance() {
        const container = document.createElement('div');
        container.id = 'test-container';
        document.body.appendChild(container);
        
        // Create test data
        const tasks = Array.from({ length: 1000 }, (_, i) => ({
            id: `task-${i}`,
            title: `Task ${i}`,
            description: `Description for task ${i}`,
            status: ['pending', 'in-progress', 'completed'][i % 3],
            priority: ['low', 'medium', 'high'][i % 3],
            createdAt: new Date().toISOString(),
            updatedAt: new Date().toISOString(),
            tags: [`tag${i % 10}`],
            isOverdue: i % 10 === 0
        }));
        
        console.time('Render 1000 tasks');
        
        // Simulate task rendering
        const html = tasks.map(task => `
            <div class="task-card ${task.status} ${task.priority}">
                <h3>${task.title}</h3>
                <p>${task.description}</p>
                <span class="status">${task.status}</span>
                <span class="priority">${task.priority}</span>
            </div>
        `).join('');
        
        container.innerHTML = html;
        
        console.timeEnd('Render 1000 tasks');
        
        // Cleanup
        container.remove();
    }
}

// Run performance tests
// PerformanceTest.runTaskServiceBenchmarks();
// PerformanceTest.measureRenderPerformance();
```

### 🎯 Week 4 Key Achievements
- Implemented advanced OOP patterns with security
- Applied multiple design patterns in a cohesive system
- Optimized performance with memoization and rate limiting
- Built comprehensive testing and debugging capabilities
- Integrated security best practices throughout
- Created a production-ready enterprise application

### 💡 Week 4 Advanced Interview Questions (Hinglish)

**Q1: Design patterns ka real-world application mein kaise use karte hain?**

**A:**
Multiple patterns combine karke robust system banate hain:
```javascript
// Singleton for service
const taskService = TaskService.getInstance();

// Observer for real-time updates
taskService.subscribe((event, data) => updateUI(data));

// Factory for creating different task types
const task = TaskFactory.createTask(type, data);

// Strategy for different notification methods
notificationService.setStrategy(new EmailStrategy());
```

**Q2: Performance optimization ke main techniques kya hain?**

**A:**
- Memoization: Expensive calculations cache karna
- Debouncing/Throttling: Frequent operations limit karna
- Virtual scrolling: Large lists efficiently render karna
- Lazy loading: On-demand resource loading
- Memory management: References properly clean karna

**Q3: Enterprise-level security considerations kya hain?**

**A:**
```javascript
// Input validation and sanitization
const sanitized = SecurityUtils.escapeHtml(userInput);

// Authentication with JWT tokens
const token = await auth.getSecureToken();

// Data encryption for sensitive information
const encrypted = await DataProtection.encryptData(data, key);

// Rate limiting and CSRF protection
rateLimiter.check();
headers['X-CSRF-Token'] = getCSRFToken();
```

---#
 Week 5: Modern Development and Project Work {#week-5}

## Day 28: Modern JavaScript Ecosystem and Tools

### Package Management with npm/yarn

**Understanding Package Managers:**
```json
// package.json - Project configuration
{
  "name": "my-javascript-project",
  "version": "1.0.0",
  "description": "A modern JavaScript application",
  "main": "src/index.js",
  "type": "module",
  "scripts": {
    "start": "node src/index.js",
    "dev": "nodemon src/index.js",
    "build": "webpack --mode production",
    "test": "jest",
    "lint": "eslint src/",
    "format": "prettier --write src/"
  },
  "dependencies": {
    "lodash": "^4.17.21",
    "axios": "^1.6.0",
    "date-fns": "^2.30.0"
  },
  "devDependencies": {
    "webpack": "^5.89.0",
    "babel-loader": "^9.1.3",
    "@babel/core": "^7.23.0",
    "@babel/preset-env": "^7.23.0",
    "eslint": "^8.54.0",
    "prettier": "^3.1.0",
    "jest": "^29.7.0",
    "nodemon": "^3.0.1"
  },
  "engines": {
    "node": ">=18.0.0"
  }
}
```

**Essential npm Commands:**
```bash
# Initialize new project
npm init -y

# Install dependencies
npm install lodash axios
npm install --save-dev webpack babel-loader

# Install globally
npm install -g nodemon

# Update packages
npm update
npm outdated

# Security audit
npm audit
npm audit fix

# Clean install
npm ci

# Run scripts
npm start
npm run build
npm test
```

### Build Tools and Bundlers

#### Webpack Configuration
```javascript
// webpack.config.js
const path = require('path');
const HtmlWebpackPlugin = require('html-webpack-plugin');
const MiniCssExtractPlugin = require('mini-css-extract-plugin');

module.exports = {
  entry: './src/index.js',
  
  output: {
    path: path.resolve(__dirname, 'dist'),
    filename: '[name].[contenthash].js',
    clean: true
  },
  
  module: {
    rules: [
      {
        test: /\.js$/,
        exclude: /node_modules/,
        use: {
          loader: 'babel-loader',
          options: {
            presets: ['@babel/preset-env']
          }
        }
      },
      {
        test: /\.css$/,
        use: [MiniCssExtractPlugin.loader, 'css-loader']
      },
      {
        test: /\.(png|svg|jpg|jpeg|gif)$/i,
        type: 'asset/resource'
      }
    ]
  },
  
  plugins: [
    new HtmlWebpackPlugin({
      template: './src/index.html'
    }),
    new MiniCssExtractPlugin({
      filename: '[name].[contenthash].css'
    })
  ],
  
  optimization: {
    splitChunks: {
      chunks: 'all'
    }
  },
  
  devServer: {
    static: './dist',
    hot: true,
    port: 3000
  }
};
```

#### Babel Configuration
```javascript
// babel.config.js
module.exports = {
  presets: [
    ['@babel/preset-env', {
      targets: {
        browsers: ['> 1%', 'last 2 versions']
      },
      useBuiltIns: 'usage',
      corejs: 3
    }]
  ],
  plugins: [
    '@babel/plugin-proposal-class-properties',
    '@babel/plugin-proposal-optional-chaining',
    '@babel/plugin-proposal-nullish-coalescing-operator'
  ]
};
```

### Code Quality Tools

#### ESLint Configuration
```javascript
// .eslintrc.js
module.exports = {
  env: {
    browser: true,
    es2021: true,
    node: true,
    jest: true
  },
  extends: [
    'eslint:recommended',
    '@eslint/js/recommended'
  ],
  parserOptions: {
    ecmaVersion: 'latest',
    sourceType: 'module'
  },
  rules: {
    'no-unused-vars': 'error',
    'no-console': 'warn',
    'prefer-const': 'error',
    'no-var': 'error',
    'arrow-spacing': 'error',
    'object-curly-spacing': ['error', 'always'],
    'array-bracket-spacing': ['error', 'never'],
    'indent': ['error', 2],
    'quotes': ['error', 'single'],
    'semi': ['error', 'always'],
    'no-trailing-spaces': 'error',
    'eol-last': 'error'
  }
};
```

#### Prettier Configuration
```javascript
// .prettierrc.js
module.exports = {
  semi: true,
  trailingComma: 'es5',
  singleQuote: true,
  printWidth: 80,
  tabWidth: 2,
  useTabs: false,
  bracketSpacing: true,
  arrowParens: 'avoid',
  endOfLine: 'lf'
};
```

### Modern JavaScript Features

#### Top-Level Await
```javascript
// main.js - Using top-level await
import { fetchUserData } from './api.js';

// No need to wrap in async function
const userData = await fetchUserData('123');
console.log(userData);

// Dynamic imports with await
const { default: lodash } = await import('lodash');
const result = lodash.chunk([1, 2, 3, 4, 5, 6], 2);
```

#### Import Maps
```html
<!-- index.html -->
<script type="importmap">
{
  "imports": {
    "lodash": "https://cdn.skypack.dev/lodash",
    "date-fns": "https://cdn.skypack.dev/date-fns",
    "@/utils": "./src/utils/index.js",
    "@/components": "./src/components/index.js"
  }
}
</script>

<script type="module">
  import _ from 'lodash';
  import { format } from 'date-fns';
  import { helper } from '@/utils';
</script>
```

#### Private Class Fields and Methods
```javascript
class ModernClass {
  // Private fields
  #privateField = 'secret';
  #privateMethod() {
    return 'private method called';
  }
  
  // Static private
  static #staticPrivate = 'static secret';
  
  // Public method
  getPrivateData() {
    return this.#privateField + ' - ' + this.#privateMethod();
  }
  
  // Static method accessing static private
  static getStaticPrivate() {
    return this.#staticPrivate;
  }
}

const instance = new ModernClass();
console.log(instance.getPrivateData()); // Works
// console.log(instance.#privateField); // SyntaxError
```

### Development Workflow

#### Git Hooks with Husky
```json
// package.json
{
  "husky": {
    "hooks": {
      "pre-commit": "lint-staged",
      "pre-push": "npm test"
    }
  },
  "lint-staged": {
    "*.js": [
      "eslint --fix",
      "prettier --write",
      "git add"
    ]
  }
}
```

#### Environment Configuration
```javascript
// config/environment.js
const environments = {
  development: {
    API_URL: 'http://localhost:3001/api',
    DEBUG: true,
    LOG_LEVEL: 'debug'
  },
  
  production: {
    API_URL: 'https://api.myapp.com',
    DEBUG: false,
    LOG_LEVEL: 'error'
  },
  
  test: {
    API_URL: 'http://localhost:3002/api',
    DEBUG: false,
    LOG_LEVEL: 'silent'
  }
};

const env = process.env.NODE_ENV || 'development';
export default environments[env];
```

### Module Federation and Micro-frontends

```javascript
// webpack.config.js for Module Federation
const ModuleFederationPlugin = require('@module-federation/webpack');

module.exports = {
  plugins: [
    new ModuleFederationPlugin({
      name: 'shell',
      remotes: {
        userModule: 'userModule@http://localhost:3001/remoteEntry.js',
        taskModule: 'taskModule@http://localhost:3002/remoteEntry.js'
      }
    })
  ]
};

// Using federated modules
const UserComponent = React.lazy(() => import('userModule/UserComponent'));
const TaskComponent = React.lazy(() => import('taskModule/TaskComponent'));
```

### Performance Monitoring

```javascript
// performance/monitor.js
class PerformanceMonitor {
  constructor() {
    this.metrics = new Map();
    this.setupObservers();
  }
  
  setupObservers() {
    // Core Web Vitals
    this.observeLCP();
    this.observeFID();
    this.observeCLS();
    
    // Custom metrics
    this.observeCustomMetrics();
  }
  
  observeLCP() {
    new PerformanceObserver((entryList) => {
      const entries = entryList.getEntries();
      const lastEntry = entries[entries.length - 1];
      
      this.recordMetric('LCP', lastEntry.startTime);
      
      // Send to analytics
      this.sendToAnalytics('lcp', lastEntry.startTime);
    }).observe({ entryTypes: ['largest-contentful-paint'] });
  }
  
  observeFID() {
    new PerformanceObserver((entryList) => {
      entryList.getEntries().forEach(entry => {
        const fid = entry.processingStart - entry.startTime;
        this.recordMetric('FID', fid);
        this.sendToAnalytics('fid', fid);
      });
    }).observe({ entryTypes: ['first-input'] });
  }
  
  observeCLS() {
    let clsValue = 0;
    
    new PerformanceObserver((entryList) => {
      entryList.getEntries().forEach(entry => {
        if (!entry.hadRecentInput) {
          clsValue += entry.value;
        }
      });
      
      this.recordMetric('CLS', clsValue);
      this.sendToAnalytics('cls', clsValue);
    }).observe({ entryTypes: ['layout-shift'] });
  }
  
  observeCustomMetrics() {
    // Time to Interactive
    this.measureTTI();
    
    // Bundle size
    this.measureBundleSize();
    
    // API response times
    this.interceptFetch();
  }
  
  measureTTI() {
    // Simplified TTI measurement
    window.addEventListener('load', () => {
      setTimeout(() => {
        const tti = performance.now();
        this.recordMetric('TTI', tti);
        this.sendToAnalytics('tti', tti);
      }, 0);
    });
  }
  
  measureBundleSize() {
    if ('connection' in navigator) {
      const connection = navigator.connection;
      const bundleSize = performance.getEntriesByType('navigation')[0].transferSize;
      
      this.recordMetric('BundleSize', bundleSize);
      this.sendToAnalytics('bundle_size', bundleSize);
    }
  }
  
  interceptFetch() {
    const originalFetch = window.fetch;
    
    window.fetch = async (...args) => {
      const start = performance.now();
      
      try {
        const response = await originalFetch(...args);
        const duration = performance.now() - start;
        
        this.recordMetric('APIResponse', duration);
        this.sendToAnalytics('api_response_time', duration);
        
        return response;
      } catch (error) {
        const duration = performance.now() - start;
        this.sendToAnalytics('api_error', { duration, error: error.message });
        throw error;
      }
    };
  }
  
  recordMetric(name, value) {
    if (!this.metrics.has(name)) {
      this.metrics.set(name, []);
    }
    
    this.metrics.get(name).push({
      value,
      timestamp: Date.now()
    });
  }
  
  sendToAnalytics(metric, value) {
    // Send to your analytics service
    if (typeof gtag !== 'undefined') {
      gtag('event', 'performance_metric', {
        metric_name: metric,
        metric_value: value
      });
    }
    
    // Or send to custom endpoint
    fetch('/api/analytics', {
      method: 'POST',
      headers: { 'Content-Type': 'application/json' },
      body: JSON.stringify({ metric, value, timestamp: Date.now() })
    }).catch(console.error);
  }
  
  getReport() {
    const report = {};
    
    this.metrics.forEach((values, name) => {
      const nums = values.map(v => v.value);
      report[name] = {
        count: nums.length,
        average: nums.reduce((a, b) => a + b, 0) / nums.length,
        min: Math.min(...nums),
        max: Math.max(...nums),
        latest: nums[nums.length - 1]
      };
    });
    
    return report;
  }
}

// Initialize monitoring
const monitor = new PerformanceMonitor();

// Export for use in other modules
export default monitor;
```

### 🎯 Key Points
- Modern tooling improves development experience
- Package managers handle dependencies efficiently
- Build tools optimize code for production
- Code quality tools maintain consistency
- Performance monitoring ensures good user experience
- Module federation enables micro-frontend architecture

### 💡 Interview Questions (Hinglish)

**Q1: Modern JavaScript development mein kya tools essential hain?**

**A:**
- Package Manager: npm/yarn dependencies ke liye
- Bundler: Webpack/Vite code optimize karne ke liye
- Transpiler: Babel modern JS ko compatible banane ke liye
- Linter: ESLint code quality maintain karne ke liye
- Formatter: Prettier consistent formatting ke liye

**Q2: Webpack kya karta hai aur kaise configure karte hain?**

**A:**
Webpack modules ko bundle karta hai:
```javascript
module.exports = {
  entry: './src/index.js',
  output: { filename: 'bundle.js' },
  module: {
    rules: [
      { test: /\.js$/, use: 'babel-loader' },
      { test: /\.css$/, use: ['style-loader', 'css-loader'] }
    ]
  }
};
```

**Q3: Performance monitoring kaise implement karte hain?**

**A:**
Core Web Vitals track karte hain:
```javascript
// LCP - Largest Contentful Paint
new PerformanceObserver(entries => {
  const lcp = entries.getEntries()[0].startTime;
  console.log('LCP:', lcp);
}).observe({ entryTypes: ['largest-contentful-paint'] });

// FID - First Input Delay
// CLS - Cumulative Layout Shift
```

---

## Day 29: Final Project Planning and Architecture

### Project: Full-Stack Task Management Application

**Project Overview:**
We'll build a comprehensive task management application that demonstrates all the concepts learned throughout the 5-week course.

**Features:**
- User authentication and authorization
- Real-time task updates
- Advanced filtering and search
- Data visualization and analytics
- Offline functionality
- Performance optimization
- Security best practices

### Architecture Design

#### System Architecture
```
┌─────────────────────────────────────────────────────────┐
│                    Frontend (SPA)                       │
├─────────────────────────────────────────────────────────┤
│ • React/Vanilla JS Components                           │
│ • State Management (Redux/Context)                      │
│ • Service Workers (PWA)                                 │
│ • WebSocket Client                                      │
└─────────────────────────────────────────────────────────┘
                              │
                              │ HTTPS/WSS
                              ▼
┌─────────────────────────────────────────────────────────┐
│                   API Gateway                           │
├─────────────────────────────────────────────────────────┤
│ • Authentication Middleware                             │
│ • Rate Limiting                                         │
│ • Request/Response Logging                              │
│ • CORS Configuration                                    │
└─────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────┐
│                 Backend Services                        │
├─────────────────────────────────────────────────────────┤
│ • Task Service                                          │
│ • User Service                                          │
│ • Notification Service                                  │
│ • Analytics Service                                     │
└─────────────────────────────────────────────────────────┘
                              │
                              ▼
┌─────────────────────────────────────────────────────────┐
│                   Data Layer                            │
├─────────────────────────────────────────────────────────┤
│ • Database (MongoDB/PostgreSQL)                        │
│ • Redis Cache                                          │
│ • File Storage                                         │
└─────────────────────────────────────────────────────────┘
```

#### Frontend Architecture
```javascript
// src/architecture/AppArchitecture.js
class AppArchitecture {
  constructor() {
    this.layers = {
      presentation: {
        components: ['TaskList', 'TaskForm', 'Dashboard', 'Analytics'],
        pages: ['Home', 'Tasks', 'Profile', 'Settings'],
        layouts: ['MainLayout', 'AuthLayout']
      },
      
      business: {
        services: ['TaskService', 'UserService', 'NotificationService'],
        stores: ['TaskStore', 'UserStore', 'UIStore'],
        utils: ['ValidationUtils', 'DateUtils', 'SecurityUtils']
      },
      
      data: {
        api: ['TaskAPI', 'UserAPI', 'AnalyticsAPI'],
        cache: ['LocalCache', 'SessionCache'],
        storage: ['LocalStorage', 'IndexedDB']
      },
      
      infrastructure: {
        routing: ['Router', 'Guards', 'Middleware'],
        auth: ['AuthService', 'TokenManager'],
        monitoring: ['ErrorTracker', 'PerformanceMonitor']
      }
    };
  }
  
  getLayerDependencies() {
    return {
      presentation: ['business'],
      business: ['data'],
      data: ['infrastructure'],
      infrastructure: []
    };
  }
  
  validateArchitecture() {
    // Ensure no circular dependencies
    // Validate layer boundaries
    // Check for proper separation of concerns
  }
}
```

### Project Structure

```
task-management-app/
├── public/
│   ├── index.html
│   ├── manifest.json
│   └── sw.js
├── src/
│   ├── components/
│   │   ├── common/
│   │   │   ├── Button/
│   │   │   ├── Modal/
│   │   │   └── Loading/
│   │   ├── tasks/
│   │   │   ├── TaskList/
│   │   │   ├── TaskCard/
│   │   │   └── TaskForm/
│   │   └── dashboard/
│   │       ├── Analytics/
│   │       └── Charts/
│   ├── pages/
│   │   ├── Home/
│   │   ├── Tasks/
│   │   ├── Dashboard/
│   │   └── Profile/
│   ├── services/
│   │   ├── api/
│   │   ├── auth/
│   │   ├── storage/
│   │   └── websocket/
│   ├── store/
│   │   ├── slices/
│   │   └── middleware/
│   ├── utils/
│   │   ├── validation/
│   │   ├── security/
│   │   └── performance/
│   ├── hooks/
│   ├── constants/
│   ├── types/
│   └── styles/
├── tests/
│   ├── unit/
│   ├── integration/
│   └── e2e/
├── docs/
├── config/
└── scripts/
```

### Core Services Implementation

#### Task Service with Advanced Features
```javascript
// src/services/TaskService.js
import { EventEmitter } from 'events';
import { TaskAPI } from '../api/TaskAPI.js';
import { CacheService } from './CacheService.js';
import { ValidationService } from './ValidationService.js';
import { SecurityService } from './SecurityService.js';

class TaskService extends EventEmitter {
  constructor() {
    super();
    this.api = new TaskAPI();
    this.cache = new CacheService('tasks');
    this.validator = new ValidationService();
    this.security = new SecurityService();
    
    this.tasks = new Map();
    this.filters = {};
    this.sortConfig = { field: 'createdAt', order: 'desc' };
    
    this.setupRealTimeUpdates();
    this.setupOfflineSupport();
  }
  
  // Real-time updates with WebSocket
  setupRealTimeUpdates() {
    this.websocket = new WebSocket(process.env.WS_URL);
    
    this.websocket.onmessage = (event) => {
      const data = JSON.parse(event.data);
      
      switch (data.type) {
        case 'TASK_CREATED':
          this.handleTaskCreated(data.payload);
          break;
        case 'TASK_UPDATED':
          this.handleTaskUpdated(data.payload);
          break;
        case 'TASK_DELETED':
          this.handleTaskDeleted(data.payload);
          break;
      }
    };
    
    this.websocket.onclose = () => {
      // Reconnect logic
      setTimeout(() => this.setupRealTimeUpdates(), 5000);
    };
  }
  
  // Offline support with service worker
  setupOfflineSupport() {
    if ('serviceWorker' in navigator) {
      navigator.serviceWorker.register('/sw.js');
      
      // Listen for sync events
      navigator.serviceWorker.addEventListener('message', (event) => {
        if (event.data.type === 'SYNC_TASKS') {
          this.syncOfflineTasks();
        }
      });
    }
  }
  
  async createTask(taskData) {
    try {
      // Validate input
      const validationResult = this.validator.validateTask(taskData);
      if (!validationResult.isValid) {
        throw new Error(validationResult.errors.join(', '));
      }
      
      // Sanitize data
      const sanitizedData = this.security.sanitizeTaskData(taskData);
      
      // Optimistic update
      const tempId = `temp_${Date.now()}`;
      const optimisticTask = {
        id: tempId,
        ...sanitizedData,
        status: 'creating',
        createdAt: new Date().toISOString()
      };
      
      this.tasks.set(tempId, optimisticTask);
      this.emit('taskCreated', optimisticTask);
      
      try {
        // API call
        const createdTask = await this.api.createTask(sanitizedData);
        
        // Replace optimistic update with real data
        this.tasks.delete(tempId);
        this.tasks.set(createdTask.id, createdTask);
        
        // Cache the task
        await this.cache.set(createdTask.id, createdTask);
        
        this.emit('taskUpdated', createdTask);
        return createdTask;
        
      } catch (apiError) {
        // Revert optimistic update
        this.tasks.delete(tempId);
        this.emit('taskDeleted', tempId);
        
        // Store for offline sync if network error
        if (this.isNetworkError(apiError)) {
          await this.storeForOfflineSync('create', sanitizedData);
          throw new Error('Task saved offline. Will sync when online.');
        }
        
        throw apiError;
      }
      
    } catch (error) {
      this.emit('error', { operation: 'createTask', error });
      throw error;
    }
  }
  
  async getTasks(options = {}) {
    try {
      const cacheKey = this.generateCacheKey('tasks', options);
      
      // Try cache first
      const cachedTasks = await this.cache.get(cacheKey);
      if (cachedTasks && !options.forceRefresh) {
        return cachedTasks;
      }
      
      // Fetch from API
      const tasks = await this.api.getTasks(options);
      
      // Update local state
      tasks.forEach(task => this.tasks.set(task.id, task));
      
      // Cache results
      await this.cache.set(cacheKey, tasks, { ttl: 300000 }); // 5 minutes
      
      return tasks;
      
    } catch (error) {
      // Return cached data if available
      const cachedTasks = await this.cache.get(this.generateCacheKey('tasks', options));
      if (cachedTasks) {
        console.warn('Using cached data due to API error:', error);
        return cachedTasks;
      }
      
      throw error;
    }
  }
  
  async updateTask(taskId, updates) {
    try {
      const existingTask = this.tasks.get(taskId);
      if (!existingTask) {
        throw new Error('Task not found');
      }
      
      // Validate updates
      const validationResult = this.validator.validateTaskUpdates(updates);
      if (!validationResult.isValid) {
        throw new Error(validationResult.errors.join(', '));
      }
      
      // Sanitize updates
      const sanitizedUpdates = this.security.sanitizeTaskData(updates);
      
      // Optimistic update
      const optimisticTask = {
        ...existingTask,
        ...sanitizedUpdates,
        updatedAt: new Date().toISOString()
      };
      
      this.tasks.set(taskId, optimisticTask);
      this.emit('taskUpdated', optimisticTask);
      
      try {
        // API call
        const updatedTask = await this.api.updateTask(taskId, sanitizedUpdates);
        
        // Update with server response
        this.tasks.set(taskId, updatedTask);
        await this.cache.set(taskId, updatedTask);
        
        this.emit('taskUpdated', updatedTask);
        return updatedTask;
        
      } catch (apiError) {
        // Revert optimistic update
        this.tasks.set(taskId, existingTask);
        this.emit('taskUpdated', existingTask);
        
        // Store for offline sync
        if (this.isNetworkError(apiError)) {
          await this.storeForOfflineSync('update', { id: taskId, ...sanitizedUpdates });
          throw new Error('Update saved offline. Will sync when online.');
        }
        
        throw apiError;
      }
      
    } catch (error) {
      this.emit('error', { operation: 'updateTask', error });
      throw error;
    }
  }
  
  async deleteTask(taskId) {
    try {
      const existingTask = this.tasks.get(taskId);
      if (!existingTask) {
        throw new Error('Task not found');
      }
      
      // Optimistic delete
      this.tasks.delete(taskId);
      this.emit('taskDeleted', taskId);
      
      try {
        // API call
        await this.api.deleteTask(taskId);
        
        // Remove from cache
        await this.cache.delete(taskId);
        
        return true;
        
      } catch (apiError) {
        // Revert optimistic delete
        this.tasks.set(taskId, existingTask);
        this.emit('taskCreated', existingTask);
        
        // Store for offline sync
        if (this.isNetworkError(apiError)) {
          await this.storeForOfflineSync('delete', { id: taskId });
          throw new Error('Delete saved offline. Will sync when online.');
        }
        
        throw apiError;
      }
      
    } catch (error) {
      this.emit('error', { operation: 'deleteTask', error });
      throw error;
    }
  }
  
  // Advanced search with full-text search
  async searchTasks(query, options = {}) {
    try {
      const searchParams = {
        q: query,
        ...options,
        highlight: true,
        fuzzy: true
      };
      
      const results = await this.api.searchTasks(searchParams);
      
      // Cache search results
      const cacheKey = this.generateCacheKey('search', searchParams);
      await this.cache.set(cacheKey, results, { ttl: 60000 }); // 1 minute
      
      return results;
      
    } catch (error) {
      // Fallback to local search
      return this.localSearch(query, options);
    }
  }
  
  localSearch(query, options = {}) {
    const tasks = Array.from(this.tasks.values());
    const searchTerms = query.toLowerCase().split(' ');
    
    return tasks.filter(task => {
      const searchableText = [
        task.title,
        task.description,
        ...task.tags
      ].join(' ').toLowerCase();
      
      return searchTerms.every(term => searchableText.includes(term));
    });
  }
  
  // Analytics and insights
  async getTaskAnalytics(timeRange = '30d') {
    try {
      const analytics = await this.api.getTaskAnalytics(timeRange);
      
      // Enhance with local calculations
      const localTasks = Array.from(this.tasks.values());
      const enhancedAnalytics = {
        ...analytics,
        local: this.calculateLocalAnalytics(localTasks, timeRange)
      };
      
      return enhancedAnalytics;
      
    } catch (error) {
      // Fallback to local analytics
      const localTasks = Array.from(this.tasks.values());
      return {
        local: this.calculateLocalAnalytics(localTasks, timeRange),
        source: 'local'
      };
    }
  }
  
  calculateLocalAnalytics(tasks, timeRange) {
    const now = new Date();
    const rangeMs = this.parseTimeRange(timeRange);
    const cutoff = new Date(now.getTime() - rangeMs);
    
    const recentTasks = tasks.filter(task => 
      new Date(task.createdAt) >= cutoff
    );
    
    return {
      total: recentTasks.length,
      completed: recentTasks.filter(t => t.status === 'completed').length,
      overdue: recentTasks.filter(t => this.isOverdue(t)).length,
      byPriority: this.groupBy(recentTasks, 'priority'),
      byStatus: this.groupBy(recentTasks, 'status'),
      completionRate: this.calculateCompletionRate(recentTasks),
      averageCompletionTime: this.calculateAverageCompletionTime(recentTasks)
    };
  }
  
  // Offline sync management
  async storeForOfflineSync(operation, data) {
    const syncItem = {
      id: `sync_${Date.now()}_${Math.random()}`,
      operation,
      data,
      timestamp: Date.now(),
      retries: 0
    };
    
    const syncQueue = await this.cache.get('syncQueue') || [];
    syncQueue.push(syncItem);
    await this.cache.set('syncQueue', syncQueue);
    
    // Request background sync
    if ('serviceWorker' in navigator && 'sync' in window.ServiceWorkerRegistration.prototype) {
      const registration = await navigator.serviceWorker.ready;
      await registration.sync.register('sync-tasks');
    }
  }
  
  async syncOfflineTasks() {
    const syncQueue = await this.cache.get('syncQueue') || [];
    const results = [];
    
    for (const item of syncQueue) {
      try {
        let result;
        
        switch (item.operation) {
          case 'create':
            result = await this.api.createTask(item.data);
            break;
          case 'update':
            result = await this.api.updateTask(item.data.id, item.data);
            break;
          case 'delete':
            result = await this.api.deleteTask(item.data.id);
            break;
        }
        
        results.push({ item, success: true, result });
        
      } catch (error) {
        item.retries++;
        
        if (item.retries < 3) {
          results.push({ item, success: false, error, retry: true });
        } else {
          results.push({ item, success: false, error, retry: false });
        }
      }
    }
    
    // Update sync queue (remove successful items, keep failed items for retry)
    const failedItems = results
      .filter(r => !r.success && r.retry)
      .map(r => r.item);
    
    await this.cache.set('syncQueue', failedItems);
    
    // Emit sync results
    this.emit('syncCompleted', results);
    
    return results;
  }
  
  // Utility methods
  generateCacheKey(prefix, params) {
    return `${prefix}_${JSON.stringify(params)}`;
  }
  
  isNetworkError(error) {
    return error.name === 'NetworkError' || 
           error.message.includes('fetch') ||
           error.code === 'NETWORK_ERROR';
  }
  
  parseTimeRange(range) {
    const units = { d: 86400000, h: 3600000, m: 60000 };
    const match = range.match(/^(\d+)([dhm])$/);
    
    if (match) {
      return parseInt(match[1]) * units[match[2]];
    }
    
    return 30 * 86400000; // Default 30 days
  }
  
  isOverdue(task) {
    return task.dueDate && new Date(task.dueDate) < new Date() && task.status !== 'completed';
  }
  
  groupBy(array, key) {
    return array.reduce((groups, item) => {
      const group = item[key];
      groups[group] = (groups[group] || 0) + 1;
      return groups;
    }, {});
  }
  
  calculateCompletionRate(tasks) {
    if (tasks.length === 0) return 0;
    const completed = tasks.filter(t => t.status === 'completed').length;
    return Math.round((completed / tasks.length) * 100);
  }
  
  calculateAverageCompletionTime(tasks) {
    const completedTasks = tasks.filter(t => t.status === 'completed' && t.completedAt);
    
    if (completedTasks.length === 0) return 0;
    
    const totalTime = completedTasks.reduce((sum, task) => {
      const created = new Date(task.createdAt);
      const completed = new Date(task.completedAt);
      return sum + (completed - created);
    }, 0);
    
    return Math.round(totalTime / completedTasks.length / (1000 * 60 * 60 * 24)); // Days
  }
  
  // Real-time event handlers
  handleTaskCreated(task) {
    this.tasks.set(task.id, task);
    this.cache.set(task.id, task);
    this.emit('taskCreated', task);
  }
  
  handleTaskUpdated(task) {
    this.tasks.set(task.id, task);
    this.cache.set(task.id, task);
    this.emit('taskUpdated', task);
  }
  
  handleTaskDeleted(taskId) {
    this.tasks.delete(taskId);
    this.cache.delete(taskId);
    this.emit('taskDeleted', taskId);
  }
  
  // Cleanup
  destroy() {
    if (this.websocket) {
      this.websocket.close();
    }
    
    this.removeAllListeners();
    this.tasks.clear();
  }
}

export default TaskService;
```

### State Management

```javascript
// src/store/taskSlice.js
import { createSlice, createAsyncThunk } from '@reduxjs/toolkit';
import TaskService from '../services/TaskService.js';

const taskService = new TaskService();

// Async thunks
export const fetchTasks = createAsyncThunk(
  'tasks/fetchTasks',
  async (options, { rejectWithValue }) => {
    try {
      return await taskService.getTasks(options);
    } catch (error) {
      return rejectWithValue(error.message);
    }
  }
);

export const createTask = createAsyncThunk(
  'tasks/createTask',
  async (taskData, { rejectWithValue }) => {
    try {
      return await taskService.createTask(taskData);
    } catch (error) {
      return rejectWithValue(error.message);
    }
  }
);

export const updateTask = createAsyncThunk(
  'tasks/updateTask',
  async ({ id, updates }, { rejectWithValue }) => {
    try {
      return await taskService.updateTask(id, updates);
    } catch (error) {
      return rejectWithValue(error.message);
    }
  }
);

export const deleteTask = createAsyncThunk(
  'tasks/deleteTask',
  async (taskId, { rejectWithValue }) => {
    try {
      await taskService.deleteTask(taskId);
      return taskId;
    } catch (error) {
      return rejectWithValue(error.message);
    }
  }
);

export const searchTasks = createAsyncThunk(
  'tasks/searchTasks',
  async ({ query, options }, { rejectWithValue }) => {
    try {
      return await taskService.searchTasks(query, options);
    } catch (error) {
      return rejectWithValue(error.message);
    }
  }
);

// Slice
const taskSlice = createSlice({
  name: 'tasks',
  initialState: {
    items: [],
    searchResults: [],
    analytics: null,
    filters: {
      status: 'all',
      priority: 'all',
      assignee: 'all',
      dateRange: 'all'
    },
    sort: {
      field: 'createdAt',
      order: 'desc'
    },
    pagination: {
      page: 1,
      limit: 20,
      total: 0
    },
    loading: {
      fetch: false,
      create: false,
      update: false,
      delete: false,
      search: false
    },
    error: null,
    offline: false,
    syncStatus: 'idle'
  },
  reducers: {
    setFilters: (state, action) => {
      state.filters = { ...state.filters, ...action.payload };
      state.pagination.page = 1; // Reset pagination
    },
    
    setSort: (state, action) => {
      state.sort = action.payload;
    },
    
    setPagination: (state, action) => {
      state.pagination = { ...state.pagination, ...action.payload };
    },
    
    clearError: (state) => {
      state.error = null;
    },
    
    setOfflineStatus: (state, action) => {
      state.offline = action.payload;
    },
    
    setSyncStatus: (state, action) => {
      state.syncStatus = action.payload;
    },
    
    // Real-time updates
    taskCreatedRealtime: (state, action) => {
      state.items.unshift(action.payload);
    },
    
    taskUpdatedRealtime: (state, action) => {
      const index = state.items.findIndex(task => task.id === action.payload.id);
      if (index !== -1) {
        state.items[index] = action.payload;
      }
    },
    
    taskDeletedRealtime: (state, action) => {
      state.items = state.items.filter(task => task.id !== action.payload);
    }
  },
  extraReducers: (builder) => {
    builder
      // Fetch tasks
      .addCase(fetchTasks.pending, (state) => {
        state.loading.fetch = true;
        state.error = null;
      })
      .addCase(fetchTasks.fulfilled, (state, action) => {
        state.loading.fetch = false;
        state.items = action.payload;
      })
      .addCase(fetchTasks.rejected, (state, action) => {
        state.loading.fetch = false;
        state.error = action.payload;
      })
      
      // Create task
      .addCase(createTask.pending, (state) => {
        state.loading.create = true;
        state.error = null;
      })
      .addCase(createTask.fulfilled, (state, action) => {
        state.loading.create = false;
        state.items.unshift(action.payload);
      })
      .addCase(createTask.rejected, (state, action) => {
        state.loading.create = false;
        state.error = action.payload;
      })
      
      // Update task
      .addCase(updateTask.pending, (state) => {
        state.loading.update = true;
        state.error = null;
      })
      .addCase(updateTask.fulfilled, (state, action) => {
        state.loading.update = false;
        const index = state.items.findIndex(task => task.id === action.payload.id);
        if (index !== -1) {
          state.items[index] = action.payload;
        }
      })
      .addCase(updateTask.rejected, (state, action) => {
        state.loading.update = false;
        state.error = action.payload;
      })
      
      // Delete task
      .addCase(deleteTask.pending, (state) => {
        state.loading.delete = true;
        state.error = null;
      })
      .addCase(deleteTask.fulfilled, (state, action) => {
        state.loading.delete = false;
        state.items = state.items.filter(task => task.id !== action.payload);
      })
      .addCase(deleteTask.rejected, (state, action) => {
        state.loading.delete = false;
        state.error = action.payload;
      })
      
      // Search tasks
      .addCase(searchTasks.pending, (state) => {
        state.loading.search = true;
        state.error = null;
      })
      .addCase(searchTasks.fulfilled, (state, action) => {
        state.loading.search = false;
        state.searchResults = action.payload;
      })
      .addCase(searchTasks.rejected, (state, action) => {
        state.loading.search = false;
        state.error = action.payload;
      });
  }
});

export const {
  setFilters,
  setSort,
  setPagination,
  clearError,
  setOfflineStatus,
  setSyncStatus,
  taskCreatedRealtime,
  taskUpdatedRealtime,
  taskDeletedRealtime
} = taskSlice.actions;

export default taskSlice.reducer;

// Selectors
export const selectTasks = (state) => state.tasks.items;
export const selectTasksLoading = (state) => state.tasks.loading;
export const selectTasksError = (state) => state.tasks.error;
export const selectFilters = (state) => state.tasks.filters;
export const selectSort = (state) => state.tasks.sort;
export const selectPagination = (state) => state.tasks.pagination;
export const selectSearchResults = (state) => state.tasks.searchResults;
export const selectOfflineStatus = (state) => state.tasks.offline;
export const selectSyncStatus = (state) => state.tasks.syncStatus;

// Complex selectors
export const selectFilteredTasks = (state) => {
  const tasks = selectTasks(state);
  const filters = selectFilters(state);
  const sort = selectSort(state);
  
  let filtered = tasks;
  
  // Apply filters
  if (filters.status !== 'all') {
    filtered = filtered.filter(task => task.status === filters.status);
  }
  
  if (filters.priority !== 'all') {
    filtered = filtered.filter(task => task.priority === filters.priority);
  }
  
  if (filters.assignee !== 'all') {
    filtered = filtered.filter(task => task.assignedTo === filters.assignee);
  }
  
  // Apply sorting
  filtered.sort((a, b) => {
    let aValue = a[sort.field];
    let bValue = b[sort.field];
    
    if (sort.field.includes('At')) {
      aValue = new Date(aValue);
      bValue = new Date(bValue);
    }
    
    if (sort.order === 'asc') {
      return aValue > bValue ? 1 : -1;
    } else {
      return aValue < bValue ? 1 : -1;
    }
  });
  
  return filtered;
};

export const selectTaskStats = (state) => {
  const tasks = selectTasks(state);
  
  return {
    total: tasks.length,
    completed: tasks.filter(t => t.status === 'completed').length,
    inProgress: tasks.filter(t => t.status === 'in-progress').length,
    pending: tasks.filter(t => t.status === 'pending').length,
    overdue: tasks.filter(t => {
      return t.dueDate && new Date(t.dueDate) < new Date() && t.status !== 'completed';
    }).length
  };
};
```

### 🎯 Key Points
- Plan architecture before coding
- Separate concerns into layers
- Implement offline-first approach
- Use real-time updates for better UX
- Include comprehensive error handling
- Design for scalability and maintainability

### 💡 Interview Questions (Hinglish)

**Q1: Full-stack application ka architecture kaise design karte hain?**

**A:**
Layered architecture follow karte hain:
- Presentation Layer: UI components
- Business Layer: Services aur logic
- Data Layer: API calls aur caching
- Infrastructure Layer: Auth, routing, monitoring

**Q2: Offline-first application kaise banate hain?**

**A:**
- Service Workers use karte hain caching ke liye
- IndexedDB mein data store karte hain
- Background sync implement karte hain
- Optimistic updates use karte hain
- Network status track karte hain

**Q3: Real-time updates kaise implement karte hain?**

**A:**
```javascript
// WebSocket connection
const ws = new WebSocket('ws://localhost:8080');

ws.onmessage = (event) => {
  const data = JSON.parse(event.data);
  // Update UI based on real-time data
  dispatch(updateTaskRealtime(data));
};
```

---## Day 
30: Final Project Implementation and Deployment

### Complete Project Implementation

Let's implement the final components of our task management application:

#### Advanced UI Components

```javascript
// src/components/TaskDashboard.js
import React, { useEffect, useState } from 'react';
import { useSelector, useDispatch } from 'react-redux';
import {
  fetchTasks,
  selectFilteredTasks,
  selectTaskStats,
  selectTasksLoading,
  setFilters
} from '../store/taskSlice.js';
import TaskList from './TaskList.js';
import TaskFilters from './TaskFilters.js';
import TaskAnalytics from './TaskAnalytics.js';
import TaskForm from './TaskForm.js';

const TaskDashboard = () => {
  const dispatch = useDispatch();
  const tasks = useSelector(selectFilteredTasks);
  const stats = useSelector(selectTaskStats);
  const loading = useSelector(selectTasksLoading);
  
  const [view, setView] = useState('list'); // list, kanban, calendar
  const [showCreateForm, setShowCreateForm] = useState(false);
  
  useEffect(() => {
    dispatch(fetchTasks());
  }, [dispatch]);
  
  const handleFilterChange = (filters) => {
    dispatch(setFilters(filters));
  };
  
  const handleViewChange = (newView) => {
    setView(newView);
  };
  
  if (loading.fetch) {
    return <div className="loading-spinner">Loading tasks...</div>;
  }
  
  return (
    <div className="task-dashboard">
      <header className="dashboard-header">
        <div className="header-content">
          <h1>Task Dashboard</h1>
          <div className="header-actions">
            <button
              className="btn btn-primary"
              onClick={() => setShowCreateForm(true)}
            >
              + New Task
            </button>
            
            <div className="view-switcher">
              <button
                className={`btn ${view === 'list' ? 'active' : ''}`}
                onClick={() => handleViewChange('list')}
              >
                List
              </button>
              <button
                className={`btn ${view === 'kanban' ? 'active' : ''}`}
                onClick={() => handleViewChange('kanban')}
              >
                Kanban
              </button>
              <button
                className={`btn ${view === 'calendar' ? 'active' : ''}`}
                onClick={() => handleViewChange('calendar')}
              >
                Calendar
              </button>
            </div>
          </div>
        </div>
        
        <TaskStats stats={stats} />
      </header>
      
      <div className="dashboard-content">
        <aside className="dashboard-sidebar">
          <TaskFilters onFilterChange={handleFilterChange} />
          <TaskAnalytics />
        </aside>
        
        <main className="dashboard-main">
          {view === 'list' && <TaskList tasks={tasks} />}
          {view === 'kanban' && <TaskKanban tasks={tasks} />}
          {view === 'calendar' && <TaskCalendar tasks={tasks} />}
        </main>
      </div>
      
      {showCreateForm && (
        <TaskForm
          onClose={() => setShowCreateForm(false)}
          onSubmit={() => setShowCreateForm(false)}
        />
      )}
    </div>
  );
};

// Task Statistics Component
const TaskStats = ({ stats }) => (
  <div className="task-stats">
    <div className="stat-card">
      <div className="stat-number">{stats.total}</div>
      <div className="stat-label">Total Tasks</div>
    </div>
    
    <div className="stat-card">
      <div className="stat-number">{stats.completed}</div>
      <div className="stat-label">Completed</div>
    </div>
    
    <div className="stat-card">
      <div className="stat-number">{stats.inProgress}</div>
      <div className="stat-label">In Progress</div>
    </div>
    
    <div className="stat-card warning">
      <div className="stat-number">{stats.overdue}</div>
      <div className="stat-label">Overdue</div>
    </div>
  </div>
);

export default TaskDashboard;
```

#### Kanban Board Component

```javascript
// src/components/TaskKanban.js
import React, { useState } from 'react';
import { useDispatch } from 'react-redux';
import { updateTask } from '../store/taskSlice.js';
import { DragDropContext, Droppable, Draggable } from 'react-beautiful-dnd';

const TaskKanban = ({ tasks }) => {
  const dispatch = useDispatch();
  
  const columns = {
    pending: { title: 'To Do', color: '#e3f2fd' },
    'in-progress': { title: 'In Progress', color: '#fff3e0' },
    review: { title: 'Review', color: '#f3e5f5' },
    completed: { title: 'Done', color: '#e8f5e8' }
  };
  
  const tasksByStatus = tasks.reduce((acc, task) => {
    const status = task.status || 'pending';
    if (!acc[status]) acc[status] = [];
    acc[status].push(task);
    return acc;
  }, {});
  
  const handleDragEnd = (result) => {
    const { destination, source, draggableId } = result;
    
    if (!destination) return;
    
    if (
      destination.droppableId === source.droppableId &&
      destination.index === source.index
    ) {
      return;
    }
    
    // Update task status
    dispatch(updateTask({
      id: draggableId,
      updates: { status: destination.droppableId }
    }));
  };
  
  return (
    <div className="kanban-board">
      <DragDropContext onDragEnd={handleDragEnd}>
        <div className="kanban-columns">
          {Object.entries(columns).map(([columnId, column]) => (
            <div key={columnId} className="kanban-column">
              <div 
                className="column-header"
                style={{ backgroundColor: column.color }}
              >
                <h3>{column.title}</h3>
                <span className="task-count">
                  {tasksByStatus[columnId]?.length || 0}
                </span>
              </div>
              
              <Droppable droppableId={columnId}>
                {(provided, snapshot) => (
                  <div
                    ref={provided.innerRef}
                    {...provided.droppableProps}
                    className={`column-content ${
                      snapshot.isDraggingOver ? 'dragging-over' : ''
                    }`}
                  >
                    {(tasksByStatus[columnId] || []).map((task, index) => (
                      <Draggable
                        key={task.id}
                        draggableId={task.id}
                        index={index}
                      >
                        {(provided, snapshot) => (
                          <div
                            ref={provided.innerRef}
                            {...provided.draggableProps}
                            {...provided.dragHandleProps}
                            className={`kanban-card ${
                              snapshot.isDragging ? 'dragging' : ''
                            }`}
                          >
                            <KanbanCard task={task} />
                          </div>
                        )}
                      </Draggable>
                    ))}
                    {provided.placeholder}
                  </div>
                )}
              </Droppable>
            </div>
          ))}
        </div>
      </DragDropContext>
    </div>
  );
};

const KanbanCard = ({ task }) => (
  <div className={`task-card priority-${task.priority}`}>
    <div className="card-header">
      <h4 className="task-title">{task.title}</h4>
      <span className={`priority-badge priority-${task.priority}`}>
        {task.priority}
      </span>
    </div>
    
    <p className="task-description">{task.description}</p>
    
    {task.dueDate && (
      <div className={`due-date ${task.isOverdue ? 'overdue' : ''}`}>
        Due: {new Date(task.dueDate).toLocaleDateString()}
      </div>
    )}
    
    {task.tags && task.tags.length > 0 && (
      <div className="task-tags">
        {task.tags.map(tag => (
          <span key={tag} className="tag">#{tag}</span>
        ))}
      </div>
    )}
    
    <div className="card-footer">
      <div className="assignee">
        <img
          src={`/api/users/${task.assignedTo}/avatar`}
          alt="Assignee"
          className="avatar"
        />
      </div>
      
      <div className="task-actions">
        <button className="btn-icon" title="Edit">
          ✏️
        </button>
        <button className="btn-icon" title="Delete">
          🗑️
        </button>
      </div>
    </div>
  </div>
);

export default TaskKanban;
```

#### Progressive Web App (PWA) Setup

```javascript
// public/sw.js - Service Worker
const CACHE_NAME = 'task-manager-v1';
const urlsToCache = [
  '/',
  '/static/js/bundle.js',
  '/static/css/main.css',
  '/manifest.json'
];

// Install event
self.addEventListener('install', (event) => {
  event.waitUntil(
    caches.open(CACHE_NAME)
      .then((cache) => {
        console.log('Opened cache');
        return cache.addAll(urlsToCache);
      })
  );
});

// Fetch event
self.addEventListener('fetch', (event) => {
  event.respondWith(
    caches.match(event.request)
      .then((response) => {
        // Return cached version or fetch from network
        if (response) {
          return response;
        }
        
        return fetch(event.request).then((response) => {
          // Check if valid response
          if (!response || response.status !== 200 || response.type !== 'basic') {
            return response;
          }
          
          // Clone response
          const responseToCache = response.clone();
          
          caches.open(CACHE_NAME)
            .then((cache) => {
              cache.put(event.request, responseToCache);
            });
          
          return response;
        });
      })
  );
});

// Background sync
self.addEventListener('sync', (event) => {
  if (event.tag === 'sync-tasks') {
    event.waitUntil(syncTasks());
  }
});

async function syncTasks() {
  try {
    // Get pending sync items from IndexedDB
    const syncItems = await getSyncItems();
    
    for (const item of syncItems) {
      try {
        await syncItem(item);
        await removeSyncItem(item.id);
      } catch (error) {
        console.error('Sync failed for item:', item, error);
      }
    }
  } catch (error) {
    console.error('Background sync failed:', error);
  }
}

// Push notifications
self.addEventListener('push', (event) => {
  const options = {
    body: event.data ? event.data.text() : 'New task notification',
    icon: '/icon-192x192.png',
    badge: '/badge-72x72.png',
    vibrate: [100, 50, 100],
    data: {
      dateOfArrival: Date.now(),
      primaryKey: 1
    },
    actions: [
      {
        action: 'explore',
        title: 'View Task',
        icon: '/icon-view.png'
      },
      {
        action: 'close',
        title: 'Close',
        icon: '/icon-close.png'
      }
    ]
  };
  
  event.waitUntil(
    self.registration.showNotification('Task Manager', options)
  );
});

// Notification click
self.addEventListener('notificationclick', (event) => {
  event.notification.close();
  
  if (event.action === 'explore') {
    event.waitUntil(
      clients.openWindow('/tasks')
    );
  }
});
```

```json
// public/manifest.json
{
  "name": "Task Manager Pro",
  "short_name": "TaskManager",
  "description": "Professional task management application",
  "start_url": "/",
  "display": "standalone",
  "theme_color": "#2196f3",
  "background_color": "#ffffff",
  "orientation": "portrait-primary",
  "icons": [
    {
      "src": "/icon-72x72.png",
      "sizes": "72x72",
      "type": "image/png"
    },
    {
      "src": "/icon-96x96.png",
      "sizes": "96x96",
      "type": "image/png"
    },
    {
      "src": "/icon-128x128.png",
      "sizes": "128x128",
      "type": "image/png"
    },
    {
      "src": "/icon-144x144.png",
      "sizes": "144x144",
      "type": "image/png"
    },
    {
      "src": "/icon-152x152.png",
      "sizes": "152x152",
      "type": "image/png"
    },
    {
      "src": "/icon-192x192.png",
      "sizes": "192x192",
      "type": "image/png"
    },
    {
      "src": "/icon-384x384.png",
      "sizes": "384x384",
      "type": "image/png"
    },
    {
      "src": "/icon-512x512.png",
      "sizes": "512x512",
      "type": "image/png"
    }
  ],
  "categories": ["productivity", "business"],
  "screenshots": [
    {
      "src": "/screenshot-wide.png",
      "sizes": "1280x720",
      "type": "image/png",
      "form_factor": "wide"
    },
    {
      "src": "/screenshot-narrow.png",
      "sizes": "720x1280",
      "type": "image/png",
      "form_factor": "narrow"
    }
  ]
}
```

### Deployment Configuration

#### Docker Setup

```dockerfile
# Dockerfile
FROM node:18-alpine AS builder

WORKDIR /app

# Copy package files
COPY package*.json ./
RUN npm ci --only=production

# Copy source code
COPY . .

# Build application
RUN npm run build

# Production stage
FROM nginx:alpine

# Copy built application
COPY --from=builder /app/dist /usr/share/nginx/html

# Copy nginx configuration
COPY nginx.conf /etc/nginx/nginx.conf

# Expose port
EXPOSE 80

CMD ["nginx", "-g", "daemon off;"]
```

```nginx
# nginx.conf
events {
    worker_connections 1024;
}

http {
    include       /etc/nginx/mime.types;
    default_type  application/octet-stream;
    
    # Gzip compression
    gzip on;
    gzip_vary on;
    gzip_min_length 1024;
    gzip_types
        text/plain
        text/css
        text/xml
        text/javascript
        application/javascript
        application/xml+rss
        application/json;
    
    server {
        listen 80;
        server_name localhost;
        
        root /usr/share/nginx/html;
        index index.html;
        
        # Security headers
        add_header X-Frame-Options "SAMEORIGIN" always;
        add_header X-Content-Type-Options "nosniff" always;
        add_header X-XSS-Protection "1; mode=block" always;
        add_header Referrer-Policy "strict-origin-when-cross-origin" always;
        add_header Content-Security-Policy "default-src 'self'; script-src 'self' 'unsafe-inline'; style-src 'self' 'unsafe-inline'; img-src 'self' data: https:;" always;
        
        # Cache static assets
        location ~* \.(js|css|png|jpg|jpeg|gif|ico|svg|woff|woff2|ttf|eot)$ {
            expires 1y;
            add_header Cache-Control "public, immutable";
        }
        
        # Handle client-side routing
        location / {
            try_files $uri $uri/ /index.html;
        }
        
        # API proxy
        location /api/ {
            proxy_pass http://backend:3001;
            proxy_set_header Host $host;
            proxy_set_header X-Real-IP $remote_addr;
            proxy_set_header X-Forwarded-For $proxy_add_x_forwarded_for;
            proxy_set_header X-Forwarded-Proto $scheme;
        }
        
        # WebSocket proxy
        location /ws {
            proxy_pass http://backend:3001;
            proxy_http_version 1.1;
            proxy_set_header Upgrade $http_upgrade;
            proxy_set_header Connection "upgrade";
            proxy_set_header Host $host;
        }
    }
}
```

#### Docker Compose

```yaml
# docker-compose.yml
version: '3.8'

services:
  frontend:
    build: .
    ports:
      - "80:80"
    depends_on:
      - backend
    environment:
      - NODE_ENV=production
    networks:
      - app-network

  backend:
    build: ./backend
    ports:
      - "3001:3001"
    depends_on:
      - database
      - redis
    environment:
      - NODE_ENV=production
      - DATABASE_URL=mongodb://database:27017/taskmanager
      - REDIS_URL=redis://redis:6379
      - JWT_SECRET=${JWT_SECRET}
    networks:
      - app-network

  database:
    image: mongo:6
    ports:
      - "27017:27017"
    volumes:
      - mongodb_data:/data/db
    environment:
      - MONGO_INITDB_ROOT_USERNAME=${MONGO_USERNAME}
      - MONGO_INITDB_ROOT_PASSWORD=${MONGO_PASSWORD}
    networks:
      - app-network

  redis:
    image: redis:7-alpine
    ports:
      - "6379:6379"
    volumes:
      - redis_data:/data
    networks:
      - app-network

  nginx:
    image: nginx:alpine
    ports:
      - "443:443"
    volumes:
      - ./nginx/ssl:/etc/nginx/ssl
      - ./nginx/nginx.conf:/etc/nginx/nginx.conf
    depends_on:
      - frontend
    networks:
      - app-network

volumes:
  mongodb_data:
  redis_data:

networks:
  app-network:
    driver: bridge
```

#### CI/CD Pipeline

```yaml
# .github/workflows/deploy.yml
name: Deploy to Production

on:
  push:
    branches: [main]
  pull_request:
    branches: [main]

jobs:
  test:
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v3
    
    - name: Setup Node.js
      uses: actions/setup-node@v3
      with:
        node-version: '18'
        cache: 'npm'
    
    - name: Install dependencies
      run: npm ci
    
    - name: Run linter
      run: npm run lint
    
    - name: Run tests
      run: npm test -- --coverage
    
    - name: Upload coverage
      uses: codecov/codecov-action@v3

  build:
    needs: test
    runs-on: ubuntu-latest
    
    steps:
    - uses: actions/checkout@v3
    
    - name: Setup Node.js
      uses: actions/setup-node@v3
      with:
        node-version: '18'
        cache: 'npm'
    
    - name: Install dependencies
      run: npm ci
    
    - name: Build application
      run: npm run build
    
    - name: Build Docker image
      run: docker build -t task-manager:${{ github.sha }} .
    
    - name: Login to Docker Hub
      uses: docker/login-action@v2
      with:
        username: ${{ secrets.DOCKER_USERNAME }}
        password: ${{ secrets.DOCKER_PASSWORD }}
    
    - name: Push Docker image
      run: |
        docker tag task-manager:${{ github.sha }} ${{ secrets.DOCKER_USERNAME }}/task-manager:latest
        docker push ${{ secrets.DOCKER_USERNAME }}/task-manager:latest

  deploy:
    needs: build
    runs-on: ubuntu-latest
    if: github.ref == 'refs/heads/main'
    
    steps:
    - name: Deploy to production
      uses: appleboy/ssh-action@v0.1.5
      with:
        host: ${{ secrets.HOST }}
        username: ${{ secrets.USERNAME }}
        key: ${{ secrets.SSH_KEY }}
        script: |
          cd /opt/task-manager
          docker-compose pull
          docker-compose up -d
          docker system prune -f
```

### Performance Optimization

```javascript
// src/utils/performance.js
class PerformanceOptimizer {
  constructor() {
    this.observers = new Map();
    this.setupOptimizations();
  }
  
  setupOptimizations() {
    // Lazy load images
    this.setupLazyLoading();
    
    // Preload critical resources
    this.preloadCriticalResources();
    
    // Setup intersection observer for analytics
    this.setupViewportTracking();
    
    // Memory cleanup
    this.setupMemoryCleanup();
  }
  
  setupLazyLoading() {
    const imageObserver = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          const img = entry.target;
          img.src = img.dataset.src;
          img.classList.remove('lazy');
          imageObserver.unobserve(img);
        }
      });
    });
    
    document.querySelectorAll('img[data-src]').forEach(img => {
      imageObserver.observe(img);
    });
    
    this.observers.set('images', imageObserver);
  }
  
  preloadCriticalResources() {
    const criticalResources = [
      '/api/user/profile',
      '/api/tasks?limit=20',
      '/static/css/critical.css'
    ];
    
    criticalResources.forEach(resource => {
      if (resource.startsWith('/api/')) {
        // Preload API data
        fetch(resource).then(response => response.json());
      } else {
        // Preload static resources
        const link = document.createElement('link');
        link.rel = 'preload';
        link.href = resource;
        link.as = resource.endsWith('.css') ? 'style' : 'script';
        document.head.appendChild(link);
      }
    });
  }
  
  setupViewportTracking() {
    const viewportObserver = new IntersectionObserver((entries) => {
      entries.forEach(entry => {
        if (entry.isIntersecting) {
          const element = entry.target;
          const componentName = element.dataset.component;
          
          // Track component visibility
          this.trackComponentView(componentName);
          
          // Lazy load component data if needed
          if (element.dataset.lazyLoad) {
            this.loadComponentData(componentName);
          }
        }
      });
    }, { threshold: 0.1 });
    
    document.querySelectorAll('[data-component]').forEach(element => {
      viewportObserver.observe(element);
    });
    
    this.observers.set('viewport', viewportObserver);
  }
  
  setupMemoryCleanup() {
    // Clean up every 5 minutes
    setInterval(() => {
      this.cleanupMemory();
    }, 300000);
    
    // Clean up on page visibility change
    document.addEventListener('visibilitychange', () => {
      if (document.hidden) {
        this.cleanupMemory();
      }
    });
  }
  
  cleanupMemory() {
    // Clear old cache entries
    if ('caches' in window) {
      caches.keys().then(cacheNames => {
        cacheNames.forEach(cacheName => {
          if (cacheName.includes('old') || cacheName.includes('temp')) {
            caches.delete(cacheName);
          }
        });
      });
    }
    
    // Clear old IndexedDB entries
    this.cleanupIndexedDB();
    
    // Force garbage collection if available
    if (window.gc) {
      window.gc();
    }
  }
  
  async cleanupIndexedDB() {
    try {
      const db = await this.openIndexedDB();
      const transaction = db.transaction(['cache'], 'readwrite');
      const store = transaction.objectStore('cache');
      
      // Remove entries older than 1 hour
      const cutoff = Date.now() - (60 * 60 * 1000);
      const request = store.openCursor();
      
      request.onsuccess = (event) => {
        const cursor = event.target.result;
        if (cursor) {
          if (cursor.value.timestamp < cutoff) {
            cursor.delete();
          }
          cursor.continue();
        }
      };
    } catch (error) {
      console.error('IndexedDB cleanup failed:', error);
    }
  }
  
  trackComponentView(componentName) {
    // Send analytics event
    if (typeof gtag !== 'undefined') {
      gtag('event', 'component_view', {
        component_name: componentName,
        timestamp: Date.now()
      });
    }
  }
  
  loadComponentData(componentName) {
    // Implement lazy loading logic for specific components
    switch (componentName) {
      case 'analytics':
        import('../components/TaskAnalytics.js');
        break;
      case 'calendar':
        import('../components/TaskCalendar.js');
        break;
      default:
        break;
    }
  }
  
  // Bundle splitting helper
  static async loadChunk(chunkName) {
    try {
      const module = await import(`../chunks/${chunkName}.js`);
      return module.default;
    } catch (error) {
      console.error(`Failed to load chunk ${chunkName}:`, error);
      throw error;
    }
  }
  
  // Performance monitoring
  measurePerformance(name, fn) {
    const start = performance.now();
    
    const result = fn();
    
    if (result instanceof Promise) {
      return result.finally(() => {
        const duration = performance.now() - start;
        this.recordMetric(name, duration);
      });
    } else {
      const duration = performance.now() - start;
      this.recordMetric(name, duration);
      return result;
    }
  }
  
  recordMetric(name, duration) {
    // Send to analytics
    if (typeof gtag !== 'undefined') {
      gtag('event', 'performance_metric', {
        metric_name: name,
        metric_value: Math.round(duration),
        metric_unit: 'milliseconds'
      });
    }
    
    // Log slow operations
    if (duration > 100) {
      console.warn(`Slow operation detected: ${name} took ${duration}ms`);
    }
  }
  
  destroy() {
    this.observers.forEach(observer => observer.disconnect());
    this.observers.clear();
  }
}

export default PerformanceOptimizer;
```

### Final Testing Strategy

```javascript
// tests/integration/TaskFlow.test.js
import { render, screen, fireEvent, waitFor } from '@testing-library/react';
import { Provider } from 'react-redux';
import { configureStore } from '@reduxjs/toolkit';
import TaskDashboard from '../src/components/TaskDashboard.js';
import taskReducer from '../src/store/taskSlice.js';

// Mock API
jest.mock('../src/services/TaskService.js');

describe('Task Management Flow', () => {
  let store;
  
  beforeEach(() => {
    store = configureStore({
      reducer: {
        tasks: taskReducer
      }
    });
  });
  
  test('complete task workflow', async () => {
    render(
      <Provider store={store}>
        <TaskDashboard />
      </Provider>
    );
    
    // 1. Create new task
    fireEvent.click(screen.getByText('+ New Task'));
    
    fireEvent.change(screen.getByLabelText('Title'), {
      target: { value: 'Test Task' }
    });
    
    fireEvent.change(screen.getByLabelText('Description'), {
      target: { value: 'Test Description' }
    });
    
    fireEvent.click(screen.getByText('Create Task'));
    
    // 2. Verify task appears in list
    await waitFor(() => {
      expect(screen.getByText('Test Task')).toBeInTheDocument();
    });
    
    // 3. Update task status
    fireEvent.click(screen.getByLabelText('Mark as complete'));
    
    await waitFor(() => {
      expect(screen.getByText('Completed')).toBeInTheDocument();
    });
    
    // 4. Filter completed tasks
    fireEvent.change(screen.getByLabelText('Status Filter'), {
      target: { value: 'completed' }
    });
    
    await waitFor(() => {
      expect(screen.getByText('Test Task')).toBeInTheDocument();
    });
    
    // 5. Delete task
    fireEvent.click(screen.getByLabelText('Delete task'));
    fireEvent.click(screen.getByText('Confirm'));
    
    await waitFor(() => {
      expect(screen.queryByText('Test Task')).not.toBeInTheDocument();
    });
  });
  
  test('offline functionality', async () => {
    // Mock offline state
    Object.defineProperty(navigator, 'onLine', {
      writable: true,
      value: false
    });
    
    render(
      <Provider store={store}>
        <TaskDashboard />
      </Provider>
    );
    
    // Create task while offline
    fireEvent.click(screen.getByText('+ New Task'));
    
    fireEvent.change(screen.getByLabelText('Title'), {
      target: { value: 'Offline Task' }
    });
    
    fireEvent.click(screen.getByText('Create Task'));
    
    // Verify offline indicator
    await waitFor(() => {
      expect(screen.getByText('Offline - Changes will sync when online')).toBeInTheDocument();
    });
    
    // Simulate going back online
    Object.defineProperty(navigator, 'onLine', {
      value: true
    });
    
    window.dispatchEvent(new Event('online'));
    
    // Verify sync indicator
    await waitFor(() => {
      expect(screen.getByText('Syncing...')).toBeInTheDocument();
    });
  });
  
  test('real-time updates', async () => {
    render(
      <Provider store={store}>
        <TaskDashboard />
      </Provider>
    );
    
    // Simulate WebSocket message
    const mockWebSocket = {
      send: jest.fn(),
      close: jest.fn()
    };
    
    global.WebSocket = jest.fn(() => mockWebSocket);
    
    // Simulate receiving real-time update
    const taskUpdate = {
      type: 'TASK_UPDATED',
      payload: {
        id: '123',
        title: 'Updated Task',
        status: 'completed'
      }
    };
    
    mockWebSocket.onmessage({ data: JSON.stringify(taskUpdate) });
    
    await waitFor(() => {
      expect(screen.getByText('Updated Task')).toBeInTheDocument();
    });
  });
});
```

### 🎯 Final Project Achievements
- Complete full-stack task management application
- Real-time updates with WebSocket
- Offline-first architecture with PWA
- Advanced UI with drag-and-drop Kanban board
- Comprehensive testing strategy
- Production-ready deployment configuration
- Performance optimization and monitoring
- Security best practices implementation

### 💡 Final Interview Questions (Hinglish)

**Q1: Production-ready application deploy karne ke liye kya considerations hain?**

**A:**
- Docker containerization for consistency
- CI/CD pipeline for automated deployment
- Load balancing aur scaling
- Security headers aur HTTPS
- Monitoring aur logging
- Database backups aur disaster recovery
- Performance optimization aur caching

**Q2: PWA (Progressive Web App) kya hai aur kaise implement karte hain?**

**A:**
PWA web app hai jo native app jaisa behave karta hai:
```javascript
// Service Worker registration
navigator.serviceWorker.register('/sw.js');

// Manifest.json for app-like experience
// Offline functionality with caching
// Push notifications
// Install prompt
```

**Q3: Real-time features kaise implement karte hain?**

**A:**
```javascript
// WebSocket connection
const ws = new WebSocket('ws://localhost:8080');

// Server-Sent Events
const eventSource = new EventSource('/api/events');

// Polling fallback
setInterval(() => {
  fetchUpdates();
}, 5000);
```

---

## Course Completion Summary

### 🎉 Congratulations! You've Completed the 5-Week JavaScript Mastery Course

**What You've Learned:**

**Week 1: JavaScript Fundamentals**
- Variables, data types, and operators
- Control flow and loops
- Functions and scope basics
- DOM manipulation fundamentals

**Week 2: Data Structures and Modern JavaScript**
- Arrays and advanced array methods
- Objects and object manipulation
- Destructuring and spread operator
- Template literals and modern syntax
- Error handling and debugging

**Week 3: Advanced JavaScript Concepts**
- Advanced functions and closures
- Asynchronous programming (callbacks, promises, async/await)
- DOM manipulation and event handling
- Object-oriented programming
- Modules and modern features

**Week 4: Advanced Concepts and Design Patterns**
- Advanced OOP and prototypes
- Design patterns (Singleton, Factory, Observer, Strategy)
- Performance optimization techniques
- Testing and debugging strategies
- Security best practices

**Week 5: Modern Development and Project Work**
- Modern JavaScript ecosystem and tools
- Build tools and bundlers (Webpack, Babel)
- Code quality tools (ESLint, Prettier)
- Full-stack application architecture
- PWA development and deployment

### 🚀 Next Steps for Continued Learning

1. **Frameworks and Libraries**
   - React.js for UI development
   - Node.js for backend development
   - Express.js for web servers
   - MongoDB/PostgreSQL for databases

2. **Advanced Topics**
   - TypeScript for type safety
   - GraphQL for API development
   - Microservices architecture
   - Cloud deployment (AWS, Azure, GCP)

3. **Specialization Areas**
   - Frontend: React, Vue.js, Angular
   - Backend: Node.js, Deno, serverless
   - Mobile: React Native, Ionic
   - Desktop: Electron

4. **Professional Development**
   - Open source contributions
   - Technical blogging
   - Conference speaking
   - Mentoring others

### 📚 Recommended Resources

**Books:**
- "You Don't Know JS" series by Kyle Simpson
- "JavaScript: The Good Parts" by Douglas Crockford
- "Clean Code" by Robert Martin
- "Design Patterns" by Gang of Four

**Online Platforms:**
- MDN Web Docs (developer.mozilla.org)
- JavaScript.info
- FreeCodeCamp
- Codecademy

**Practice Platforms:**
- LeetCode for algorithms
- HackerRank for challenges
- Codewars for kata practice
- GitHub for project hosting

### 🏆 Your JavaScript Journey Continues

You now have a solid foundation in JavaScript and modern web development. The key to mastery is continuous practice and building real projects. Keep coding, keep learning, and most importantly, keep building amazing things!

**Happy Coding! 🚀**

---

*This comprehensive guide contains over 2000 lines of detailed explanations, practical examples, and real-world applications. Use it as a reference throughout your JavaScript development journey.*
