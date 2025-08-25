# JavaScript Syntax Overview

<br>

# Adding JavaScript to HTML

Adding JavaScript to an HTML file
```HTML
<script>
  // JavaScript Code
</script>
```

<br>

Linking a JavaScript file to an HTML file
```HTML
<script src="FILENAME.js"></script>
```

<br>

# Comments

```JavaScript
// Single Line Comment

/*
Multi-Line Comment
*/
```

<br>

# Variables

* JavaScript has dynamic typing (Data types are determined automatically meaning that the user doesn't have to specify it)

## Primitive Data Types

* A value is only primitive when it's not an object

| Primitve Data Type | Description |
| --- | --- |
| String | Textual data (Can also be a template literal using `${VARIABLE_NAME}` to insert the value of a variable into a string) |
| Number | Numeric data (Always has decimals even if we don't see them) |
| BigInt | Larger integers than the Number type can hold |
| Boolean | Logical `true` or `false` |
| Null | Intentional absence of any object value (An empty value) |
| Undefined | A declared variable that hasn't been assigned a value yet |
| Symbol | A value that's unique and can't be changed

<br>

## Objects

| Object Type | Description |
| --- | --- |
| Object | A collection of key-value pairs |
| Array | An ordered collection of values |
| Function | A callable block of code |

<br>

Block scope variable (*Only accessible within the `{}` it's declared in*)
```JavaScript
let VARIABLE_NAME = VALUE;
```

<br>

Global scope variable (*Globally accessible*)
```JavaScript
var VARIABLE_NAME = VALUE;
```

<br>

Block scope variable where the value will always remain the same and can't be mutated (*Only accessible within the `{}` it's declared in*)
```JavaScript
const VARIABLE_NAME = VALUE;
```

<br>

Assign a new value to a variable
```JavaScript
VARIABLE_NAME = NEW_VALUE;
```

<br>

# Type Coersion

* JavaScript will automatically convert one of the values to match the other one when dealing with two values that aren't the same type

<br>

# Truthy and Falsy Values

The following automatically becomes true or false when converting to a boolean
* Falsy values: `0`, `undefined`, `null`, `NaN`, `""`
* Truthy values: Anything that's not a falsy value