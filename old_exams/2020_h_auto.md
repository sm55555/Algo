# Java

```java

class Solution {
        static int max = -1;
        static int[] a;
    public int solution(int k, int[] rates) {
        int answer = 0;
        boolean check = false;
        int dollar =0;
        int len = rates.length;
        max = k;
        a = new int[rates.length];

        for(int i=0; i< a.length; i++){
            a[i] = rates[i];
        }
        // rates.length
        //     System.out.println("살때 " + rates[i] + " : " + k);
        go(k,0,dollar,len,check);
        System.out.println(max + "!!!!");

        answer = max;

        return answer;
    }

    public void go(int k, int idx, int dollar, int len, boolean check){

        if(i

```
