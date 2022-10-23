# Bitwise Operator

Bitwise operator compares on binary values.

Operators:
```
&  Bitwise AND
|  Bitwise OR
^  Bitwise XOR
>> Bitwise shift right
<< Bitwise shift left
`  Bitwise NOT
```
**Bitwise AND & Bitwise OR:** Comparing two values with bitwise operators.

```java
package com.basics;

public class condition {
	public static void main(String[] args) {
		
		int value1=5;
		int value2=10;
		
		int checkedAnd= value1&value2;
		System.out.println(checkedAnd); //0
		
		int checkedOr= value1|value2;
		System.out.println(checkedOr);  //15
	}
}
```
Here, value1 and value2 need to convert to binary values.  

value1:  
Decimal: 5 Binary:  0101  
value2:  
Decimal: 10 Binary: 1010  

checkedAnd: 0000 decimal: 0  
checkedOr:  1111 decimal: 15

converting the binary result into decimal value.

**Bitwise shift right & Bitwise shift left:**  
Shifting right means dividing the value by 2 and 
shifting left means multiplying the value by 2.

```java
package com.basics;

public class condition {
	public static void main(String[] args) {
		
		int value1=12;
		
		int rightShift = value1>>2;		//3
		System.out.println(rightShift);
		
		int leftShift= value1<<2;		//48
		System.out.println(leftShift);
	}
}
```
Here, in right shift below operations happened,  
```
value1= value1/2;   //6  
value1= value1/2;   //3  
```
in right shift below operations happened,  
```
value1= value1*2;   //24  
value1= value1*2;   //48 
```