---
label: "2.2 - Escape Sequences and String Concatenation"
icon: code
order: -2
---

# Unit 2: Lesson 2 - Escape Sequences and String Concatenation

## Coding Activity 1
+++ U2_L2_Activity_One.java
```java
/* Lesson 2 Coding Activity Question 1 */

import java.util.Scanner;

public class U2_L2_Activity_One
{
  public static void main(String[] args)
  {
    // Initialize Scanner
    Scanner scan = new Scanner(System.in);
    
    // User Input
    /// Type of Item
    System.out.println("What type of item are you buying?");
    String itemType = scan.nextLine();
    /// Number of Item(s)
    System.out.println("How many are you buying?");
    int itemQuantity = scan.nextInt();
    /// Unit Weight of Item
    System.out.println("How much does each one weigh?");
    double unitWeight = scan.nextDouble();
    
    // Final Output
    System.out.println(itemQuantity + " " + itemType + " at " + unitWeight + " pounds each will weigh " + (unitWeight * itemQuantity) + " pounds total");
  }
}
```
+++

## Coding Activity 2
+++ U2_L2_Activity_One.java
```java
public class U2_L2_Activity_Two
{
  public static void main(String[] args)
  {
    // Final Output
    System.out.println("\"That brain of mine is something more than merely mortal; as time will show.\"\nAda Lovelace\nThe first computer programmer");
  }
}
```
+++

## Coding Activity 3
+++ U2_L2_Activity_One.java
```java
/* Lesson 2 Coding Activity Question 3 */

import java.util.Scanner;

public class U2_L2_Activity_Three
{
  public static void main(String[] args)
  {
    // Final Output
    System.out.print("(\\(\\\n( - -)\n((\') (\')");
  }
}
```
+++
