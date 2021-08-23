#js

1) When we compare two variables of different type e.g. a boolean with a string or a number with String using `==` operator, it automatically converts one type into another and return value based upon content equality, while `===` operator is strict equality operator in Java, and only return true if both variable of same type and also contains same value. This will be much clear with following example of `==` and `===` operator in JavaScript :

```js
0==false   // true, because false is equivalent of 0
0===false  // false, because both operands are of different type
2=="2"     // true, auto type coercion, string converted into number
2==="2"    // false, since both operands are not of same type
```



2)  `==` operator is known as type coercion operator and anytime if both values are same and compared using `==` operator, type coercion happens. On the other hand `===` is known as strictly equality operator. It's much similar Java's equality operator (`==`), which gives compilation error if you compare two variables, whose types are not compatible to each other. In fact, you should always use `===` operator for comparing variables or just for any comparison.

3)  While comparing variable using strict equality operator in Java, two object are strictly equal to each other if both are of same type and they refer to same instance. Similarly two String are equal to each other if contents of each others are same e.g. same characters at same position. Another good follow-up question is what would be result of comparing null and undefined using `==` and `===` operator in JavaScript. Well answer is simple, when you use `==` operator it will return true, while if you use `===` or strict equality operator, it will return false. 

4) One more follow-up question of `==` vs `===` operator is difference between != and !== operator in JavaScript. I think it's pretty easy to deduct that !== operator is strict non equality operator, which will take type into consideration while comparing two variables or two values in JavaScript.

5) Last but not the least question related to this JavaScript interview question is, what happen if you compare Nan with any number or Nan itself, using  `===` operator,  You should remember that NaN (Not a Number) is not equal to anything, including NaN.