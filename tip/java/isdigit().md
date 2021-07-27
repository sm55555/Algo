### isdigit 숫자 판별 함수


```java

import java.io.BufferedReader;
import java.io.InputStreamReader;
import java.util.LinkedList;
import java.util.StringTokenizer;

public class Test {

	public static void main(String[] args) throws Exception {

		System.out.println(isdigit("dddd"));
		System.out.println(isdigit("dd-&*^dd"));
		System.out.println(isdigit("123"));

	}

	private static boolean isdigit(String temp) {
		// TODO Auto-generated method stub

		try {
			Integer.parseInt(temp);
			return true;
		} catch (Exception e) {
			// TODO: handle exception
			return false;
		}

	}
}

```

### 결과

```java

false
false
true

```
