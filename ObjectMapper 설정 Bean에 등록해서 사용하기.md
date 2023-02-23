# ObjectMapper 설정 Bean에 등록해서 사용하기

~~~
@Configuration
public class ObjectMapperConfig {
  @Bean
	public ObjectMapper ObjectMapper() {
    ObjectMapper om = new ObjectMapper();
    ....
    //필요한 설정 적용
    ...
    return om;
  }
}
~~~
