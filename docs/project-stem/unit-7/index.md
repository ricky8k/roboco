---
label: "Unit 7: ArrayList"
icon: code
order: -1
---

# Unit 7: ArrayList
!!! Under Construction
This page is currently a work-in-progress! *Various elements may be incomplete or contain errors.*
<p><img src="/static/roboco.gif" width="200"></p>
!!!

## Unit 7: Lesson 1: ArrayList

### Coding Activity 1
+++ U7_L1_Activity_One.java
```java
import java.util.Scanner;
import java.util.ArrayList;

public class U7_L1_Activity_One
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
    System.out.println("\n" + words.size() + "\n" + words);
    /// Modify words
    if (words.size() > 2)
    {
      words.set(words.size() - 1, words.get(0));
      words.remove(0);
    }
    System.out.println(words);
  }
}
```
+++

## Unit 7: Lesson 2: Traversing ArrayLists

### Coding Activity 1
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

### Coding Activity 2
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

### Coding Activity 3
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

## Unit 7: Lesson 3: Array Algorithms with ArrayLists

### Coding Activity 1
+++ U7_L3_Activity_One.java
```java
import java.util.ArrayList;

public class U7_L3_Activity_One
{
  public static void shiftLeft(ArrayList<String> list)
  {
    // Move First in Array to Last
    if (list.size() >= 2)
    {
      list.add(list.get(0));
      list.remove(0);
    }
  }
}

```
+++

### Coding Activity 2
+++ U7_L3_Activity_Two.java
```java
import java.util.ArrayList;

public class U7_L3_Activity_Two
{
  public static void printStatistics(ArrayList<Integer> list)
  {
    // Create Variables
    int sum = 0;
    String mode = "no single mode";
    /// Temporary Storage
    int count = 0, maxCount = 1, savedNum = 0;
    
    // Calculation
    for (Integer num: list)
    {
      // Sum
      sum += num;
      /// Check for Mode
      count = 0;
      for (Integer num2: list)
      {
        if (num == num2)
          count++;
      }
      // Mode
      if (num != savedNum)
      {
        if (count > maxCount)
        {
          mode = num.toString();
          /// Update Temp. Storage
          savedNum = num;
          maxCount = count;
        }
        else if (count == maxCount)
        {
          mode = "no single mode";
        }
      }
    }
    // Average
    double avg = (double) sum / list.size();
    
    // Final Output
    System.out.println("Sum: " + sum + "\nAverage: " + avg + "\nMode: " + mode);
  }
}
```
+++

## Unit 7: Lesson 4: Linear Search

### Coding Activity 1
+++ U7_L4_Activity_One.java
```java
import java.util.ArrayList;

public class U7_L4_Activity_One
{
  public static int countSecondInitial(ArrayList<String> list, String letter)
  {
    // Initialize Variable
    int count = 0;
    
    // Check for letter in list
    for (String str: list)
    {
      if (str.toLowerCase().substring(1, 2).equals(letter.toLowerCase()))
        count++;
    }
    
    // End
    return count;
  }
}
```
+++

### Coding Activity 2
+++ U7_L4_Activity_Two.java
```java
import java.util.ArrayList;

public class U7_L4_Activity_Two
{
  public static int searchSecond(ArrayList<String> list, String word)
  {
    // Check for word in list
    for (String str: list)
    {
      if (str.equals(word))
      {
        for (int i = list.indexOf(word) + 1; i < list.size(); i++)
        {
          if (list.get(i).equals(word))
            return i;
        }
      }
    }
    
    // Not Found
    return -1;
  }
}
```
+++

## Unit 7: Lesson 5: Selection Sort

### Coding Activity 1
+++ U7_L5_Activity_One.java
```java
public class U7_L5_Activity_One
{
  public static void sortAndPrintReverse(String[] arr)
  {
    // Sort arr
    for (int pos = arr.length - 1; pos >= 1; pos--)
    {
      int maxIndex = pos;
      for (int j = pos; j >= 0; j--)
      {
        if (arr[j].compareTo(arr[maxIndex]) < 0)
        {
          maxIndex = j;
        }
      }
      // Swap Function
      String temp = arr[pos];
      arr[pos] = arr[maxIndex];
      arr[maxIndex] = temp;
    }
    
    // Final Output
    for (String s: arr)
    {
      System.out.print(s + " ");
    }
  }
}
```
+++

### Coding Activity 2
+++ U7_L5_Activity_Two.java
```java
import java.util.ArrayList;

public class U7_L5_Activity_Two
{
  public static void selectSortReverse(ArrayList<Integer> list)
  {
    // Sort list
    for (int pos = 0; pos < list.size() - 1; pos++)
    {
      // Initialize maxIndex
      int index = pos;
      // Check for Position
      for (int j = pos + 1; j < list.size(); j++)
      {
        if (list.get(j) > list.get(index))
        {
          index = j;
        }
      }
      // Swap Function
      int temp = list.get(pos);
      list.set(pos, list.get(index));
      list.set(index, temp);
    }
  }
}
```
+++