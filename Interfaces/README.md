# Interface
  
* to fully abstract a class interface from its implementation.  
* lacks instance variables, their methods have no body.  
* dont justg apply to classes in an inheritance hierarchy like that in abstract classes.  
* All methods must be declared public in the implementing class.  
* variables are public, final and static.  
* syntax :
```
class A implements intf1,intf2,... 
{
// body
}
```
* can have declarations to refer to class objects that implemented it for runtime polymorphism.  
* A class partially implementing an interface is declared abstract.  
* nested interfaces within class or interfaces can be used outside the scope of outer class/interface using the full qualification to them.  
* an interface can be extended by other interfaces.
