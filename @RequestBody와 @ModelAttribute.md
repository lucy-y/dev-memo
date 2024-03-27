# @RequestBody와 @ModelAttribute

```
클라이언트에서 보낸 데이터를 Java에서 사용할 수 있는 객체로 만들어 주는 Annotaion.
기능은 동일하나, 내부 수행 동작에서 차이가 있음.
```

## @RequestBody
```
요청 본문의 body에 JSON, XML, TEXT 데이터로 요청하여 HttpMessageConveter를 통해 파싱되어 객체(DTO)에 맞는 타입으로 변환돼 바인딩
```


## @ModelAttribute
```
HTTP 파라미터 데이터를 특정 JAVA 객체(DTO)에 바인딩을 하는 방식이기 때문에 바인딩하려는 DTO객체에 Setter메소드가 반드시 필요
```

## 요약
- 요청 파라미터를 조회하는 기능: @RequestParam , @ModelAttribute
- HTTP 메시지 바디를 직접 조회하는 기능: @RequestBody
