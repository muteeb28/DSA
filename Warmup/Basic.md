**Problem Statement (1): Print “Hello World”**
A simple program that outputs the text “hello world” to the console.

**Explanation**

* `console.log("hello world")` is a built-in JavaScript function that prints whatever is inside the quotes to the console.
* When the JavaScript engine executes this line, it sends the string `"hello world"` to the runtime’s standard output (the console).

**Dry Run**

* **Input:** None (the code itself is the input)
* **Step 1:** The engine sees `console.log("hello world")`.
* **Step 2:** It evaluates the string literal `"hello world"`.
* **Step 3:** It passes that string to `console.log`, which prints `hello world` on the console.

**Code Implementation**

```js
// how to print hello world
console.log("hello world");
```

---

**Problem Statement (2): Demonstrate Basic Arithmetic with Variables**
Define two numeric constants, perform addition, multiplication, modulus, and division, and print all results on one line.

**Explanation**

* We declare `const a = 10` and `const b = 20`. These are two constant numeric values.
* We compute four different results:

  1. `sum = a + b` → adds 10 and 20.
  2. `multiply = a * b` → multiplies 10 by 20.
  3. `remainder = a % b` → finds the remainder when 10 is divided by 20.
  4. `quotient = a / b` → divides 10 by 20 and returns a floating‐point result.
* Finally, `console.log(sum, multiply, remainder, quotient)` prints all four computed values separated by spaces.

**Dry Run**

* **Input:**

  * `a = 10`
  * `b = 20`
* **Step 1:** `sum = 10 + 20 = 30`
* **Step 2:** `multiply = 10 * 20 = 200`
* **Step 3:** `remainder = 10 % 20 = 10` (since 10 ÷ 20 = 0 remainder 10)
* **Step 4:** `quotient = 10 / 20 = 0.5`
* **Step 5:** `console.log(30, 200, 10, 0.5)` prints `30 200 10 0.5`.

**Code Implementation**

```js
// Data Types
// variables
const a = 10;
const b = 20;

const sum = a + b;
const multiply = a * b;
const remainder = a % b;
const quotient = a / b;

console.log(sum, multiply, remainder, quotient); // Outputs: 30 200 10 0.5
```

---

**Problem Statement (3): Concatenate Two Strings (First and Last Name)**
Take two string variables (`firstName` and `lastName`), join them with a space, and print the full name.

**Explanation**

* `let firstName = "hazik"` and `let lastName = "ali"` assign two separate strings.
* We create `const fullName = firstName + " " + lastName`. The `+` operator, when used on strings, concatenates them.
* The `" "` literal between them ensures there is a space between first and last name.
* Finally, `console.log(fullName)` prints the combined `"hazik ali"` string to the console.

**Dry Run**

* **Input:**

  * `firstName = "hazik"`
  * `lastName = "ali"`
* **Step 1:** Evaluate `firstName + " "` → `"hazik "`.
* **Step 2:** Then `"hazik " + lastName` → `"hazik ali"`.
* **Step 3:** `fullName = "hazik ali"`.
* **Step 4:** `console.log("hazik ali")` prints `hazik ali`.

**Code Implementation**

```js
// concatenation of string
let firstName = "hazik";
let lastName = "ali";

const fullName = firstName + " " + lastName;
console.log(fullName); // Outputs: hazik ali
```

---

> *Note on JavaScript Engine (Comment)*
> Under the hood, the JavaScript engine continually performs tasks such as garbage collection and optimizing code execution. When you declare variables or create objects, the engine allocates memory; over time, when those references are no longer needed, the garbage collector frees that memory. All of this happens “behind the scenes” so that you can focus on writing code.

---

**Problem Statement (4): Store Multiple Values in an Array and Access Them**
Create an array of numbers, then calculate the sum of two specific elements by accessing their indices.

**Explanation**

1. `let arr = [2, 34, 5, 56, 6]` declares an array named `arr` containing five numeric elements.
2. To sum two array elements, we use bracket-index notation: `arr[3] + arr[2]`. Because arrays are zero-indexed:

   * `arr[2]` refers to the third element (`5`).
   * `arr[3]` refers to the fourth element (`56`).
3. We assign that result to `let add = arr[3] + arr[2]`.
4. `console.log(add)` prints the result of adding 56 and 5 (which is `61`).

**Dry Run**

* **Input:**

  * `arr = [2, 34, 5, 56, 6]`
* **Step 1:** Identify `arr[2] = 5` and `arr[3] = 56`.
* **Step 2:** Compute `5 + 56 = 61`.
* **Step 3:** `add = 61`.
* **Step 4:** `console.log(61)` prints `61`.

**Code Implementation**

```js
// array to store multiple values
let arr = [2, 34, 5, 56, 6];

// sum of two numbers (third and fourth elements)
let add = arr[3] + arr[2];
console.log(add); // Outputs: 61
```

---

**Problem Statement (5): Access Nested Array Elements**
Demonstrate how to retrieve values from a nested array structure.

**Explanation**

1. Declare `let arr2 = ["sam", 4, [5, 10, [4, 4]]]`. Here, `arr2` has three elements:

   * Index 0 → `"sam"` (a string)
   * Index 1 → `4` (a number)
   * Index 2 → another array: `[5, 10, [4, 4]]`
2. To access the first element of that inner array (i.e., `5`), we use `arr2[2][0]`:

   * `arr2[2]` evaluates to `[5, 10, [4, 4]]`
   * Then `[5, 10, [4, 4]][0]` is `5`.
3. To access the second element of the innermost array (`4`, from `[4, 4]`), we use `arr2[2][2][1]`:

   * `arr2[2][2]` is `[4, 4]`
   * Then `[4, 4][1]` is `4`.

**Dry Run**

* **Input:**

  * `arr2 = ["sam", 4, [5, 10, [4, 4]]]`
* **Step 1:** Resolve `arr2[2]` → `[5, 10, [4, 4]]`.
* **Step 2:** Resolve `arr2[2][0]` → `5`.
* **Step 3:** Log `5`.
* **Step 4:** Resolve `arr2[2][2]` → `[4, 4]`.
* **Step 5:** Resolve `arr2[2][2][1]` → `4`.
* **Step 6:** Log `4`.

**Code Implementation**

```js
// array inside array
let arr2 = ["sam", 4, [5, 10, [4, 4]]];

console.log(arr2[2][0]);      // Outputs: 5
console.log(arr2[2][2][1]);   // Outputs: 4
```

---

**Problem Statement (6): Create and Use an Object with Key-Value Pairs**
Define an object with multiple properties, access numeric and string properties, and concatenate two string properties.

**Explanation**

1. We declare an object named `obj` with the following key–value pairs:

   * `a: 9` (a numeric property)
   * `firstName: "hazik"` (string)
   * `lastName: "ali"` (string)
   * `bol: true` (boolean)
2. To access the numeric property `a`, we use either `obj["a"]` or `obj.a`. Here, we’ll use bracket notation: `obj["a"]` → `9`.
3. To concatenate the first and last name stored in the object, we do `obj["firstName"] + " " + obj["lastName"]`. This produces `"hazik ali"`.
4. We then `console.log` each result to print them.

**Dry Run**

* **Input:**

  * `obj = { a: 9, firstName: "hazik", lastName: "ali", bol: true }`
* **Step 1:** Evaluate `obj["a"]` → `9`.
* **Step 2:** `console.log(9)` prints `9`.
* **Step 3:** Evaluate `obj["firstName"] + " " + obj["lastName"]` → `"hazik" + " " + "ali"` → `"hazik ali"`.
* **Step 4:** `console.log("hazik ali")` prints `hazik ali`.

**Code Implementation**

```js
// object contains key-value pairs
let obj = {
  a: 9,
  firstName: "hazik",
  lastName: "ali",
  bol: true
};

// Access numeric property
console.log(obj["a"]);               // Outputs: 9

// Concatenate firstName and lastName
console.log(obj["firstName"] + " " + obj["lastName"]); // Outputs: hazik ali
```

---

Whenever you have another snippet or problem, just share it, and I’ll follow this same pattern—Problem Statement → Explanation → Dry Run → Code Implementation—so you can easily remember how you solved it.
