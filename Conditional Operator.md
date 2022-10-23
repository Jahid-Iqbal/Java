# Conditional Operator

If you want to check which value is larger by executing a condition then you need to do the following.

```java
package com.basics;

public class condition {
	public static void main(String[] args) {
		
		int value1=5;
		int value2=10;
		if(value1>value2)
			System.out.println(value1);
		else
			System.out.println(value2);
	}
}
```
But what if you can check the same condition, writing only one line of code like as,

```java
condition ? expression1 : expression2
```
Executing the expression1 if the condition is true else executing expression2.

```java
package com.basics;

public class condition {
	public static void main(String[] args) {
		
		int value1=5;
		int value2=10;
		
		int checkedValue=value1>value2 ? value1 : value2;
		
		System.out.println(checkedValue);   //10
	}
}
```