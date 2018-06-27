# Inheritance
  
* obtaining the attributes of a superclass ( or parent) by a subclass (child).  
* "extends" keyword is used :
```
class sub_class extends super_class        // can extends only one superclass at a time
{
....body......
}
```
  
* All members of the superclass except the private ones are inherited by the subclass.  
* A superclass instance can refer to a subclass object, but can only invoke or access the inherited members.  
  
**super keyword**
  
* to call superclass constructor  
* to refer to super class members when subclass members with the same name hide them.  
  
* Constructors are called starting from the superclass to the subclass in order , in a class hierarchy whenever an object is created.  
  
**Method overriding**
  
* when subclass has method with same name and type signature as its superclass.  
