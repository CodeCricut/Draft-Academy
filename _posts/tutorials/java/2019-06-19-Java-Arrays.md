---
layout: post
title:  "Java Arrays"
categories: java
---
***
## <br/> Arrays Overview

In everyday life, we categorize things into list all of the time. We put related documents into folders, books into bookshelves, and shirts on hanger. When we refer to these things, we usually don't talk about each item one by one; we talk about the group of them as a whole. We say "the folder", "the books", or "the shirts on the hangar" as apposed to "document a, document b, document c...". 

In Java, we often want to group variables just like we do in real life. Luckily for us, there is a way to do this. To group variables, we use **Arrays**. Arrays are simply lists of objects, with a few caveats. Let's look at an example of when we could use Arrays to make our lives easier.

<br/>
Here we have a program that needs to print every letter in the alphabet. Without a grouping mechanism, it is very time consuming and error prone to list out every letter:

```java
char a = 'a';
char b = 'b';
char c = 'c';
char d = 'd';
...

System.out.println(a);
System.out.println(b);
System.out.println(c);
System.out.println(d);
...
```

<br/>

To just print every letter in the alphabet, it would take almost 50 lines. Let's do the same thing, but this time using Arrays:

```java
char[] alphabet = {'a', 'b', 'c', 'e', 'f', 'g', 'h', 'i', 'j', 'k', 
'l', 'm', 'n', 'o', 'p', 'q', 'r', 's', 't', 'u', 'v', 'w', 'x', 'y', 'z'};

for (int i = 0; i < char.length; i++){
    System.out.println(alphabet[i]);
}
```

If you have never seen an Array being used before, you are probably a little confused right now. Let's break down what we just did into steps.

1. Specify what type of variables you want to store in your Array. In our case, we wanted to store variables of type `char`.
2. We type `[]`, which tells Java that we want an Array of type `char`.
3. We give our Array a name. In our case, we named it `alphabet`.
4. We gave our Array a value of `{'a', 'b', 'c', ...}`. This is where we are assigning the Array it's values, or what variables it will actually store. More on this later.


# <br/> Declaring an Array

Java gives us the ability to declare a variable, then assign a value to it later. For a primitive type like `int`, it would look like this:

```java
int num;
```

Once we have the variable, we could assign a value to it like this:

```java
num = 10;
```

We can do the same exact thing with Arrays. To declare an Array, we do the following:
```java
// type[] name;
int[] intArray;
double[] doubleArray;
char[] charArray;
String[] stringArray;
```

We specify the type of Array we are making, then that it is an Array by using `[]`, then give it a good name. 

After we declared the integer `num` up above, we gave it a value. We can do the same thing with Arrays, which will be in a few sections

# <br/> Allocating Memory

Before Java can start adding items into an Array, it needs to know how big the Array is. If the size was unknown, then Java would have to guess at the size, which would either mean there was not enough slots, or way too many. To specify how many spots we want in Array, we do the following:

```java
int[] intArray; // declare the Array
intArray = new int[10]; // allocating memory
```

This would tell Java that we want an Array named `intArray` that has 10 spots. In Java, we call the size or capacity of an Array its **length**. It is useful to know the length of an Array, especially if we want to loop each of its items.

# <br/> Assigning Values

After we declare and allocate memory for an Array, the obvious next step is to put some values inside of it! There are a few ways of doing this. One method is to use an **Array Literal**. An Array Literal is a way of telling Java "Hey, I know how many items I want in the Array, and I know what the values are. Add all of these items in for me." To use an Array Literal, you do the following:

```java
char[] alphabet = {'a', 'b', 'c', ...};
```

We saw this example up above, and hopefully now it makes more sense to you.


Another way of assigning values to an Array is to directly tell Java what each value is equivalent to. 
```java
char[] alphabet = new char[26]; // this should look familiar
alphabet[0] = 'a';
alphabet[1] = 'b';
alphabet[2] = 'c';
...
```

As you can see, we are assigning each value individually. But how are we accessing each slot in the Array 'alphabet'? Well, we are accessing each slot by its **index**. An index is a specific integer given to items in an Array that allows us to access those items individually, rather than the whole Array. An index in Java is very similar to an index in a book; you have a number, and that number corresponds to a specific item in the Array (or book). Indexs in programming are a little funny, though, because they start at 0 instead of 1. 

```java
// 0,   1,   2,       25
[ 'a', 'b', 'c', ..., 'z']
```

This has a few funny results, both good and bad. The first result is good: you can easily loop through an Array with the following for-loop:

```java
for (int i = 0; i < array.length; i++){
    //This will access each array item
}
```

This is useful, however there is also another result: The last index of the Array will be one less than the length of the Array. This is not neccesarily bad, however it does confuse many new programmers.

# <br/> Drawbacks

Although Arrays are very useful, there are some drawbacks to using them. For one, once you tell Java how long you want them to be, you can never change the length again. This means that if you want to have a dynamic list of items, you should use an Array. An ArrayList would be better suited for that purpose, however have not learned about those yet. 

Another disadvantage is that if you try to access a slot in an Array that hasn't been assigned a value, you will crash your program and get a `Null pointer exception`. If your anything like me, you will become very familiar with this error in the future.

Arrays are also limited in that they can only store one type of data. Want to store some names as well as ages in an Array? Well, it's not going to work (not that storing those things together is a good idea, anyway). 

***


# <br/> Conclusion

Arrays are very useful data structures that allow you to store related variables in one container. They make it easy to loop through each item individually, or use refer to all of them as a group. There are drawbacks to using Arrays, however. Their size is fixed, and you can only store variables of the same type in one Array. If you have to store a set number of alike items in a group, then Arrays will work. If you need a data structure that is more flexible, look into [ArrayLists]({{site.baseurl}}/java/2019/06/18/Java-ArrayLists.html), [HashSets](https://docs.oracle.com/javase/7/docs/api/java/util/HashSet.html), or [HashMaps](https://docs.oracle.com/javase/8/docs/api/java/util/HashMap.html).






