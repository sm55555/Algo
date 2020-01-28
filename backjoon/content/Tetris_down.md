# Java

```java

import java.util.Scanner;

public class down {
		static int n;
		static int m;
		static int[][] map;
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		n = sc.nextInt();
		m = sc.nextInt();
		
		map = new int[n][m];
		
		for (int i = 0; i < n; i++) {
			for (int j = 0; j < m; j++) {
				map[i][j] = sc.nextInt();				
			}
		}
		
		print();		
		down();
		print();

	}
	
	private static void down() {
		// TODO Auto-generated method stub
		for (int i = 0; i < m; i++) {
			for (int j = n-2; j >=0; j--) {
				for (int j2 = n-1; j2 > j; j2--) {
					if(map[j][i] == 1 && map[j2][i] == 0) {
						map[j][i] = 0;
						map[j2][i] = 1;
						break;
					}
				}
			}
		}
	}

	private static void print() {
		// TODO Auto-generated method stub
		for (int i = 0; i < n; i++) {
			for (int j = 0; j < m; j++) {
				System.out.print(map[i][j] + " ");
			}
			
			System.out.println();
		}
		
		System.out.println("---------");
	}
	
}


```
