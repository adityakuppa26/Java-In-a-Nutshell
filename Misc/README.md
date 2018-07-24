# Autoboxing and Enumerations
  
* Enumeration is a list of names constants.  
* in java , an enumeration defines a class type.  
```
eg :
enum Apple                        // declaration
{
  adi,kit,sat,mri
}

Apple ap;
ap=Apple.sat;                 // initialisation
if(ap==Apple.adi)
{
  .....
}
System.out.println(Apple.mri);    //  outputs mri
Apple allval[]=Apple.values();      // returns a list of enum contents
```
  
**Type Wrappers**
  
* classes for encapsulation of primitive data types into objects.  
* as you cant pass primitive data type by reference.  
* many standard data structures in JAVA operate on objects only.  
* Double,Float,Integer,Short,Byte,Character,Boolean  
* Character(char ch) is a wrapper for char.  
char charValue() is used to obtain char value in the character object.  
```
eg:
main()
{
  Integer i=new Integer(100);   // boxing
  int io=i.intValue();          // unboxing
  System.out.println(i+" "+io);
}

output : 100 100
```
* all type wrappers override toString() to return the value contained in it.  
* process of encapsulating a value within an object is called boxing.  
* extracting a value from a type wrapper is called unboxing.  

  
