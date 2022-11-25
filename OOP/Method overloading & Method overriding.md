# Method Overloading
>A class has multiple methods having same name but different signature. May be different in parameter type or number of parameters etc.

**Example:**  
Let say you call a method `add(4,5)` and consider below 3 scenarios.  

Scenario-1: Matches the arguments  
`add(int a, int b);`  
a=4 and b=5. No discrepancy follows.

Scenario-2: Doesn't match but arguments can be promoted.  
`add(int a, long b);`  
a=4 and b=5; Though 5 is an int value but it can be promoted to long.

```java
public class Practice {
	
	public void print(int a, int b) {
		System.out.println("A= "+(a+b));		
	}
	public void print(int a, long b) {
		System.out.println("B= "+(a+b));
	}
	public void print(long a, int b) {
		System.out.println("C= "+(a+b));
	}
}
	public static void main(String[] args) {
		Practice p= new Practice();
		p.print(1, 5);  //A=6
        p.print(1,5l);  //B=6   l determines long
        p.print(1l,5);  //C=6
	}

```

Scenario-3: Matches multiple methods/ Ambiguity  
`add(int a, long b);`  
`add(long a, int b);`  
a=4 and b=5. First method, 4 is int and 5 can be promoted to long. Second method, 4 can be promoted to long and 5 is int. So compiler will be confused that which add method should be called. That is an ambiguity problem.

# Method Overriding
>Methods having same name and same signatures as like the parent class is called method overriding.

The name and signatures are same as the parent class but the implementation can be different.

**Example:** 
```java
public class Practice {
	
	public void print(int a, int b) {
		System.out.println("Practice= "+(a+b));		
	}
}
public class ChildPractice extends Practice {
    public void print(int a, int b) {
		System.out.println("Child Practice="+(a+b));		
	}
	public static void main(String[] args) {
		Practice p= new Practice();
		p.print(1, 5);  //Practice=6

        Practice cp= new ChildPractice();
        p.print(1,5);   //Child Practice=6
	}
}
```

### Differences
|Method Overloading|Method Overriding|
|------------------|-----------------|
Same name|Same name|
Within the same class|In different classes|
Arguments are not same.|Same arguments.|
