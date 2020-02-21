---
description: Demonstration of the fact that collections can hold references to objects.
---

# Collections and References

We want to accomplish two things here: 

* Show that we can put our own custom objects into a collection.
* Demonstrate the ramifications of the fact that collections hold **references** to objects.

Our first approach to adding Employees to the list is a bit naive: we create a new reference for each new employee added to the list. The second approach is a bit more efficient: we just reuse the same reference.

We need to talk through why this works:

1. We create an object and have a reference to it.
2. We then put a copy of the reference in the list \(we now have two references to the same object\).
3. We now create a new object and reuse our original reference to point to the new object.
4. We then put a copy of the reference to the new object in the list.
5. And so on...

In the final example:

1. Copy an object reference out of the list into a new reference.
2. Change the value of a property using the new reference.
3. The value is reelected when using the reference from the list.
4. This is because there is only one object, but two references.

{% hint style="info" %}
Run the following code in IntelliJ to get a better understanding of how this works.
{% endhint %}

{% tabs %}
{% tab title="References Class" %}
```java
package com.company.lists;

import java.util.ArrayList;
import java.util.List;

public class References {

    public static void main(String[] args){
        // Create a list of Employees
        List<Employee> staff = new ArrayList<>();

        // Add some employees to our list
        Employee emp = new Employee("Joe Smith", "HR");
        Employee emp2 = new Employee("Jane Doe", "Finance");

        staff.add(emp);
        staff.add(emp2);

        // Now reuse the emp reference to add another Employee to the list
        emp = new Employee("George Washington", "Operations");

        staff.add(emp);
        // Now the staff List has 3 objects
        System.out.println("How many employees do we have? " + staff.size());
        
        // Print the names of all 3 objects  
        for (Employee temp : staff) {
            System.out.println(temp.getName());
        }
        
        // Store a reference to the first object in the List
        Employee testEmployee = staff.get(0);
        
        // Print the name of the first object in the List
        System.out.println(testEmployee.getName());
        
        // Change the name of the first object in the list
        testEmployee.setName("Joseph J. Smith");
        
        // Print the name of the first object in the list after changing it
        System.out.println(testEmployee.getName());
        
        // Print all employees in the list with the first name in the list changed
        for (Employee temp : staff) {
            System.out.println(temp.getName());
        }
    }
}
```
{% endtab %}

{% tab title="Employee Class" %}
```java
package com.company.lists;

public class Employee {

    private String name;
    private String department;

    public Employee(String name, String department) {
        this.name = name;
        this.department = department;
    }

    public String getName() {
        return name;
    }

    public void setName(String name) {
        this.name = name;
    }

    public String getDepartment() {
        return department;
    }

    public void setDepartment(String department) {
        this.department = department;
    }
}
```
{% endtab %}
{% endtabs %}

## Testing Collections

* Order matters when comparing a List to another List.
  * JUnit will compare the first element of one List to the first element of a second List, and so forth.
* Order **does not** matter when comparing unordered collections, like Sets
* A common tactic is to check the size of the List for an expected value.
* We can compare Lists using \`assertEquals\`, and the \`.equals\` method is applied recursively to all members of the List.

