---
layout: post
title:  "Java Program Essentials"
categories: java
---
***
## Boilerplate Code

Before you can get to learning how to program in Java, there are a few things you need to setup. Every program includes some basic code that allows other code to run, called ["boilerplate code"](https://www.google.com/search?rlz=1C1GCEA_enUS795US795&ei=1DIJXe6VBYn--gT2pKrAAQ&q=boilerplate+code&oq=boilerplate+c&gs_l=psy-ab.1.0.0i131j0l2j0i20i263j0j0i20i263j0l4.3501.4046..4726...0.0..0.111.222.0j2......0....1..gws-wiz.......0i71.-AlsqD1wKR4).

# <br/> Java Class

For now, the first thing you should include in your Java program is a class which you will nest the rest of your code in. Every Java file requires a class, and the class should be named the same as the file. Take a look:

```java
public class MyClass{
    // I will place all of my code here
}
```

It should be noted that MyClass is simply what I named my class, but you should name your class according to what it does. By convention, class names should be capitalized, and have no spaces.
<br/> Learn more about Java naming conventions in the [Java Documentation](https://www.oracle.com/technetwork/java/codeconventions-135099.html).

# <br/> Main Method

Every program needs a starting point. You might think that the files will simply be read from top to bottom, but that is not the case. The program has to be told where to start explicity. To do this, we need to make a main method. 

```java
public class MyClass{
    public static void main(String[] args){
        // this is where my program will start
    }
}
```

If you are anything like me when I was learning to code, you might be confused. You might be asking yourself, "What does public mean, or static, or void, or String[], or..." 

Take a deep breath. There is no need to worry about what these things mean yet. In time, these things will become clear to you, but for now, there is no reason to learn the meaning of these words. Doing so will only complicate your learning, and make you more confused than you are now. 

All you need to know is that your program begins in this spot when you start it.

# <br/> Importing

Eventually when you start using more complicated data types or using libraries, you will have to *import* some things. Importing things allows you to use code from an outside source inside of your class. You can think of it as simply copying some code, then pasting it as a substitute for your import statement. 

To import something, simply type the import keyword at the top of your class file, followed by the file you want to import. It should be noted that filepaths are seperated by periods, and not slashes like you might commonly see. 

When you learn about ArrayLists, you will have to import them. Below is an example of how to do so.

```java
// import packages at the top of your file, outside your class
import java.util.ArrayList; 

public class MyClass{
    public static void main(String[] args){
        // this is where my program will start
    }
}
```

To learn more, look at the [Java Packages and Importing Tutorial](https://docs.oracle.com/javase/tutorial/java/package/usepkgs.html).

***

## Conclusion

Every program requires most of the items listed, and it will become a habit to include these things in every new program you make. If you have a nice IDE such as [Eclipse](https://www.eclipse.org/ide/) or [IntelliJ](https://www.jetbrains.com/idea/), most of these things will be done automatically when you make a new program. 


Now that the boring stuff is out of the way, we can get to learning to code!