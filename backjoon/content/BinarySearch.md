# Java

```java

import java.util.Scanner;

public class Binary {
		static int[] a = {1,2,6,10,20,40,100};
	public static void main(String[] args) {
		
		Scanner sc = new Scanner(System.in);		
		int target = sc.nextInt();		
		Binary_search(target);
		
	}
	private static void Binary_search(int target) {
		// TODO Auto-generated method stub
		int mid;
		int left = 0;
		boolean check = false;
		int right = a.length-1;
		
		while(left <= right) {
			
			mid = (left+right)/2;
			
			if(target == a[mid]) {
				System.out.println("Found " + mid + " index");
				check = true;
				return;
			}
			
			if(target < a[mid]) {
				right = mid-1;
				
			}
			
			if(target > a[mid]) {
				left = mid+1;
			}
			
		}
		
		if(!check) {
			System.out.println("Not Found");
			return;
		}
		
	}
}


```
