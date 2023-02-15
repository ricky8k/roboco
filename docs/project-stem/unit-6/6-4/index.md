---
label: "6.4 - Algorithms on Arrays"
icon: code
order: -4
---

# Unit 6: Lesson 4 - Algorithms on Arrays

## Coding Activity 1
+++ U6_L4_Activity_One.java
```java
public class U6_L4_Activity_One
{
  public static String insert(String[] words, String newWord, int place)
  {
    // Valid place in words[]
    if (place >= 0 && place < words.length)
    {
      // Replace words[place] with newWord
      for (int i = words.length - 1; i > place; i--)
      {
        words[i] = words[i - 1];
      }
      words[place] = newWord;
      // Create return
      String strReturn = "";
      for (int i = 0; i < words.length; i++)
      {
        strReturn += words[i];
      }
      return strReturn;
    }
    // Invalid place in words[]
    else
    {
      // Create return
      return "you need a valid number";
    }
  }
}
```
+++

## Coding Activity 2
+++ U6_L4_Activity_Two.java
```java
public class U6_L4_Activity_Two
{
  public static void swap(int[] arr, int i, int j)
  {
    // Check i & j
    if (i >= 0 && j >= 0)
    {
      // Store into temp. array
      int[] tempNum = {arr[i], arr[j]};
      // Write to arr
      arr[i] = tempNum[1];
      arr[j] = tempNum[0];
    }
  }
  
  public static void allReverseSwap(int[] arr)
  {
    // Store into temp. array
    int[] tempArr = new int[arr.length];
    for (int i = 0; i < arr.length; i++)
    {
      tempArr[i] = arr[(arr.length - 1) - i];
    }
    // Write to arr
    for (int i = 0; i < tempArr.length; i++)
    {
      arr[i] = tempArr[i];
    }
  }
}
```
+++
