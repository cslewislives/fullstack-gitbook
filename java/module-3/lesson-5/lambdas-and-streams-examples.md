---
description: Examples of various aggregate operations.
---

# Lambdas and Streams Examples

### Filter and ForEach Examples

* The filter example matches the example from the Lambda Syntax page.
* The forEach operation take a lambda expression that doesn't return anything. We must have the curly braces in this example because we have more than one statement. 

> **NOTE: This code is an entire class—we've just broken it up so we can insert comments/directions.**

```java
package com.company;

import com.fasterxml.jackson.core.type.TypeReference;
import com.fasterxml.jackson.databind.ObjectMapper;
import com.opencsv.bean.CsvToBeanBuilder;

import java.io.File;
import java.io.FileNotFoundException;
import java.io.FileReader;
import java.io.IOException;
import java.util.List;
import java.util.Map;
import java.util.Set;
import java.util.stream.Collectors;

public class App {

    public static void main(String[] args) {
        try {
            List<Motorcycle> bikes = new CsvToBeanBuilder<Motorcycle>(new FileReader("motorcycles.csv")).withType(Motorcycle.class).build().parse();

            // Print the information for all Suzuki motorcycles in inventory
            String make = "Suzuki";
            System.out.println("All " + make + " motorcycles in inventory: ");
            bikes
                    .stream()
                    .filter(b -> b.getMake().equals(make))
                    .forEach(bike -> {
                        System.out.println("===============");
                        System.out.println("Make: " + bike.getMake());
                        System.out.println("Model: " + bike.getModel());
                        System.out.println("Color: " + bike.getColor());
                        System.out.println("Year: " + bike.getYear());
                        System.out.println("Displacement: " + bike.getDisplacement());
                        System.out.println("Horsepwer: " + bike.getHorsepower());
                        System.out.println("Weight: " + bike.getWeight());
                    });
```

### Another Filter and ForEach Example

* Here, we filter so we only get bikes that weigh less than 500 pounds.

```java
// Print the information for all motorcycles the weigh less than 500 pounds
int weight = 500;
bikes
        .stream()
        .filter(bike -> bike.getWeight() < weight)
        .forEach(bike -> {
            System.out.println("===============");
            System.out.println("Make: " + bike.getMake());
            System.out.println("Model: " + bike.getModel());
            System.out.println("Color: " + bike.getColor());
            System.out.println("Year: " + bike.getYear());
            System.out.println("Displacement: " + bike.getDisplacement());
            System.out.println("Horsepwer: " + bike.getHorsepower());
            System.out.println("Weight: " + bike.getWeight());
        });
```

### Collection Example

* Here, we put the results in a collection rather than just print the results to the screen.

```java
// Rather than printing out the matching motorcycles, let's put them into a list
List<Motorcycle> lightBikes =
bikes
    .stream()
    .filter(bike -> bike.getWeight() < weight)
    .collect(Collectors.toList());

System.out.println(lightBikes.size());
```

### Group By Example

* Here, we group all of the bikes by manufacturer. This results in a `Map<String, List<Motorcycle>>` where the key is the name of the manufacturer.

```java
// We can also group our motorcycles by Make.
Map<String, List<Motorcycle>> groupedBikes =
bikes
        .stream()
        .collect(Collectors.groupingBy(b -> b.getMake()));

Set<String> keys = groupedBikes.keySet();
for(String key : keys) {
    System.out.println(key);
}
```

### Average Example

* Here we transform the stream of Motorcycles into a stream of integers \(which are the horsepower values for each bike\) and then we calculate the average horsepower.
* Note the use of `getAsDouble()`.

```java
// Print the average horsepower of the motorcycles in inventory
double avgHorsepower =
bikes
    .stream()
    .mapToInt(b -> b.getHorsepower())
    .average()
    .getAsDouble();

System.out.println("Average horsepower is: " + avgHorsepower);
```

### Find Maximum Example

* Here, we find the maximum horsepower value.

```java
int maxHorsePower =
bikes
        .stream()
        .mapToInt(bike -> bike.getHorsepower())
        .max()
        .getAsInt();

System.out.println("Max horsepower: " + maxHorsePower);
```

{% embed url="https://youtu.be/RR8L4rjmsHc" %}

