# Switch 
Four keywords need to be introduced here.  
1. switch
2. case
3. break
4. default

```java
switch(expression){
    case exp1:
        //code to be executed
        break;
    case exp2:
        //code to be executed
        break;
    default:
        //code to be executed
}
```
Here, entering into the conditional statement with an expression and each time check the cases. When any case implies then execute that code block. `break` will move the program execution outside the `switch` statement. If none of the cases will be executed then `default` will be executed.

**Example:**
```java
package com.basics;
import java.util.*;
public class SwitchCase {
	public static void main(String[] args) {
		int a=1;
		switch(a) {
		case 1: System.out.println(a);
		break;
		case 2:System.out.println(a);
		break;
		case 3:System.out.println(a);
		default:
			System.out.println("Not valid");
		}	
	}
}
```
Here, for input `1` `case 1` would be executed and move outside of the `switch` block by executing the `break` statement. If the value of a doesn't match any cases then execute the default case. If input would be `5` then `default` would be executed as no case implied.