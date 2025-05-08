# Iterator
- https://developer.mozilla.org/ko/docs/Web/JavaScript/Guide/Iterators_and_generators

## 반복문 vs Iterator
- [이터레이터도 필터 쓸 수 있다(Since March 2025)](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Global_Objects/Iterator/filter)

### 성능테스트 코드
```
let arr = [];
for (let i = 0; i < 1000000; i++) {
  arr.push(Math.floor(Math.random() * 1000)); // 100만 개의 랜덤 숫자
}

console.time('filter');
let filtered1 = arr.filter(x => x % 2 === 0);  // 짝수 필터링
console.timeEnd('filter');

console.time('values-filter');
let filtered2 = arr.values().filter(x => x % 2 === 0);  // values()와 filter 사용
console.timeEnd('values-filter');
```
### 결과
```
filter: 14.096923828125 ms
values-filter: 0.0439453125 ms

filter: 15.927978515625 ms
values-filter: 0.080078125 ms

filter: 14.4619140625 ms
values-filter: 0.01806640625 ms
```
