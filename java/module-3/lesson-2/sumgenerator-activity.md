# SumGenerator - Activity

![SumGenerator](../../../.gitbook/assets/image%20%2894%29.png)

Follow the instructions below. Do not look at the Solution Code tabs until you have completed your attempt. 

{% tabs %}
{% tab title="Instructions" %}
Goals:

* Write tests to satisfy the requirements below.
* Then implement the code to pass the tests.

Complete the following:

* **Write the tests first** and implement the `evenSum` and `oddSum` method from the `SumGenerator` library.
* Create a new class called `Numbers`
  * This class should have the following properties and the associated getters/setters:
    * int sum
    * int evenSum
    * int oddSum
  * This class should also have a constructor which takes in a single integer, `n`
    * Use the `SumGenerator` class to set the values for `sum`, `evenSum`, and `oddSum`
  * This class does not require any testing.
* You need an additional class called `SumList` with 1 property - a List of instances of the above class.
* **Write the tests first** and implement a method called `addToList` which takes in an integer, and adds a new instance of the `Numbers` class to the List.
{% endtab %}

{% tab title="Summing" %}
```java
import java.util.ArrayList;
import java.util.List;

public class Summing {

    private List<Numbers> numsList;

    public Summing() {
        numsList = new ArrayList<>();
    }

    public List<Numbers> getNumsList() {
        return numsList;
    }

    public void setNumsList(List<Numbers> numsList) {
        this.numsList = numsList;
    }

    public void addNumber(int n) {
        Numbers newNum = new Numbers();

        newNum.setPrimeSum(calculatePrimeSum(n));
        newNum.setEvenSum(calculateEvenSum(n));
        newNum.setOddSum(calculateOddSum(n));
        newNum.setSum(calculateSum(n));

        numsList.add(newNum);
    }

    public int[] flattenList() {
        int[] flatList =  new int[numsList.size() * 4];

        for(int i = 0; i < numsList.size() * 4; i += 4) {
            Numbers currNum = numsList.get(i / 4);

            flatList[i] = currNum.getPrimeSum();
            flatList[i + 1] = currNum.getEvenSum();
            flatList[i + 2] = currNum.getOddSum();
            flatList[i + 3] = currNum.getSum();
        }

        return flatList;
    }

    private static int calculatePrimeSum(int n) {
        int sum = 0;
        for(int i = 2; i <= n; i++) {
            boolean prime = true;
            for(int j = 2; j < i; j++) {
                if( i % j == 0) {
                    prime = false;
                    break;
                }
            }
            if(prime) {
                sum += i;
            }
        }

        return sum;
    }

    private static int calculateEvenSum(int n) {
        int halfN = n / 2;
        return halfN * (halfN + 1);
    }

    private static int calculateOddSum(int n) {
        int halfN = n / 2;
        int evenSum = halfN*(halfN + 1);
        int totalSum = n * (n + 1) / 2;
        return totalSum - evenSum;
    }

    private static int calculateSum(int n) {
        return n * (n + 1) / 2;
    }
}
```
{% endtab %}

{% tab title="Numbers" %}
```java
import java.util.Objects;

public class Numbers {

    private int primeSum;
    private int evenSum;
    private int oddSum;
    private int sum;

    public int getPrimeSum() {
        return primeSum;
    }

    public void setPrimeSum(int primeSum) {
        this.primeSum = primeSum;
    }

    public int getEvenSum() {
        return evenSum;
    }

    public void setEvenSum(int evenSum) {
        this.evenSum = evenSum;
    }

    public int getOddSum() {
        return oddSum;
    }

    public void setOddSum(int oddSum) {
        this.oddSum = oddSum;
    }

    public int getSum() {
        return sum;
    }

    public void setSum(int sum) {
        this.sum = sum;
    }

    @Override
    public boolean equals(Object o) {
        if (this == o) return true;
        if (o == null || getClass() != o.getClass()) return false;
        Numbers numbers = (Numbers) o;
        return getPrimeSum() == numbers.getPrimeSum() &&
                getEvenSum() == numbers.getEvenSum() &&
                getOddSum() == numbers.getOddSum() &&
                getSum() == numbers.getSum();
    }

    @Override
    public int hashCode() {
        return Objects.hash(getPrimeSum(), getEvenSum(), getOddSum(), getSum());
    }
}
```
{% endtab %}
{% endtabs %}

