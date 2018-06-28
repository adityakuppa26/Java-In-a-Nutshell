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
* if you have to access the superclass version ofthe overrridden method, use "super".  
* Overridden methods allow for run time polymorphism.  
  
**Abstract Classes**
  
* provides the structure of an abstraction without providing a complete implementation of every method.  
* any class with one or more abstract methods is declared abstract.  
* an abstract class can have no objects of its own, but can be declared to refer to its subclass's objects.  
* any subclass of an abstract class must either implement all of the abstract methods or itself be declared as abstract.  
  
**Final Keyword**
```
-> for variables, prefixing them with final keyword makes them act as constants.
-> to prevent overriding : declare the superclass methods as final , to avoid over-riding.  
-> to prevent inheritance : declare superclass as final, to avoid inheriting it. 

Note : A class can't be abstract and final at the same time. 
```
