# JavaScript Interview Questions & Answers

> This repository contains Javascript interview questions with beginner to intermediate to advanced level questions and answers. This repo will also helps you to find questions around find the output.

---

### Table of Contents

<!-- TOC_START -->
| No. | Questions |
| --- | --------- |
| 1 | [What are the differences between var, let, and const in JavaScript?](#what-are-the-differences-between-var-let-and-const-in-javaScript) |
| 2 | [How does variable hoisting work in JavaScript wrt var, let, const?](#how-does-variable-hoisting-work-in-javaScript-wrt-var-let-const) |
<!-- TOC_END -->

<!-- QUESTIONS_START -->
1. ### What are the differences between var, let, and const in JavaScript?

   1. **var:**

      **Scope:** Function-scoped. Variables declared with `var` are accessible within the function they are declared in.

      **Hoisting:** `var` declarations are hoisted to the top of their scope and initialized with `undefined`.

      **Re-declaration:** Allowed within the same scope.

      ```javascript
      function example() {
        console.log(x); // undefined due to hoisting
        var x = 5;
        console.log(x); // 5
      }
      example();
      ```

   2. **let:**

      **Scope:** Block-scoped. Accessible only within the block (`{}`) they are declared in.

      **Hoisting:** `let` declarations are hoisted but not initialized. Accessing them before declaration results in a `ReferenceError`.

      **Re-declaration:** Not allowed within the same scope.

      ```javascript
      {
        console.log(y); // ReferenceError: Cannot access 'y' before initialization
        let y = 10;
        console.log(y); // 10
      }
      ```

   3. **const:**

      **Scope:** Block-scoped.

      **Hoisting:** Similar to `let`, `const` declarations are hoisted but not initialized. Accessing them before declaration results in a `ReferenceError`.

      **Re-declaration:** Not allowed within the same scope.

      **Assignment:** Must be initialized at the time of declaration and cannot be reassigned.

      ```javascript
      {
        const z = 15;
        z = 20; // TypeError: Assignment to constant variable.
      }
      ```

      **[⬆ Back to Top](#table-of-contents)**

2. ### How does variable hoisting work in JavaScript wrt var, let, const?

    Hoisting is JavaScript's default behavior of moving declarations to the top of their scope before code execution.

     1. **var:** Declarations are hoisted and initialized with undefined.
   
      ```javascript
      console.log(a); // undefined
      var a = 3;

      // it is interpreted as

      var a;
      console.log(a); // undefined
      a = 3;
      ```
     2. **let and const:**  Declarations are hoisted but not initialized. Accessing them before declaration results in a `ReferenceError`.

      ```javascript
      console.log(b); // ReferenceError
      let b = 5;
      ```

   **[⬆ Back to Top](#table-of-contents)**

---
 
## Disclaimer

The questions provided in this repository are the summary of frequently asked questions across numerous companies. We cannot guarantee that these questions will actually be asked during your interview process, nor should you focus on memorizing all of them. The primary purpose is for you to get a sense of what some companies might ask — do not get discouraged if you don't know the answer to all of them ⁠— that is ok!

Good luck with your interview 😊

---
