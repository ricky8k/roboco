---
label: "Unit 6: Array"
icon: code
order: -1
---

# Unit 6: Array

## Unit 6: Lesson 1: One-Dimensional Arrays

### Coding Activity 1
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
    double[] arr = new double[3];
    /// User Input
    arr[0] = scan.nextDouble();
    arr[1] = scan.nextDouble();
    arr[2] = scan.nextDouble();
    
    // Final Output
    System.out.println("Contents: " + arr[0] + " " + arr[1] + " " + arr[2]);
    System.out.println("Sum: " + (arr[0] + arr[1] + arr[2]));
  }
}
```
+++

### Coding Activity 2
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

## Unit 6: Lesson 2: Traversing an Array

### Coding Activity 1
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

### Coding Activity 2
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

### Coding Activity 3
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

## Unit 6: Lesson 3: Arrays of Strings

### Coding Activity 1
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

### Coding Activity 2
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

### Coding Activity 3
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

## Unit 6: Lesson 4: Algorithms on Arrays

### Coding Activity 1
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

### Coding Activity 2
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

## Unit 6: Lesson 5: The Enhanced For Loop

### Coding Activity 1
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

### Coding Activity 2
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

### Coding Activity 3
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

## Assignment 6: Array Statistics
### Coding Activity
+++ StudentStatsArray.java
```java
public class StudentStatsArray 
{
  // Initialize Array
  private final Student[] students;
  
  // Add private final variable to hold Students array
  public StudentStatsArray(Student[] students) 
  {
    this.students = students;
  }

  // Returns the average gpa of the students
  public double averageGpa() 
  {
    // Temporary Storage
    double total = 0;
    // Gather GPAs
    for (Student s: students)
    {
      total += s.getGpa();
    }
    // End
    return total / students.length;
  }

  // Returns the gpa range of the students
  public double getGpaRange() 
  {
    // Temporary Storage
    double maxGpa = students[0].getGpa(), minGpa = students[0].getGpa();
    // Gather GPAs
    for (Student s: students)
    {
      if (s.getGpa() > maxGpa)
      {
        maxGpa = s.getGpa();
      }
      else if (s.getGpa() < minGpa)
      {
        minGpa = s.getGpa();
      }
    }
    // End
    return maxGpa - minGpa;
  }

  // Returns the name of the student that has the longest length
  public String getLongestName() 
  {
    // Temporary Storage
    String longestName = "";
    // Check for longestName
    for (Student s: students)
    {
      if (s.getName().length() > longestName.length())
        longestName = s.getName();
    }
    // End
    return longestName;
  }

  // Returns a count of the number freshman students
  public int getNumFreshman() 
  {
    // Temporary Storage
    int numFreshman = 0;
    // Check for Freshman
    for (Student s: students)
    {
      if (s.getYear() == 1)
        numFreshman++;
    }
    // End
    return numFreshman;
  }

  // Returns the index of the first student with a name equal to name. 
  // Returns -1 if not found
  public int search(String name) 
  {
    // Search for Student
    for (int i = 0; i < students.length; i++)
    {
      if (students[i].getName().contains(name))
      {
        return i;
      }
    }
    // Not Found
    return -1;
  }

  // Returns the index of the first student with a gpa greater than or equal to the gpa
  // Returns -1 if not found
  public int search(double gpa) 
  {
    // Search for First GPA
    for (int i = 0; i < students.length; i++)
    {
      if (students[i].getGpa() >= gpa)
        return i;
    }
    // Not Found
    return -1;
  }

  // Returns 1 if the students are sorted in ascending order by their gpa; -1 if they
  // are sorted in descending order; 0 otherwise.
  public int sortStatus() 
  {
    // Temporary Storage
    int sort = 0;
    double prevGpa = 0;
    
    // Scan for Ascending Order
    prevGpa = students[0].getGpa();
    for (Student s: students)
    {
      if (s.getGpa() >= prevGpa)
      {
        sort = 1;
        prevGpa = s.getGpa();
      }
      else
      {
        sort = 0;
        break;
      }
      if (sort == 0)
        break;
    }
    // Check Order
    if (sort == 1)
      return sort;
    // Scan for Descending Order
    prevGpa = students[0].getGpa();
    for (Student s: students)
    {
      if (s.getGpa() <= prevGpa)
      {
        sort = -1;
        prevGpa = s.getGpa();
      }
      else
      {
        sort = 0;
        break;
      }
      if (sort == 0)
        break;
    }
    // End
    return sort;
  }

  // Returns the array of students in JSON like format
  public String toString() 
  {
    // Temporary Storage
    String output = "";
    // Gather Student Data
    for (Student s: students)
    {
      output += ("{\n\tname: " + s.getName() + ",\n\tgpa: " + s.getGpa() + ",\n\tyear: " + s.getYear() + "\n},");
    }
    // End
    return "[\n" + output + "\n]";
  }
}
```
+++