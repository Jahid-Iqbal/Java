# String Builder

**Declaration:**

```java
	public static void main(String[] args) {
		StringBuilder sBuilder= new StringBuilder("Jahid Iqbal");
		
		System.out.println(sBuilder);
	}
```
In StringBuffer all changes happened in place or reflected in source variable.

```java
	public static void main(String[] args) {
		StringBuilder sBuilder= new StringBuilder("Jahid Iqbal");
		
		System.out.println(sBuilder);	//Jahid Iqbal
		sBuilder.reverse();
		System.out.println(sBuilder);	//labqI dihaJ
	}
```
