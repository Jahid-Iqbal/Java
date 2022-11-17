# Constructors

* Having same name as class
* Constructor does not have any return type
* Constructor called implicitly when any instance/ objects are created.

**Purpose of Constructors:**  
Without Constructors the scenarios are:  

* To initialize an object.

```java
public class Employee{
    String name="Jahid";
    int empId=101;
}
public class Main{
    public static void main(String[] args){
        Employee jahid= new Employee();
        /*name: Jahid, empId:101*/
        Employee iqbal= new Employee();
        /*name: Jahid, empId:101*/
    }
}
```
Every time returning the same value.
```java
public class Employee{
    String name;
    int empId;
}
public class Main{
    public static void main(String[] args){
        Employee jahid= new Employee();
        jahid.name="Jahid";
        jahid.empId=101;
        Employee iqbal= new Employee();
        iqbal.name="Iqbal";
        iqbal.empId=102;
    }
}
```
For each person assigning new information but need to write a bunch of line of code. Constructor solved this problem.
```java
public class Employee{
    public Employee(String name, int empId){
        this.name= name;
        this.empId= empId;
    }
}
public class Main{
    public static void main(String[] args){
        Employee jahid= new Employee("jahid",101);
        Employee iqbal= new Employee("Iqbal",102);
    }
}
```
Each instance is calling the constructor separately and assigning new values.  

Different Types of Constructors:  
* Default Constructor
* No-Args Constructor
* Parameterized Constructor