# Advanced js - Day 7

## Appx II - Vid 4

-   ES6

    -   BABEL
        -   is a library that compiles js code to a version that every browser understands
    -   let

    ```js
    // let creates a new scope inside a {} -- let sees {}
    // var creates a new scoper inside a function() -- var does not see the {}, just function scope
    const player = "moba";
    let experience = 100;
    let wizardLevel = false;

    // if both wizardLevels were `var` both logs would be `true`
    // if outer was var & inner was let would be `inside true` & `outside false`
    // if outer was let & inner was var would create a error
    if (experience > 90) {
    	let wizardLevel = true;
    	console.log("inside", wizardLevel); // 'inside' true
    }
    console.log("outside", wizardLevel); // 'outside' false
    ```

    -   const

    ```js
    // const scope is the same as let -- block level {}

    // const could not get changes after assignment
    const player = "moba";
    player = "mira"; // syntax error

    // const could not declare unassigned
    const player2; // syntax error

    // const is good for function declaration
    const boo = function(){ console.log('boo') };
    boo();

    // const is good for constant values as TAX_RATE
    const TAX_RATE = 0.09;

    // const objects could not get reassigned but properties of const object can change
    const user = {
        name: "moba",
        experience: 50
    };
    user = {name:"mira"} // syntax error
    user.experience = 60 // --> 60 -- user --> {name:"moba", experience: 60}
    ```

    -   object destructuring

    ```js
    const obj = {
    	player: "moba",
    	experience: 100,
    	wizardLevel: true,
    };

    /* 7 */ const player = obj.player;
    /* 8 */ const experience = obj.experience;
    /* 9 */ let wizardLevel = obj.wizardLevel;

    // below does the same thing as line 7 & 8 & 9
    const { player, experience } = obj;
    let { wizardLevel } = obj;
    ```

    -   object properties (keys)

    ```js
    // below is the way of dynamically creating object keys
    const name = "moba";
    const obj = {
        [name]: "Mohammad", // moba: "Mohammad",
        ["mira" + "geeta"]: "mira" // mirageeta: "mira"
        [1+2]: 100 // 3: 100
    }
    ```

    ```js
    const a = "moba";
    const b = true;
    const c = {};

    const obj = {
    	a, // a:a  // a:"moba"
    	b, // b:b  // b: true
    	c, // c:c  // c: {}
    };
    ```
    
    - template strings
    ```js
    const name = "moba"
    const age = 24;
    const pet = "cat"

    greeting = "Hello " + name + ". You seem to be " + (age-10) + ". What a nice " + pet + "!";
    
    // using bacticks (`), u can write cleaner dynamic strings
    greetingTemplStr = `Hello ${name}. You seem to be ${age-10}. What a nice ${pet}!`;
    ```
    
    - default arguments
    ```js
    // functions could have default arguments for their parameters
    // so they can be called without the arguments passed
    function greet(name='', age=50, pet="cow") {
        `Hello ${name}. You seem to be ${age-10}. What a nice ${pet}!`;
    }
    greet();                // 'Hello . You seem to be 40. What a nice cow!'
    greet("moba", 24, cat); // 'Hello moba. You seem to be 14. What a nice cat!'
    ```
    - symbols
        - another js type
        - makes unique types, whether having the same value
    ```js
    // symbols are used to create object properties (keys) so they become unique with same names
    let s1 = Symbol();
    let s2 = Symbol('boo');
    let s3 = Symbol('boo');
    
    s2 === s3 // false
    s2 == s3  // false

    s2 === s2 // true
    ```
    - arrow functions
    ```js
    function add(a, b){
        return a+b;
    }
    // arrow functions does not need return expr. if they have `single line unblocked` expr. like below
    const add_ar = (a, b) => a + b;

    add(1,2) === add_ar(1,2) // true
    ```