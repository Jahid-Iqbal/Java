# Abstraction

**Features:**  
* Abstract classes or methods must be declared with `abstract` keyword.
* It can contain abstract or no-abstract methods
* It can not be instantiated.
* It can have constructor and static methods.
* It can have final methods as well.
* Abstract methods must be overridden.

**Example:**  
```java
public abstract class Shape {
	
	String color;
	
	Shape(String color){
		System.out.println("Shape constructor");
		this.color=color;
	}
	abstract double area();
	public abstract String toString();
}

import java.util.*;
public class Circle extends Shape {
	
	double radius;
	Circle(String color,double radius){
		super(color);
		System.out.println("Circle constructor");
		this.radius= radius;
	}
	
	double area() {
		return (Math.PI*Math.pow(radius, 2));
	}
	
	public String toString() {
		return "Color is "+super.color+" Area is "+area();
	}
}

public class Main {

	public static void main(String[] args) {
		Circle area=  new Circle("Red",5.5);
		System.out.println(area.toString());
	}
}
/*
Shape constructor
Circle constructor
Color is Red Area is 95.03317777109125
*/
```