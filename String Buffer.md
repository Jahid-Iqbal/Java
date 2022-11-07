# StringBuffer
>Creating objects in Heap Memory and every time updating the content in original object. So, StringBuffer is mutable.

```java
public final class StringBuffer
    extends AbstractStringBuilder
    implements Serializable, Comparable<StringBuffer>, CharSequence
{
	StringBuffer();
	StringBuffer(int capacity);
	StringBuffer(String str);
	StringBuffer(charSequence seq);
}	
```

**Capacity of the Constructors:**  
```java
public static void main(String[] args) {
		//no-argument constructor
	StringBuffer sb=new StringBuffer();
	System.out.println(sb.capacity());	//16. default capacity
		
	sb.append("Jahid");
	System.out.println(sb.capacity());	//16
		
	sb.append("Jahid is learning");
	System.out.println(sb.capacity());	//34. Updating the capacity as the string exceeded the limit.

		//Constructor with String argument
	StringBuffer sb=new StringBuffer("Jahid");
	System.out.println(sb.capacity());	//16+5=21. default+length of string
		
	sb.append("Jahid is");
	System.out.println(sb.capacity());	//21
		
	sb.append("Jahid is learning");
	System.out.println(sb.capacity());	//44. Updated the capacity.

		//Constructor with integer arguments
	StringBuffer sb=new StringBuffer(15);
	System.out.println(sb.capacity());	//15. User defined capacity.
		
	sb.append("Jahid is");
	System.out.println(sb.capacity());	//15
		
	sb.append("Jahid is learning");
	System.out.println(sb.capacity());	//32
}
```
The default capacity of no-argument constructor is 16. If user will exceed the limit then the capacity will be updated following below statement.  
`newCapacity= (oldCapacity*2)+2`

**Declaration:**
```java
	public static void main(String[] args) {
		StringBuffer sBuffer= new StringBuffer("Abdullah");
		
		System.out.println(sBuffer);	//Abdullah
	}
```

In StringBuffer all changes happened in place or reflected in source variable.
```java
	public static void main(String[] args) {
		StringBuffer sBuffer= new StringBuffer("Jahid Iqbal");
		
		System.out.println(sBuffer);	//Jahid Iqbal
		sBuffer.delete(1, 5);
		System.out.println(sBuffer);	//J Iqbal
	}
```
**Important Methods:**  

**`append(String str):StringBuffer`:**  
Appends the specified string at the end of this character sequence. Increases the length Returns a StringBuffer.

```java
	public static void main(String[] args) {
		StringBuffer sBuffer= new StringBuffer("Jahid");
		
		System.out.println(sBuffer);	//Jahid
		sBuffer.append(" Iqbal");
		System.out.println(sBuffer);	//Jahid Iqbal
	}
```

**`delete(int startIndex, int endIndex):StringBuffer`:**  
Removes the character sequence starting from startIndex and ends in endIndex. startIndex is inclusive and endIndex is exclusive. If startIndex is equal to endIndex then no changes occurred.
```java
	public static void main(String[] args) {
		StringBuffer sBuffer= new StringBuffer("Jahid Iqbal");
		
		System.out.println(sBuffer);	//Jahid
		sBuffer.delete(1, 5);
		System.out.println(sBuffer);	//J Iqbal
	}
```

**`setLength(int newLength):void`:**  
The character sequence is changed to newLength as specified. If newLength is greater than the current length then null character assign to rest index.
```java
	public static void main(String[] args) {
		StringBuffer sBuffer= new StringBuffer("Jahid Iqbal");
		
		System.out.println(sBuffer);	//Jahid
		sBuffer.setLength(15);          //newLength>currentLength
		System.out.println(sBuffer);	//Jahid Iqbal####
		sBuffer.setLength(5);           //newLength<currentLength
		System.out.println(sBuffer);	//Jahid
    }
```
**`equal(String str):String`:**  
Comparing over the reference of the objects.
```java
	public static void main(String[] args) {
		
		StringBuffer sb1= new StringBuffer("Jahid");
		StringBuffer sb2=sb1;
		
		StringBuffer sb3= new StringBuffer("Iqbal");
		
		System.out.println(sb1.equals(sb2));	//true
		System.out.println(sb1.equals(sb3));	//false
	}
```
**`replace(int startIndex, int endIndex, String str):StringBuffer`:**  
Replacing the string starting from `startIndex` and ends in `endIndex` (exclusive) by `str`
```java
	public static void main(String[] args) {

		StringBuffer sb1= new StringBuffer("Hello Dear");
		System.out.println(sb1.replace(6, 10, "Iqbal"));
	}
```