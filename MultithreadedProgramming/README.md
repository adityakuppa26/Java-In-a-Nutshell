# Multithreaded Prog
  
* A multi threaded program contains two or more parts that can run concureently. Each part of such program is called a thread.  
* JAVA thread model : thread priority , synchronization, messaging  
**Main Thread**
```
-> when a java program starts , one thread begins running immediately , this is called the main thread.  
-> it is the one which spawns other child threads.
-> it must be the last thread to finish.
```
  
**Creating a Thread**
  
**Using Runnable interface**
one needs to implement only one method of this interface i.e the public void run() method.  
```
example :
class NewThread implements Runnable
{
  Thread t;
  NewThread()
  {
    t=new Thread(this,"demo");
    t.start();
  }
  public void run()
  {
    try
    {
      //body
    }
    catch(InterruptedException e)
    {
      ....
    }
  }
}
class Demo
{
  public void main()
  {
    new NewThread();
    try
    {
     //body
    }
    catch(InterruptedException e)
    {
      .....
    }
  }
}
```
O/P : 
