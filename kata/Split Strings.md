# **Codewars**
## **Split Strings**

CComplete the solution so that it splits the string into pairs of two characters. If the string contains an odd number of characters then it should replace the missing second character of the final pair with an underscore ('_').

Examples:
```
* 'abc' =>  ['ab', 'c_']
* 'abcdef' => ['ab', 'cd', 'ef']
```
  
## **Solution:**

```JavaScript
function solution(str){
   return str.length ==0 ?  [] : str.length%2 == 1 ? (str+'_').match(/.{2}/g) : str.match(/.{2}/g)
}
```
or 
```JavaScript
function solution(str){
   return (str+"_").match(/.{2}/g)||[]
}
```