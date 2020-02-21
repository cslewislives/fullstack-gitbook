---
description: Rules and an example of constructors and inheritance.
---

# Constructors and Inheritance

Inheritance introduces a layer of complexity on constructors: which constructor is run when I instantiate a class that extends another class? 

### Rules of Constructors

1. The base class constructor can be invoked in a derived class by calling `super`.
2. You can only call `super` from within the constructor of the derived class, nowhere else.
3. The call to `super` must be the first statement in the constructor.
4. The call to `super` must match the signature of a valid constructor in the base class.
5. If you do not explicitly call `super` in the constructor of a derived class, the compiler will automatically call the base class default constructor. If one doesn’t exists, a compilation error will occur.
6. If your derived class does not define a constructor, the compiler provides the derived class with a default constructor that does nothing but call `super`, invoking the default constructor of the base class.

### Example: `super` Keyword

```java
public class MyException extends Exception {
    
    public MyException(String message) {
        super(message);
    }
    
    public MyException(String message, Throwable cause) {
        super(message, cause);
    }
}
```

*  `Exception` has two constructors this is made possible with **overloading**. Our constructors just call the base class versions by using the `super` keyword.

#### Two Big Takeaways

* If you don't provide a constructor for your class \(perfectly fine\), the JVM will provide a default constructor for you. This constructor has no parameters and has an empty body.
* If you **do** provide a constructor for your class \(also perfectly fine\), the JVM **will no longer provide a default constructor for you**. This is generally not a problem, except in \#5 above.

