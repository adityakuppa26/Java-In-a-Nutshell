* In java, string is basically an object that represents sequence of char values. An array of characters works same as java string.  
* Generally, string is a sequence of characters. But in java, string is an object that represents a sequence of characters. The java.lang.String class is used to create string object.  
* Declaration :
```
String s1="Welcome";  
String s2="Welcome";//will not create new instance
String s=new String("Welcome");
```
  
* In java, string objects are immutable. Immutable simply means unmodifiable or unchangeable.Once string object is created its data or state can't be changed but a new string object is created.  
* There are three ways to compare string in java:  
1.By equals() method  
2.By = = operator  
3.By compareTo() method  
```
eg:

The String equals() method compares the original content of the string. It compares values of string for equality. 

class Teststringcomparison1{  
 public static void main(String args[]){  
   String s1="Sachin";  
   String s2="Sachin";  
   String s3=new String("Sachin");  
   String s4="Saurav";  
   System.out.println(s1.equals(s2));//true  
   System.out.println(s1.equals(s3));//true  
   System.out.println(s1.equals(s4));//false  
 }  
}  

The = = operator compares references not values. 

class Teststringcomparison3{  
 public static void main(String args[]){  
   String s1="Sachin";  
   String s2="Sachin";  
   String s3=new String("Sachin");  
   System.out.println(s1==s2);//true (because both refer to same instance)  
   System.out.println(s1==s3);//false(because s3 refers to instance created in nonpool)  
 }  
}  

The String compareTo() method compares values lexicographically and returns an integer value that describes if
first string is less than, equal to or greater than second string.
```
  
* 
