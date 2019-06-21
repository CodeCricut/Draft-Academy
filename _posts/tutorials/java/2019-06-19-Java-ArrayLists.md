---
layout: post
title:  "Java ArrayLists"
categories: java
---
***
## <br/> ArrayLists Overview

Java [Arrays]({{site.baseurl}}/java/2019/06/18/Java-Arrays.html) are somewhat limited in their capability; Their size is not dynamic, and you can't add a item to the next available slot. They are good for some things, but don't fit every usecase.

Say you want to have a grocery list that starts of with 4 things. As the week goes by, you think of more things you want to add to the list. If you were storing the grocery list in an Array, you wouldn't be able to add more items. This is where ArrayLists come in. 

ArrayLists are resizeable Arrays. In other words, they are **dynamic**. You can add items to or remove items off the end of them, and even add or remove items at a specific index. 

# <br/> Adding Items

Let's see how the example we described before would be coded:

```java
List<String> shoppingList = new ArrayList<>();
shoppingList.add("Orange juice");
shoppingList.add("Cat litter");
shoppingList.add("Hamburger buns");
shoppingList.add("Socks");
// initial shopping list: [Orange Juice, Cat litter, Hamburger buns, Socks]
shoppingList.add("Graham crackers");
```

As you can see, we were able to add more items to the ArrayList, which we couldn't do with Arrays.

# <br/> Accessing Items by Index

Continuing our grocery list example, say you want to print every item in the ArrayList. How would you do that? The process would be very similar as looping through an Array, except we use the method `get()` to access items at an index,and we use the method `size()` instead of the attribute `length`.

```java
...
for(int i = 0; i < shoppingList.size(); i++){ // .size() instead of .length
    System.out.println(shoppingList.get(i)); // .get(i) instead of [i]
}
```

If you haven't learned about methods yet, you might be confused about why we used `.size()` and `.get()`, or why there are even parethesis after the words. The reasoning is a little outside the scope of this lesson, but just know that `.size()` tells us the size of the ArrayList, and `.get()` gives us the value of whatever index we put in the parenthesis.

Note: If you are familiar with Foreach loops, you can also iterate over each item by using them.

# <br/> Inserting and Removing Items by Index

Another cool thing about ArrayLists is that you can add or remove items by index. When you add an item, the index of all of the items after automatically get incremented by one, and so does the size of the ArrayList. Conversly, removing items decrements the index of all of the following items and decreases the size by one.

```java
// inserting and removing items
Initial List: ["Santana", "Morrison", "Minaj", "McCartney", "Hendrix"] 
List after .remove(2): ["Santana", "Morrison", "McCartney", "Hendrix"] 
List after .add(1, "Berry"): ["Santana", "Berry", "Morrison", "McCartney", "Hendrix"] 
```

To learn more about ArrayLists and more capailities like `.clear()`, visit the [Java Documentation](https://docs.oracle.com/javase/8/docs/api/java/util/ArrayList.html).


