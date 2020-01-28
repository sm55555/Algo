# Java (one-dimensional array)

* count is nCk

```java

import java.util.Scanner;

public class backtracking_wall {
		static int[] a;
		static int n;
		static int k;
		static int cnt =0;
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		
		n = sc.nextInt();
		k = sc.nextInt();
		
		a = new int[n];
		
		go(0,0);
		System.out.println("cnt is " + cnt);
	}
	private static void go(int index, int zz) {
		// TODO Auto-generated method stub
		if(index ==k) {
			cnt++;
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

# Java (tow-dimensional array)

```java

import java.util.Scanner;

public class backtracking_wall {
		static int[][] a;
		static int[] temp_a;
		static int n;
		static int m;
		static int k;
		static int cnt =0;
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);		
		n = sc.nextInt();
		m = sc.nextInt();
		k = sc.nextInt();		
		a = new int[n][m];
		temp_a = new int[n*m];
		
		go(0,0);
		
		System.out.println("cnt is " + cnt);
		
	}
	private static void go(int index, int zz) {
		// TODO Auto-generated method stub		
		if(index ==k) {
			cnt++;
			int temp_index =0;
			for (int i = 0; i < n; i++) {
				for (int j = 0; j < m; j++) {
					a[i][j] = temp_a[temp_index++];
					
					System.out.print(a[i][j] + " ");
				}
				System.out.println();
			}
			
			System.out.println("--------");
			
			
			
			return;
		}
		
		for (int i = zz; i < n*m; i++) {
			
			if(temp_a[i] ==0) {
				temp_a[i] = 1;
				go(index+1, i);
				temp_a[i] = 0;
			}
			
		}
	}
	
} 


```
