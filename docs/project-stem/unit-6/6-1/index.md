---
label: "6.1 - One-Dimensional Arrays"
icon: code
order: -1
---

# Unit 6: Lesson 1 - One-Dimensional Arrays

## Coding Activity 1
+++ U6_L1_Activity_One.java
```java
import java.util.Scanner;

public class U6_L1_Activity_One
{
  public static void main(String[] args)
  {
    // Initialize Scanner
    Scanner scan = new Scanner(System.in);
    
    // Create Array
    double[] arr = new double[4];
    /// User Input
    arr[1] = scan.nextDouble();
    arr[2] = scan.nextDouble();
    arr[3] = scan.nextDouble();
    
    // Final Output
    System.out.println("Contents: " + arr[1] + " " + arr[2] + " " + arr[3]);
    System.out.println("Sum: " + (arr[1] + arr[2] + arr[3]));
  }
}
```
+++

## Coding Activity 2
+++ U6_L1_Activity_Two.java
```java
import java.util.Scanner;
public class U6_L1_Activity_Two
{
  public static void main(String[] args)
  {
    // Create Array
    int[] h = new int[10];
    h[0] = 1;
    h[1] = h[0] + 2;
    h[2] = h[1] + 3;
    h[3] = h[2] + 4;
    h[4] = h[3] + 5;
    h[5] = h[4] + 6;
    h[6] = h[5] + 7;
    h[7] = h[6] + 8;
    h[8] = h[7] + 9;
    h[9] = h[8] + 10;
    
    // Initialize Scanner
    Scanner scan = new Scanner(System.in);
    
    // User Input
    int i = scan.nextInt();
    
    // Final Output
    if (i > 0 && i <= 10)
      System.out.print(h[i - 1]);
  }
}
```
+++
