---
label: "Unit 8: 2D Array"
icon: code
order: -1
---

# Unit 8: 2D Array
!!! Under Construction
This page is currently a work-in-progress! *Various elements may be incomplete or contain errors.*
<p><img src="/static/roboco.gif" width="200"></p>
!!!

## Unit 8: Lesson 1: 2-D Arrays

### Coding Activity 1
+++ U8_L1_Activity_One.java
```java
public class U8_L1_Activity_One
{
  public static int sumOfDiag(int[][] arr)
  {
    // Initialize Variable
    int sum = 0;
    
    // Add Lead Diagonal
    for (int i = 0; i < arr.length; i++)
    {
      // Validate
      if (i > arr[0].length - 1)
      {
        break;
      }
      sum += arr[i][i];
    }
    
    // End
    return sum;
  }
}
```
+++

### Coding Activity 2
+++ U8_L1_Activity_Two.java
```java
public class U8_L1_Activity_Two
{
  public static int[][] productTable(int r, int c)
  {
    // Initialize Variable
    int[][] arr = new int[r][c];

    // Create Product Table
    for (int row = 0; row < arr.length; row++)
    {
      for (int column = 0; column < arr[row].length; column++)
      {
        arr[row][column] = row * column;
      }
    }
    
    // End
    return arr;
  }
}
```
+++