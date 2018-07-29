# Handlebars 버전 에러

## 에러 원인

Spring boot 2.0.3을 사용중에 `handlebars-spring-boot-starter` 버전 0.2.x를 사용하니깐 다음과 같은 로그를 뱉어냈다.

>org.springframework.beans.factory.UnsatisfiedDependencyException: Error creating bean with name 'handlebarsBeanPostProcessor' defined in class path resource

## 에러 해결 방법

handlebars 버전을 0.2.x에서 0.3.0으로 변경하기.

나는 의존성 관리를 위해 빌드도구 Maven을 사용하고 있으므로 다음과 같이 handlebars의 버전을 0.3.0으로 수정했다.

```xml
<dependency>
    <groupId>pl.allegro.tech.boot</groupId>
    <artifactId>
        handlebars-spring-boot-starter
    </artifactId>
    <version>0.3.0</version>
</dependency>
```