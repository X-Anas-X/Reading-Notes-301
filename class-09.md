# _What is functional programming?_
- Functional programming is a programming paradigm a style of building the structure and elements of computer programs that treats computation as the evaluation of mathematical functions and avoids changing-state and mutable data.
* The first fundamental concept we learn when we want to understand functional programming is pure functions.
+ When data is immutable, its state cannot change after it’s created. If you want to change an immutable object, you can’t. Instead, you create a new object with the new value.
>- Functions as first-class entities can:
>> refer to it from constants and variables.
>>> pass it as a parameter to other functions.
>>>> return it as result from other functions.

>- We want the total amount of all books in our shopping cart. Simple as that. The algorithm?
>> filter by book type.
>>> transform the shopping cart into a collection of amount using map.
>>>> combine all items by adding them up with reduce.
- It's important to get your code right the first time because in many businesses there isn't much value in refactoring. 
