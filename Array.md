# Array

>Collections of values of the same type.

**Array Declaration:**  
data_type variable_name [array_size];  
int array[10];

Creating an Array:  
int number[]= new int[10];

Assigning Values:  
```
number[0]=100;
number[1]=200;
number[2]=300;
number[3]=400;
number[4]=500;
```

**Sum of array elements:**
```java
package array;

import java.util.*;

public class SumOfArrayElements {
	public static void main(String[] args) {
		int array[]= new int[5];
		int sumElements=0;
		
		Scanner scan= new Scanner(System.in);
		
		for(int i=0;i<array.length;i++) {
			array[i]=scan.nextInt();    //1 2 3 4 5
		}
		
		for(int i=0;i<array.length;i++) {
			sumElements+=array[i];
		}
		System.out.println(sumElements);    //15
	}
}
```
