# Javascript Basics

### Practice Javascript from your web browser

All of the three major browsers - Google Chrome, Mozilla Firefox and Microsoft Edge have a built-in Javascript engine. You can use this to practice your Javascript coding skills. 

To open the Developer Tools from Google Chrome, right-click on any page element and click *Inspect Element*. Select the Console tab (second tab from the left):

![img](https://github.com/JBRC-ph/EmpowermentTechnologies/raw/master/images/Chrome-Developer-Console.png)

### Simple Statements

Run this on the console: `console.log("Hello, world!");`

and watch the console say hello to the world.

### Variables

Use `var #{variable_name}` to declare a variable.

Use `var #{variable_name} = #{value}` to declare and initialize a variable.

Example:

```
var x = 5
var y = 3
```

After initializing the x and y variables, type `x + y` and watch Javascript calculate the sum for you.

Javascript can do [string interpolation](https://en.wikipedia.org/wiki/String_interpolation):

```
var myName = 'Wally';
console.log(`Hello, ${myName}!`);
```

### Conditional Statements

```
var x = 3;
if (x > 2) {
  console.log("x is greater than 2");
} else {
  console.log("x is not greater than 2");
}
```

Another example:

```
var now = new Date();
var hour = now.getHours();
if (hour < 12) {
  console.log("Good Morning!");
} else if ( (hour >= 12) && (hour <= 6) ) {
  console.log("Good Afternoon!");
} else {
  console.log("Good Evening!");
}
```

### Loops

Use a loop when you want to run a stement N times, or until a condition is met.

#### Run a statement 3 times:

```
var i = 0;
while (i < 3) {
  console.log("Hello, world!");
  i = i + 1;
}
```

What happens if you remove the line `i = i + 1;`?

Be careful with unterminated loops! It can crash your browser.

Here's another form of the loop:

```
var i = 0;
do {
  console.log("Hello, world!");
  i = i + 1;
} while (i < 3);
```

What's the main difference between `while-do` and `do-while`?

Here's another form of the loop, this time using the `for` keyword:

```
for (var i = 0; i < 3; i = i + 1) {
  console.log("Hello, world!");
}
```

### Functions

Use functions to encapsulate program logic.

Let's put our greeting logic inside a function:

```
function greeting() {
  var now = new Date();
  var hour = now.getHours();
  if (hour < 12) {
    console.log("Good Morning!");
  } else if ( (hour >= 12) && (hour <= 6) ) {
    console.log("Good Afternoon!");
  } else {
    console.log("Good Evening!");
  }
}
```

After declaring the function, you can conveniently call it with `greeting()`.

### Data Structures

#### Arrays

Use an array to store a list of values.

Example:

```
let myFriends = ["Alice", "Bob", "Charlie"];
for (let friend of myFriends) {
  console.log(`Hello, ${friend}!`);
}
```

#### Objects

```
var bob = {
  name: "Bob",
  age: 21,
  email: "bob@o.a.co"
}

console.log(`Name: ${bob.name}`);
console.log(`Age: ${bob.age}`);
```

### Accessing the Document Object Model (DOM)

#### Access a page element's text

```
document.getElementById('id').innerHTML;
```

#### Access a form element's value

```
document.getElementById('id').value;
```

#### Modify a page element

```
document.getElementById('id').innerHTML = 'new value';
```

#### Modify a form element's value

```
document.getElementById('id').value = 'new value';
```

### Putting it all Together: Create a Pounds to Kilos calculator

Create a simple form with two labels and two input boxes:

```
<html>
  <body>
    <form id="lbs_to_kg_converter">
      <label>Pounds</label>
      <input type="text" id="pounds">
      <br>
      <label>Kilograms</label>
      <input type="text" id="kilograms">
      <br>
      <input type="button" value="Convert">
    </form>
  </body>
</html>>
```

Add an `onClick` event handler to the Convert button. Change this line:

```
<input type="button" value="Convert">
```

to:

```
<input type="button" value="Convert" onclick="convert()">
```

Add the Javascript reference in `<head>`:

```
  <head>
    <script src="converter.js"></script>
  </head>
```

Create the `converter.js` file:

```
function poundsToKilograms(pounds) {
    return pounds * 2.2;
}

function convert() {
    document.getElementById("kilograms").value = 
        poundsToKilograms( document.getElementById("pounds").value );
}
```

### Homework

Create a page that accepts lat/long values of a location and displays a Google Maps vicinity map of the given location.

https://www.w3schools.com/graphics/google_maps_intro.asp
