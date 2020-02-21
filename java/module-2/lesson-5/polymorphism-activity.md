# Polymorphism - Activity

![Polymorphism](../../../.gitbook/assets/image%20%2816%29.png)

Follow the instructions below. Do not look at the Solution Code tab until you have completed your attempt. 

{% tabs %}
{% tab title="Instructions" %}
1. Instantiate three objects - one each of the `Developer`, `TeamLead`, and `Architect` types.
2. Use Intellisense to show what methods are available for each one.
3. Now, instantiate two new objects, both of the `Developer` type
   * The first should be a new `TeamLead`
   * The second should be a new `Architect`
4. Again, use Intellisense to show what methods are availble for these new objects.
5. Are they what was expected?

Use the following hierarchy for this activity:

Developer -&gt; TeamLead -&gt; Architect

```java
public class Developer {

    public void estimateStoryPoints() {
        System.out.println("Estimating my story points. (Developer)");
    }

    public void checkInCode() {
        System.out.println("Checking in code. (Developer)");
    }
}

// ============================

public class TeamLead extends Developer {

    public void planSprint() {
        System.out.println("Planning sprint. (TeamLead)");
    }

    public void assignWork(Developer dev) {
        System.out.println("Assigning work (Developer)");
    }

    public void estimateStoryPoints() {
        System.out.println("Estimating my story points (TeamLead)");
        System.out.println("Make sure everyone on my team has estimated their story points.");
    }
}

// ================================

public class Architect extends TeamLead {

    public void createTechRoadmap() {
        System.out.println("Creating tech road map. (Architect)");
    }

    public void evaluateVendor() {
        System.out.println("Evaluating vendor. (Architect)");
    }
}
```
{% endtab %}

{% tab title="Solution Code" %}
```java
public class App {

    public static void main(String[] args) {
        Developer dev = new Developer();
        TeamLead lead = new TeamLead();
        Architect arch = new Architect();

        // Use Intellisense to show all the methods and features that you'd expect
        // to see on these objects.

        Developer dev2 = new TeamLead();
        Developer dev3 = new Architect();

        // This doesn't work b/c Developer doesn't have a planSprint() method
        // dev2.planSprint();
        // This doesn't work b/c Developer doesn't have an evaluateVendor() method
        // dev3.evaluateVendor();

        TeamLead lead2;
        // This causes a problem b/c TeamLead has more features than Developer so the
        // compiler can't do this conversion for us
        // lead2 = dev2;

        // This works b/c the dev2 reference is pointing to a TeamLead. We constructed
        // a TeamLead object; we just happened to point at it with a Developer reference.
        // Here, we have to cast (i.e., tell the compiler how to treat the type of dev2) dev2
        // into a TeamLead type ... and everything just works!
        lead2 = (TeamLead)dev2;
        lead2.planSprint();
    }
}
```

* We can use a Developer reference to refer to a TeamLead or Architect object; this is because TeamLeads and Architects **are** Developers
* When you do this, we only have access to the Developer methods on the objects.
* The underlying object for `dev2` is actually a TeamLead—because that is what we actually constructed. We just happened to point at the object with a Developer reference.
* We have to cast the object to point at it with a TeamLead reference \(even though the underlying object is actually a TeamLead\); see code comments above.
*  We can access a TeamLead method \(`planSprint()`\) once we're pointing to the object with a TeamLead reference.
* This is a one-way proposition. All TeamLeads are Developers but not all Developers are TeamLeads!
{% endtab %}
{% endtabs %}

 

