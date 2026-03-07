## 动静态
In the above declaration and instantiation, lst is of type “List61B”. This is called the **“static type”**

However, the objects themselves have types as well. the object that lst points to is of type SLList. Although this object is intrinsically an SLList (since it was declared as such), it is also a List61B, because of the **“is-a”** relationship we explored earlier. But, because the object itself was instantiated using the SLList constructor, We call this its **“dynamic type”**.

Aside: the name “dynamic type” is actually quite semantic in its origin! Should lst be reassigned to point to an object of another type, say a AList object, lst’s dynamic type would **now be AList and not SLList**! It’s dynamic because it changes based on the type of the object it’s currently referring to.

## Interface Inheritance VS Implement Inheritance

Interface inheritance (what): Simply tells what the subclasses should be able to do.
    - EX) all lists should be able to print themselves, how they do it is up to them.
- Implementation inheritance (how): Tells the subclasses how they should behave.
    - EX) Lists should print themselves exactly this way: by getting each element in order and then printing them.

When you are creating these hierarchies, remember that the relationship between a subclass and a superclass should be an “is-a” relationship. AKA Cat should only implement Animal Cat **is an** Animal. You should not be defining them using a “has-a” relationship. Cat **has-a** Claw, but Cat definitely should not be implementing Claw.

Finally, Implementation inheritance may sound nice and all but there are some drawbacks:

- We are fallible humans, and we can’t keep track of everything, so it’s possible that you overrode a method but forgot you did.
- It may be hard to resolve conflicts in case two interfaces give conflicting default methods.
- It encourages overly complex code
