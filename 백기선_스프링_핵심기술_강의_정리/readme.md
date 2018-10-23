# 백기선님의 스프링 핵심기술 인프런 강의 정리

## IoC 컨테이너 1부 : 스프링 IoC 컨테이너와 빈

* 스프링이란?

    소규모 애플리케이션 또는 기업용 **애플리케이션을 자바로 개발하는 데** 있어 유용하고 **편리한 기능을 제공하는 프레임워크**

* IoC란?

    Inversion of Control, 의존 관계 주입(Dependency Injection)이라고도 한다.

    의존 객체를 직접 생성하지 않고 주입받아 사용한다.

    생성자 주입의 경우 스프링이 없어도 개발자가 직접 주입할 수 있다.

> DI의 종류
> * Constructor Injection
> * Setter Injection
> * Interface-based Injection
> * Service Locator Injection

* BeanFactory

    IoC의 가장 핵심 클래스

* Bean

    Spring IoC 컨테이너가 관리하는 객체

  * 해당 객체가 Bean인지 아닌지 어떻게 알 수 있는가?

    IoC 컨테이너에 등록되었는가 아닌가에 따라 달라진다

  * 컨테이너로부터 의존성 주입을 받으려면 Bean이어야 한다

* Spring IoC 컨테이너에 등록된 Bean들은 기본적으로 Singleton Scope를 가지는 Bean으로 등록된다

* Scope  
  * Singleton : 하나만 생성되어 재사용한다
  * ProtoType : 매번 새로운 객체를 생성한다
  * Singleton의 이점
    * 하나만으로 재사용하기 때문에 메모리 절약
    * 이미 컨테이너에서 만들어진 객체이기 때문에 Runtime시 성능 최적화에 유리함

* 라이프 사이클 인터페이스
  * Spring IoC 컨테이너에 등록된 Bean에만 해당된다
  * Bean이 생성, 소멸될 때 다른 처리를 할 수 있다

* ApplicationContext
  * BeanFactory를 상속받는다
  * BeanFactory에 비해 다양한 기능을 가지고 있다

## IoC 컨테이너 2부 : Application Context 와 다양한 빈 설정

* SpringBoot의 장점

  dependency 관리

* Spring IoC 컨테이너는 **빈 설정 파일**이 있어야 한다

![beanConfig](images/beanConfig.jpg)

* Application.xml에 하나씩 빈을 등록하는 것은 고전적인 방식
* 빈의 스코프
  * protoType : 매번 새로운 객체를 생성
  * request : 요청당 새로운 객체를 생성
  * session : 세션당 새로운 객체를 생성
  * singleton : 하나의 객체로 재사용함

* xml 파일에서 일일이 빈을 등록하는 게 번거로워서 등장한 것이 " "component-scan"이다

* @Component 애노테이션이 붙은 클래스는 빈으로 등록된다
* @Component를 확장한 애노테이션 4가지
  * Controller
  * Repository
  * Service
  * Indexed

* 의존성 주입을 받을 때 사용되는 애노테이션
  * Autowired
  * Inject : 또 다른 의존성 주입이 필요함
  * Resource

위의 각 애노테이션의 차이점은 다음에서 확인
[링크1](https://www.linkedin.com/pulse/difference-between-inject-vs-autowire-resource-pankaj-kumar), [링크2](https://www.sourceallies.com/2011/08/spring-injection-with-resource-and-autowired/#more-2350)

* Java 파일을 이용한 빈 설정
  * @Configuration을 클래스에 붙여줘야 한다
  * @Configutation은 해당 클래스가 설정파일임을 알려준다

* Setter 주입 VS Constructor 주입
  * Setter 주입을 받게 되면 주입 받는 클래스 내부에서 애노테이션을 통한 주입을 받을 수 있다, 그러나 생성자 주입을 받는 객체는 생성자에서 넘어온 객체를 통해서만 주입받을 수 있다

* @SpringBootApplication 애노테이션은 ApplicationContext를 대신 생성해준다