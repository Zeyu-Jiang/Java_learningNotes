# What is an object 
**Object** is an entity that has *State* and *Behavior* 

>states: represents data(value) of an object.
>behavior: represents behavior (functionality) of an object.
>For Example: Pen is an object. Its name is Reynolds, color is white etc. known as its state. It is used to write, so writing is its behavior. 

It can be physcial and logical. 


# What is a class
**Class** a collection of objects. It is logical.
It contains
*fields*: a [instance]() variable is an instance of fields.  `int id`
*methods*: a initialization object method.
```java
class Student{
    int id;
    String name;

    void addStudent(int i, String s){
        id = i;
        name = s;
    }
}
```
*constructors*: is a special type of method that initilize object. Syntax of default constructor: `<class_name>(){}`
type1 default constructor.
```java
class Bike1{
    Bike1(){System.out.println("a bike object is created")}; 
    // thr print task is a sample showing that constructor can do other tasks like regular methods do.

    void main(){
        .. ;
    }
}
```
type2 parameterized constructor.
```java
class Bike2{
    String name;

    Bike2(String s){
        name = s;
        
    }

    void main(){
        .. ;
    }
}
```

Constructor overloading
>Constructor overloading is a technique in Java in which a class can have any number of constructors that differ in parameter lists.
>The compiler differentiates these constructors by taking into account the number of parameters in the list and their type.

```java
class Student5{  
    int id;  
    String name;  
    int age;  
    Student5(int i,String n){  // this is the first constructor.
    id = i;  
    name = n;  
    }  
    Student5(int i,String n,int a){  // this is the second constructor. 
    id = i;  
    name = n;  
    age=a;  
    }  
    void display(){System.out.println(id+" "+name+" "+age);}  
   
    public static void main(String args[]){  
    Student5 s1 = new Student5(111,"Karan");  
    Student5 s2 = new Student5(222,"Aryan",25);  
    s1.display();  
    s2.display();  
   }  
}  
```

Copy constructor
method1 using copy constructor.
```java
class Student{
    String name;

    Student(String s){
        name = s;
    }

    Student(Student student){
        name = student.name; 
    }
}

class Example{

    public static void main(String[] args){
        Student s1 = new Student("Jason"); // when creating a new object, just put the value in the brackets. no value type needed.
        Student s2 = new Student(s1); 

        System.out.println(s1.name);
        System.out.println(s2.name);
    }
}
```

method2 Coping values without constructor
```java
class Student{
    String name;

    Student(String s){
        name = s;
    }

    Student(){}
}

class Example{

    public static void main(String[] args){
        Student s1 = new Student("Zeyu"); 
        Student s2 = new Student(); 
        s2.name = s1.name;

        System.out.println(s1.name);
        System.out.println(s2.name);
    }
}
```
*blocks* 
*nested class and interface*

keywords `new` is used to allocate memory at run time.

# Object and Class Example: main outside class
This is a common used approach. 
```java
class Student{ // this is the first class. 
    String name;
    String sex;
    int age;

    void addStudent(String n,String s, int a){ // initilization object method.
        name = n;
        sex = s;
        age = a;
    }

    void printDetail(){ // another method examole.
        System.out.println(name+" "+sex+" "+age);
     }
}

class Teacher{ // this it the second class.
    String name;
    String subject;

    void addTeacher(String n, String s){
        name = n;
        subject = s;
    }

    void printDetail(){
        System.out.println(name+" "+subject);
    }
}

public class Example{ // this class contain the main method. so the file name should be the same with this class, Example.

    public static void main(String[] args){
        Student std1 = new Student();
        Teacher teacher1 = new Teacher();
        Teacher teacher2 = new Teacher();

        std1.addStudent("Jason","Male",28);
        std1.printDetail();
        teacher1.addTeacher("Mark","");
        teacher2.addTeacher("Logan","Physics");
        teacher1.printDetail();
        teacher2.printDetail();

    }
}
```

# The name conventions in Java
**class name**: starts with uppercase letter and should be noun.
```java
class Student{};
```

**interface name**

**method name**: starts with lowercase letter and should be a verb.
```java
void actionPerformed();
```

**variable name**: starts with lowercase letter.
```java
String firstName
```
