# Java Strings and Arrays Workshop

## Learning Objectives
- Use common Java string operations to manipulate a URL
- Use arrays to store collections of data

## Strings and String Methods

There are lots of methods supplied with the String class which will allow you to manipulate Strings in a variety of ways. These are similar in many ways to the ones found in other languages such as JavaScript but they often come with their own specific syntax (this is the case with most programming languages).

### Defining Strings 

As we've already seen defining a String and outputting it is as simple as doing:

```java
package com.booleanuk;

public class Main {
    String name = "Ada Lovelace";

    public static void main(String[] args) {
        Main main = new Main();
        System.out.println(main.name);
    }
}
```

and then running the code using `main()` as the entry point.

We can do lots of other things once we have a String defined.

### Accessing Specific Characters from the String

We can use the `charAt()` to get the character at a given index (with 0 being the first letter).

`System.out.println(main.name.charAt(4));`

We can't get to the final letter directly however using -1 as we can in some other languages:

`System.out.println(main.name.charAt(-1));`

This will cause an error, instead we need to find the length of the String and use one less than it to get to the final character:

`System.out.println(main.name.charAt(main.name.length()-1));`

### Replace

We can replace individual characters or sequences of characters using the replace method

`System.out.println(main.name.replace("da", "nd"));`

## Investigate the following ways of manipulating Strings

Use the documentation supplied by Oracle to help: [Documentation](https://docs.oracle.com/en/java/javase/18/docs/api/java.base/java/lang/String.html#method-summary)

- Change Case 
- Remove Whitespace 
- Accessing sub-strings 
- Concatenation

## StringBuilder and its Methods

When you start using loops in Java and manipulating Strings inside them one of the warnings you will get from IntelliJ is that you are using Strings inside a loop when a StringBuilder might be more appropriate. The StringBuilder class in Java is closely related to Strings but is used whenever you need to build a String dynamically as you go along. 

It has a wide range of useful methods that you can use (including a reverse() method to return the reverse of the StringBuilder object).

```
StringBuilder mySB = new StringBuilder(main.name);
System.out.println(mySB.reverse());
```

Have a play with using StringBuilder using some of the documentation here: [Documentation](https://docs.oracle.com/en/java/javase/18/docs/api/java.base/java/lang/StringBuilder.html)

## Arrays and Array Methods

### Defining an array

Arrays are sequences of values that can be accessed and changed. All the elements in an array have to be of the same type, so to define an array of ints we can do:

`int[] numbers = {3, 5, 7, 9};`

Which creates an array of 4 ints. Add the `numbers` array above to the Main class as a member below the `name` variable.

If we want to see the whole array then we would need to use the following code (typing the Arrays part will cause IntelliJ to add an import for it at the top).

`System.out.println(Arrays.toString(main.numbers));`

Just doing 

`System.out.println(main.numbers);`

causes it to print out an identifier for the Array object rather than the array itself.

We can't add extra values in as the size of the array is fixed when we create it. We can access any of the values in the array and we can change them at any time using their index. So we can access the third value in it in the `main()` method as shown:

`System.out.println(main.numbers[2]);`

We could replace the value at that point with another value and then check it using:
```
main.numbers[2] = 21;
System.out.println(Arrays.toString(main.numbers));
```

Some documentation on arrays can be found [here](https://www.w3schools.com/java/java_arrays.asp).


