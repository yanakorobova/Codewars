# **Codewars**
## **Remove anchor from URL**

Complete the function/method so that it returns the url with anything after the anchor `(#)`removed.
Here's the deal:

Examples
"www.codewars.com#about" --> "www.codewars.com"
"www.codewars.com?page=1" -->"www.codewars.com?page=1"

## **Solution:**

```JavaScript
function generateHashtag (str) {
  if (str.trim() !== ''){
    newStr = '#' + str.split(/ +/g).map( a=> a[0].toUpperCase()+a.slice(1)).join('') 
    return newStr.length <= 140 && newStr
  }
  else return false
}
```