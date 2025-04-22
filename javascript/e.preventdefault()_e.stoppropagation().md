# e.preventdefault()와 e.stoppropagation() 차이

- 이벤트 처리에서 자주 쓰이는 메서드

## e.preventDefault()
- 기본 동작을 막는 것
~~~
document.querySelector("a").addEventListener("click", function(e) {
  e.preventDefault(); // 링크 클릭 시 이동을 막음
  console.log("링크 클릭했지만 이동 안 함");
});
~~~

## e.stoppropagation()
- 이벤트 전파(버블링/캡처링)를 막는 것
- 현재 이벤트가 상위(혹은 하위) DOM으로 넘어가지 않도록 차단
~~~
document.querySelector("button").addEventListener("click", function(e) {
  e.stopPropagation(); // 이벤트가 부모로 전달되지 않음
  console.log("버튼만 클릭됨, 상위 div까지 안 감");
});
~~~

## 핵심 차이점 정리

| 구분 | `e.preventDefault()` | `e.stopPropagation()` |
|------|----------------------|------------------------|
| 목적 | 기본 동작 차단 | 이벤트 전파 차단 |
| 영향 | 브라우저 동작 제어 | DOM 이벤트 흐름 제어 |
| 예시 | a 클릭해도 링크 이동 안 함 | 자식 클릭해도 부모 이벤트 발생 안 함 |


## 버블링 외에도 다른 차이점/주의할 점

- `e.preventDefault()`는 **이벤트 전파와는 무관**하며, 오직 **브라우저의 기본 동작 차단**에만 관여한다.
- `e.stopPropagation()`은 **기본 동작엔 영향을 주지 않으며**, 단지 **이벤트가 상위/하위 요소로 전파되지 않도록 막는다**.
- 추가로 `e.stopImmediatePropagation()`는 **같은 요소에 등록된 다른 이벤트 리스너들조차 실행되지 않게 한다**.

### reference
- https://developer.mozilla.org/ko/docs/Web/API/Event/preventDefault
- https://developer.mozilla.org/ko/docs/Web/API/Event/stopPropagation

  
