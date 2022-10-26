# **Codewars**
## **Square Every Digit**

Welcome. In this kata, you are asked to square every digit of a number and concatenate them.

For example, if we run 9119 through the function, 811181 will come out, because 92 is 81 and 12 is 1.

Note: The function accepts an integer and returns an integer

## **Solution:**

```JavaScript
function squareDigits(num){
  var answer = [];
  var arrSt = num.toString().split('');
  var arrNum = arrSt.map(Number)
  for (let i = 0; i < arrNum.length; i++) {
  answer.push(arrNum[i]**2);
}  
  var int = parseInt(answer.join(""), 10);
  return int;
}
```