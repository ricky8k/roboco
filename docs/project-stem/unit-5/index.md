---
label: "Unit 5: Writing Classes"
icon: code
order: -1
---

# Unit 5: Writing Classes

## Unit 5: Lesson 1: Void Methods

### Coding Activity 1
+++ U5_L1_Activity_One.java
```java
/* Lesson 1 Coding Activity Question 1 */

import java.util.Scanner;

public class U5_L1_Activity_One
{
  public static void myMethod()
  {
    // Final Output
    System.out.println("I'm a void method!");
  }
}
```
+++

## Unit 5: Lesson 2: Parameters

### Coding Activity 1
+++ U5_L2_Activity_One.java
```java
/* Lesson 2 Coding Activity Question 1 */

import java.util.Scanner;

public class U5_L2_Activity_One
{
  public static void timeOfDay(int x)
  {
    // Final Output
    if (x == 0) // 00:00 (Midnight)
      System.out.println("midnight");
    else if (x == 12) // 12:00 (Noon)
      System.out.println("noon");
    else if (x == 18) // 18:00 (Dusk)
      System.out.println("dusk");
    else if (x > 0 && x < 12) // 00:01 - 11:59 (Morning)
      System.out.println("morning");
    else if (x > 12 && x < 18) // 12:01 - 17:59 (Afternoon)
      System.out.println("afternoon");
    else if (x > 18 && x < 24) // 18:01 - 23:59 (Evening)
      System.out.println("evening");
  }
}
```
+++

### Coding Activity 2
+++ U5_L2_Activity_Two.java
```java
/* Lesson 2 Coding Activity Question 2 */

import java.util.Scanner;

public class U5_L2_Activity_Two
{
  public static void reverser(String str)
  {
    // Initialize Variable
    String revStr = "";
    
    // Reverse str
    for (int i = str.length(); i > 0; i--)
    {
      revStr = revStr + str.substring(i - 1, i);
    }
    
    // Final Output
    System.out.println(revStr);
  }
}
```
+++

### Coding Activity 3
+++ U5_L2_Activity_Three.java
```java
/* Lesson 2 Coding Activity Question 3 */

import java.util.Scanner;

public class U5_L2_Activity_Three
{
  public static void printDouble(double num, int n)
  {
    // Final Output
    for (int i = 0; i < n; i++)
    {
      System.out.println(num);
    }
  }
}
```
+++

### Coding Activity 4
+++ U5_L2_Activity_Four.java
```java
/* Lesson 2 Coding Activity Question 4 */

import java.util.Scanner;

public class U5_L2_Activity_Four
{
  public static void coinConverter(int n)
  {
    // Coin Conversion
    int dollars = n / 100;
    int quarters = (n - (dollars * 100)) / 25;
    int dimes = (n - (dollars * 100) - (quarters * 25)) / 10;
    int nickels = (n - (dollars * 100) - (quarters * 25) - (dimes * 10)) / 5;
    int pennies = (n - (dollars * 100) - (quarters * 25) - (dimes * 10) - (nickels * 5));
    
    // Final Output
    System.out.println("Dollar Bills: " + dollars);
    System.out.println("Quarters: " + quarters);
    System.out.println("Dimes: " + dimes);
    System.out.println("Nickels: " + nickels);
    System.out.println("Pennies: " + pennies);
  }
}
```
+++

## Unit 5: Lesson 3: Parameters - Primitive vs. Class

### Coding Activity 1
+++ U5_L3_Activity_One.java
```java
/* Lesson 3 Coding Activity Question 1 */

import java.util.Scanner;
import shapes.*;

public class U5_L3_Activity_One
{
  public static void makeEqTriangle(RegularPolygon x)
  {
    x.setNumSides(3);
  }
}
```
+++

### Coding Activity 2
+++ U5_L3_Activity_Two.java
```java
/* Lesson 3 Coding Activity Question 2 */

import java.util.Scanner;
import shapes.*;
import testing.Math;

public class U5_L3_Activity_Two
{
  public static void randomize(Rectangle x)
  {
    // Randomize Length
    int length = (int) ((Math.random() * 11) + 10);
    if (length % 2 != 0)
      length++;
    
    // Randomize Width
    int width = (int) ((Math.random() * 7) + 7);
    if (width % 2 == 0)
      width++;
    
    // Set New Length & Width for Rectangle x
    x.setLength(length);
    x.setWidth(width);
  }
}
```
+++

### Coding Activity 3
+++ U5_L3_Activity_Three.java
```java
/* Lesson 3 Coding Activity Question 3 */

import java.util.Scanner;
import shapes.*;

public class U5_L3_Activity_Three
{
  public static void updateNumSides(RegularPolygon x, int y)
  {
    x.setNumSides(y);
  }
}
```
+++

## Unit 5: Lesson 4: Return Methods

### Coding Activity 1
+++ U5_L4_Activity_One.java
```java
/* Lesson 4 Coding Activity Question 1 */

import java.util.Scanner;
import shapes.*;

public class U5_L4_Activity_One
{
  public static int totalSides(RegularPolygon x, RegularPolygon y)
  {
    // Calculate
    int total = x.getNumSides() + y.getNumSides();
    
    return total;
  }
}
```
+++

### Coding Activity 2
+++ U5_L4_Activity_Two.java
```java
/* Lesson 4 Coding Activity Question 2 */

import java.util.Scanner;

public class U5_L4_Activity_Two
{
  public static double distance(int x1, int y1, int x2, int y2)
  {
    // Calculate
    double total = Math.sqrt(Math.pow((x2 - x1), 2) + Math.pow((y2 - y1), 2));
    
    return total;
  }
}
```
+++

### Coding Activity 3
+++ U5_L4_Activity_Three.java
```java
/* Lesson 4 Coding Activity Question 3 */

import java.util.Scanner;
import shapes.*;

public class U5_L4_Activity_Three
{
  public static double circDiff(Circle x, Circle y)
  {
    // Calculate
    double total = Math.abs(x.getCircumference() - y.getCircumference());
    
    return total;
  }
}
```
+++

### Coding Activity 4
+++ U5_L4_Activity_Four.java
```java
/* Lesson 4 Coding Activity Question 4 */

import java.util.Scanner;

public class U5_L4_Activity_Four
{
  public static int substringCount(String x, String y)
  {
    // Count
    int count = 0;
    for (int i = 0; i <= x.length() - y.length(); i++)
    {
      if (x.substring(i, i + y.length()).equals(y))
      {
        count++;
      }
    }
    
    return count;
  }
}
```
+++

## Unit 5: Lesson 5: Classes - The Basics

### Coding Activity 1
+++ Person.java
```java
public class Person
{
  // Initialize Variables
  private String firstName;
  private String lastName;
  private int age;
  private String ssn;
  
  public Person(String f, String l, int a, String s)
  {
    // Store Variables to Class
    firstName = f;
    lastName = l;
    age = a;
    ssn = s;
  }
  
  public String toString()
  {
    // Default Output
    return "SSN: " + ssn + "\n\tName: " + firstName + " " + lastName + "\n\tAge: " + age; 
  }
}
```
+++

### Coding Activity 2
+++ Oven.java
```java
public class Oven 
{
  // Represents the maximum possible temperature of an oven
  private int maxTemp;

  // Represents the current temperature of an oven
  private int currentTemp;

  // Constructs an oven with the given max temp and starting temp. The maximum
  // temperature of an oven must be greater than 0, but no more than 500.
  // The starting temperature should be less than or equal to the maximum t
  // temperature, but no less than 0.
  public Oven(int maxTemperature, int startTemperature) 
  {
    // Set maxTemp
    if (maxTemperature > 0 && maxTemperature <= 500)
    {
      maxTemp = maxTemperature;
    }
    else
    {
      maxTemp = 500;
    }
    // Set currentTemp
    if (startTemperature <= maxTemp && startTemperature >= 0)
    {
      currentTemp = startTemperature;
    }
    else if (startTemperature > maxTemp)
    {
      currentTemp = maxTemp;
    }
    else
    {
      currentTemp = 0;
    }
  }

  // Returns the maximum temperature of an oven
  public int getMaxTemp() 
  {
    return maxTemp;
  }

  // Returns the current temperature of an oven
  public int getCurrentTemp() 
  {
    return currentTemp;
  }

  // Turns an oven off by setting the current temperature to 0.
  public void turnOff() 
  {
    if (currentTemp > 0)
    {
      currentTemp = 0;
    }
  }

  // Returns whether the current temperature of an oven is greater than 0. Should
  // return false if the current temperature is 0.
  public boolean isOn() 
  {
    if (currentTemp > 0)
    {
      return true;
    }
    else
    {
      return false;
    }
  }

  // Sets the current temperature of an oven to the given value. Remember,
  // the current temperature should not exceed the max temp.
  public void preheat(int temp) 
  {
    if (temp < maxTemp)
    {
      currentTemp = temp;
    }
  }
}
```
+++

## Unit 5: Lesson 6: Constructors

### Coding Activity 1
+++ Plane.java
```java
public class Plane
{
  private int location;
  private String str = "";
  
  // Plane() ; No parameter
  public Plane()
  {
    // Set location
    location = 0;
  }
  
  // Plane() ; With parameter
  public Plane(int loc)
  {
    // Set location if loc is in range
    if (loc >= -2000 && loc <= 2000)
    {
      location = loc;
    }
    // Fallback location
    else
    {
      location = 0;
    }
  }
  
  // upward() ; Move plane by 100
  public void upward()
  {
    if (location + 100 <= 2000)
    {
      location += 100;
    }
  }
  
  // downward() ; Move plane by -100
  public void downward()
  {
    if (location - 100 >= -2000)
    {
      location -= 100;
    }
  }
  
  // getLocation() ; Return location
  public int getLocation()
  {
    return location;
  }
  
  // toString()
  public String toString()
  {
    str = "";
    for(int i = location / 100; i > -20; i--)
    {
      str += " ";
    }
    str += "@";
    return str;
  }
}
```
+++

## Unit 5: Lesson 7: Documenting a Class

### Coding Activity 1
+++ Rectangle.java
```java
public class Rectangle
{
  // Create Variables
  private double bs, ht;
  
  // Rectangle()
  /// Default
  public Rectangle()
  {
    bs = 1;
    ht = 1;
  }
  
  /// Parameter
  public Rectangle(double x, double y)
  {
    if (x > 1)
      bs = x;
    else
      bs = 1;
    if (y > 1)
      ht = y;
    else
      ht = 1;
  }
  
  // equals()
  public boolean equals(Rectangle x)
  {
    return (bs == x.getBase()) && (ht == x.getHeight());
  }
  
  // getArea()
  public double getArea()
  {
    return bs * ht;
  }
  
  // getBase()
  public double getBase()
  {
    return bs;
  }
  
  // getDiagonal()
  public double getDiagonal()
  {
    return Math.sqrt(Math.pow(bs, 2) + Math.pow(ht, 2));
  }
  
  // getHeight()
  public double getHeight()
  {
    return ht;
  }
  
  // getPerimeter()
  public double getPerimeter()
  {
    return (bs * 2) + (ht * 2);
  }
  
  // setBase()
  public void setBase(double x)
  {
    if (x > 0)
    {
      bs = x;
    }
  }
  
  // setHeight()
  public void setHeight(double x)
  {
    if (x > 0)
    {
      ht = x;
    }
  }
  
  // toString()
  public String toString()
  {
    String str = "rectangle with base " + bs + ", height " + ht;
    return str;
  }
}
```
+++

## Unit 5: Lesson 8: Static vs. Instance

### Coding Activity 1
+++ Car.java
```java
public class Car
{
  // Initialize Variables
  private String carMake;
  private String carModel;
  private int carYear;
  private double carMpg;
  private static int count = 0;
  private int carId;
  
  // Car() - Default
  public Car()
  {
    // User Input
    carMake = "None";
    carModel = "None";
    carYear = 2000;
    carMpg = 0.0;
    // Update carId
    count++;
    carId = count;
  }
  
  // Car()
  public Car(String make, String model, int year, double mpg)
  {
    // User Input
    carMake = make;
    carModel = model;
    /// Verify year
    if (year >= 1885 && year <= 2022)
    {
      carYear = year;
    }
    else if (year > 2022)
    {
      carYear = 2022;
    }
    else if (year < 1885)
    {
      carYear = 2000;
    }
    /// Verify mpg
    if (mpg >= 0)
    {
      carMpg = mpg;
    }
    else
    {
      carMpg = 0;
    }
    // Update carId
    count++;
    carId = count;
  }
  
  // toString()
  public String toString()
  {
    return "ID: " + carId + "\nMake: " + carMake + "\nModel: " + carModel + "\nYear: " + carYear + "\nMPG: " + carMpg;
  }
}
```
+++

## Assignment 5: Player

### Coding Activity
+++ Player.java
```java
public class Player 
{
  // Initialize Variables
  /// Player
  private static int numPlayers = 0;
  private String name;
  private int hp;
  /// Coordinates
  private int x;
  private int y;
  private int z;
  private int direction;
  
  // Create Player
  /// Make Player with Default Values
  public Player()
  {
    // Player
    /// Update Number of Players
    numPlayers++;
    /// Player Name
    name = "P" + numPlayers;
    System.out.print(numPlayers);
    /// Player Health
    hp = 20;
    /// Coordinates
    x = 0;
    y = 0;
    z = 0;
    /// Direction
    direction = 1;
  }
  
  /// Make Player with Name, X, Y, Z
  public Player(String n, int a, int b, int c)
  {
    // Player
    /// Update Number of Players
    numPlayers++;
    /// Player Name
    name = n;
    /// Player Health
    hp = 20;
    /// Coordinates
    x = a;
    y = b;
    z = c;
    /// Direction
    direction = 1;
  }
  
  /// Make Player with Name, X, Y, Z, HP, Direction
  public Player(String n, int a, int b, int c, int h , int d)
  {
    // Player
    /// Update Number of Players
    numPlayers++;
    /// Player Name
    name = n;
    /// Player Health
    if (h < 0)
      hp = 0;
    else
      hp = h;
    /// Coordinates
    x = a;
    y = b;
    z = c;
    /// Direction
    if (d >= 1 && d <= 6)
      direction = d;
    else
      direction = 1;
  }
  
  // Return Player Data
  /// Fetch Current # of Players
  public static int getNumPlayers()
  {
    return numPlayers;
  }
  /// Fetch Current Player Name
  public String getName()
  {
    return name;
  }
  /// Fetch Current X-Coordinate
  public int getX()
  {
    return x;
  }
  /// Fetch Current Y-Coordinate
  public int getY()
  {
    return y;
  }
  /// Fetch Current Z-Coordinate
  public int getZ()
  {
    return z;
  }
  /// Fetch Current Player HP
  public int getHp()
  {
    return hp;
  }
  /// Fetch Current Player Direction
  public int getDirection()
  {
    return direction;
  }
  /// Get Distance from Player to Coordinates
  public double getDistance(int a, int b, int c)
  {
    return Math.sqrt(Math.pow(a - x, 2) + Math.pow(b - y, 2) + Math.pow(c - z, 2));
  }
  /// Get Distance from Player to Player
  public double getDistance(Player p)
  {
    return Math.sqrt(Math.pow(p.getX() - x, 2) + Math.pow(p.getY() - y, 2) + Math.pow(p.getZ() - z, 2)); 
  }
  /// Convert to String
  public String toString()
  {
    return "Name: " + name + "\nHealth: " + hp + "\nCoordinates: X " + x + " Y " + y + " Z " + z + "\nDirection: " + direction;
  }
  
  // Modify Player
  /// Set Player HP
  public void setHp(int h)
  {
    if (h < 0)
      hp = 0;
    else
      hp = h;
  }
  /// Set Player Direction
  public void setDirection(int d)
  {
    if (d >= 1 && d <= 6)
      direction = d;
  }
  /// Move Player
  public void move(int d, int u)
  {
    // Set Direction
    int direction = getDirection();
    if (d >= 1 && d <= 6)
    {
      direction = d;
    }
    // Move
    if (direction == 1) // North
    {
      x += u;
    }
    else if (direction == 2) // South
    {
      x -= u;
    }
    else if (direction == 3) // Up
    {
      y += u;
    }
    else if (direction == 4) // Down
    {
      y -= u;
    }
    else if (direction == 5) // East
    {
      z += u;
    }
    else if (direction == 6) // West
    {
      z -= u;
    }
  }
  /// Teleport Player
  public void teleport(int a, int b, int c)
  {
    x = a;
    y = b;
    z = c;
  }
  /// Teleport Player to Player
  public void teleport(Player p)
  {
    x = p.getX();
    y = p.getY();
    z = p.getZ();
  }
  /// Attack Player
  public void attack(Player p, int d)
  {
    if (p.getHp() > 0)
    {
      if (p.getHp() - d >= 0)
        p.setHp(p.getHp() - d);
      else
        p.setHp(0);
      setHp(getHp() + (d / 2));
    }
  }
}
```
+++
