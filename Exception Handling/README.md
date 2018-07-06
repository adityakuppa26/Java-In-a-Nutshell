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
  
**Uncaught Exceptions**
  
* When the user doesnt catch an exception , the JVM 's default handler handles the thrown exception.  
* User catches and handles exception beacuse:  
-> allows him to fix the error manually.  
-> prevents program from automatically terminating.  
  
**Multiple Catch**
  
* a try can be followed by a number of catch statements.  
* it is important to take care that exception subclasses must come before superclasses, otherwise it creates an unreachable code situation.  
  
**Nested Try**
  
* a try block can be nested in other try.  
* the error in inner try is handled by its catch if any, else it is passed to outer try for handling until a match is found. If no match , then it's handled by the default JVM handler.  
  
**Throw**
  
* to manually throw an exception.  
* Syntax:
```
throw Throwable_Instance;
```
Throwable_Instance must be of type Throwable class or its subclass.  
* Example:
```
try
{
  throw new ArithmeticException();
}
catch(ArithmeticException e)
{
  ....    // catches the thrown exception
}
```
