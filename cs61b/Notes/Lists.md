---
date: 2025-03-11
tags:
  - Lists
---

#### IntLists

初始设想是利用链表：


```Java
public class IntList {  
      public int first;  
      public IntList rest;  
  
      public IntList(int f, IntList r) {  
      first = f;  
      rest = r;  
    }  
}
```

### SLList

显然，在这上面直接添加函数方法会很裸奔，我们选择将核心提出，并创建新的类：

```Java
public class IntNode {  
      public int item;  
      public IntNode next;  
  
      public IntNode(int i, IntNode n) {  
      item = i;  
      next = n;  
  }  
}
```


这里的 SLList 即为新的列表数据结构，同样的，可以添加得到一系列实用的方法，如`addfirst`,`addlast`,`getfirst`,`getlast`,但是这时得到的数据结构仍然有不方便以及危险的地方：

- first 结点依然裸奔!
- 空列表无法舒适地 addlast

为此，我们继续优化，首先将结点类型改为 private，其次设置哨兵结点(sentinel)，即添加一个始终位于最前端的结点，确保数据结构不是空的，这样便以一种类似**数分中“一致连续”的手法**处理了上述问题，实现了一致性。这也是编写代码的重要原则之一

代码就略了，我懒

实际上不会改变 A 中数据的值，因为这里的 x 也是 A 中数据按照值传递到 x 的

---


在 SLList 中，我们优化了裸数据结构带来的不便，同时添加了哨兵结点来维持不变性，但是，这样的 Lists 仍然具有一些可以优化的地方：

- `addLast`时，总会遍历整个链表，如果我的列表长达一百万项，这将浪费时间
- 单向遍历，不利于快速访问元素/删除元素，尤其是靠后的元素，每次访问都需要经历不必要的遍历

由此，我们引出双向链表——**Double Linked List**，即`DLList`

#### DLList

添加前向指针(这个说法不严谨但是我先这么写)，使得列表变成可以双向访问的类型：

```Java
public class IntNode {
    public IntNode prev;
    public int item;
    public IntNode next;
}
```
同时为末端结点同样设置一个哨兵结点，由此得到的数据结构会类似下面的拓扑图：

[![dllist_double_sentinel_size_2.png](https://joshhug.gitbooks.io/hug61b/content/chap2/fig23/dllist_double_sentinel_size_2.png)](https://joshhug.gitbooks.io/hug61b/content/chap2/fig23/dllist_double_sentinel_size_2.png "dllist_double_sentinel_size_2.png")

dllist_double_sentinel_size_2.png

也可以首尾共用一个哨兵结点，实现环形结构：

[![dllist_circular_sentinel_size_2.png](https://joshhug.gitbooks.io/hug61b/content/chap2/fig23/dllist_circular_sentinel_size_2.png)](https://joshhug.gitbooks.io/hug61b/content/chap2/fig23/dllist_circular_sentinel_size_2.png "dllist_circular_sentinel_size_2.png")

dllist_circular_sentinel_size_2.png

最后，加入“模板”(在 C++里是模板)，使得我们的列表“通用化”——

一个可以容纳任何类型的通用 `DLList` 看起来如下：

```Java
public class DLList {
    private IntNode sentinel;
    private int size;

    public class IntNode {
        public IntNode prev;
        public int item;
        public IntNode next;
        ...
    }
    ...
}
```

与之相对比的是之前的代码：
```Java
public class DLList {
    private IntNode sentinel;
    private int size;

    public class IntNode {
        public IntNode prev;
        public int item;
        public IntNode next;
        ...
    }
    ...
}
```
现在我们已经定义了一个 `DLList` 类的通用版本，我们还必须使用特殊的语法来实例化这个类。为此，在声明时，我们将所需的类型放在尖括号内，并在实例化时使用空的尖括号。例如：

```Java
DLList<String> d2 = new DLList<>("hello");  
d2.addLast("world");
```

由于泛型仅适用于引用类型，我们无法将原始类型如 `int` 或 `double` 放入尖括号中，例如 `<int>` 。相反，我们使用原始类型的引用版本，在 `int` 情况下是 `Integer` ，例如。

```Java
DLList<Integer> d1 = new DLList<>(5);  
d1.insertFront(10);
```
有关使用通用类型的更多细微差别，我们将把它们推迟到本书的后面章节。现在，请使用以下经验法则：

- 在实现数据结构的.java 文件中，在类名之后的文件顶部只需指定一次泛型类型名称。
- 在其他 .java 文件中，使用您的数据结构时，在声明时指定特定的期望类型，并在实例化时使用空的尖括号运算符。
- 如果您需要实例化一个泛型到原始类型，请使用它们的原始等效项 `Integer` ， `Double` ， `Character` ， `Boolean` ， `Long` ， `Short` ， `Byte` 或 `Float` 。

细节：在实例化时，您也可以在尖括号内声明类型，尽管这并非必需，只要您也在同一行上声明变量。换句话说，下面的代码行是完全有效的，即使右侧的 `Integer` 是多余的。

```Java
DLList<Integer> d1 = new DLList<Integer>(5);
```

#### AList

最后，我们将使用另一种不同的手法来实现 List——数组！这样可以极大优化查找元素带来的时间损失，首先下面是数组相关的基础知识：

##### Array(数组)

实例化数组的三种方法：

- `x = new int[3];`
- `y = new int[]{1, 2, 3, 4, 5};`
- `int[] z = {9, 10, 11, 12, 13};`

包含数组基本操作的代码：

```Java
int[] z = null;
int[] x, y;

x = new int[]{1, 2, 3, 4, 5};
y = x;
x = new int[]{-1, 2, 5, 4, 99};
y = new int[3];
z = new int[0];
int xL = x.length;

String[] s = new String[6];
s[4] = "ketchup";
s[x[3] - x[1]] = "muffins";

int[] b = {9, 10, 11};
System.arraycopy(b, 0, x, 3, 2);
```

最后一行展示了一种将信息从一个数组复制到另一个数组的方法。 `System.arraycopy` 接受五个参数：

- The array to use as a source
- Where to start in the source array
- The array to use as a destination
- Where to start in the destination array
- How many items to copy

`System.arraycopy(b, 0,x, 3, 2)` 相当于 Python 中的 `x[3:5] = b[0:2]`

### AList(使用数组实现列表)

这一节有趣的主要是如何在数组满员时“扩展数组”，一开始我们使用的是逐 1 相加，但是测试结果表明这样的效率甚至远远不如 `SLList` !

[![fig25/insert_experiment.png](https://joshhug.gitbooks.io/hug61b/content/chap2/fig25/insert_experiment.png)](https://joshhug.gitbooks.io/hug61b/content/chap2/fig25/insert_experiment.png "fig25/insert_experiment.png")

fig25/insert_experiment.png

将加的数额改成 100？1000？不，这样做的时间消耗始终是平方级别的，我们使用乘法来扩展数组，实现效率的极大提升！

```Java
public void insertBack(int x) {
    if (size == items.length) {
           resize(size + RFACTOR);
    }
    items[size] = x;
    size += 1;
}
```

```Java
public void insertBack(int x) {
    if (size == items.length) {
           resize(size * RFACTOR);
    }
    items[size] = x;
    size += 1;
}
```

最后记得将 AList 数组列表模板化，以适应不同的使用需求

注意这里的语法有细微区别，这是 Java 中数组的特性所决定的：

Java 不允许我们创建一个泛型对象数组，因为泛型的实现方式存在一个模糊的问题。也就是说，我们不能做类似以下的事情：

```Java
Glorp[] items = new Glorp[8];
```

相反，我们必须使用下面的抽象语法：

```Java
Glorp[] items = (Glorp []) new Object[8];
```

这将产生一个编译警告，暂时不用管。我们将在后面更详细地讨论