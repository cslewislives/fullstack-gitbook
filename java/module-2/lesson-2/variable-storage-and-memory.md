---
description: The nitty gritty of memory
---

# Variable Storage & Memory

This article is a bit more conceptual, but still important to understand. Before we go too deep, let's review what we've learned about objects. 

### Review of Instantiating Objects

Constructors are special methods that are called when we instantiate an object from a class \(we saw that in the last lesson\). The constructor is used to **initialize** our object. Initialization means setting values for the properties so the object is in a known state. 

We indicate that we want to instantiate a new object by using the `new` keyword. We have already used the `new`keyword when using the Scanner \(we just didn't know what it was doing\). Recall `Scanner myScanner = new Scanner(System.in);`

Notice that we pass `System.in` into the Scanner constructor so that the constructor can initialize `myScanner` to use System.in \(i.e., the console\) as the place `myScanner` will read from. There are other options that you could pass in here instead. Like every constructor that takes a parameter, the value can vary. 

When the `new` keyword and a constructor are used together, the Java Virtual Machine creates a new object in a part of memory called the **heap** \(more on this in a minute\) and hands us a **reference** to that object. References contain the location of the newly created object on the heap and allow us to access/use the object \(more on this in a minute as well\).

{% embed url="https://youtu.be/oxKkf42xpjY" %}

## Stack vs Heap

The stack and the heap are two distinct areas of memory. When primitive variables \(`int`, `boolean`, `double`, etc\)  are created, their values are pushed onto the stack. When an object is created, it is added to the heap and the memory address of its location in the heap is added to the stack.

The stack is highly ordered like a stack of books. Variables go on the top and come off the top of the stack. 

The heap is like a non-highly ordered blob of memory like an amoeba rather than a stack of books. Okay, maybe that's taking it a little far, but it's how I always liked to imagine it. Objects go on the heap. Why? Because there's more room and it's more flexible. In the heap they have an address. That address goes on the stack. 

![](../../../.gitbook/assets/image%20%2826%29.png)

## Memory Management

Java is a managed language. This means that developers are not responsible for explicitly reserving and releasing memory resources. Practically, this simply means that you can create objects and other variables and forget about them. 

This means that we can just create objects \(using the `new` operator\) whenever we need them. The JVM will allocate the necessary memory.

This also means that we don't need to explicitly release the memory for our objects when we're done using them.

The process of reclaiming memory is called **garbage collection** and the component responsible for the process is called the **garbage collector**

Objects on the heap are eligible for garbage collection when there are no more references pointing to them.

We can explicitly have a reference stop pointing to an object by setting the reference to `null`, For example `bigCat = null`, but we pretty much never need to do this. 

References will go away automatically when the method in which they are declared returns. At that point, the reference will be removed from the stack and destroyed.

{% embed url="https://youtu.be/U4uBhvvTkQc" %}

## Parameter Passing

When we pass a parameter into a method a new copy of the variable is made on the stack. For primitives, this works just as you would expects. If `x = 4` and you pass `x` into a function, a new copy of `4` is created on the stack. As you would expect, no matter what you do to the new copy of `4`, nothing happens to the original `x` variable. 

Reference variables like objects work a bit differently. When you pass a reference variable into a method, a new copy of the reference address is created on the stack but **both references still point to the same object on the heap**. This means that any changes made inside the method, impact the original object that was passed in. 

```java
public class Cat {
    private String name;
    
    public void setName(String name){
        this.name = name; 
    }
    
    public String getName() {
        return this.name;
    }    
}
```

```java
public class App {
    public static void main(String[] args){
        Cat chuck = new Cat();
        chuck.setName("Chuck");
        changeName(chuck);
        System.out.println(chuck.getName());
    }
    
    public static Cat changeName (Cat innerCat){
        innerCat.setName("Jazzy");
        return innerCat;
    }
}
```

