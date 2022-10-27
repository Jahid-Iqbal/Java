# Variables
>A variable is piece of memory location that can store data. A variable has a data type.

`int value=10;`

![picture](https://github.com/Jahid-Iqbal/Java/blob/main/Pictures/variable.png)

Here, value is a variable which represent memory space in JVM. The stored value or literal is 10.  
The value of the variable can be changed. Like, if you do `value=value * 10;` then the value of the variable will be changed to 100.

**Different Types of Variables:**  
1. Local Variable
2. Instance Variable
3. Static Variable

### Local Variable:  
The variable that declared inside any function, constructor or code blocks are called local variable for that function.

```java
	public static int sum() {
		int a=10;       //local variable
		int b=10;
		int sum=a+b;	
		return sum;
	}
```
**Declaration:** Inside method , constructor or blocks.

**Scope:** Inside method , constructor or blocks.

**When Get Allocated:** When method, constructor or blocks started executing. Variable destroyed when exit the method.

**Stored Memory:** Stack Memory

**Default Values:** The variable doesn't has nay default value. Must need to initialized otherwise through error.

**Access Specifier:** Cannot use any access specifier. Like as,
```java
public static int sum() {
		public int a=10;       //Illegal modifier for parameter a; only final is permitted
		int b=10;
		int sum=a+b;	
		return sum;
```
### Instance Variable
The variable that declared inside the class but not inside any method, constructor or code blocks.

```java
public class Variables {
	
	int instanceVariable=1000;		//instance variable
	public int sum() {
		int localVariable=10;					//local variable
		int sum=instanceVariable+localVariable;
		return sum;
	}
}
```
### Static Variable
The variable that declared with static keyword and inside the class but outside of the function, constructor or blocks.

```java
public class Variables {
	public static int staticVariable=1000;		//static variable
	public int sum() {
		int localVariable=10;					//local variable
		int sum=staticVariable+localVariable;
		return sum;
	}
}
```
**How to access the static variable:**  
1. Directly
2. Using class name (ClassName.variableName)
3. Using object reference.

**Differences:**  
Variable|Declaration|Scope|When Get Allocated|Stored Memory|Default values|Access Modifier (public,private)|
--------|-----------|-----|------------------|-------------|--------------|---------------|
Local Variable|Inside method , constructor or blocks.|Accessible only inside method , constructor or blocks.|Variable takes memory space when method, constructor or blocks started executing. Variable destroyed when exit the method.|Stack Memory|The variable doesn't has nay default value. Must need to initialized otherwise through error.|Cannot use any access specifier.|
Instance Variable|Inside the class but not inside the method, constructor or blocks.| Anywhere inside the class but not inside the static methods, constructors or blocks.| Variable takes memory space when object created and destroyed when object terminates.|Heap Memory| They have default values.| Access modifier can be used.|
Static Variable| Declares using static keyword and inside the class but outside the method, constructor and blocks.|Anywhere inside the class including static methods.|Variable takes memory space when .class file loaded and destroyed when .class file terminates.|Non-Heap memory or static memory.|Variables have default values.|Access modifier can be used.|
