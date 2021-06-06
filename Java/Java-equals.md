# Java equals() 문자열 비교

> 📍 문자열(string) 비교 equals와 == 의 차이점

공통점
 * boolean type으로 반환한다.

차이점
  * 형태의 차이
    - equals () 는 **메소드** 
    - == 는 비교를 위한 **연산자** 
  * 주소값 비교와 내용 비교
    - equals 메소드는 비교하고자 하는 대상의 내용 자체를 비교
    - == 연산자는 비교하고자 하는 대상의 주소값을 비교
 
 
> 주소값이라는 것은 확실하게 집주소나 이메일주소처럼 확정적으로 정해져서 보여지는 것은 아니지만, 대상을 구별할 수 있게하는 값  

> 💡**Call By Value**는 기본적으로 대상에 주소값을 가지지 않는 것으로 값을 할당받는 형태로 사용 
> * primitive type (int, float, double, byte ..등)
> * 인자를 넘겨줄 때마다 메모리 공간을 할당해야 해서 메모리 더 잡아 먹는다

> 💡**Call By Reference** 대상을 선언했을 때, 주소값이 부여된다. 어떠한 객체를 불러왔을때 그 주소값을 불러온다. 
>  * Class, Object(객체)가 해당
>  * 포인터를 이용해 주소를 넘김

 
### 예시
~~~java
String a = "aaa";     //-> 할당된 주소값 200
String b = a;         //-> 할당된 주소값 200
String c = new String ("aaa");  //-> 할당된 주소값 300

System.out.println( a.equals(b)); //true
System.out.println( a==b); //true
System.out.println( a==c); //false
System.out.println( a.equals(c)); //true
~~~ 

>  변수 c가 다른 주소값을 할당받은 이유는 "aaa" 라는 문자열을 대입한 것이 아니라
new String ("aaa") 를 통해 새로운 문자열을 선언하였기 때문.