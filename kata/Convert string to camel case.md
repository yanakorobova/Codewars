# **Codewars**
## **Convert string to camel case**

Complete the method/function so that it converts dash/underscore delimited words into camel casing. The first word within the output should be capitalized **only** if the original word was capitalized (known as Upper Camel Case, also often referred to as Pascal case).

**Examples**

```
"the-stealth-warrior" gets converted to "theStealthWarrior"
"The_Stealth_Warrior" gets converted to "TheStealthWarrior"
```

## **Solution:**

```JavaScript
function toCamelCase(str){
  return str.split(/[-_]/).map((a,i) =>{
     return i != 0 ? a[0].toUpperCase() + a.slice(1) : a
}).join('')
}
```