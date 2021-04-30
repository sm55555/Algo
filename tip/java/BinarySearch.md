# Java

```java

import java.util.Scanner;

public class Binary {
		static int[] a = {1,2,4,5,7,10,20,40,50,70,90,100};
	public static void main(String[] args) {
		
		Scanner sc = new Scanner(System.in);		
		int target = sc.nextInt();		
		Binary_search(target);
		
	}
	private static void Binary_search(int target) {
		// TODO Auto-generated method stub
		int left = 0;
		int right = a.length-1;
		int mid;
		boolean check = false;
		
		while(left <= right) {
			
			mid = (left + right)/2;
			
			if(target == a[mid]) {
				check = true;
				System.out.println("find " + mid);
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
			System.out.println("No");
		}
		
	}

}


```
