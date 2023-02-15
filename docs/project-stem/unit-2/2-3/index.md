---
label: "2.3 - String Methods"
icon: code
order: -3
---

# Unit 2: Lesson 3 - String Methods

## Coding Activity 1
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

## Coding Activity 2
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

## Coding Activity 3
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

## Coding Activity 4
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
