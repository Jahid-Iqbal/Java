# String

>String is nothing but a sequence of characters.

```java
package string;

public class StringDemo01 {
	public static void main(String[] args) {
		String s1="Hello world!";
		String s2= new String("New String");
		
		System.out.println(s1);     //Hello world!
		System.out.println(s2);     //New String
	}
}
```

**Important Methods:**  

**`equal(Object o):boolean`:**  
Compares this string with specified object or string.  
Returns true if the argument is not null and the content of both objects are exactly same.
```java
	public static void main(String[] args) {
		String s1="New String";
		String s2= new String("New String");
		
		if(s1.equals(s2))
			System.out.println("Equal");
		else
			System.out.println("Not Equal");
	}
    //Equal
```
**`equalIgnoreCase(Object o):boolean`:**  
Compares this string with specified object or string ignoring the case.  
Returns true if the argument is not null and the content of both objects are exactly same.
```java
	public static void main(String[] args) {
		String s1="New String";
		String s2= new String("new String");
		
		if(s1.equals(s2))						//Not Equal
			System.out.println("Equal");
		else
			System.out.println("Not Equal");
	
		if(s1.equalsIgnoreCase(s2))				//Equal
			System.out.println("Equal");
		else
			System.out.println("Not Equal");
	}
```

**`contains(CharSequence s):boolean`:**  
Returns true if the String contains the specified object or string.
```java
	public static void main(String[] args) {
		String s1="new String";
		String s2= new String("New String");
	
		System.out.println(s1.contains("tri"));		//true
		System.out.println(s1.contains(s2));		//false
	}
```
**`isEmpty():boolean`:**  
Check whether the string empty or not. Calling the `length()` method implicitly. If `length()` method returns `0` then `isEmpty()` method returns `true`.  
Returns true if the String is empty, false otherwise.

```java
	public static void main(String[] args) {
		String s1="";
		String s2= new String("New String");
	
		System.out.println(s1.isEmpty());		//true
		System.out.println(s2.isEmpty());		//false
	}
```
**`concat(String s):String`:**  
Concatenates the specified string at the end of the string. If the arguments string length is 0 then return this string.
```java
	public static void main(String[] args) {
		String firstName="Abdullah Bin";
		String lastName= new String(" Omar");
	
		System.out.println(firstName.concat(lastName));     //Abdullah Bin Omar
	}
```
**`toUpperCase():String`:**  
Converts each character of the string to upper case letter and return the string.
```java
	public static void main(String[] args) {
		String firstName="Abdullah";
	
		System.out.println(firstName.toUpperCase());	//ABDULLAH
	}
```
**`toLowerCase():String`:**  
Converts each character of the string to lower case letter and return the string.

```java
	public static void main(String[] args) {
		String firstName="Abdullah";
	
		System.out.println(firstName.toLowerCase());	//abdullah
	}
```

**`startsWith(String prefix):boolean`:**  
Check whether the string starts with the specified prefix or not. If yes then return true.

```java
	public static void main(String[] args) {
		String firstName="Abdullah";
	
		System.out.println(firstName.startsWith("Ab"));	//true
		System.out.println(firstName.startsWith("bd"));	//false
	}
```

**`endsWith(String suffix):boolean`:**  
Check whether the string ends with the specified suffix or not. If yes then return true.

```java
    public static void main(String[] args) {
		String firstName="Abdullah";
	
		System.out.println(firstName.endsWith("ah"));	//true
		System.out.println(firstName.endsWith("bd"));	//false
	}
```

**`charAt(int index):char`:**  
Return the character at the specified position.
```java
	public static void main(String[] args) {
		String firstName="Abdullah";
	
		System.out.println(firstName.charAt(0));	//A
		System.out.println(firstName.charAt(5));	//l
	}
```
**`codePointAt(int index):int`:**  
Returns the unicode code point of the character at the specified position ranges from 0 to length()-1.

```java
	public static void main(String[] args) {
		String firstName="Abdullah";
	
		System.out.println(firstName.codePointAt(0));	//65
		System.out.println(firstName.codePointAt(5));	//108
	}
```
**`indexOf(char c):int`:**  
Returns the index of the first occurrence of the specified character. Returns -1 if the element is not found.
```java
	public static void main(String[] args) {
		String firstName="Abdullah";
	
		System.out.println(firstName.indexOf("b"));	//1
		System.out.println(firstName.indexOf("a"));	//6
	}
```
**`lastIndexOf(char c):int`:**  
Returns the index of the last occurrence of the specified element. Returns -1 if the element is not found. 
```java
	public static void main(String[] args) {
		String firstName="Abdullah Bin Omar";
	
		System.out.println(firstName.lastIndexOf("a"));	//15
		System.out.println(firstName.lastIndexOf("A"));	//0
	}
```

**`trim():String`:**  
Removes all the spaces from forward and backward side of a sentence and returns the string.  Such as, In below example 2 spaces are available in string "  Abdullah Bin Omar". trim() method removes those.
```java
	public static void main(String[] args) {
		String firstName="  Abdullah Bin Omar";
		String blankSpace="    ";
	
		System.out.println(firstName.trim());	//Abdullah Bin Omar
		System.out.println(blankSpace.trim());	//	
	}
```
**`replace(char oldChar, char newChar):String`:**  
Replace the oldChar by newChar and returns the new string. If oldChar doesn't find in their string then returns this string.

```java
	public static void main(String[] args) {
		String firstName="Abdullah Bin Omar";
		
		System.out.println(firstName.replace("O", "U"));	//Abdullah Bin Umar
        System.out.println(firstName.replace("Bin", "Ibn"));	//Abdullah Ibn Omar
	}
```
**`split(String regex): String[]`:**  
Splits the string depending on the specified regular expression and returns an Array of string.
```java
	public static void main(String[] args) {
		String firstName="Abdullah Bin Omar";
		
		String[] s=firstName.split(" ");
		
		for(String x: s) {
			System.out.println(x);
		}
        //Abdullah
        //Bin
        //Omar
	}
```
