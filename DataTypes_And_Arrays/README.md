# Primitive Data Types
  
**Integers**
  
* Byte (8 bits) 
```
-> Used to work with datastream from network or file. 
-> Also used when working with raw binary data that cant be stored in other types.
```
  
* Short (16 bits)
  
* Int (32 bits) - most widely used integer data type.
  
* long (64 bits) 
  
**Floating Numbers**
  
* float (32 bits) - single precision floating numbers.
  
* double (64 bits) - doble precision floating numbers.
  
**Character**
  
* char (16 bytes ) - uses Unicode to represent many international languages.
  
** Boolean**
  
* true / false - these are non-numeric values in JAVA unlike C or C++ where these could be represented by non-zero and zero numbers respectively.  
  
# Type Conversions 
  
* Can take place when :
```
1. the two types are compatible.
2. destination type is larger than the source type.
```
  
* Explicit Conversion :
```
say we want to convert int to byte ,
byte b ; int a;
b = (byte) a;
here , modulo 256 value is assigned to b , if value of a is not in byte's range.
```
  
# Arrays
  
* Contiguous memory locations to store the homogenous values sequentially.  
* Provides random access.  
* int month[] = new int[12];  // here , all elements of the array are initialized to zero.
* int month[] = { 1,2,3,4,5,...12}; // auto-sizing  
