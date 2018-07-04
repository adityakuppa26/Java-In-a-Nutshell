# Exception Handling
  
* An exception is an abnormal condition that arises in a code piece at runtime ; a run-time error.  
* JAVA exception is an object.  
* Structure to handle exceptions :
```
try
{
  // block of code to monitor for errors
}
catch ( ExceptionType er)
{
  // exception handler
}
finally
{
  // block of code executed after try/catch block
}
```
  
**Exception Types**
  
* All exception types are subclasses of class Throwable.  
* Throwable class has two major subclasses : Exception and Error.  
* Exception class deals with the exceptional conditions that user program is expected to catch.  
* Error class deals with the exceptions that cant be caught by user program, these are usually handled by the JVM.  
