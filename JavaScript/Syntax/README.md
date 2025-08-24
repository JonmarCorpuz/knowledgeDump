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

# Variables

## Primitive Data Types

| Primitve Data Type | Description |
| --- | --- |
| String | Textual data |
| Integer | Whole numeric data |
| Double | Floating point numeric data |
| Boolean | Logical true or false values |
| Null | Intentional absence of any object value |
| Undefined | A declared variable that hasn't been assigned a value yet |

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

Block scope variable where the value always remains the same (*Only accessible within the `{}` it's declared in*)
```JavaScript
const VARIABLE_NAME = VALUE;
```

<br>

