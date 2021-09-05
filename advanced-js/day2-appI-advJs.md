# Advanced js - Day 2

## Appx I - Vid 5

-   if statement:

    ```js
    var name = "moba";
    // var name = "mia";
    // var name = "mira";

    if (name === "moba") {          //check if name is moba
    	alert("hi moba!");
    } else if (name === "mia") {    // then check if it is mia
    	alert("hi mia!");
    } else {                        // name's neighther moba nor mia
    	alert("hi dear ananymous!");
    }
    ```

-   logic ops:

    ```js
    var name = "mana";

    // the || is true if one is true
    name === "mana" || name === "mia";      // true
    true || false;  // true

    // the && is true if both are true
    name === "mana" && name === "mia";      // false
    true && false;  // false

    // the ! is reverses the truthy
    name === "mana" && !(name === "mia");   // true
    true && !false; // true
    ```

---

## Appx I - Vid 6

-   run js on a webpage
    ```html
    <!-- put this at the bottom of body tag -->
    <script type="text/javascript">
    	alert("Hello");
    </script>

    <!-- import from a .js file -->
    <script type="text/javascript" src="path/to/index.js"></script>
    ```
    -   the js file
    ```js
    // index.js
    alert("Hello");
    ```
    -   print out st. in browser console
    ```js
    console.log("text to printed in browser console");
    ```
-   tips:
    -   put script tag at the end of body
        -   putting it on the head tag will cause page to wait for loading heavy scripts
        -   so let the markup load first, then js stuff
