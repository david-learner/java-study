# 용어 정리

## 서버

* Web Server
* WAS (Web Applicatoin Server)
* Apache
  * Web Server의 한 종류
  * C언어로 개발됨
  * Httpd(Http Daedom)라고 불리기도 함
  * 로드밸런싱 가능함
* Apache Tomcat
  * WAS의 한 종류
  * Java로 개발됨
  * Tomcat 5.5부터는 Apache(Web Server)의 native 모듈을 이용하여 Apache와 비슷한 성능으로 정적(static) 파일을 처리할 수 있음
  * Servlet Container를 통해 Java로 작성된 Servlet들의 life cycle을 관리할 수 있음

## 기타

* JPA
  * Java Persistence API
  * 자바 진영에서 만든 ORM 표준
  * JPA의 구현체로는 Hibernate, TopLink, JDO가 있다
* Hibernate
  * Hibernate ORM의 줄임말
  * Java를 위한 Object/Realation Mapping Framework
* ORM
  * Object-Realation Mapping
  * OOP를 지원하는 시스템과 다른 시스템 사이에서 발생하는 타입 불일치를 해결하기 위해 데이터를 변환하는 프로그래밍 기술

* ORM, JPA, Hibernate ORM
  * 자바 진영에서 ORM 표준으로 지정한 것이 JPA
  * JPA에 기술된 spec에 따라 구현된 구현체가 Hibernate ORM(줄여서 Hibernate)

## 자바

* 클래스파일(.class)
* 바이트코드
* native
  * JNI(Java Native Interface)를 사용하는 native code로 작성된 메서드에 붙이는 접근제어자(modifier)
  * 오직 메서드에만 붙일 수 있다
  * C나 C++로 작성된 메서드는 native method 또는 foreign method 라고 부른다
  * native 키워드의 목적
    * 시스템의 성능 향샹
    * To achieve misson level / memory level communication
    * 자바가 아닌 언어로 작성된 기존 코드를 사용하기 위해서
* reference
  * 레퍼런스란 메모리에 저장된 객체의 위치를 가르키는 것이다
  * C나 C++에서 사용되는 pointer와 100% 동일하지 않다 (pointer vs reference에 대해 조사하기 [링크](https://stackoverflow.com/questions/57483/what-are-the-differences-between-a-pointer-variable-and-a-reference-variable-in))

* 참고
  * Tomcat : http://limmmee.tistory.com/4
  * Apache : https://askubuntu.com/questions/248404/is-there-any-difference-between-apache2-and-httpd
  * Tomcat VS Apache : https://stackoverflow.com/questions/38194756/usage-difference-between-apache-and-apache-tomcat
  * JPA : https://en.wikipedia.org/wiki/Java_Persistence_API
  * JPA : 책<자바 ORM 표준 JPA 프로그래밍>, 9p
  * ORM : https://en.wikipedia.org/wiki/Object-relational_mapping
  * native : https://www.geeksforgeeks.org/native-keyword-java/