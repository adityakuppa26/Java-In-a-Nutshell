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
* The automatic conversion of primitive data types into its equivalent Wrapper type is known as auto-boxing and opposite operation is known as auto-unboxing. This is the new feature of Java5. So java programmer doesn't need to write the conversion code.  
```
class BoxingExample1{  
  public static void main(String args[]){   
        Integer a3=5;       // auto-Boxing  
        
        int a=a3;           // auto-unboxing , a contains value 5
        
        Integer i=new Integer(50);  
          
        if(i<100){            //unboxing internally  
        System.out.println(i);  
        }  
 }   
}  
```
  
* finally, using type wrappers for every basic operation might be tempting but it is far less efficient than the equivalent code written using the primitive data types.  
  
  
