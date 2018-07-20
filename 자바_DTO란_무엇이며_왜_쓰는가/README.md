# 자바 DTO란 무엇이며 왜 쓰는가

## DTO 정의

DTO는 Data Transfer Object(데이터 전송 객체)다.

서로 다른 계층간 데이터 전달이 필요할 경우 DTO를 사용한다.

예를 들어 Spring Web Application 개발한다면 아래와 같이 Web Layer에서 Service Layer로 데이터를 전달하려고 할 때 DTO를 사용할 수 있다.

![spring-web-app-architecture](images/spring-web-app-architecture.png)

## DTO와 Persistent Object

Persistent Object는 Database에서 가져온 데이터를 담고 있는 객체정도로 생각하자.

일반적으로 Persistent Object의 클래스 복잡도가 크게 높지 않다면 Persistent Object는 DTO의 역할을 포함해도 괜찮다.

하지만 복잡도가 증가한다면 데이터 전달에 초점을 맞춘 객체를 만들어야 하는데 그것이 DTO가 되는 것이다.

나는 아직까지 DTO를 별도로 분리할 만큼의 복잡도를 경험해보지 않았지만 위에서 언급한 Spring Web Application Architecture를 최대한 따르려는 노력과 일부러 DTO를 만들어보는 연습을 하고 있다.

## 결론

처음부터 복잡도가 높아질 것을 예상하여 DTO를 만들게 되면 초기 리팩토링하는 단계에서 귀찮아진다.
따라서 개발 초기에는 Persistent Object에 DTO 역할을 포함시키고 이후에 복잡도가 증가하면 DTO를 따로 분리해 내는 것이 개발 속도 저하를 막을 수 있다.

평소에 점점 복잡해지는 Persistent Object에서 DTO를 분리하는 연습을 해두면 좋다.

### 참고문서

* https://www.slipp.net/questions/22
* https://www.slipp.net/wiki/pages/viewpage.action?pageId=2031636
* https://www.slipp.net/questions/23
* https://www.petrikainulainen.net/software-development/design/understanding-spring-web-application-architecture-the-classic-way/