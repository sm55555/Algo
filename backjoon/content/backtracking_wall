# Java

```java

import java.util.Scanner;

public class backtracking_wall {
		static int[] a;
		static int n;
		static int k;
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		
		n = sc.nextInt();
		k = sc.nextInt();
		
		a = new int[n];
		
		go(0,0);
	}
	private static void go(int index, int zz) {
		// TODO Auto-generated method stub
		if(index ==k) {
			for (int i = 0; i < n; i++) {
				System.out.print(a[i] + " ");
			}
			System.out.println();
			
			return;
		}
		
		for (int i = zz; i < n; i++) {
			if(a[i] ==0) {
				a[i] =1;
				go(index+1,i);
				a[i] =0;
			}
		}
	}
}


```
