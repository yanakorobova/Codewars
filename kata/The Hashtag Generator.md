# **Codewars**
## **The Hashtag Generator**

The marketing team is spending way too much time typing in hashtags.
Let's help them with our own Hashtag Generator!

Here's the deal:

* It must start with a hashtag (#).
* All words must have their first letter capitalized.
* If the final result is longer than 140 chars it must return false.
* If the input or the result is an empty string it must return false.

### **Examples**

```
" Hello there thanks for trying my Kata"  =>   "#HelloThereThanksForTryingMyKata"
"    Hello     World    "                                =>  "#HelloWorld"
"                                         "                   =>  false
```
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
