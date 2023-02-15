---
label: "1.4 - Number Calculations"
icon: code
order: -4
---

# Unit 1: Lesson 4 - Number Calculations

## Coding Activity 1
+++ U1_L4_Activity_One.java
```java
/* Lesson 4 Coding Activity Question 1 */

import java.util.Scanner;

class U1_L4_Activity_One
{
  public static void main(String[] args)
  {
    // Initialize Scanner
    Scanner scan = new Scanner(System.in);
    
    // User Input 
    System.out.println("Enter starting number (must be an integer)");
    System.out.print(">");
    int num = scan.nextInt();
    
    // Final Output
    num++;
    System.out.println("number is now " + num);
    num++;
    System.out.println("number is now " + num);
    num++;
    System.out.println("number is now " + num);
    num++;
    System.out.println("number is now " + num);
    num--;
    System.out.println("number is now " + num);
    num--;
    System.out.println("number is now " + num);
    num--;
    System.out.println("number is now " + num);
    num--;
    System.out.println("number is now " + num);
  }
}
```
+++
[!button Raw](/docs/project-stem/unit-1/1-4/raw/1.4-Activity1.java)

## Coding Activity 2
+++ U1_L4_Activity_Two.java
```java
/* Lesson 4 Coding Activity Question 2 */

import java.util.Scanner;

class U1_L4_Activity_Two 
{
  public static void main(String[] args) 
  {
    // Initialize Scanner
    Scanner scan = new Scanner(System.in);
    
    // User Input
    int numFeet = scan.nextInt();
    
    // Calculation
    int numYards = numFeet / 3;
    
    // Final Output
    System.out.println(numYards);
  }
}
```
+++
[!button Raw](/docs/project-stem/unit-1/1-4/raw/1.4-Activity2.java)

## Coding Activity 3
+++ U1_L4_Activity_Three.java
```java
/* Lesson 4 Coding Activity Question 3 */

import java.util.Scanner;

class U1_L4_Activity_Three 
{
  public static void main(String[] args) 
  {
    // Initialize Scanner
    Scanner scan = new Scanner(System.in);
    
    // Prepare Variables
    double pi = 3.14;
    
    // User Input
    System.out.println("Enter a circumference:");
    double circumference = scan.nextDouble();
    
    // Circumference to Radius
    double radius = (circumference / 2) / pi;
    System.out.println("Radius: " + radius);
    
    // Circumference to Area
    double area = (radius * radius) * pi;
    System.out.println("Area: " + area);
  }
}
```
+++
[!button Raw](/docs/project-stem/unit-1/1-4/raw/1.4-Activity3.java)

## Coding Activity 4
+++ U1_L4_Activity_Four.java
```java
/* Lesson 4 Coding Activity Question 4 */

import java.util.Scanner;

class U1_L4_Activity_Four 
{
  public static void main(String[] args) 
  {
    // Initialize Scanner
    Scanner scan = new Scanner(System.in);
    
    // User Input
    System.out.println("Enter a price:");
    double price = scan.nextDouble();
    
    // Final Output
    double change = 10 - price;
    System.out.println("Change from $10: $" + change);
  }
}
```
+++
[!button Raw](/docs/project-stem/unit-1/1-4/raw/1.4-Activity4.java)