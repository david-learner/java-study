# POJO란 무엇인가

## POJO의 등장

EJB라는 기업용 애플리케이션 개발을 돕는 것이 있었다.
기업용 애플리케이션을 개발할 때 애플리케이션의 핵심 로직을 구현하는 것이외에도 고려해야할 사항이 너무 많은 것이 문제다.

EJB의 목적은 기업용 애플리케이션 개발시 고려해야할 사항을 줄이는 것이였고 실제로 그렇게 되었다. 하지만 또 다른 복잡한 문제들이 생겼고 사람들은 지쳐갔다.
이 때 등장한 것이 POJO다.

POJO 프로그래밍은 객체지향 원리에 따라 만들어진 자바 언어의 기본에 충실하게 비즈니스 로직을 구현하는 것을 말한다.

그리고 단순히 EJB 이전의 프로그래밍으로 돌아가는 것이 아니라 EJB에서 좋았던 것들을 그대로 가져와서 더 나은 방식으로 개발할 수 있게 돕는 POJO기반 프레임워크가 등장하기 시작했다.

POJO 기반 프레임워크로는 Hibernate과 Spring이 있다.

## POJO의 정의

POJO는 Plain Old Java Object의 약자이며 평범하고 오래된 자바 객체라는 뜻이다.

자바 언어 명세에서 강제하는 것을 제외하고 어떠한 제약이 없는 자바 객체를 말한다.

따라서 상속이나 인터페이스의 구현을 강제할 수 없다.
애노테이션도 포함될 수 없다는데 왜 그런지 잘 모르겠다.

> 1. Extend prespecified classes, as in
>
>       ```public class Foo extends javax.servlet.http.HttpServlet { ...```
> 2. Implement prespecified interfaces, as in
>
>       `public class Bar implements javax.ejb.EntityBean { ...`
> 3. Contain prespecified annotations, as in
>
>       `@javax.persistence.Entity public class Baz { ...`
>
> wikipedia - POJO

## 결론
POJO를 이용한 POJO 프로그래밍은 객체지향의 장점을 살려 프로그래밍할 수 있는 것이다.

### 참고자료

* http://itewbm.tistory.com/entry/POJOPlain-Old-Java-Object
* http://bsnippet.tistory.com/17
* https://en.wikipedia.org/wiki/Plain_old_Java_object
* https://www.quora.com/What-is-the-difference-between-POJO-JavaBeans-VO