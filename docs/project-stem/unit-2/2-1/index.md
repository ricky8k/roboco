---
label: "2.1 - Strings and Class Types"
icon: code
order: -1
---

# Unit 2: Lesson 1 - Strings and Class Types

## Coding Activity 1
+++ U2_L1_Activity_One.java
```java
/* Lesson 1 Coding Activity Question 1 */

import java.util.Scanner;

public class U2_L1_Activity_One
{
  public static void main(String[] args)
  {
    // Initialize Scanner
    Scanner scan = new Scanner(System.in);
    
    // User Input
    System.out.println("What is your name?");
    String name = scan.nextLine();
    System.out.println("What is your favorite number?");
    int number = scan.nextInt();
    
    // Final Output
    System.out.println("Your name is " + name + " and you like the number " + number + ".");
  }
}
```
+++

## Coding Activity 2
+++ U2_L1_Activity_Two.java
```java
/* Lesson 1 Coding Activity Question 2 */

import java.util.Scanner;

public class U2_L1_Activity_Two
{
  public static void main(String[] args)
  {
    // Initialize Scanner
    Scanner scan = new Scanner(System.in);
    
    // Initial Order
    String itemName = "apple pie";
    System.out.println("The current order is " + itemName);
    // Change Order
    System.out.println("I want to eat something else, what do you want to eat?");
    itemName = scan.nextLine();
    
    // Final Output
    System.out.println("The order has changed to " + itemName);
  }
}
```
+++
