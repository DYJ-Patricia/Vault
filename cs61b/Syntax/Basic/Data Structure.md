---
date: 2025-03-12
tags:
  - Java
---

## Arrays (fixed-size)[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0b#arrays-fixed-size "Direct link to Arrays (fixed-size)")

Java arrays are a lot like Python lists. However, Java arrays are _fixed-size_, so we can't add or remove elements (that is, no `append`, `remove`, etc.).

|Python|Java|
|---|---|
|```<br>zeroedLst = [0, 0, 0]lst = [4, 7, 10]lst[0] = 5print(lst[0])print(lst)print(len(lst))<br>```|```<br>int[] zeroedArray = new int[3];int[] array = {4, 7, 10};array[0] = 5;System.out.println(array[0]);System.out.println(Arrays.toString(array));System.out.println(array.length);<br>```|

- In `new int[3]`, the `int` is the type in the array; and `3` is the length. With this syntax, all elements take on their "default value". For `int`, this is 0.
- Arrays do not print nicely, for reasons beyond the scope of HW 0. To print an array, you can call `Arrays.toString(array)`.
- Arrays do not have a length _method_. It is an _instance variable_, so it does not have parentheses.
- Java does **not** support _negative indexing_ or _slicing_.

## Foreach Loop / Enhanced For Loop[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0b#foreach-loop--enhanced-for-loop "Direct link to Foreach Loop / Enhanced For Loop")

|Python|Java|
|---|---|
|```<br>lst = [1, 2, 3]for i in lst:    print(i)<br>```|```<br>int[] array = {1, 2, 3};for (int i : array) {    System.out.println(i);}<br>```|

- Notice the type declaration of the iterating variable, as well as the usage of `:` instead of `in`.
- We can also use this syntax on certain other types, such as `List`s and `Set`s.

## Lists (resizable)[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0b#lists-resizable "Direct link to Lists (resizable)")

|Python|Java|
|---|---|
|```<br>lst = []lst.append("zero")lst.append("one")lst[0] = "zed"print(l[0])print(len(l))if "one" in lst:    print("one in lst")for elem in lst:    print(elem)<br>```|```<br>List<String> lst = new ArrayList<>();lst.add("zero");lst.add("one");lst.set(0, "zed");System.out.println(lst.get(0));System.out.println(lst.size());if (lst.contains("one")) {    System.out.println("one in lst");}for (String elem : lst) {    System.out.println(elem);}<br>```|

- Java has the `List` interface. We largely use the [`ArrayList`](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/ArrayList.html) implementation.
- The `List` interface is _parameterized_ by the type it holds, using the angle brackets `<` and `>`.
- `List`s, again, do not support slicing or negative indexing.

## Sets[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0b#sets "Direct link to Sets")

|Python|Java|
|---|---|
|```<br>s = set()s.add(1)s.add(1)s.add(2)s.remove(2)print(len(s))if 1 in s:    print("1 in s")for elem in s:    print(elem)<br>```|```<br>Set<Integer> set = new HashSet<>();set.add(1);set.add(1);set.add(2);set.remove(2);System.out.println(set.size());if (set.contains(1)) {    System.out.println("1 in set");}for (int elem : set) {    System.out.println(elem);}<br>```|

- Java has the `Set` interface. There are two main implementations: [`TreeSet`](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/TreeSet.html), and [`HashSet`](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/HashSet.html). `TreeSet` keeps its elements in "sorted" order, and is fast. In contrast, `HashSet` does not have a defined "order", but is (usually) really fast.
    - We will formalize these notions of "fast" later on in the course when we learn about asymptotic analysis.
- A `Set` cannot contain duplicate items. If we try to add an item already in the set, nothing happens.

## Dictionaries / Maps[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0b#dictionaries--maps "Direct link to Dictionaries / Maps")

|Python|Java|
|---|---|
|```<br>d = {}d["hello"] = "hi"d["hello"] = "goodbye"print(d["hello"])print(len(d))if "hello" in d:    print("\"hello\" in d")for key in d.keys():    print(key)<br>```|```<br>Map<String, String> map = new HashMap<>();map.put("hello", "hi");map.put("hello", "goodbye");System.out.println(map.get("hello"));System.out.println(map.size());if (map.containsKey("hello")) {    System.out.println("\"hello\" in map");}for (String key : map.keySet()) {    System.out.println(key);}<br>```|

- Java has the `Map` interface. There are two main implementations: [`TreeMap`](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/TreeMap.html), and [`HashMap`](https://docs.oracle.com/en/java/javase/17/docs/api/java.base/java/util/HashMap.html). Similarly to sets, `TreeMap` keeps its keys sorted and is fast; `HashMap` has no defined order and is (usually) really fast.
- A `Map` cannot contain duplicate keys. If we try to add a key already in the map, the value is overwritten.
- In the angle brackets, we have the "key type" first, followed by the "value type".
- `Map`s cannot directly be used with the `:` for loop. Typically, we call `keySet` to iterate over a set of the keys, and use those to retrieve the values. One may also iterate over the `entrySet` to get both the keys and values.

## Classes[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0b#classes "Direct link to Classes")

|Python|Java|
|---|---|
|```<br>class Point:    def __init__(self, x, y):        self.x = x        self.y = y    def distanceTo(self, other):        return math.sqrt(            (self.x - other.x) ** 2 +            (self.y - other.y) ** 2        )    def translate(self, dx, dy):        self.x += dx        self.y += dy<br>```|```<br>public class Point {    public int x;    public int y;    public Point(int x, int y) {        this.x = x;        this.y = y;    }    public Point() {        this(0, 0);    }    public double distanceTo(Point other) {        return Math.sqrt(            Math.pow(this.x - other.x, 2) +            Math.pow(this.y - other.y, 2)        )    }    public void translate(int dx, int dy) {        this.x += dx;        this.y += dy;    }}<br>```|

We can use these classes as follows:

|Python|Java|
|---|---|
|```<br>p1 = Point(5, 9)p2 = Point(-3, 3)print(f"Point 1: ({p1.x}, {p1.y})")print("Distance:", p1.distanceTo(p2))p1.translate(2, 2)print(f"Point 1: ({p1.x}, {p1.y})")<br>```|```<br>Point p1 = new Point(5, 9);Point p2 = new Point(-3, 3);System.out.println("Point 1: ( " + p1.x    + ", " + p1.y + ")");System.out.println("Distance: "    + p1.distanceTo(p2));p1.translate(2, 2);System.out.println("Point 1: ( " + p1.x    + ", " + p1.y + ")");<br>```|

## Main[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0b#main "Direct link to Main")

Java programs may also have a special method called `main`. When you execute a program, the `main` method is called. The `main` method runs whatever code is inside, which may call other methods defined within the program.

We define the `main` method with the signature `public static void main(String[] args)`. You will learn the meaning of each part of this signature later in the class. For now, you can treat `main` as a "play button" for the code you have written.

To run the code in the previous example, we may create a `main` method in the `Point` class like this:

|Python|Java|
|---|---|
|```<br>class Point:    # other methods...    # end of Point classif __name__ == '__main__':    p1 = Point(5, 9)    p2 = Point(-3, 3)    print(f"Point 1: ({p1.x}, {p1.y})")    print("Distance:", p1.distanceTo(p2))    p1.translate(2, 2)    print(f"Point 1: ({p1.x}, {p1.y})")<br>```|```<br>public class Point {    // other methods...    public static void main(String[] args) {        Point p1 = new Point(5, 9);        Point p2 = new Point(-3, 3);        System.out.println("Point 1: ( " + p1.x            + ", " + p1.y + ")");        System.out.println("Distance: "            + p1.distanceTo(p2));        p1.translate(2, 2);        System.out.println("Point 1: ( " + p1.x            + ", " + p1.y + ")");    }    // end of Point class}<br>```|

Notice that in Java, the `main` method is defined _within_ a class.

If you are coding in IntelliJ, you can actually "play" the `main` method! IntelliJ will display a green play button to the left of the `main` method's signature. Click it to run the code inside.


## Index of Minimum of a List of Numbers[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0b#index-of-minimum-of-a-list-of-numbers "Direct link to Index of Minimum of a List of Numbers")

|Python|Java|
|---|---|
|```<br>def min_index(numbers):    # Assume len(numbers) >= 1    m = numbers[0]    idx = 0    for i in range(len(numbers)):        if numbers[i] < m:            m = numbers[i]            idx = i    return idx<br>```|```<br>public static int minIndex(int[] numbers) {    // Assume numbers.length >= 1    int m = numbers[0];    int idx = 0;    for (int i = 0; i < numbers.length; i++) {        if (numbers[i] < m) {            m = numbers[i];            idx = i;        }    }    return idx;}<br>```|

## Exceptions[​](https://www.learncs.site/docs/curriculum-resource/cs61b/homeworks/hw0/hw0b#exceptions "Direct link to Exceptions")

Lastly, let's look at how we can throw exceptions in Java compared to Python with previous example.

|Python|
|---|
|```<br>def minIndex(numbers):    if len(numbers) == 0:        raise Exception("There are no elements in the list!")    m = numbers[0]    idx = 0    ...    return m<br>```|
|Java|
|---|
|```<br>public static int minIndex(int[] numbers) {    if (numbers.length == 0) {        throw new Exception("There are no elements in the array!");    }    int m = numbers[0];    int idx = 0;    ...    return m;}<br>```|