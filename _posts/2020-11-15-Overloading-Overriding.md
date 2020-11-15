---
title: "오버로딩과 오버라이딩 개념"
date: 2020-11-15
categories: Overloading Overriding
---

## Overloading 
하나의 클래스에 같은 이름의 메서드를 여러 개 정의하는 것
 - 이름이 같아야 한다. 
 - 매개변수가 같아야 한다. 
 - 리턴 타입이 같아야 한다.

사전적 의미 : 과부하


``` 
    // test에 매개변수로 int형 2개 호출
    void test(int a, int b){
        System.out.println("매개변수 "+ a + "와 " + b);
    }
   
    // test에 매개변수 double형 1개 호출
    void test(double d){
        System.out.println("매개변수 " + d);
    }
```
<br>

## Overriding
상클래스로부터 상속받은 메서드의 내용을 상속받는 클래스에 맞게 변경(재정의)하는 것
 - 이름이 같아야 한다.
 - 매개변수가 달라야 한다(매개변수의 수, 배치(순서) 등)

사전적 의미 : 재정의
```
class Dog{
    public void bark(){
        System.out.println("짖다");
    }
}
class Hound extends Dog{
    public void sniff(){
        System.out.println("냄새를 맡다");
    }

    public void bark(){
        System.out.println("짖다");
    }
}

public class OverridingTest{
    public static void main(String [] args){
        Dog dog = new Hound();
        dog.bark();
    }
}
```
---
참조
https://hyeonstorage.tistory.com/185
https://www.programcreek.com/2009/02/overriding-and-overloading-in-java-with-examples/

