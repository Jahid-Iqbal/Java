# Class
>Class is the collection of objects.

* Class is not a real world entity.
* Class does not occupy memory.

**Example:**  
- Animal
- Birds
- Vehicle

Syntax:  

access-modifier ClassName{  
    - methods  
    - constructors   
} 

If multiple classes are defined inside a single file then below scenarios will be happened.  
- Multiple classes can be declared.

```java
public class Practice {

}
class Practice2{
	
}
class Practice3{
	
}
```
- At most one public class can be there.
- If the file contains any public class then, file name should be as like as the public class name.
- If each class contains main method then .class file will be generated for each class containing main method.

```java
class A{
	public static void main(String[] args){
		System.out.println("A");
	}

}
class B{
	public static void main(String[] args){
		System.out.println("B");
	}
}
class C{

}
```
Run the file using below command.
```sh
javac run.java
```
System created files `A.class`, `B.class`, `C.class`.

