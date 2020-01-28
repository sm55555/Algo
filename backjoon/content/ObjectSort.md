# Java

```java

import java.util.ArrayList;
import java.util.Collections;

public class Collection_Test {
		static class fish implements Comparable<fish>{
			int x;
			int y;
			int z;
			
			fish(int x, int y, int z){
				this.x = x;
				this.y = y;
				this.z = z;				
			}

			@Override
			public int compareTo(fish o) {
				// TODO Auto-generated method stub
				if(this.z < o.z) {
					return -1;
				}else if(this.z > o.z) {
					return 1;
				}else if(this.x < o.x) {
					return -1;
				}else if(this.x > o.x) {
					return 1;
				}else if(this.y < o.y) {
					return -1;
				}else if(this.y > o.y) {
					return 1;
				}else {
					return 0;
				}
			}
			
			@Override
			public int compareTo(fish o) {
				// TODO Auto-generated method stub
				if(this.z != o.z) {
					return this.z-o.z;
				}else if(this.x != o.x) {
					return this.x-o.x;
				}else if(this.y != o.y) {
					return this.y-o.y;
				}else {
					return 0;
				}
			}

		}
		
	public static void main(String[] args) {
		ArrayList<fish> q = new ArrayList();
		q.add(new fish(5,5,10));
		q.add(new fish(5,4,100));
		q.add(new fish(2,6,5));
		q.add(new fish(2,6,4));
		q.add(new fish(10,0,2));
		q.add(new fish(5,5,2));
		q.add(new fish(5,2,1));
		
		Collections.sort(q);
				
		for(fish f : q) {
			System.out.println(f.x + " " + f.y + " " + f.z);
		}
		
	}
}


```
