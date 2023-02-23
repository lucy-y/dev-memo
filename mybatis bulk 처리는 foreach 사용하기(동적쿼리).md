# mybatis bulk 처리는 foreach 사용하기(동적쿼리)
- INSERT, UPDATE, DELETE 는 foreach 사용해서 처리하기

## foreach 사용법
~~~
ex) list = [1,2,3,4,5,..]
<foreach item="item" index="index" collection="list" open="(" separator="," close=")">
// INSERT, UPDATE, DELETE 쿼리 필요한 포맷으로 기재
</foreach>
~~~

- collection : 전달받은 인자. List or Array 형태만 가능(mapper단 parametertype내 형 지정)
- item : 전달받은 인자 값을 alias 명으로 대체
- open : 구문이 시작될때 삽입할 문자열 (옵션)
- close : 구문이 종료될때 삽입할 문자열 (옵션)
- separator : 반복 되는 사이에 출력할 문자열
- index : 반복되는 구문 번호이다. 0부터 순차적으로 증가 (옵션)
