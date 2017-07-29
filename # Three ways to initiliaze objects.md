# Three ways to initiliaze objects
method1 through reference
```java
class Student{
    String name;
}

public class Example{

    public static void main(String[] args){
        Student student = new Student();
        student.name = "Jason";
        System.out.println(student.name);
    }
}
```

method2 initilization through method
```java
class Student{
    String name;

    void insertStudent(String s){
        name = s;
    }
}

public class Example{

    public static void main(String[] args){
        Student student = new Student();
        student.insertStudent("Zeyu");
        System.out.println(student.name);
    }
}
```

method3 inililization through constructor. *this is an example using parameterized constructor.*
```java
class Student{
    String name;

    Student(String s){
        name = s;
    };
}

public class Example{

    public static void main(String[] args){
        Student student = new Student("xu3gong");
        System.out.println(student.name);
    }
}
```