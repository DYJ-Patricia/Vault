---
date: 2025-03-12
tags:
  - Java
---

## Types

|Python|Java|What?|
|---|---|---|
|`bool`|`boolean`|Python uses `True` and `False`; Java uses `true` and `false`.|
|`int`|`int`|While Python `int`s are unbounded, Java `int`s have a (large) max and min value.|
|`float`|`double`|Decimal values. Java `doubles` are again bounded.|
|`str`|`String`|Java `String`s use double quotes (`"`), and can be any text.|
|no equivalent|`char`|Java `char` represents a _single_ character, and uses single quotes (`'`).|

   原文出处[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0a#comments "Direct link to Comments")

## Comments

|Python|Java|
|---|---|
|```<br># This is a single line comment.<br>```|```<br>// This is a single line comment.<br>```|

Java also has multi-line comments that are started by `/*` and ended by `*/`.

## `while` Loop[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0a#while-loop "Direct link to while-loop")

|Python|Java|
|---|---|
|```<br>i = 0while i < 10:    print(i)    i += 1<br>```|```<br>int i = 0;while (i < 10) {    System.out.println(i);    i++;}<br>```|

- The parentheses, `(` and `)` around the condition are required.
- In Java, `++` is often used instead of `+= 1`.
- We really do use `System.out.println` to print in Java. Sorry.
- Instead of indenting, we use curly braces, `{` and `}` to wrap the code that is part of the while loop. Java doesn't require indenting, but it's good style!

## `for` Loop (counting up)[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0a#for-loop-counting-up "Direct link to for-loop-counting-up")

|Python|Java|
|---|---|
|```<br>for i in range(10):    print(i)<br>```|```<br>for (int i = 0; i < 10; i ++) {    System.out.println(i);}<br>```|

In Java, the `for` loop has the syntax:

```
for (initialization; termination; increment) {    // loop body}
```

This is roughly equivalent to the while loops:

|Python|Java|
|---|---|
|```<br>initializationwhile termination:    # loop body    increment<br>```|```<br>initializationwhile (termination) {    // loop body    increment}<br>```|

The `while` loops and the `for` loop exit when the termination condition is false. The `for` loops in the comparison table go "until" `i = 10`.

## `for` Loop (counting down)[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0a#for-loop-counting-down "Direct link to for-loop-counting-down")

|Python|Java|
|---|---|
|```<br>for i in range(9, -1, -1):  print(i)<br>```|```<br>for (int i = 9; i >= 0; i --) {  System.out.println(i);}<br>```|

- Note the different "initialization", "termination", and "increment" blocks in the Java `for` loop.
- Similarly to `++`, `--` is often used instead of `-= 1`.
- The `for` loops in the comparison table go "until" `i < 0`.

## Conditionals[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0a#conditionals "Direct link to Conditionals")

|Python|Java|
|---|---|
|```<br>if i % 3 == 0 and i % 5 == 0:    print("FizzBuzz")elif i % 3 == 0:    print("Fizz")elif i % 5 == 0:    print("Buzz")else:    print(i)<br>```|```<br>if (i % 3 == 0 && i % 5 == 0) {    System.out.println("FizzBuzz");} else if (i % 3 == 0) {    System.out.println("Fizz");} else if (i % 5 == 0) {    System.out.println("Buzz");} else {    System.out.println(i);}<br>```|

The boolean operators are as follows:

|Python|Java|
|---|---|
|`and`|`&&`|
|`or`|`|
|`not`|`!`|
|`==`|`==`|

- Note the difference between `elif` and `else if`.
- NOTE: In Java, `==` is used for identity, and `.equals()` is used for equality. For primitive types, this means the same thing, but for reference types, it may be different. For this assignment, you do not need to know the difference; we'll learn more about this later.

## Exponentiation[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0a#exponentiation "Direct link to Exponentiation")

|Python|Java|
|---|---|
|```<br>x = 2**10<br>```|```<br>int x = Math.pow(2, 10);<br>```|

Note that `^` in Java is the "XOR" operator, not the exponentiation operation. That is, `2 ^ 10` is valid code, but it will return `8`, not `1024`.

## Function Declaration and Usage[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0a#function-declaration-and-usage "Direct link to Function Declaration and Usage")

|Python|Java|
|---|---|
|```<br>def greet(name):    return "Hello, " + name# Elsewhere...print(greet("Josh"))<br>```|```<br>public static String greet(String name) {    return "Hello, " + name;}// Elsewhere...System.out.println(greet("Josh"));<br>```|

- In Java, functions have a specific return type that comes before the function name. Functions also specify their arguments' types.
    - When a function returns nothing, it has a return type of `void`.
- For now, all our functions will have `public static` in front. We'll learn what these mean later.
- Calling a function looks the same as in Python.

## Strings[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0a#strings "Direct link to Strings")

|Python|Java|
|---|---|
|```<br>s = "hello"s += " world"s += str(5)s_length = len(s)substr = s[1:5]c = s[2]if "hello" in s:    print("\"hello\" in s")for letter in s:    print(letter)<br>```|```<br>String s = "hello";s += " world";s += 5;int sLength = s.length();String substr = s.substring(1, 5);char c = s.charAt(2);if (s.indexOf("hello") != -1) {    System.out.println("\"hello\" in s");}for (int i = 0; i < s.length(); i++) {    char letter = s.charAt(i);    System.out.println(letter);}<br>```|

- In Java, `String`s are not directly iterable. We either iterate over an index and use `charAt`, or we convert it to an array (coming soon).
- In Java, you can add anything to a `String`s, and it will be implicitly converted to a `String` without needing to explicitly cast.


## Hello World[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0a#hello-world "Direct link to Hello World")

|Python|Java|
|---|---|
|```<br>print("Hello World")<br>```|```<br>public class HelloWorld {    public static void main(String[] args) {        System.out.println("Hello World");    }}<br>```|



