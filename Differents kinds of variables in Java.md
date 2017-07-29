# Differents kinds of variables in Java
**Instatnce Variables** get the memory at the time of object creation, each object will have the copy of the instance variable. It will not reflect other objects.
```java
class Student{
	String name; 
	int age = 18; // It is an instance variable. when the Jason's age is changed to 20, Zeyu's age is still 18.

	Student(String s){
		name = s;
	};
}

public class Example{

	public static void main(String[] args){
		Student student1 = new Student("Zeyu");
		Student student2 = new Student("Jason");
		student2.age = 20;
		System.out.println(student1.name+" "+student1.age);
		System.out.println(student2.name+" "+student2.age);
	}
}
```
>output:
>Zeyu 18
>Jason 20


**Class Variables** are shared to all objects. class variables will get memory only once. If any object changes the value of the static variable.
```java
class Student{
	String name; 
	static int age = 18; // it is a class variable(static variable). When Zeyu's age is changed to 20, Jason's age is also changed to 20 since the variable will get memory only once.  


	Student(String s){
		name = s;
	};
}

public class Example{

	public static void main(String[] args){
		Student student1 = new Student("Zeyu");
		Student student2 = new Student("Jason");
		student1.age = 20;
		System.out.println(student1.name+" "+student1.age);
		System.out.println(student2.name+" "+student2.age);
	}
}
```
>output
>Zeyu 20
>Jason 20

**Local Variables** are only visible to the methods in which they are declared. They are not accessible from the rest of the class.
```java
public class Example{

	public static int sum1(int a, int b){ // both methods have the same variable called sum, which is a local variable. So the value could be different.
		int sum = a + b;
		return sum;
	}

	public static int sum2(int a, int b){
		int sum = a + b;
		return sum;
	}
	public static void main(String[] args){
		System.out.println(sum1(3,4));
		System.out.println(sum2(7,4));

	}
}
```
>output
>7
>11

**Parameters** They are variables that are passed to the method of a class.
```java
public class Example{

	public static int sum1(int a, int b){ // int a and b are parameters.
		int sum = a + b;
		return sum;
	}
}
```