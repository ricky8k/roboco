---
label: "7.2 - Traversing ArrayLists"
icon: code
order: -2
---

# Unit 7: Lesson 2 - Traversing ArrayLists

## Coding Activity 1
+++ U7_L2_Activity_One.java
```java
import java.util.Scanner;
import java.util.ArrayList;

public class U7_L2_Activity_One
{
  public static void main(String[] args)
  {
    // Initialize Scanner
    Scanner scan = new Scanner(System.in);
    
    // Create Variables
    ArrayList<String> words = new ArrayList<String>();
    String input = "";
    
    // User Input
    System.out.println("Please enter words, enter STOP to stop the loop.");
    while (!(input.equals("STOP")))
    {
      input = scan.nextLine();
      // Check input
      if (!(input.equals("STOP")))
        words.add(input);
    }
    
    // Final Output
    System.out.println(words);
    /// Reverse Order
    for (int i = 0; i < words.size(); i++)
    {
      System.out.println(words.get((words.size() - 1) - i) + words.get(i));
    }
  }
}
```
+++

## Coding Activity 2
+++ U7_L2_Activity_Two.java
```java
import java.util.ArrayList;

public class U7_L2_Activity_Two
{
  public static int highestNum(ArrayList<Integer> arr)
  {
    // Check for Highest Num in arr
    int n = 0;
    for (int i = 0; i < arr.size(); i++)
    {
      if (arr.get(i) > n)
      {
        n = arr.get(i);
      }
    }
    
    // End
    return n;
  }
}
```
+++

## Coding Activity 3
+++ U7_L2_Activity_Three.java
```java
import java.util.ArrayList;

public class U7_L2_Activity_Three
{
  public static ArrayList<Integer> getEvens(ArrayList<Integer> vals)
  {
    // Check for Even Nums in vals
    ArrayList<Integer> even = new ArrayList<Integer>();
    for (int i = 0; i < vals.size(); i++)
    {
      if (vals.get(i) % 2 == 0)
      {
        even.add(vals.get(i));
      }
    }
    
    // End
    return even;
  }
}
```
+++
