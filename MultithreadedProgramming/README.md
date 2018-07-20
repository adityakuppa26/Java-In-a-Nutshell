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
  
**Extending Thread Class**
  
Must override the run() method.
```
example :
class Demo extends Thread
{
  Demo()
  {
    super("demo");
    System.out.println("child"+this);
    start();
  }
  public void run()
  {
    ......
  }
}
class ExtThread{
main()
{
  new Demo();
  try
  {
    ...
  }
  catch()
  {
  ..
  }
}
}
```
  
**isAlive and join**
  
* main() must wait until children threads end. How does the main thread know when they end ?  
* There are two methods for the above question : 
```
-> final boolean isAlive() : tells if a thread is still existing or not
-> final void join() throws InterruptedException : waits until the thread on which it is called terminates
```
  
**Thread Priority**
  
* 1-10  
* MIN_PRIORITY(1) , MAX_PRIORITY(10), NORM_PRIORITY(5) are the instance variables of Thread class.  
* final void setPriority(int level) : to set the priority of a thread    
* final int getPriority() : gives the alloted priority of a thread  
  
**Synchronization**
  
* when two or more threads need access to the shared resources at the same time.  
* uses monitors.  
  
**Synchronized Methods**
  
* while a thread is inside a synchronised method , all other threads that try to call it on the same instance have to wait , until the inside thread is done.  
* append "synchronized" beofre a method, to make it a synchronized method of a class.  
  
**Synchronized statement**
  
* say you want a synchronized access to objects of a class that has no synchronized methods , this class was created by a third party and you dont have source code.  
* put the calls to the methods defined by this class inside a "synchronized" block.  
```
synchronized(object)
{
  // calls 
}
```
  
**Interthread Communication**
  
* to avoid polling , eg: producer-consumer problem  
* provides 3 methods :  
```
wait() : calling thread goes to sleep until notified.
notify() : wakes up a thread that called wait() on the same object.
notifyAll() : wakes up all the threads that called wait() on the same object.
```
