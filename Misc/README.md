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
  
