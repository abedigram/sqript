# Advanced js - Day 6

## Appx II - Vid 2

-   Scope

    -   means variable access

    ```js
    function aa() {
    	console.log("aa");
    }
    // aa is part of window scope
    window.aa();
    window; // aa is a part of window
    ```

    ```js
    // var a is part of bb scope so is not accessible outside bb
    // functions have access to root scope (outer scope in general)
    var b = "root scope var";
    function bb() {
    	var a = "bb";
    	console.log(a); // log "bb"
    	console.log(b); // log "root scoper var"
    }
    console.log(a); // refrence error
    ```

    ```js
    var b = "root scope var";
    function bb() {
    	b = "bb"; // b is the outer b so will change it
    }
    b; // --> bb
    ```

    ```js
    // root scope (window)
    var fun = 5;

    function funFunction() {
    	// child scope
    	var fun = "hello"; // outer fun is no accessible
    	console.log(fun); // log "hello"
    }

    function funerFunction() {
    	// child scope
    	var fun = "bye"; // outer fun is no accessible
    	console.log(fun); // log "bye"
    }

    function funestFunction() {
    	// child scope
    	fun = "AHHH"; // changes the root fun
    	console.log(fun); // log "AHHH"
    }

    // js looks in the closer scope, if did not find, goes to the outer scope and so on
    console.log(fun); // log 5
    funFunction(); // log "hello"
    funerFunction(); // log "bye"
    funestFunction(); // log "AHHH"
    console.log(fun); // log "AHHH"
    ```

---

## Appx II - Vid 3

-   ternary op

    -   the same as if else but compact

    ```js
    // condition ? expr1 : expr2
    function isUserValid(bool) {
    	return bool;
    }

    var answer = isUserValid(true) ? "granted" : "denied"; // --> granted
    var answer = isUserValid(false) ? "granted" : "denied"; // --> denied

    // traditional if else manner
    function condition(bool) {
    	if (isUserValid(bool)) {
    		return "granted";
    	} else {
    		return "denied";
    	}
    }

    var answer2 = condition(true); // --> granted
    var answer2 = condition(false); // --> denied
    ```

-   switch

```js
function moveCommand(direction) {
	var whatHappens;
	switch (direction) {
		case "forward": // if(direction == "forward")
			whatHappens = "you encounter a monster";
			break;
		case "back": // else if
			whatHappens = "you arrived home";
			break;
		case "right": // else if
			whatHappens = "you found a river";
			break;
		case "left": // else if
			whatHappens = "you run into a troll";
			break;
		default: // else
			whatHappens = "please enter a valid direction";
	}
	return whatHappens;
}
moveCommand("left") // --> "you run into a troll"
```
