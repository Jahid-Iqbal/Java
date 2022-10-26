# String Buffer

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