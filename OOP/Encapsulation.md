# Encapsulation
>Encapsulation is a process of wrapping data and codes in a single unit.

**Advantages:**  
- Data Hiding
- Data access can be made as read-only or write-only by using getter and setter methods.
- Control over data. If you want to store positive values only then you can impose logic in setter methods.
- Easy to test.

**Example:**

```java
public class Students {
	String name;
	int id;
	String address;
	
	public void setName(String name) {
		this.name=name;
	}
	
	public void setId(int id) {
		this.id=id;
	}
	
	public void setAddress(String address) {
		this.address=address;
	}
	
	public String getName() {
		return name;
	}
	public int getId() {
		return id;
	}
	public String getAddress() {
		return address;
	}

}

public class Main {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		Students jahid= new Students();
		
		jahid.setName("Jahid");
		jahid.setId(101);
		jahid.setAddress("Gawair");
		
		System.out.println("Name: "+jahid.getName()+"\nID: "+jahid.getId()+"\nAddress: "+jahid.getAddress());
	}
}
/*
Name: Jahid
ID: 101
Address: Gawair
 */
```