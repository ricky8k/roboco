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

## Unit 8: Lesson 2: 2-D Array Algorithms

### Coding Activity 1
+++ TemperatureMonth.java
```java
public class TemperatureMonth
{
  private double[][] temperatures;

  public TemperatureMonth(double[][] t)
  {
    temperatures = t;
  }

  public double[] getMaxTempWeekly()
  {
    // Initialize Variable
    double[] arr = new double[temperatures.length];

    // Check for Max Temperatures
    for (int pos = 0; pos < temperatures.length; pos++)
    {
      // Reset Temporary Storage
      double maxTemp = temperatures[pos][0];
      // Scan Row
      for (int pos2 = 0; pos2 < temperatures[pos].length; pos2++)
      {
        if (temperatures[pos][pos2] > maxTemp)
          maxTemp = temperatures[pos][pos2];
      }
      // Add maxTemp in Row to arr
      arr[pos] = maxTemp;
    }
    
    // End
    return arr;
  }

  public double[] getMinTempWeekly()
  {
    // Initialize Variable
    double[] arr = new double[temperatures.length];

    // Check for Min Temperatures
    for (int pos = 0; pos < temperatures.length; pos++)
    {
      // Reset Temporary Storage
      double minTemp = temperatures[pos][0];
      // Scan Row
      for (int pos2 = 0; pos2 < temperatures[pos].length; pos2++)
      {
        if (temperatures[pos][pos2] < minTemp)
          minTemp = temperatures[pos][pos2];
      }
      // Add minTemp in Row to arr
      arr[pos] = minTemp;
    }
    
    // End
    return arr;
  }

  public double getRange()
  {
    // Temporary Storage
    double min = temperatures[0][0], max = temperatures[0][0];
    
    // Check Range
    for (int pos = 0; pos < temperatures.length; pos++)
    {
      // Scan Row
      for (int pos2 = 0; pos2 < temperatures[pos].length; pos2++)
      {
        // Check for Max Value
        if (temperatures[pos][pos2] > max)
          max = temperatures[pos][pos2];
        // Check for Min Value
        if (temperatures[pos][pos2] < min)
          min = temperatures[pos][pos2];
      }
    }
    
    // End
    return max - min;
  }

  public double getCertainTemp(int week, int day)
  {
    // End
    return temperatures[week][day];
  }
}
```
+++
