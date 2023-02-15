---
label: "6.2 - Traversing an Array"
icon: code
order: -2
---

# Unit 6: Lesson 2 - Traversing an Array

## Coding Activity 1
+++ U6_L2_Activity_One.java
```java
public class U6_L2_Activity_One
{
  public static boolean containsNeg(double[] arr)
  {
    // Create Variable
    Boolean isNegative = false; /* False if no negatives are found */
    
    // Check Array for Negative Value(s)
    for (int i = 0; i < arr.length; i++)
    {
      if (arr[i] < 0)
      {
        isNegative = true; /* True when negative is found */
        break;
      }
    }
    
    // End
    return isNegative;
  }
}
```
+++

## Coding Activity 2
+++ U6_L2_Activity_Two.java
```java
public class U6_L2_Activity_Two
{
  public static int numDivisibleBy3(int[] arr)
  {
    // Create Variable
    int numsDivisible = 0; /* 0 if no divisible values */
    
    // Check Array for Divisible Value(s)
    for (int i = 0; i < arr.length; i++)
    {
      if (arr[i] % 3 == 0)
      {
        numsDivisible++; /* Adds 1 to total when divisible */
      }
    }
    
    // End
    return numsDivisible;
  }
}
```
+++

## Coding Activity 3
+++ U6_L2_Activity_Three.java
```java
public class U6_L2_Activity_Three
{
  public static int numDivisible(int num, int[] arr)
  {
    // Create Variables
    int divisor = num; /* Divide by provided num */
    int numsDivisible = 0; /* 0 if no divisible values */
    
    // Check Array for Divisible Value(s)
    for (int i = 0; i < arr.length; i++)
    {
      if (arr[i] % divisor == 0)
      {
        numsDivisible++;
      }
    }
    
    // End
    return numsDivisible;
  }
}
```
+++
