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
  

  
