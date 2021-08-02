### Java 

```java
import java.util.*;

public class Main {

	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);


		char[] c = sc.next().toCharArray();
		Arrays.sort(c);
		String temp = new String(c);

		System.out.println(temp);
	}

}
```

#### 결과

![image](https://user-images.githubusercontent.com/38831314/127588327-d4cd5fc3-592f-4685-9bc3-b25a83c94ca3.png)
