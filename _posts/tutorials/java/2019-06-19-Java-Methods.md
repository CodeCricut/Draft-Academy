---
layout: post
title:  "Java Methods"
categories: java
---
***
## <br/> Method Basics

As you begin to develop your coding skills and build larger and larger programs, you will need a way to organize your code. Up to this point, you have probably been using code comments. Code comments are good, however they aren't a solve-all solution. They may annotate your code, but they don't really present a clear list of steps. This is where **methods** come in. 

For now, you can think of methods like little containers of code. These containers perform specific functions, and can work with each other to accomplish a bigger goal. Let's look at an example to give you a better understanding of what methods can do in their simplest form. 

Here is a simple program that loops through an Array of scores and prints the grade based on their value, as well as a message based on the grade:

```java
// Grading Script
int[] scores = {87, 96, 58, 78, ..., 95};
char grade;

public static void main(String[] args) {
    for (int i = 0; i < scores.length; i++){
        System.out.print("Grade: ");
        if (score >= 90){
            grade = 'A';
        }
        else if (score >= 80){
            grade = 'B';
        }
        else if (score >= 70){
            grade = 'C';
        }
        else if (score >= 60){
            grade = 'D';
        }
        else {
            grade = 'F';
        }
        System.out.println(grade);
        if (grade = 'A'){
            System.out.println("Great Job!");
        }
        else if (grade = 'B'){
            System.out.println("Keep it up.");
        }
        else if (grade = 'C'){
            System.out.println("Nice job. Can you get an A next time?");
        }
        else {
            System.out.println("You got this next time!");
        }
    }
}
```

Now, maybe it's just me, but this seems pretty hard to read. I have to skim through the entire thing just to get the gist of what it does. Wouldn't it be better if I could group the code in a way that allowed me to only have to read the main points? Methods allow us to do that (and much more). 

Here is the code rewritten using methods:

```java
// Grading Script
int[] scores = {87, 96, 58, 78, ..., 95};
char grade;

public static void main(String[] args) {
    for (int i = 0; i < scores.length; i++){
        DetermineStudentGrade()
        System.out.println("Grade: " + grade;);
        PrintEncouragingMessage();
    }
}

private static void DetermineStudentGrade(){
    if (score >= 90){
            grade = 'A';
        }
        else if (score >= 80){
            grade = 'B';
        }
        else if (score >= 70){
            grade = 'C';
        }
        else if (score >= 60){
            grade = 'D';
        }
        else {
            grade = 'F';
        }
}

private static void PrintEncouragingMessage(){
    if (grade = 'A'){
            System.out.println("Great Job!");
        }
        else if (grade = 'B'){
            System.out.println("Keep it up.");
        }
        else if (grade = 'C'){
            System.out.println("Nice job. Can you get an A next time?");
        }
        else {
            System.out.println("You got this next time!");
        }
}
```

Rewriting the code like this may be longer, but it is much cleaner and easier to understand. As long as you name your methods well, you (or anyone else) reading your code will not have to read every single line to understand what the program is doing. In a way, you are making a summary of your code by using methods. 

This is an important idea in programming, and computer science in general, called **abstraction**. Abstraction is simplification of a process. It is a way of presenting the effect of a process, rather than the exact steps taken to result in that effect. We use abstraction all of the time in our day to day lives, whether we know it or not. 

Here are a few examples of abstraction:
 * We don't need to know how a car works internally to drive it
 * We don't think of all of the bits and bytes that travel when we use credit cards
 * We don't need to know about intermolecular forces to use a rubber band
 * We don't need to think about fluid dynamics to draw a bath

These are just a few, perhaps hyperbolic, examples of when we use abstraction in the real world. 


# <br/> More Method Features

Methods are very useful for abstracting code, as we have seen. But what happens when we need some code to return some type of value. For example, what if we want a method that returns the average of three numbers? As it turns out, methods can actually return a value. Read more about it [here](need to add link).

Okay, so we can return a value. But what if we need to pass in a value. I mean, in the example we just used, we would need some way of passing the method the values we want to find the average of. Surprise, surprise, it turns out we can pass methods variables. These variables are called arguments, and you can learn all about them [here](need to add link).

If you are still interesed in methods after following the pages linked above, visit the [Java tutorial](https://docs.oracle.com/javase/tutorial/java/javaOO/methods.html).