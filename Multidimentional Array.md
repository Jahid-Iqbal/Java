# 2D Array

Declaration:  

`type [][] array_name= new type[row][column];`

`int [][] numbers= new int[2][3];`

Total number of stored elements in an Array= row*column.

**Example:**  
```java
package array;

import java.util.*;
public class Array_2D {
	public static void main(String[] args) {
		Scanner scan = new Scanner(System.in);
		
		int matrix[][]=new int[2][3];
		
		for(int i=0;i<matrix.length;i++) {
			for(int j=0;j<matrix[i].length;j++) {
				matrix[i][j]=scan.nextInt();
			}
		}
		
		for(int i=0;i<matrix.length;i++) {
			for(int j=0;j<matrix[i].length;j++) {
				System.out.print(matrix[i][j]+" ");
			}
			System.out.println(); 
		}	
	}
}
```