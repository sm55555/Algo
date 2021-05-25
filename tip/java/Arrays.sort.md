# Arrays sort 원소 길이로 정렬

```java

import java.io.*;
import java.util.*;

public class Main {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);

		int n = sc.nextInt();

		String[] a = new String[n];

		for (int i = 0; i < n; i++) {
			a[i] = sc.next();

		}

		Arrays.sort(a, new Comparator<String>() {

			@Override
			public int compare(String o1, String o2) {
				// TODO Auto-generated method stub

				if (o1.length() != o2.length()) {
					return o1.length() - o2.length();
				}

				return 0;
			}
		});

		for (String s : a) {
			System.out.println(s);
		}

	}
}

```
