---
description: An example of an unchecked exception.
---

# Unchecked Exception

**Example 1: No code to handle the unchecked exception:**

1. Create and run this first example.
2. Test it with 0 and 11 and then a number in range to show that it works.
3. Test it with "a" and watch it blow up.
4. Point out that even though the code could throw and exception \(it just did!\), we didn't need to handle it because it was unchecked.

```java
package com.company.exceptions;

import java.util.Scanner;

public class App3 {

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);

        String userInput;
        int number;

        do {
            System.out.println("Please enter a number between 1 and 10");
            userInput = scanner.nextLine();
            number = Integer.parseInt(userInput);
        } while(number < 1 || number > 10);

        System.out.println("Thanks for playing - you chose: " + number);
    }
}
```

