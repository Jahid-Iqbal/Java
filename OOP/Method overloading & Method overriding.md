# Method Overloading
>A class has multiple methods having same name but different signature. May be different in parameter type or number of parameters etc.

**Example:**  
Let say you call a method `add(4,5)` and consider below 3 scenarios.  

Scenario-1: Matches the arguments  
`add(int a, int b);`  
a=4 and b=5. No discrepancy follows.

Scenario-2: Doesn't match but arguments can be promoted.  
`add(int a, long b);`  
a=4 and b=5; Though 5 is an int value but it can be promoted to long.

Scenario-3: Matches multiple methods/ Ambiguity  
`add(int a, long b);`  
`add(long a, int b);`  
a=4 and b=5. First method, 4 is int and 5 can be promoted to long. Second method, 4 can be promoted to long and 5 is int. So compiler will be confused that which add method should be called. That is an ambiguity problem.

# Method Overriding
>Methods having same name and same signatures as like the parent class is called method overriding.

The name and signatures are same as the parent class but the implementation can be different.

### Differences
|Method Overloading|Method Overriding|
|------------------|-----------------|
Same name|Same name|
Within the same class|In different classes|
Arguments are not same.|Same arguments.|
