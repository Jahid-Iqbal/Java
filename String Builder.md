# StringBuilder
>StringBuilder class creates immutable objects and contains non-synchronized methods.

StringBuilder classes syntax and inside methods are similar as StringBuffer.
```java
public final class StringBuilder
    extends AbstractStringBuilder
    implements Serializable, Comparable<StringBuffer>, CharSequence
{
	StringBuilder();
	StringBuilder(int capacity);
	StringBuilder(String str);
	StringBuilder(charSequence seq);
}	
```

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
