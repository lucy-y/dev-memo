# scheduler와 async

## scheduler
- Spring Boot start dependency 의존
- Project Application Class의 @SpringBootApplication의 위나 아래에 @EnableScheduling 추가
~~~
@EnableScheduling
@SpringBootApplication
public class Application {
~~~

- scheduler를 사용할 Class에 @Component, Method에 @Scheduled 추가
- @Scheduled를 붙이는 메소드는 void 타입으로 생성, 매개변수 없이 생성

## async
- 스케줄링 설정한 메소드를 비동기처리하기 위해 사용
- Project Application Class의 @SpringBootApplication의 위나 아래에 @EnableAsync 추가
~~~
@EnableAsync
@SpringBootApplication
public class Application {
~~~
- 필요로 하는 메소드 위에 @Async 어노테이션 사용하면 된다.

## config
- 작성필요
