---
label: "7.4 - Linear Search"
icon: code
order: -4
---

# Unit 7: Lesson 4 - Linear Search

## Coding Activity 1
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

## Coding Activity 2
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
