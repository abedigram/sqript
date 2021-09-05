# Advanced js - Day 3

## Appx I - Vid 7

-   functions

    -   () means execute
        -   without writing it just the func def will be printed

    ```js
    // first way to declare a func
    function sayHello() {
    	console.log("hello");
    }
    // functions need to be called
    sayHello();
    ```

    ```js
    // second way: function expression
    sayBye = function () {
    	console.log("bye");
    };
    // function() is an anonymous func and sayBye has the ref to it
    // it could be not anonymous like below:
    // sayBye = function byebye(){
    sayBye();
    ```

    ```js
    // DRY (do not repeat yourself)
    // with function args u can do the same action with multiple inputs
    function sing(song) {
    	console.log(sing);
    }
    sing("do");
    sing("re");
    sing("me");
    ```

    ```js
    // to get st. out of a func, use return
    function mul(a, b) {
    	// a & b are paremeters whereas 3 & 5 are arguments
    	return a * b;
    }
    // if u dont return anything, output will be undefined
    var a = mul(3, 5); // a --> 15

    // when multiple, the first return just do the output and function stops execution
    function mult(a, b) {
    	return a * b;
    	return a;
    	return b;
    } // returns a*b
    ```

    ```js
    // functions are variables so they can passed to another function
    alert(mul(3, 5)); // --> alert(15)
    ```

---

## Appx I - Vid 8

-   array

    -   array is a data structure
        -   a data structure stores data and helps to explore data
            -   as sorted drawers do to find docs

    ```js
    var list = [1, 2, 3];
    // array could store data of any type (not recomended)
    var list_2 = [
    	1,
    	true,
    	undefined,
    	"bib",
    	function apple() {
    		console.log("apples");
    	},
    ];
    // array order starts at 0
    list[1]; // --> true
    list[4]; // -->  f apple
    // arrays could store arrays
    var list_3 = [[1, 2, 3]];
    list_3[0]; // --> [1, 2, 3]
    list_3[0][1]; // --> 2
    ```

    ```js
    // arrays have build-in functions:
    var list = ["cat", "tiger", "bear", "bird"];
    list.shift(); // --> "cat" -- list --> ["tiger", "bear", "bird"]
    list.pop(); // --> "bird" -- list --> ["tiger", "bear"]
    list.push("elephant"); // 3 (length) list --> ["tiger", "bear", "elephant"]
    newlist = list.concat(["bee", "deer"]); // --> ["tiger", "bear", "elephant", "bee", "deer"] -- list --> ["tiger", "bear", "elephant"]
    list.sort(); // --> ["bear", "elephant", "tiger"]

    // google w3c array methods for more
    ```
