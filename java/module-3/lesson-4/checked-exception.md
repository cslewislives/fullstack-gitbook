---
description: Simple File I/O Example
---

# Checked Exception

**Example 1: Not handling the exception**

* Create and run this simple example and look at the stack trace when the error is encountered.

```java
package com.company.exceptions;

import java.io.FileWriter;
import java.io.IOException;
import java.io.PrintWriter;

public class App {

    public static void main(String[] args) throws IOException {

        PrintWriter writer = new PrintWriter(new FileWriter("/Home/foo/output.txt"));

        writer.println("File line 1");
        writer.println("File line 2");

        writer.flush();
        writer.close();
    }
}
```

**Example 2: Handle the exception and print a friendly error message:**

1. Create and run this example, remember the try/catch/finally block is what we use to handle Java exceptions.
2. Run the example with the error to compare and contrast what happened with the previous example.
3. Look at the `getMessage()` method on the exception; this is a standard method that can be used to display or log an error message.
4. The `finally` block runs even if an exception occurs.
5. Fix the error by changing `"/Home/foo/output.text"` to `"output.txt"` and run the program again. The `finally` block also runs when there is no exception thrown.

```java
package com.company.exceptions;

import java.io.FileWriter;
import java.io.IOException;
import java.io.PrintWriter;

public class App2 {

    public static void main(String[] args) {

        try {
            PrintWriter writer = new PrintWriter(new FileWriter("/Home/foo/output.txt"));

            writer.println("File line 1");
            writer.println("File line 2");

            writer.flush();
            writer.close();
        } catch (IOException e) {
            System.out.println("An error occurred: " + e.getMessage());
        } finally {
            System.out.println("Finishing up in the finally block...");
        }
    }
}
```

