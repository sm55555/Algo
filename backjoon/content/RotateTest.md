# Java

```java

import java.util.Scanner;


public class Rotate_Test {
		static int n;
		static int m;
		static int[][] map;
		static int[][] map_copy;
		static int start_x =0;
		static int start_y =0;
		static class point{
			int x;
			int y;
			point(int x, int y){
				this.x = x;
				this.y = y;
				
			}
		}
		static int[] dx = {-1,1,0,0};
		static int[] dy = {0,0,-1,1};
		static int[] cw = {3,1,2,0};
		static int[] ccw = {1,3,0,2};
		
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		
		n = sc.nextInt();
		m = sc.nextInt();
		map = new int[n][m];
		map_copy = new int[n][m];
		
		for (int i = 0; i < n; i++) {
			for (int j = 0; j < m; j++) {
				map[i][j] = sc.nextInt();
				map_copy[i][j] = map[i][j];
			}
		}
		
		rotate(0,0,cw);
		rotate(0,0,ccw);
		rotate(0,0,cw);
		rotate(0,0,ccw);
		rotate(0,0,cw);
		rotate(0,0,ccw);
		
		for (int i = 0; i < n; i++) {
			for (int j = 0; j < m; j++) {
				System.out.print(map[i][j] + " ");
			}
			System.out.println();
		}
		
		System.out.println("----------");
		
		
		
	}

	private static void rotate(int i, int j, int[] cw2) {
		// TODO Auto-generated method stub
		int x = i;
		int y = j;
		
		for (int k = 0; k < 4; k++) {
			while(true) {
				int nx = x + dx[cw2[k]];
				int ny = y + dy[cw2[k]];
				
				if(nx <0 || ny <0 || nx >=n || ny >=m) {
					break;
				}
				
				map[nx][ny] = map_copy[x][y];
				
				x = nx;
				y = ny;
			}
		}
		
		for (int k = 0; k < n; k++) {
			for (int k2 = 0; k2 < m; k2++) {
				map_copy[k][k2] = map[k][k2];
			}
		}
	}
	
}


```
