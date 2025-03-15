---
date: 2025-03-14
---

继承与实现！继续学习 Java 的编程特性，同时更加深入地学习列表等数据结构！这一节的内容主要包括：继承，转换，扩展，高阶函数，多态与 Java 库和包，我们书接上文，从我们熟悉的 SLList 和 DLList，AList 讲起······

假设我们有一个计算最长单词的函数：
```Java
public static String longest(SLList<String> list) {
    int maxDex = 0;
    for (int i = 0; i < list.size(); i += 1) {
        String longestString = list.get(maxDex);
        String thisString = list.get(i);
        if (thisString.length() > longestString.length()) {
            maxDex = i;
        }
    }
    return list.get(maxDex);
}
```

对于 AList 类型的列表怎么办？我们当然可以使用函数重载(Overload，类比 C++)，写两个一模一样的方法：

```Java
public static String longest(AList<String> list) {  
    int maxDex = 0;  
    for (int i = 0; i < list.size(); i += 1) {  
         String longestString = list.get(maxDex);  
         String thisString = list.get(i);  
         if (thisString.length() > longestString.length()) {  
             maxDex = i;  
        }  
    }  
     return list.get(maxDex);  
 }
```
真是颇费笔墨！呃啊！代码维护性降低了！以后有新的列表类型加入时还得再写一遍！

类比 C++中子类与父类的操作，我们直接掏出**Inheritance**，御敌于国门之外——

[![subclass](https://joshhug.gitbooks.io/hug61b/content/assets/subclass.png)](https://joshhug.gitbooks.io/hug61b/content/assets/subclass.png "subclass")

subclass

#### Interface Inheritance

##### 接口继承

首先登场的是接口继承(虽然这个翻译怪怪的)！选用 `List61B` 作为二者的超类，注意这里的语法规则：

```Java
public interface List61B<Item> {
    public void addFirst(Item x);
    public void add Last(Item y);
    public Item getFirst();
    public Item getLast();
    public Item removeLast();
    public Item get(int i);
    public void insert(Item x, int position);
    public int size();
}
```

接下来，我们在两个子类中**分别实现上述方法**即可，注意声明类的时候的特殊语法！

```Java
public class AList<Item> implements List61B<Item>{...}
```

`implements List61B<Item>` 本质上是一个承诺。AList 表示**“我承诺我将拥有并定义 List61B 接口中指定的所有属性和行为”**，二者的关系实际上是**”is-a”**，不是**“has-a”**

##### Overriding

在子类中实现所需的功能时，在方法签名的顶部包含 `@Override` 标签是有用的（实际上在 61B 中是必需的）。在这里，我们只为一个方法做了这样的操作。

```Java
@Override
public void addFirst(Item x) {
    insert(x, 0);
}
```

即使不包括此标签，也可以覆盖该方法。因此，在技术上不必包括它。但是，包括标签可以作为程序员的保障，向编译器发出警告，表明您打算覆盖此方法。假设要覆盖 `addLast` 方法。如果您入错误并意外地写成 `addLsat` 会怎么样？如果不包括@Override 标签，那么可能无法发现错误。而如果您包括@Override，编译器将会停止并提示在程序运行之前修复错误。

#### Implement Inheritance

##### 实现继承

我们也可以在超类中即对某些方法进行实现，对于不需要重写该方法的子类，调用该方法即直接调用超类的实现，而也有的子类需要重写该方法，再各做修改即可。为了做到这一点，必须在方法签名中包含 `default` 关键字。

```Java
default public void print() {
    for (int i = 0; i < size(); i += 1) {
        System.out.print(get(i) + " ");
    }
    System.out.println();
}
```
List61B 类的所有子类都可以使用这个方法！

然而，对于 SLList， `get` 方法需要在每次调用时遍历整个列表。最好在遍历时直接打印！我们希望 SLList 以不同于其接口规定的方式打印。为了做到这一点，我们需要覆盖它。在 SLList 中，我们实现了这个方法；

 ```Java
 @Override
public void print() {
    for (Node p = sentinel.next; p != null; p = p.next) {
        System.out.print(p.item + " ");
    }
}
```

现在，每当我们在 SLList 上调用 print()时，它将调用这个方法，而不是 List61B 中的方法。

##### 静态类型与动态类型^[[[Textbook#动静态]]]

Java 怎么知道使用哪个方法？这就需要提到我们的静态类型与动态类型——[[Trivial Keywords#静态类型与动态类型]]

假设有以下代码(这是合法的)：

```Java
List61B<String> lst = new SLList<String>();
```


当 Java 运行一个被覆盖的方法时，它会在其动态类型中搜索适当的方法签名并运行它。

#### Interface Inheritance VS Implement Inheritance^[[[Trivial Keywords#两种继承方式]]]

二者的区别与优劣如何？我这里直接摘录教材原文[[Textbook#Interface Inheritance VS Implement Inheritance]]



#### Extends

之前我们讲到类可以继承 `interface` ，这里的继承方式又分为实现继承与接口继承(而前者是有风险的)，那么类想要继承类该怎么办呢？

使用 `extend` 关键字，即可实现对类的继承，这里的继承可类比 C++里的 public 继承，但是没有 C++里面类型那么多，一个典型的例子如下(接续 Week 3 中提到的两种继承自 List61B 的 Lists)：

```Java
public class RotatingSLList<Item> extends SLList<Item>
```
关系图如下所示：

[![img](https://joshhug.gitbooks.io/hug61b/content/assets/list_subclasses.png)](https://joshhug.gitbooks.io/hug61b/content/assets/list_subclasses.png "img")

img

通过使用 `extends` 关键字，**子类**继承父类的**所有成员**。”成员”包括：

- All instance and static variables
- All methods
- All nested classes

**构造函数不会被继承**，私有成员不能被子类直接访问

##### Object class

Java 中的所有类都是 Object 的后代，或也可以说成”是 Object 类”(is-a)

Object 类提供了很多基本的方法，例如`toString()` ， `equals()` 等，可以选择重写也可以选择不重写

##### Type Checking and Casting

Java 在编译时进行类型检查，此处检查时的依据是**静态类型**而不是动态类型，因此在代码中有时候会有必要添加显式的”强制类型转换”来**告诉编译器**这个地方该讲什么什么东西**视作**什么什么东西，例如：

```Java
Poodle largerPoodle = (Poodle) maxDog(frank, frankJr); // compiles! Right hand side has compile-time type Poodle after casting
```
但是类型转换也有风险，正如货币天然是金银，但金银天然不是货币，可能会引发类型转换错误：

```Java
Poodle frank = new Poodle("Frank", 5);  
Malamute frankSr = new Malamute("Frank Sr.", 100);  
  
Poodle largerPoodle = (Poodle) maxDog(frank, frankSr); // runtime exception!
```
在这种情况下，我们比较一只贵宾犬和一只马拉穆特犬。如果没有进行强制转换，编译器通常不会允许调用 `maxDog` 进行编译，因为右侧的编译时类型将是 Dog，而不是 Poodle。然而，强制转换允许这段代码通过，当 `maxDog` 在运行时返回马拉穆特犬时，我们尝试将马拉穆特犬强制转换为贵宾犬时，会遇到一个运行时异常 - 一个 `ClassCastException`

#### Inheritance Cheatsheet

`VengefulSLList extends SLList` 表示 VengefulSLList “是” SLList，并继承了 SLList 的所有成员：

- Variables, methods nested classes
- Not constructors Subclass constructors must invoke superclass constructor first. The `super` keyword can be used to invoke overridden superclass methods and constructors.

覆盖方法的调用遵循两个简单规则：

- Compiler plays it safe and only allows us to do things according to the static type.
- For overridden methods (_not overloaded methods_), the actual method invoked is based on the dynamic type of the invoking expression
- Can use casting to overrule compiler type checking.

#### HoF and Subtype Polymorphism

这一节讲的主要是高阶函数以及子类的多态性

Java 中没有 Python 中那般方便的函数参数，也没有 JavaScript 里的回调函数，亦没有 C++里的函数指针

那么在 Java 中，该如何实现高阶函数的操作呢？答案是使用类继承的模式来书写，即使这样十分冗长。这是因为 Java 是纯面向对象编程的语言。

在了解到 HoF 的书写模式后，进一步深入，我们便得到了类似 C++里面类似”运算符重载”的操作，这在下一节，即可迭代对象与迭代器里又有着新的应用

#### Higher Order Functions

编写一个接口，定义任何接受整数并返回整数的函数 - 一个 `IntUnaryFunction` 。

```Java
public interface IntUnaryFunction {  
     int apply(int x);  
}
```
现在我们可以编写一个类， `implements IntUnaryFunction` 以表示一个具体的函数。让我们创建一个函数，该函数接受一个整数并返回该整数的 10 倍

```Java
public class TenX implements IntUnaryFunction {  
  /* Returns ten times the argument. */  
     public int apply(int x) {  
         return 10 * x;  
     }  
}
```

此时，我们已经用 Java 编写了 `tenX` 函数的 Python 等价函数。现在让我们写 `do_twice` ：

```Java
public static int do_twice(IntUnaryFunction f, int x) {  
    return f.apply(f.apply(x));  
}
```

在 Java 中，对 `print(do_twice(tenX, 2))` 的调用将如下所示：

```Java
System.out.println(do_twice(new TenX(), 2));
```

事实上，这里的接口扮演的角色即可以类比为 C++里的函数指针，而在实际调用时候的 `new Tenx()` 参数也可以换成其他的 subclass，以便于实现不同函数效果，为此我们只需要为不同的 subclass 写出不同的 apply 方法即可

##### Polymorphism

多态性，指的是对象可以具有多种形式或类型。在面向对象编程中，多态性涉及对象如何被视为其自身类的实例，其超类的实例，其超类的超类的实例等

考虑一个静态类型为 Deque 的变量 `deque` 。在执行时，调用 `deque.addFirst()` 将取决于 `addFirst` 被调用时 `deque` 的运行时类型或动态类型。正如我们在上一章中看到的，Java 使用动态方法选择来决定调用哪个方法

从狗狗们的故事引入————

还是以一直陪伴我们的 Dog 类为例，现在我想写一个函数 maxDog，给出两条狗里更大的那一条：

```Java
public Dog maxDog(Dog d1,Dog d2){  
    if (d1 > d2)  
      return d1;  
    else  
      return d2;  
 }
```

暗藏玄坤！大于号是可以用的吗？这里很显然会出问题，我们需要对 Dog 类的比较方法进行一个定义

考虑从现有接口 Comparable 继承，这是来自 Java 的内置接口，用来实现比较功能：

[![img](https://joshhug.gitbooks.io/hug61b/content/assets/comparable_interface.png)](https://joshhug.gitbooks.io/hug61b/content/assets/comparable_interface.png "img")

img

```Java
public class Dog implements Comparable<Dog> {  
...  
     public int compareTo(Dog uddaDog) {  
        return this.size - uddaDog.size;  
    }  
 }
```

上面的**OurComparable**是我们自己实现的可比较对象的接口，但是显然没有官方的完善

由此便实现了类似 C++中对“<,>”符号的**运算符重载**，只不过是 Java 特色重载

那么，如果我不想按照 size 的大小比较狗狗，而是按照狗狗名字的首字母顺序来给狗狗比较大小，又该怎么办呢？

也就是说，我需要**实现多种不同的比大小方法**时该怎么办？引出我们的第二位兄弟：`Comparator`。Java 这样做的方式是通过使用 `Comparator` 。由于比较器是一个对象，我们将使用 `Comparator` 的方式是在 Dog 内编写一个实现 `Comparator` 接口的嵌套类，该接口的内容如下：

```Java
public interface Comparator<T> {  
    int compare(T o1, T o2);  
}
```

这表明 `Comparator` 接口要求任何实现类实现 `compare` 方法。 `compare` 的规则就像 `compareTo` ：

- Return negative number if o1 < o2.
- Return 0 if o1 equals o2.
- Return positive number if o1 > o2.

实现的完整代码如下：

```Java
import java.util.Comparator;

public class Dog implements Comparable<Dog> {
    ...
    public int compareTo(Dog uddaDog) {
        return this.size - uddaDog.size;
    }

    private static class NameComparator implements Comparator<Dog> {
        public int compare(Dog a, Dog b) {
            return a.name.compareTo(b.name);
        }
    }

    public static Comparator<Dog> getNameComparator() {
        return new NameComparator();
    }
}
```
==这里注意用static不然不能用类名直接调用==

```Java
public class NameMaximizer {  
    public static void main(String[] args) {  
        Dog d1=new Dog("Elyse",3);  
        Dog d2=new Dog("Sture",9);  
       Comparator<Dog>nc =  (Comparator<Dog>) Dog.getNameComparator();  
        if (nc.compare(d1,d2)>0){  
            System.out.println(d1);  
        }else{  
            System.out.println(d2);  
        }  
    }  
}
```

```Java
public interface Comparable<T>{  
    public int compareTo(T object);  
    //实现大小比较  
  
}
```

```Java
public interface Comparator<T>{  
    int compare(T a,T b);  
}
```
Note that we’ve declared NameComparator to be a static class. A minor difference, but we do so because we do not need to instantiate a Dog to get a NameComparator. Let’s see how this Comparator works in action.

[![img](https://joshhug.gitbooks.io/hug61b/content/assets/comparator.png)](https://joshhug.gitbooks.io/hug61b/content/assets/comparator.png "img")

img


### Exceptions，Iterators，Iterables，Object Methods

进入下一部分，这一部分主要是一些 Java 语法知识的补充，包括异常、迭代、对象方法，了解完毕这些之后，CS61B 的第一部分(即 Java 的学习)也就宣告结束了(得益于自己 CPP 的底子，不然这些东西学起来不可能这么快······)

#### Exceptions

异常会导致正常的控制流停止。实际上，我们可以选择抛出自己的异常。在 Python 中，您可能已经看到过这种情况，使用 `raise` 关键字。在 Java 中，异常是对象，我们使用以下格式抛出异常：

```Java
throw new ExceptionObject(parameter1, ...)
```

一个典型例子如下：

```Java
/* Associates the specified value with the specified key in this map.  
Throws an IllegalArgumentException if the key is null. */  
public void add(T x) {  
    if (x == null) {  
        throw new IllegalArgumentException("can't add null");  
    }  
    if (contains(x)) {  
        return;  
    }  
    items[size] = x;  
    size += 1;  
 }
```
为什么这么做？以下是课本原文，我做如下摘抄：

We get an Exception either way - why is this better?

1. We have control of our code: we consciously decide at what point to stop the flow of our program
2. More useful Exception type and helpful error message for those using our code

However, it would be better if the program doesn’t crash at all. There are different things we could do in this case. Here are some below:

**Approach 1**: Don’t add `null` to the array if it is passed into `add`

**Approach 2**: Change the `contains` method to account for the case if `items[i] == null`.

Whatever you decide, it is important that users know what to expect. That is why documentation (such as comments about your methods) is very important.

#### Iterators and Iterables

##### 实现原始ArraySet
```Java
public class Naive_ArraySet<T> {  
    private T[] Items;  
    private int size;  
    public Naive_ArraySet(){  
        Items=(T[]) new Object[100];  
        size=0;  
    }  
    public boolean contains(T x){  
        for (int i =0;i<Items.length;i++){  
            if(Items[i]==x){  
                return  true;  
            }  
        }  
        return false;  
    }  
    public void add(T x){  
        if (!contains(x)){  
            Items[size]=x;  
            size+=1;  
        }  
    }  
}
```
Java 内置的Lists和Sets都是自带迭代器的，可以直接用`for(int i : aset)`遍历，然而我们自己构造的这个ArraySet显然不满足，那我们可以先手搓一个。

##### 实现可迭代ArraySet

`Set<Integer> javaset = new HashSet<Integer>()`

```Java
for (int x : javaset) {
   System.out.printlin(x);
}
```
以上代码是以下代码的shorthand形式：
```Java
Public Iterator<E> iterator();

Interator<Integer> seer=javaset.iteator();
while(seer.hasnext()){
    int x = seer.next();
    System.out.printlin(x);
}
```

迭代器与可迭代对象。这部分内容实际上就是 python 中迭代器的概念加上上文提到的用 Java 实现比较器的手段

相关的接口代码如下：

```Java
public interface Iterable<T> {
    Iterator<T> iterator();
}
```

```Java
public interface List<T> extends Iterable<T>{
    ...
}
```

```Java
public interface Iterator<T> {
    boolean hasNext();
    T next();
}
```

We are going to add iteration through keys to our `ArraySet` class. First, we write a new class called ArraySetIterator, nested inside of ArraySet:

```Java
private class ArraySetIterator implements Iterator<T> {
    private int wizPos;

    public ArraySetIterator() {
        wizPos = 0;
    }

    public boolean hasNext() {
        return wizPos < size;
    }

    public T next() {
        T returnItem = items[wizPos];
        wizPos += 1;
        return returnItem;
    }
}
```

This ArraySetIterator implements `Iterator<T>`, which means it implements a `hasNext()` method, and a `next()` method, using a `wizPos` position as an index to keep track of its position in the array. For a different data structure, we might implement these two methods differently.

**Thought Exercise:** How would you design `hasNext()` and `next()` for a linked list?

Now that we have the appropriate methods, we could use a ArraySetIterator to iterate through an `ArraySet`:

```Java
ArraySet<Integer> aset = new ArraySet<>();
aset.add(5);
aset.add(23);
aset.add(42);

Iterator<Integer> iter = aset.iterator();

while(iter.hasNext()) {
    System.out.println(iter.next());
}
```

We still want to be able to support the enhanced for loop, though, to make our calls ==cleaner==. So, we need to make `ArraySet` implement the Iterable interface. The essential method of the Iterable interface is `iterator()`, which returns an Iterator object for that class. All we have to do is return an instance of our `ArraySetIterator` that we just wrote!

```Java
public Iterator<T> iterator() {
    return new ArraySetIterator();
}
```

Now we can use enhanced for loops with our `ArrraySet`!


```Java
ArraySet<Integer> aset = new ArraySet<>();
...
for (int i : aset) {
    System.out.println(i);
}
```
在此基础上我们实现了可迭代版本的 Arraysets，完整的代码如下：

 ```Java
 import java.util.Iterator;

public class ArraySet<T> implements Iterable<T> {
    private T[] items;
    private int size; // the next item to be added will be at position size

    public ArraySet() {
        items = (T[]) new Object[100];
        size = 0;
    }

    /* Returns true if this map contains a mapping for the specified key.
     */
    public boolean contains(T x) {
        for (int i = 0; i < size; i += 1) {
            if (items[i].equals(x)) {
                return true;
            }
        }
        return false;
    }

    /* Associates the specified value with the specified key in this map.
       Throws an IllegalArgumentException if the key is null. */
    public void add(T x) {
        if (x == null) {
            throw new IllegalArgumentException("can't add null");
        }
        if (contains(x)) {
            return;
        }
        items[size] = x;
        size += 1;
    }

    /* Returns the number of key-value mappings in this map. */
    public int size() {
        return size;
    }

    /** returns an iterator (a.k.a. seer) into ME */
    public Iterator<T> iterator() {
        return new ArraySetIterator();
    }

    private class ArraySetIterator implements Iterator<T> {
        private int wizPos;

        public ArraySetIterator() {
            wizPos = 0;
        }

        public boolean hasNext() {
            return wizPos < size;
        }

        public T next() {
            T returnItem = items[wizPos];
            wizPos += 1;
            return returnItem;
        }
    }

    public static void main(String[] args) {
        ArraySet<Integer> aset = new ArraySet<>();
        aset.add(5);
        aset.add(23);
        aset.add(42);

        //iteration
        for (int i : aset) {
            System.out.println(i);
        }
    }

}
```
==总结==:
- Here we've seen **Iterable**, the interface that makes a class able to be iterated on, and requires the method `iterator()`, which returns an Iterator object. And we've seen **Iterator**, the interface that defines the object with methods to actually do that iteration. You can think of an Iterator as a machine that you put onto an iterable that facilitates the iteration. Any iterable is the object on which the iterator is performing.

With these two components, you can make fancy for loops for your classes!
#### Object Methods

如上文所述，Java 中所有的类都是 Object 类的子类，也可以说 Object 是最顶端的 superclass，继承的方法如下：

- `String toString()`
- `boolean equals(Object obj)`
- `Class <?> getClass()`
- `int hashCode()`
- `protected Objectclone()`
- `protected void finalize()`
- `void notify()`
- `void notifyAll()`
- `void wait()`
- `void wait(long timeout)`
- `void wait(long timeout, int nanos)`

这里专注理解前两个即可

##### toString()

相当于将某个对象字符串化的时候该怎么办？toString()解决的就是这个问题
当你运行 `System.out.println(dog)`时, 实际上调用的是这个:

```Java
String s = dog.toString()
System.out.println(s)
```

那我们怎么实现自己的`toString`太打印一个`ArraySet`呢？初始想法是运用字符串的方法，如下：
```Java
public String toString() {
    String returnString = "{";
    for (int i = 0; i < size; i += 1) {
        returnString += keys[i];
        returnString += ", ";
    }
    returnString += "}";
    return returnString;
}
```
然后，它太过裸露原始，`returnString += keys[i];`实际上是新建了字符串，而不是把内容增添上去，每次新增字符串又太过耗费时间。
为了解决这个问题，Java 有一个名为 StringBuilder 的特殊类。它创建一个可变的字符串对象，因此可以继续追加同一个字符串对象，而不必每次都创建一个新的字符串对象。
```Java
public String toString() {
        StringBuilder returnSB = new StringBuilder("{");
        for (int i = 0; i < size - 1; i += 1) {
            returnSB.append(items[i].toString());
            returnSB.append(", ");
        }
        returnSB.append(items[size - 1]);
        returnSB.append("}");
        return returnSB.toString();
    }
```
##### equals()

注意，Java 中 `==` 在比较对象的时候实际上比较的是**二者是否是同一个对象**，即二者存储的地址是否相同。而这显然不符合特定情况下我们的要求，所以我们采取 `equals` 来**重载我们的 `=`**

---




补充一个继承的知识点：

- 不能用 `super.super.something` 的方式来调用父类的父类，因为你只能有一个爹

补充一个动态方法选择：

- 编译时，在其静态类型中查看有无合适的签名，若有则**锁定该签名**，否则 Compile Error
- 运行时，在锁定签名的前提下，再在其动态类型查找有无更合适的方法，若无，则进一步查询其父类