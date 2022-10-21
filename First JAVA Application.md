# Printing Hello World

Creating a JAVA class under project and write down the code as follows

```js
package oct_21_2022;

public class HelloWorld {

	public static void main(String[] args) {
		System.out.print("Hello Word");	//Hello Word
	}
}
```
Escaping Sequence: A special character followed by '/' to escape some spaces.  
`/b` backspace  
`/t` tab  
`/n` new line  
`/r` carriage return  
`/"` double quote  
`/'` single quote  
`//` backslash  

```js
package oct_21_2022;

public class HelloWorld {

	public static void main(String[] args) {
		System.out.println("Abdullah \nDhaka");
		//Abdullah 
		//Dhaka
		System.out.println("\"Jaba programming\""); 	//"Jaba programming"
		System.out.println("1 \t2");		//1		2
	}
}
```