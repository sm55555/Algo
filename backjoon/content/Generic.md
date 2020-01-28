# Java

```java


public class Generic<T> {
	static class A{
		int id;
	
		A(int id){
			this.id = id;
		}
	}
	
	static void runValue() {
		String a = "Ccccc";
		String b = a;
		b = "33333";
		System.out.println("runValue " + a);
	}
	
	static void runReference() {
		A a = new A(1);
		A b = a;
		b.id =2;
		System.out.println("runReference " + a.id);
	}
	
	public static void main(String[] args) {
		runValue();
		runReference();
	}
}


```
