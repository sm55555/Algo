# Java

```java

import java.util.PriorityQueue;
import java.util.Scanner;

public class MST {
		static class point implements Comparable<point>{
			int x;
			int y;
			int z;
			
			point(int x, int y, int z){
				this.x = x;
				this.y = y;
				this.z = z;
			}

			@Override
			public int compareTo(point o) {
				// TODO Auto-generated method stub
				if(this.z != o.z) {
					return this.z - o.z; 
				}else {
					return 0;
				}
				
			}
		}
		static int[] parent;
		static int v; 
		static int e;
		static PriorityQueue<point> q;
		static int result = 0;
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		// v is Point, e is Line 
		int v = sc.nextInt();
		int e = sc.nextInt();
		
		parent = new int[v+1];
		q = new PriorityQueue();
		
		for (int i = 1; i <=v; i++) {
			parent[i] = i;
		}
		
		
		// 간선 정렬
		for (int i = 0; i < e; i++) {
			int a = sc.nextInt();
			int b = sc.nextInt();
			int c = sc.nextInt();
			q.add(new point(a,b,c));			
		}
		
		for (int i = 0; i < e; i++) {
			point p = q.poll();
			int start = p.x;
			int end = p.y;
			
			
			if(find(start) == find(end)) {
				continue;
			}else {
				union(start, end);
				result += p.z;
			}

		}
		
		System.out.println(result);
		
	
	}
	
	private static int find(int a) {
		// TODO Auto-generated method stub
		if(a ==parent[a]) {
			return a;
		}else{
			return parent[a] = find(parent[a]);
		}
		
	}
	
	private static void union(int x, int y) {
		// TODO Auto-generated method stub
		x = find(x);
		y = find(y);
		
		if(x == y) {
			return;
		}else {
			parent[x] = y;
		}		
	}
}

```
