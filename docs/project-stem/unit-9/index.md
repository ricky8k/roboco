---
label: "Unit 9: Inheritance"
icon: code
order: -1
---

# Unit 9: Inheritance
!!! Under Construction
This page is currently a work-in-progress! *Various elements may be incomplete or contain errors.*
<p><img src="/static/roboco.gif" width="200"></p>
!!!

## Unit 9: Lesson 1: Inheritance

### Coding Activity 1
+++ SpecialityCoffee.java
```java
public class SpecialityCoffee extends Coffee
{
  // Initialize Variable
  private String flavor;
  
  // Default SpecialityCoffee()
  public SpecialityCoffee()
  {
    super();
    flavor = "Vanilla";
  }
  
  // 3-Constructor SpecialityCoffee()
  public SpecialityCoffee(String size, String type, String flavor)
  {
    this(size, false, 1, type, flavor);
  }
  
  // 5-Constructor SpecialityCoffee()
  public SpecialityCoffee(String size, boolean isSkinny, int shots, String type, String flavor)
  {
    super(size, isSkinny, shots, type);
    this.flavor = flavor;
  }
  
  // Output to String
  public String toString()
  {
    return super.toString() + " with " + flavor;
  }
}
```
+++


## Unit 9: Lesson 2: Inheritance Overriding Methods

### Coding Activity 1
+++ SpecialityCoffee.java
```java
public class SpecialityCoffee extends Coffee 
{
  // Initialize Variable
  private String flavor;

  // Default SpecialityCoffee()
  public SpecialityCoffee() 
  {
    // Calls super-constructor to create default coffee then sets flavor
    super();
    flavor = "vanilla";
  }

  // 3-Constructor SpecialityCoffee()
  public SpecialityCoffee(String size, String type, String flavor) 
  {
    // Calls constructor below with a mix of parameters and default values
    this(size, false, 1, type, flavor);
  }

  // 5-Constructor SpecialityCoffee()
  public SpecialityCoffee(String size, boolean isSkinny, int shots, String type, String flavor)
  {
    // Calls super-constructor to set first 4 variables then sets flavor
    super(size, isSkinny, shots, type);
    this.flavor = flavor;
  }
  
  // Get Price of Speciality Coffee
  public int getPrice()
  {
    // Temporary Storage
    int price = super.getPrice();
    
    // Check Size of Coffee
    if (super.getSize().matches("large|extra large")) /* L or XL */
    {
      price += 50;
    }
    else /* Other Size */
    {
      price += 30;
    }
    
    // End
    return price;
  }
  
  // Output to String
  public String toString() 
  {
    // Calls Coffee toString and appends flavor to end
    return super.toString() + " with " + flavor;
  }
}
```
+++

### Coding Activity 2
+++ DoubleCone.java
```java
public class DoubleCone extends Cone
{
  // Initialize Variables
  private String flavor;
  private String flavor2;
  private String topping;
  
  // 2-Constructor DoubleCone()
  public DoubleCone(String f, boolean w)
  {
    // Creates Cone with 2x flavor f
    super(f, w);
    flavor = f;
    flavor2 = f;
  }
  
  // 3-Constructor DoubleCone()
  public DoubleCone(String f1, String f2, boolean w)
  {
    // Creates Cone with flavors f1 and f2
    super(f1, w);
    flavor = f1;
    flavor2 = f2;
  }
  
  // Set Flavor of Double Cone
  public void setFlavor(String f)
  {
    // Overwrites flavor and flavor2 to f
    super.setFlavor(f);
    flavor = f;
    flavor2 = f;
  }
  
  // Set Flavor of Double Cone
  public void setFlavor(String f1, String f2)
  {
    // Overwrites flavor to f1 and flavor2 to f2
    super.setFlavor(f1);
    flavor = f1;
    flavor2 = f2;
  }
  
  // Add Topping to Double Cone
  public void addTopping(String t)
  {
    // Sets topping to t
    topping = t;
  }
  
  // Output to String
  public String toString()
  {
    // Temporary Storage
    String output = "double " + super.toString();
    
    // Check Flavors
    if (flavor.equals(flavor2)) /* Same 2 Flavors */
    {
      output += " x2";
    }
    else /* Different 2 Flavors */
    {
      output += " and " + flavor2;
    }
    
    // Check Topping
    if (topping != null)
      output += " with " + topping;
    
    // End
    return output;
  }
}
```
+++