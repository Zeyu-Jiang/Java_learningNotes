#Java Inheritance
1. single inheritance
```java
// Animal class is single inherited by Dog class.
class Animal{
    void eat(){System.out.println("eat");}
}

class Dog extends Animal{
    void drink(){System.out.println("drink");}
}


public class Example{

    public static void main(String[] args){
        Dog dog = new Dog();
        dog.eat();
        dog.drink();
    }
}
```

2. multilevel inheritance
```java
// BabyDog class extends Dog class, which extends Animal class
class Animal{
    void eat(){System.out.println("eat");}
}

class Dog extends Animal{
    void drink(){System.out.println("drink");}
}

class BabyDog extends Dog{
    void run(){System.out.println("run");}
}

public class Example{

    public static void main(String[] args){
        BabyDog baby = new BabyDog();
        baby.eat();
        baby.drink();
        baby.run();
    }
}
```

3. inheritance
```java
// Both Cat and Dog class extend Animal class.
class Animal{
    void eat(){System.out.println("eat");}
}

class Dog extends Animal{
    void drink(){System.out.println("drink");}
}

class Cat extends Animal{
    void run(){System.out.println("run");}
}

public class Example{

    public static void main(String[] args){
        Dog dog = new Dog();
        Cat cat = new Cat();

        dog.eat();
        cat.eat();
    }
}
```

#Java Aggregation
If a class has an entity reference, it is known as Aggregation. For example, An Employee class HAS-A Address class.
```java
class Employee{
    int id;
    String name;
    Address address;

    Employee(int id, String name, Address address){
        this.id = id;
        this.name = name;
        this.address = address;
    }

    void printInfo(){
        System.out.println(id+" "+name+" "+address.city+" "+address.country);
    }
}

class Address{
    String city,country;

    Address(String city, String country){
        this.city = city;
        this.country = country;
    }
}

public class Example{

    public static void main(String[] args){
        Address add1 = new Address("Chongqing","China");
        Address add2 = new Address("Seattle","US");

        Employee jason = new Employee(1001,"Jason",add1);
        Employee zeyu = new Employee(1002,"Zeyu",add2);

        jason.printInfo();
        zeyu.printInfo();
    }
}
``` 