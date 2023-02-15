---
label: "6.5 - The Enhanced For Loop"
icon: code
order: -5
---

# Unit 6: Lesson 5 - The Enhanced For Loop

## Coding Activity 1
+++ U6_L5_Activity_One.java
```java
public class U6_L5_Activity_One
{

  public static void reverse(String[] words)
  {
    // For Each String in words[]
    for (String s : words)
    {
      // Print Term in Reverse Order
      for (int i = s.length() - 1; i >= 0; i--)
      {
        System.out.print(s.substring(i, i + 1));
      }
      // Output
      System.out.println();
    }
  }
}
```
+++

## Coding Activity 2
+++ U6_L5_Activity_Two.java
```java
public class U6_L5_Activity_Two
{
  public static int product(int[] arr)
  {
    // Create Variable
    int p = 1;
    // For Each Int in arr[]
    for(int k : arr)
    {
      p *= k;
    }
    // End
    return p;
  }
}
```
+++

## Coding Activity 3
+++ U6_L5_Activity_Three.java
```java
public class U6_L5_Activity_Three
{
  public static double avg(int[] arr)
  {
    // Create Variable
    double s = 0;
    // For Each Int in arr[]
    for (double n : arr)
    {
      s += n;
    }
    // Divide by arr[] Length
    s /= arr.length;
    // End
    return s;
  }
}
```
+++
