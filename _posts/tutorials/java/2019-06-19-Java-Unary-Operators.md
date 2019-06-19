---
layout: post
title:  "Java Unary Operators"
categories: java
---
***
## <br/> Unary Operator Basics

In math, we sometimes put symbols before numbers to denote something about them. For example, we put the '-' sign before numbers below 0, and we can put the '+' symbol to denote numbers above 0.

In Java, we can do the same thing, and a little more. Java has what are called 'Unary Operators'. Unary operators allow you to perform some operation on a number. Unlike arithemetic operators, unary operators perform an operation on one number or variable, not two.

Let's look at some examples.

<br/>
In this example, we want to show that the variable `positive` is positive 1, and the variable `negative` is negative 2:
```java
int positive = +1;
int negative = -2;
```
It should be noted that positive numbers do not require the unary operator `+` to be interpreted as positive by Java.

<br/> There are more unary operators that perform calculations on numbers:

```java
int num1 = 1;
int num2 = 2;

num1++; // this adds one to num1
num2--; // this subtracts one from num2
```

<br/> If you are working with booleans (true or false expressions), you can negate the value of the boolean by using the `!` unary operator. Here are a few examples:

```java
boolean isTired = true;
boolean isAwake = false;
if (! isTired){ // if isTired is false
    isAwake = true;
}
```

To learn more, visit the [Java tutorials](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/op1.html).
