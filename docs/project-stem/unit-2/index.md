---
label: "Unit 2: Using Objects"
icon: code
order: -1
---

# Unit 2: Using Objects

## Unit 2: Lesson 1 - Strings and Class Types

### Coding Activity 1
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

### Coding Activity 2
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

## Unit 2: Lesson 2 - Escape Sequences and String Concatenation

### Coding Activity 1
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

### Coding Activity 2
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

### Coding Activity 3
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

## Unit 2: Lesson 3 - String Methods

### Coding Activity 1
+++ U2_L3_Activity_One.java
```java
/* Lesson 3 Coding Activity Question 1 */

import java.util.Scanner;

public class U2_L3_Activity_One
{
  public static void main(String[] args)
  {
    // Initialize Scanner
    Scanner scan = new Scanner(System.in);
    
    // User Input
    System.out.println("Enter a string:");
    String initStr = scan.nextLine();
    System.out.println("Enter a number:");
    int x = scan.nextInt();
    
    // Final Output
    String finalStr = initStr.substring(0, x) + initStr.substring(initStr.length() - x);
    System.out.println(finalStr);
  }
}
```
+++

### Coding Activity 2
+++ U2_L3_Activity_Two.java
```java
/* Lesson 3 Coding Activity Question 2 */

import java.util.Scanner;

public class U2_L3_Activity_Two
{
  public static void main(String[] args)
  {
    // Initialize Scanner
    Scanner scan = new Scanner(System.in);
    
    // User Input
    System.out.println("Enter a string:");
    String initStr = scan.nextLine();
    System.out.println("How many characters would you like to delete at the end?");
    int delChar = scan.nextInt();
    
    // Final Output
    String finalStr = initStr.substring(0, initStr.length() - delChar);
    System.out.println(finalStr);
  }
}
```
+++

### Coding Activity 3
+++ U2_L3_Activity_Three.java
```java
/* Lesson 3 Coding Activity Question 3 */

import java.util.Scanner;

public class U2_L3_Activity_Three
{
  public static void main(String[] args)
  {
    // Initialize Scanner
    Scanner scan = new Scanner(System.in);
    
    // User Input
    /// First Word
    System.out.println("Enter first word:");
    String w1 = scan.nextLine().toLowerCase();
    /// Second Word
    System.out.println("Enter second word:");
    String w2 = scan.nextLine().toLowerCase();
    
    // Comparing First Letters (ignores dash)
    int wordResult = w1.compareTo(w2);
    
    // Final Output
    System.out.println("Result: " + wordResult);
  }
}
```
+++

### Coding Activity 4
+++ U2_L3_Activity_Four.java
```java
/* Lesson 3 Coding Activity Question 4 */

import java.util.Scanner;

public class U2_L3_Activity_Four
{
  public static void main(String[] args)
  {
    // Initialize Scanner
    Scanner scan = new Scanner(System.in);
    
    // User Input
    System.out.println("Enter a sentence:");
    String sentence = scan.nextLine();
    
    // Final Output
    System.out.println(sentence.indexOf(" "));
  }
}
```
+++

## Unit 2: Lesson 4 - Classes and Objects

### Coding Activity 1
+++ U2_L4_Activity_One.java
```java
/* Lesson 4 Coding Activity Question 1 */

import java.util.Scanner;
 
public class U2_L4_Activity_One
{
  public static void main(String[] args)
  {
    // Initialize Scanner
    Scanner scan = new Scanner(System.in);
    
    // User Input
    /// Get First String
    System.out.println("Enter first string");
    String s1 = scan.nextLine();
    /// Get Second String
    System.out.println("Enter second string");
    String s2 = scan.nextLine();
    /// Get # of Letters for Each String
    System.out.println("Enter number of letters from each word");
    int n = scan.nextInt();
    
    // Final Output
    /// Print Last n Letters of s1 + First n Letters of s2
    System.out.println(s1.substring(s1.length() - n, s1.length()) + s2.substring(0, n));
  }
}
```
+++

### Coding Activity 2
+++ U2_L4_Activity_Two.java
```java
/* Lesson 4 Coding Activity Question 2 */

import java.util.Scanner;

public class U2_L4_Activity_Two{
  public static void main(String[] args){
  
    // User Input
    Scanner scan = new Scanner(System.in);
    String str1 = scan.nextLine();
    String str2 = str1;
    
    // Final Output
    str1 = str1.toUpperCase();
    str2 = (str2.substring(0, 1).toUpperCase()) + str2.substring(1, str2.length()); 
    System.out.println(str2);
    System.out.println(str1);
  }
}
```
+++
