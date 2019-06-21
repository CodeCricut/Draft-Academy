---
layout: post
title:  "Java Method Arguments"
categories: java
---
***
## <br/> Argument Basics

In the method examples we looked at in [method basics]({{site.baseurl}}/java/2019/06/19/Java-Methods.html) and [method return keyword]({{site.baseurl}}/java/2019/06/19/Java-Method-Return-Keyword.html), we used varibles within our methods that were declared and initialized at the start of the class. This means that we were free to use the variables as we pleased. But what if we want to use variables that are declared within a seperate method? Any variables declared in a seperate method would unusable by our method due to scope. Luckily, there is a way to pass methods some variables which can then be used by that method, regardless of the scope. 

Let's look at the average number example we looked at in the method return keyword article.

```java
static int num1 = 20;
static int num2 = 10;

public static void main(String[] args) {
    double averageOfNums = averageMethod();
}
public static double averageMethod(){
    double average = (num1 + num2)/2;
    return average;
}
```

If we were to declare `num1` or `num2` inside of the `main` method, then this program would break do to the variables being out of scope for `averageMethod`. How would we solve this problem? By using arguments, we can directly pass `averageMethod` the two variables to use, and the scope will not matter. Here is how we would rewrite the example:

```java
public static void main(String[] args) {
    static int num1 = 20;
    static int num2 = 10;
    double averageOfNums = averageMethod(num1, num2);
}
public static double averageMethod(int num1, int num2){
    double average = (num1 + num2)/2;
    return average;
}
```
We did a few things here:
1. We declared `num1` and `num2` inside of the main method. If we did not use arguments, this would break our program. 
2. We put the variables we just declared in the parenthesis of `averageMethod()` when we called it
3. We put `int num1` and `int num2` in the parenthesis of `averageMethod` when we were writing the method.

Step 2 is where we told Java what values we wanted to pass to `averageMethod()`. Step 3 is where we were defining what variables are acceptable by `averageMethod()`. We are explicity saying that we want the method to take in two integers, and we are giving the integers the name `num1` and `num2`. The variables declared in the method do not have to be named the same thing when calling the method. For example, we could have rewritten this program like this:

```java
public static void main(String[] args) {
    static int num1 = 20;
    static int num2 = 10;
    double averageOfNums = averageMethod(num1, num2);
}
public static double averageMethod(int numberOne, int numberTwo){
    double average = (numberOne + numberTwo)/2;
    return average;
}
```

This fact may be confusing to you, but it is important to realize that **variables declared in a method do not have to be named the same thing as the variables used to call that method**.

# <br/> Reusing Methods

Arguments give methods a lot of versatility. They allow them to perform the same function on multiple sets of data. We could expand the average number program to pring the averages of many numbers by simply calling `averageMethod()` multiple times with different arguments.

```java
public static void main(String[] args) {
    System.out.println(averageMethod(1, 10));
    int ten = 10;
    System.out.println(averageMethod(-12, ten));
    System.out.println(averageMethod(100, 0));
}
public static double averageMethod(int numberOne, int numberTwo){
    double average = (numberOne + numberTwo)/2;
    return average;
}
```

To learn more about method arguments, visit the [Java tutorials](https://docs.oracle.com/javase/tutorial/java/javaOO/arguments.html).