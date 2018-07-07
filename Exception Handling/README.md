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
  
**Throws**
  
* when a method is capable of causing an exception it does not handle, it must specify it so that callers can guard themselves against it.  
* if not mentioned , it is caught by the default handler and program doesn't compile (in case of checked exceptions).  
* Example :
```
void demo() throws ArithmeticException
{
  ..... // body
  throw new ArithmeticException;
}
main()
{
  try
  {
    demo();
  }
  catch(ArithmeticException e)
  {
    .......
  }
}
```
  
**Finally**
  
* create a block of code that will be executed after try/catch blocks complete.  
* it is executed if or not a catch exists , if or not an exception occurs or even when no match for a catch is found.  
* Usually used to free up resources held or to close file handlers.  
  
**Types Of Exceptions**
  
* Unchecked : need not be included in any method's throws list, compiler doesn't check if a method handles or throws these exceptions.  
* Checked : must be included in throws list , else the program is not compiled.  
