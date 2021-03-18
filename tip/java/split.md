# split

<img src="https://user-images.githubusercontent.com/38831314/111597613-b0fb1a80-8811-11eb-97c4-95811eacceb7.png">

```java

String 문자열 = "가:나:다:가나다";
String[] 나눈배열 = 문자열.split(":");


//나눈배열 : {"가", "나", "다", "가나다"}
System.out.println(나눈배열[0]);
//결과 : 가
System.out.println(나눈배열[나눈배열.length-1]);
//결과 : 가나다

```

#### 정상적으로 결과가 나온다.

<img src="https://user-images.githubusercontent.com/38831314/111597914-0505ff00-8812-11eb-9f9b-f5fe1a6b4036.png">

```java

String 문자열 = "가.나.다.가나다";
String[] 나눈배열 = 문자열.split(".");
		
System.out.println(나눈배열[0]);
System.out.println(나눈배열[나눈배열.length-1]);

```

#### ArrayIndexOutBounds 에러가 뜬다.


이건 split의 인자로 들어가는 String 토큰이 regex 정규식이기 때문이다. 
정규식에서 .은 무작위의 한 글자를 의미한다. 그러면 모든 문자가 토큰이 되기 때문에 배열에 남는 게 없게 되는 것이다.

따라서 이스케이프 문자를 앞에 붙여 줘야 한다. 그런데 String 안에 이스케이프 문자인 \를 써 주려면 \\라고 써 줘야 한다. 
따라서 \\라고 쓰는 것이다. 그래서 \\.이라고 쓰면 정규식 쪽에서는 \.라고 인식을 하고 실제 .을 찾게 되는 것이다.

아무튼 split를 쓸 때 뭔가 작동을 안 하면 \\을 붙여 보라.
