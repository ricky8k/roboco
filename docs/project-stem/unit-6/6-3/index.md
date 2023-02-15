---
label: "6.3 - Arrays of Strings"
icon: code
order: -3
---

# Unit 6: Lesson 3 - Arrays of Strings

## Coding Activity 1
+++ U6_L3_Activity_One.java
```java
public class U6_L3_Activity_One
{
  public static String findShortest(String[] words)
  {
    // Create Variable
    String shortestWord = words[1];
    
    // Compare words[i] to shortestWord
    for (int i = 0; i < words.length; i++)
    {
      if (words[i].length() < shortestWord.length())
      {
        shortestWord = words[i]; // Make words[i] the new shortestWord
      }
    }
    
    // End
    return shortestWord;
  }
}
```
+++

## Coding Activity 2
+++ U6_L3_Activity_Two.java
```java
public class U6_L3_Activity_Two
{ 
  public static void removeVowels(String[] words)
  {
    // Create Variable
    String noVowels = "";

    // Check/Remove Vowels & Output
    for (int i = 0; i < words.length; i++)
    {
      // Refresh noVowels for next word
      noVowels = "";
      for (int j = 0; j < words[i].length(); j++)
      {
        // Remove Vowel(s)
        if (words[i].substring(j, j + 1).matches("a|e|i|o|u"))
        {
          noVowels += "";
        }
        // Keep Constant(s)
        else
        {
          noVowels += words[i].substring(j, j + 1);
        }
      }
      // Final Output
      System.out.print("\n" + noVowels);
    }
  }
}
```
+++

## Coding Activity 3
+++ U6_L3_Activity_Three.java
```java
public class U6_L3_Activity_Three
{
  public static void printUn(String[] words)
  {
    // Check Words & Output
    for (int i = 0; i < words.length; i++)
    {
      if (words[i].length() > 2 && words[i].substring(0, 2).equals("un"))
      {
        System.out.println(words[i]);
      }
    }
  }
}
```
+++
