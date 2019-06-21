---
layout: post
title:  "Java Method Return Keyword"
categories: java
---
***
## <br/> The Return Keyword

If you already know about the basics of methods, you know that they are extremely useful. They help us abstract our code into modular pieces, and overal give our programs a better and easier to follow flow. However, with the knowledge of methods that we learned in [this]({{site.baseurl}}/java/2019/06/19/Java-Methods.html) lesson, there is still more to be desired. If we ever need to return a specific value from a method, then we need some way of retrieving that value. 

Up to this point, we have been using methods to do things like change the value of variables and print to the console. These are what we call [side effects](https://en.wikipedia.org/wiki/Side_effect_(computer_science)) in the computer science world. Since the main point of the method is not to do these things, they are side effects. 

So you may be asking, "if changing the value of a variable or printing to the console is a side effect, then what is the main point of a method?" Technically speaking, the point of a method in Java is to perform an operation. Operations often equate to some value, and many times we want to retrieve this value without having to use a side effect. Methods allow us to return such values with a `return` keyword.

If I wanted to write a method that found the average of two numbers and **return** the value, I could do it like this:

```java
static int num1 = 20;
static int num2 = 10;

public static double averageMethod(){
    double average = (num1 + num2)/2;
    return average;
}
```

This very simple method finds the average of two numbers, then uses the keyword `return` to return the average that was found. 

Once you have a method that returns a value, you can store the value in a new or existing variable of the same type.
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

To access the value returned by the method, we simply set a variable equal to the name of the method. Notice that we used double in three places here: 
1. As the return type of the method
2. As the data type for `average`
3. As the date type for `averageOfNums`

Generally when you want to access a return variable from a method, the variable type that your are declaring should match the return type. Sometimes an [implicit conversion](https://docs.scala-lang.org/tour/implicit-conversions.html) can be done, but it is good practice to always match the data types.

To learn more about the return keyword, visit the [Java tutorial](https://docs.oracle.com/javase/tutorial/java/javaOO/returnvalue.html).

