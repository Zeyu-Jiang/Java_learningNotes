#The extends keyword
*This page belongs to the page of modifiers in Java*

The extends keyword represents the relationship between two classes. 
For example, the relationship `class Programmer extents class Employee{}` means that class Programmer is a sub-class of class Employee.
you can say class Employee is inherited.
or you can say Programmer IS-A Employee. It means that Programmer is a type of Employee.
```java
class Employee{
    int salary = 4000;

    void printSalary(){System.out.println(salary);}
}

class Programmer extends Employee{
    int bonous;

    Programmer(int bonous){
        this.bonous = bonous;
    }
    void printBonous(){System.out.println(bonous);}
}


public class Example{

    public static void main(String[] args){
        Programmer jason = new Programmer(300);

        jason.printSalary();
        jason.printBonous();
    }
}
``` 