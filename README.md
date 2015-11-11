<a href="http://4yopping.com">
    <img src="http://4yopping.com/4yopping.png" alt="4yopping Logo"
         title="4yopping Logo" align="right" width="120px" height="125px" />
</a>

# 4yopping's Node.js Style Guide

This is a guide for writing consistent and aesthetically pleasing node.js code.
It is inspired by what is popular within the community, and flavored with some
personal opinions.


## Formatting


### 2 Spaces for indentation

Use 2 spaces for indenting your code and swear an oath to never mix tabs and
spaces - a special kind of hell is awaiting you otherwise.


### Use single quotes

Use single quotes, unless you are writing JSON.

*Right:*

```js
var foo = 'bar';
```


### Naming Conventions


### Use UpperCamelCase for class names

Class names should be capitalized using `UpperCamelCase`.

*Right:*

```js
class BankAccount {
}
```

*Wrong:*

```js
class bank_Account {
}
```


### Use lowerCamelCase for function names

Function names should be capitalized using `lowerCamelCase`.

*Right:*

```js
function bankAccount() {
}
```

*Wrong:*

```js
function bank_Account() {
}
```

### Use lowerCamelCase for variables, properties

Variables, properties and function names should use `lowerCamelCase`.  They
should also be descriptive. Single character variables and uncommon
abbreviations should generally be avoided.

*Right:*

```js
var adminUser = db.query('SELECT * FROM users ...');
let myObject = {
	adminUser: 'test'
};
```

*Wrong:*

```js
var admin_user = db.query('SELECT * FROM users ...');
let my_object = {
	admin_user: 'test'
};
```

## Use UPPERCASE for Constants

Constants should be declared as regular variables or static class properties,
using all uppercase letters.

*Right:*

```js
var SECOND = 1 * 1000;

function File() {
}
File.FULL_PERMISSIONS = 0777;
```

*Wrong:*

```js
const SECOND = 1 * 1000;

function File() {
}
File.fullPermissions = 0777;
```

[const]: https://developer.mozilla.org/en/JavaScript/Reference/Statements/const


### Use lowerCamelCase for db (schema) properties

DB properties names should use `lowerCamelCase`.  They
should also be descriptive.

*Right:*

```js
var schema = new Schema({
	isUser:[Boolean],
	ofNumber: [Number],
});
```

*Wrong:*

```js
var schema = new Schema({
	is_user:[Boolean],
	of_number: [Number],
});
```

### Use snake_case for files names

Files names should use `snake_case`.  They
should also be descriptive.

*Right:*

```js
var schema = new Schema({
	isUser:[Boolean],
	ofNumber: [Number],
});
```

*Wrong:*

```js
var schema = new Schema({
	is_user:[Boolean],
	of_number: [Number],
});
```


# Linting

## ES5
Use this file for code in ES5
[View config file](./jshintrc)

## ES6 / ES2015
Use this file for code in ES6 / ES2015
[View config file](./eslintrc)
