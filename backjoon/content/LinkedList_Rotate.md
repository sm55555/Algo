# Java

only using LinkedList

```java

import java.util.LinkedList;
import java.util.Scanner;

public class LinkedList_Test {
	
	public static void main(String[] args) {
		
		LinkedList<Integer> q = new LinkedList();
		
		for (int i = 1; i <= 9; i++) {
			q.add(i);
		}
	
		Scanner sc = new Scanner(System.in);
		
		int dir = sc.nextInt();
		int num = sc.nextInt();
		
		num %= 9;
		if(dir ==0) {
			// go left
			for (int i = 0; i < num; i++) {
			 	int temp = q.removeFirst();
			 	q.addLast(temp);
			}
			
		}else {
			// go right
			for (int i = 0; i < num; i++) {
				int temp = q.removeLast();
			 	q.addFirst(temp);
			}
			
		}
		
		for (int i = 0; i < 9; i++) {
			System.out.print(q.get(i) + " ");
		}
	}
}


```
