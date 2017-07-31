# The static keyword
*This page belongs to the page of modifiers in Java*

1. *static* can be variable. A static variable is different from instance variable.
instance variable
```java
class Number{
    int count; //it is a instance variable. it will be initilizaed to "0" when an object is created.
}
```
static variable
```java
class Number{
    static int count = 0; //it is a instance variable. All the objects will use the same variable. 
}
```

2. *static* can be method.
```java
class Desk{
    String name, brand;
    static String sologan = "This is a test!";

     Desk(String name, String brand){ // the object name should be case sensetive.
        this.name = name;
        this.brand = brand;
     }

     // This is a non-static method example.
     void display(){
        System.out.println(name+" "+brand);
     }

     // This is a static method example.
     /**
     *A static method can be invoked without the need for creating an instance(an object) of the class.
     *A static method belongs to the class rather than the object of the class.
     *A static method can only access to a static variable directly. 
     */
     static void show(){
        System.out.println(sologan);
     }
}

public class Example{

    public static void main(String[] args){
        Desk desk1 = new Desk("Jason","IKEA");
        
        desk1.display();
        Desk.show(); // A static method should be invoked with the class name rather than the object name. 

    }
}
```