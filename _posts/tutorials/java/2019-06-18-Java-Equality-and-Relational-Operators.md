---
layout: post
title:  "Java Equality and Relational Operators"
categories: java
---
***
## <br/> Equality and Relational Operators Overview

A program that follows a strict set of instructions is useful, however is also limited. For example, if we need certain parts of code to only run in certain conditions, then we need to have some way of defining conditions. 

We use conditions all the time when going about our day. For example, we might go to bed if it is past midnight, or go to school or work if it is a weekday. These are conditions that we follow (sometimes loosely). Java follows them exactly. 

Let's take a look at an example you might already be familiar with: [while-loops](/java/2019/06/18/While-Loops.html).

While-loops use a conditional expression that is evaluted before the loop code is run. Inside this conditional expression, you usually have two variables or values and some kind of equality or relational operator (there are exceptions). Each conditional expression evaluates to either `true` or `false`. In the case of a while loop, the loop runs if the conditional expression is `true`. 

Here are some examples of conditional expressions used in while loops, and a description of what the equality or relational operator does:

In this example, the loop runs while `i` is **less than** 10. 
```java
int i = 0;
while (i < 10){
    System.out.println(i);
    i ++;
}
```
<br/>
In this example, the loop runs while `i` is **greater than** 0. 
```java
int i = 10;
while (i > 0){
    System.out.println(i);
    i --;
}
```
<br/>
In this example, the loop runs while `i` is **equal to** 5. 
```java
int i = 5;
while (i == 5{
    System.out.println(i);
}
```
<br/>
In this example, the loop runs while `i` is **less than or equal to** 10. 
```java
int i = 0;
while (i <= 10{
    System.out.println(i);
    i ++;
}
```
<br/>
In this example, the loop runs while `i` is **more than or equal to** 0. 
```java
int i = 10;
while (i >= 0{
    System.out.println(i);
    i --;
}
```
<br/>
<br/>
In this example, the loop runs while `i` is **not equal to** 10. 
```java
int i = 0;
while (i != 10{
    System.out.println(i);
    i ++;
}
```
***
<br/>

## Conclusion

To have a dynamic program, we need a way of defining conditions that when true, will run certain code. Equality and relational operators help give us the ability to do this. We saw that they can be used in [while-loops](/java/2019/06/18/While-Loops.html), and they can also be used in [if statements](/java/2019/06/18/Java-If-Statements.html) and [for-loops](/java/2019/06/19/Java-For-Loops.html).

Equality and relational operators are only part of the equation for defining good conditions. [Unary operators](need to add link) and [conditional operators](need to add link) also help defind conditional expressions. 

For more information on equality and relational operators, see the [Java tutorial](https://docs.oracle.com/javase/tutorial/java/nutsandbolts/op2.html) on the subject.