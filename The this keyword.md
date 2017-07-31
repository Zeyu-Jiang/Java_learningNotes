#The this keyword
1. *this* can be used to refer current class instance variable. 
```java
class Desk{
    String name, brand;
    static double price = 20.0;

    // Since the names of the parameters of the constructor are the same as the names of class instance variales,
    // So using this can distinguish them from each other.
    Desk(String name, String brand){ 
        this.name = name;
        this.brand = brand;
    }

    // We can use another way to avoid using the keyword this. Just define the parameters by different names.
    Desk(String n, String b, double p){
        name = n;
        brand = b;
    }


    void display(){System.out.println(name+" "+brand);}
    void show(){System.out.println(name+" "+brand+" "+price);}
}

public class Example{

    public static void main(String[] args){
        Desk desk1 = new Desk("Jason","IKEA");
        desk1.display();
        Desk desk2 = new Desk("Zeyu","IKAE");
        desk2.show();
    }
}
```

2. *this* to invoke current class method. If you do not use the *this* keyword, the compiler automatically adds this keyword while invoking the method. 
```java
class Desk{
    String name, brand;
    double price;

    Desk(String name, String brand, double price){
        this.name = name;
        this.brand = brand;
        this.price = insertPrice(price);
        display();
    }

    void display(){System.out.println(name+" "+brand+" "+ price);} //this.display() and display() are both Okay.
    double insertPrice(double price){return price * price;};
}

public class Example{

    public static void main(String[] args){
        Desk desk1 = new Desk("Jason","IKEA",20.0);
    }
}
```

3. *this* to invoke current class constructor.
*calling default constructor from parameterized constuctor*
```java
class Desk{
    // This is a default constructor. 
    Desk(){
        System.out.println("Hello desk~");
    } 

    //This is a parameterized constructor.
    Desk(int price){
        this(); // calling default constructor from parameterised constructor.
        System.out.println("The price is "+price);
    }

}

public class Example{

    public static void main(String[] args){
        Desk desk2 = new Desk(45);// calling default constructor from parameterised constructor.
    }
}
```
*calling parameterized constructor from default constuctor*
```java
class Desk{
    //This is a parameterized constructor.
    Desk(int price){
        System.out.println("The price is "+price);
    }

    Desk(){
        this(10); // should offer an instance here. 
        System.out.println("Hello desk~");
    }

}

public class Example{

    public static void main(String[] args){
        Desk desk1 = new Desk(); // calling parameterized constructor from default constuctor.
    }
}
```
