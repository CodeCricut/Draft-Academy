---
layout: post
title:  "Java Conditional Operators"
categories: java
---
***
## <br/> Conditional Operators Overview

[Equality and relational operators](/java/2019/06/18/Java-Equality-and-Relational-Operators.html) are useful for making conditional expressions that can be used in [while-loops](/java/2019/06/18/While-Loops.html) and [for-loops](need to add link), but they don't cover every possible condition. For example, what if you only wanted to run some code if two expressions were true? Well, perhaps you could nest some if statements, but then what if you wanted to run some code if any one of a few conditional expressions was true. Unless you copied code into multiple if statements, there would be no way to do this. That is, if **Conditional Operators** didn't exist. 

There are two main condional operators (three in total). They are the AND operator, and the OR operator. As the names suggest, the AND operator only evaluates to true if the condition on the left and right are true, and the OR operator evaluates to true if either condition on the left and right is true.

These operators are used to string together conditional expressions into a larger conditional expression. The AND operator is written as `&&`, and the OR operator is written as `||`.

***

Example of AND operator:

```java
int i = 5;
while (i > 0 && i < 10){
    System.out.println(i);
    i ++;
}
```
The conditional expression only evaluates to `true` if `i` is **more than** 0 and `i` is **less than** 10.
<br/>

Example of OR operator:

```java
int i = -5;
while (i < 0 || i > 10){
    System.out.println(i);
    i ++;
}
```
The conditional expression only evaluates to `true` if `i` is **less than** 0 and `i` is **more than** 10.
<br/>

***

# <br/> Short-Circuit Logic

Conditional operators exibit short-circuiting behavior. Short-circuiting behavior means that the second operand is evaluated only if need be. This means different things for the AND operator and the OR operator. 

In the case of the AND operator, it means that if the operand on the left is false, then the operand on the right is not evaluted. If the first operand is false, there is no reason to evalute the second one, as it can't possibly change the result of the conditional expression.

In the case of the OR operator, it means that if the first operator is true, then the second one is not evaluated. Only one operand needs to be true for the condition to evaluate to true, so there is no reason to evaluate the second operand if the first one is true.

<br/>

To learn more about conditional operators, read about them in the [Java tutorials](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/op2.html).


