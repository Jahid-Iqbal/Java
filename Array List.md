# Array List

Array List is similar to Array. Some deference are their. Such as, Array is static and Array List is dynamic means you don't need to declare the size of the array during declaring the array. In Array you can use `array_name.length()` method but in Array List you can use `arrayList_name.size()` method to identify the array size. On array list you can apply foreach loop or iterator.

**Declaration:**  
`ArrayList<data_type> array_name= new ArrayList<data_type>();`

`ArrayList<Integer> listArray= new ArrayList<Integer>();`

**Example:**
```java
package array;

import java.util.ArrayList;
public class ArrayListEx01 {
	public static void main(String[] args) {
		
		ArrayList<Integer>listArray= new ArrayList<Integer>();
		
		listArray.add(33);
		listArray.add(44);
		System.out.println(listArray);	//[33, 44]
		listArray.add(1, 667);
		System.out.println(listArray);	//[33, 667, 44]		
	}
}
```
**Example:**  Printing values using foreach loop
```java
package array;

import java.util.ArrayList;
public class ArrayList01 {
	public static void main(String[] args) {
		
		ArrayList<Integer>listArray= new ArrayList<Integer>();
		
		listArray.add(77);
		listArray.add(44);
		listArray.add(1, 667);
		
		for(int value: listArray) {
			System.out.print(value+" ");    //77 667 44
		}		
	}
}
```
**Example:**  Printing values using iterator
```java
package array;

import java.util.ArrayList;
import java.util.Iterator;
public class ArrayList01 {
	public static void main(String[] args) {
		
		ArrayList<Integer>listArray= new ArrayList<Integer>();
		
		listArray.add(77);
		listArray.add(44);
		listArray.add(1, 667);
		
		Iterator itr= listArray.iterator();
		
		while(itr.hasNext()) {
			System.out.print(itr.next()+" ");
		}		
	}
}
```

**Important Methods:**  

**`add()`:** add(element). The passed element will be appended at the end of the list and return true. The data type depends on the ArrayList type.

**`add(index, element)`:** Inserting the specific element at the specific position. shift all the of that index and onwards to the right.

**`addAll(Collection<?extends Integer>c):boolean`:**  
Appends all the specified elements at the end to this list.  
Returns true if the list is updated as a result of this call.

```java
		System.out.println(list1);				//[77, 33, 44, 77, 77]
		System.out.println(list2);				//[277, 233, 244, 277, 277]
		boolean isUpdated=list3.addAll(list1);	
		boolean isUpdated2=list3.addAll(list2);	
		System.out.println(list3);				//[77, 33, 44, 77, 77, 277, 233, 244, 277, 277]
		System.out.println(isUpdated);			//true
		System.out.println(isUpdated2);			//true
```

**`size()`:**  Returns the number of elements in the list.

**`remove(index):integer`:**  
Remove the element of the specified index and return the value of that index. Such as, `int r=listArray.remove(0);`

**`removeAll(Collection<?> c): boolean`:**  
Remove all the elements of the specified array list. Such as,

```java
System.out.println(listArray);	//[77, 667, 44]
boolean r= listArray.removeAll(listArray);
System.out.println(listArray);	//[]
System.out.println(r); 			//true
```
**`clear():void`:**  
Removes all the elements of specified array list.
```java
System.out.println(listArray);	//[77, 667, 44]		
listArray.clear();
System.out.println(listArray);	//[]
```
**`isEmpty():boolean`:**  
Check whether the array list is empty or not. Returns true if the array list is empty, false otherwise.
```java
System.out.println(listArray);	//[77, 667, 44]	
boolean isEmpty=listArray.isEmpty();
System.out.println(isEmpty);	//false
listArray.clear();
boolean ie=listArray.isEmpty();
System.out.println(ie);	//true
```

**`contains(Object o):boolean`:**  

Return true if the list contains the specified element.
```java
		System.out.println(listArray);	//[77, 667, 44]	
		boolean value=listArray.contains(77);
		System.out.println(value); 		//true
```
**`indexOf(Object o):int`:**  
Returns the index of the first occurrence of the specified element. Returns -1 if the element is not found.  
In below example, element 77 is available at index 0,3,4 but `indexOf()` method returned 0 as the first occurrence at the list.

```java
		System.out.println(listArray);	//[77, 667, 44, 77, 77]
		int index=listArray.indexOf(77);
		System.out.println(index); 		//0
        int invalidIndex=listArray.indexOf(10000);
		System.out.println(invalidIndex); 		//-1
```
**`lastIndexOf(Object o):int`:**  
Returns the index of the last occurrence of the specified element. Returns -1 if the element is not found.  
In below example, element 77 is available at index 0,3,4 but `lastIndexOf()` method returned 4 as the last occurrence at the list.
```java
		System.out.println(listArray);	//[77, 667, 44, 77, 77]
		int index=listArray.lastIndexOf(77);
		System.out.println(index); 		//4
        int invalidIndex=listArray.lastIndexOf(10000);
		System.out.println(invalidIndex); 		//-1
```
**`set(int index, Integer element): Integer`:**  
Replaces the element at the specified position in the list with specified element.  
Returns the element previously at the specified position.  
In below code snippet, 667 is replaced by 33 using set() method and return the replaced value 667.
```java
		System.out.println(listArray);			//[77, 667, 44, 77, 77]
		int replacedElement=listArray.set(1, 33);
		System.out.println(listArray);			//[77, 33, 44, 77, 77]
		System.out.println(replacedElement);	//667
```

**`get(int index):Integer`:**  
Returns the element at the specified position in this list.
```java
        System.out.println(listArray);			//[77, 667, 44, 77, 77]
		int element=listArray.get(2);
		System.out.println(element);			//44
```
**Array list sorting:**

```java
package array;

import java.util.ArrayList;
import java.util.Collections;
public class ArrayList01 {
	public static void main(String[] args) {
		
		ArrayList<Integer>list1= new ArrayList<Integer>();

		list1.add(77);
		list1.add(44);
		list1.add(1, 33);
		list1.add(2);
		list1.add(-55);
		//Ascending order
		System.out.println(list1);		//[77, 33, 44, 2, -55]
		Collections.sort(list1);
		System.out.println(list1);		//[-55, 2, 33, 44, 77]
		//Descending order
		Collections.sort(list1,Collections.reverseOrder());
		System.out.println(list1);		//[77, 44, 33, 2, -55]
	}
}
```