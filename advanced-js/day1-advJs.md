# Advanced js - Day 1

## Appx I - Vid 2

- implicit mentions:

    -   balsamiq mockups
    -   threejs.org

---

## Appx I - Vid 3

-   7 types

    -   Number
        ```js
        // in browser console
        3 + 4;          // 7
        3 * 4;          // 12
        12 / 4;         // 3
        (3 + 4) * 2;    // 14
        12 % 6;         // 0
        12 % 5;         // 2
        ```
    -   String

        ```js
        // in browser console
        "MohammadBagher"
        'Abedi'
        "Sa" + "lam"        // "Salam"

        'js isn't fine'     // error
        'js isn\'t fine'    // use \ to escape ' or "
        "js isn't fine"     // or use ' & " in turn

        20 + "48"           // "2048"
        20 - "48"           // -28
        "Sa" - "lam"        // NaN (always) (Nan is part of Number type)
        ```

    -   Boolean

        ```js
        // in browser console
        true;
        false;

        // comparisons:
        3 > 2;      // true
        5 > 10;     // false
        5 >= 5;     // true
        5 <= 5;     // true
        3 === 3;    // true
        3 !== 3;    //false
        ```

-   side mentions:
    clear browser console:
    ```js
    clear();
    ```

---

## Appx I - Vid 4

-   js variables (to store values)
    ```js
    // in browser console
    var name = "the blue orange fox ate three chicks"; // var name starts with letter
    name;   // "the blue orange fox ate three chicks"
    var $name;      // var name starts with $
    var _name;      // var name starts with _
    var firstName;  // camelCase notation
    ```
-   a simple calculator

    ```js
        // prompt's output is entered value as String
        prompt()             // opens browser prompt to get user input
        prompt("question")  // prompt with String arg as title

        var first = prompt("enter first")
        var second = prompt("enter second")
        var sum = Number(first) + Number(second) // cast variables to number & sum
        alert(sum) //opens dialog showing the given value
        alert("The sum is: "sum) //value could get casted
    ```

-   reassignment | the 4th type: Undefined
    ```js
    var a = false;  // create & assign
    a;              // -> false
    a = "Hello";    // reassign
    a;              // -> "Hello"
    var b;          // just create
    b;              // -> undefined (the type with the means of nothing is assigned)
    ```
-   tips:
    -   use **;** at the end of each expression (~line);
-   side mentions:
    -   Shift + Enter goes to next line in browser console
