# Overview
  
* A class is a collection of objects or entities that share similar attributes.  
* A class is just a logical construct, it doesnt physically exist.  
```
Class declaration :

class Box
{
  int width,height,length;    // instance variables
  Box(int width,int length, int height )    // Constructor
  {
    this.width=width;
    this.length=length;
    this.height=height;
  }
  void volume()             // method
  {
    System.out.println(width*height*length);
  }
}
```
  
* An instance of a class is a reference to the memory location where the object is stored.       
* An instance of a class (or an object of a class) has physical existence.  
```
Instance declaration :

Box mybox= new Box(2,3,4); 
```
  
* A constructor is a method of a class bearing the same name as that of the class and having no return type.  
* A constructor ( Box() above ) is used to automatically initialize the instance variables of an object as soon as it is created.  
  
* "this" keyword is used by the class methods to refer to the object that invoked it. ( see above example )  
  
**Garbage Collection**
  
Space allocated for objects is released automatically when no reference to that object exists by the JVM.  
  
* finalize () method defines the specific actions that will occur when an object is just about to be reclaimed by the garbage collector. It is usually used to free the non-JAVA resources held by the object.  
  
**Overloading Methods**
  
* Same method names with different signatures.  
* Constructors can be overloaded as well.  
  
**Access Control**
  
* public : can be used by code outside yhe class.
* private : cant be used by the code outside the class.  
* protected : is used with reference to inheritance.  
* default : can be used by the code in the same package.  
  
**Static keyword**
  
* to use a class member without reference to a specific instance i.e independent of any class object.  
* for static variables, only copy of it exists and all instances share it .  
* for static methods :  
```
-> they can only call other static methods.
-> they must only access static data.
-> they cant refer to "this" or "super" in anyway.
```
  
**Nested classes**
  
* objects of inner class can be created only within the scope of outer class , to create an inner class object from outside the outer class , the full qualified name of the inner class must be used.  
* inner class can access members of outer class but not vice-versa.  
  

  

  
