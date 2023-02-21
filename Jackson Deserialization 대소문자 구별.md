# Jackson Deserialization 대소문자 구별.md

Jackson으로 json 문자열을 Java 객체로 Deserialization 할 때 property 이름 대소문자를 구별하기 때문에

Object 객체 생성할때 옵션을 주거나, class로 readValue를 할 경우에 @JsonProperty("name")을 이용해서 처리

~~~
new ObjectMapper().configure(MapperFeature.ACCEPT_CASE_INSENSITIVE_PROPERTIES, true);
~~~
