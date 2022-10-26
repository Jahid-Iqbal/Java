# Data Types

Two categories of data types are available.

1. Primitive
 - Boolean (size is not defined. JVM defines the size)
 - Numeric
    - Character
        - char (2 byte)
    - Integral
        - Integer
            - byte (8 bit or 1 byte)
            - short (2 byte)
            - int (4 byte)
            - long (8 byte)
        - Floating
            - float (4 byte)
            - double (8 byte)


2. Non-Primitive
    - String
    - Array
    - Class
    - etc.

**Primitive Data types details with ranges:**  

Data Type | Default Size        | Default Value             | Range | Corresponding Wrapper Class| 
----------|--------------       |---------------            |-------|----------------------------|
boolean   | Not defined         | false                     |Only true and false| Boolean        |
char      | 2 bytes (16 bits)   | 0 (represents blank space)| 0 to 65535| Character|
byte      | 1 bytes (8 bits)    | 0                         |-2<sup>7</sup> to 2<sup>7</sup>-1 <br> -128 to 127|Byte|
short     | 2 bytes (16 bits)   |0                          |-2<sup>15</sup> to 2<sup> 15 </sup> -1 <br> -32768 to 32767|Short|
int       |4 bytes (64 bits)    | 0                         | -2<sup>31</sup> to 2 <sup> 31</sup>-1|Integer|
long      | 8 bytes (64 bits)   |0                          |-2<sup>63</sup> to 2<sup>63</sup>-1|Long|
float     | 4 bytes (32 bits)   | 0.0                       |-3.4e38 to 3.4e38|Float|
double    |8 bytes (64 bits)    |0.0                        |-1.7e308 to 1.7e308|Double|

**Difference Between Primitive and Non-Primitive Data Types:**  
- Primitive data types are pre-defined, size of the data is fixed but non-primitive data types are created by the programmer, size is not fixed. Such as,  

```java
//Primitive
char c='a';     //2 bytes
//Non-Primitive
String name="Jahid";    //10 bytes. 2 bytes for each character

//Primitive
int value=10;   //4 bytes
//Non-Primitive
int array[]={10,20,30,40,50};   //20 bytes. 4 bytes for each number.
```
- Primitive type has always a value but non-primitive types can be null.