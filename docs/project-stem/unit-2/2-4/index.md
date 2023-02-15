---
label: "2.4 - Classes and Objects"
icon: code
order: -4
---

# Unit 2: Lesson 4 - Classes and Objects

## Coding Activity 1
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

## Coding Activity 2
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
