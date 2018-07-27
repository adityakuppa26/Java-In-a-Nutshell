# JAVA I/O
  
* java performs i/o through streams .  
* a stream is an abstraction that either produces or consumes information.  
* a stream hides the details of the actual physical devices connected and thereby standardizing the i/o operations for various devices.  
* java provides two types of streams :
```
-> Byte streams : handles input-output of bytes. 
                  Used for reading or writing raw binary data.
                  has two abstract classes InputStream and OutputStream at the top of class hierarchy.
-> Character streams : provides convenient means for handling i/o of characters.
                       has abstract classes Reader and Writer at the top of class hierarchy.
```
  
**Note**
```  
-> System.in is an object of type InputStream.  
-> System.out and System.err are objects of type PrintStream.  
-> these are byte streams even though they are used to read and write characters.  
```
  
# Reading Console Input
  
**BufferedReader**
  
* character stream i/o class.  
* constructor :
```
BufferedReader(Reader inputReader) ;

eg:

BufferedReader br = new BufferedReader(new InputStreamReader(System.in));

InputStreamReader takes the byte stream input from the System.in object and converts it to the character stream.
```
  
* Example :
```
main()
{
  char c;
  BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
  System.out.println("enter data , 'q' to quit");
  do
  {
    c=br.read();              // read() reads character by character.
    System.out.println(c);    // use readLine() to read an entire string.
  }while(c!='q');
}
```
  
# Writing Console Output
  
* although using System..out for writing to console is acceptable , it is used mostly for debugging purposes. For real - world programs , the recommended method of writing to console is through PrintWriter stream.  
* Example :
```
main()
{
  PrintWriter pw=new PrintWriter(System.out,true) ;  // true indicates that java flushes the output stream everytime 
                                                     // after println()
  pw.println("hello");
  int i=-7;
  pw.println(i);
}
```
