# Java

n X n-1 X n-2.....1

```java

import java.util.Scanner;

public class combi {
		static int[] a;
		static boolean[] c;
		static int n;
		static int count;
	public static void main(String[] args) {
		
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();		
		a = new int[n];
		c = new boolean[n];
		
		go(0);
		
		System.out.println(count);
	}
	private static void go(int index) {
		// TODO Auto-generated method stub
		if(index == n) {
			count++;
			for (int i = 0; i < a.length; i++) {
				System.out.print(a[i] + " ");
			}
			System.out.println();
			return;
		}
		
		for (int i = 0; i < a.length; i++) {
			
			if(c[i]) {
				continue;
			}
			
			c[i] = true;
			a[index] = i;
			go(index+1);
			c[i] = false;
		}
		
	}
	
	
}


```

n X n X n....... for n 

```java

import java.util.Scanner;

public class combi {
		static int[] a;
		static int n;
		static int count;
	public static void main(String[] args) {
		
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();		
		a = new int[n];
		
		go(0);
		
		System.out.println(count);
	}
	private static void go(int index) {
		// TODO Auto-generated method stub
		if(index == n) {
			count++;
			for (int i = 0; i < a.length; i++) {
				System.out.print(a[i] + " ");
			}
			System.out.println();
			
			return;
		}
		
		for (int i = 0; i < a.length; i++) {			
			a[index] = i;
			go(index+1);
		}
		
	}
	
	
}


```


