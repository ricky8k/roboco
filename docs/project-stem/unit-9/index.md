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