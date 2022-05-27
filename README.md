Object.defineProperty(대상 객체, 객체의 속성, {
//정의할 내용
ex)
// 속성값 접근시 동작정의
get: function() {

},
// 속성값 할당시 동작정의
set: function() {

}
})

- 객체의 동작을 재정의함

* Vue 의 핵심은 Reactivity

- 즉시 실행함수 로 statements에 해당하는 부분을 또다른 scope에 넣어주는 역할
- 기본적인 api 들이 이런방식으로 사용됨

```javascript
(function () {
  statements;
})();
```

# 뷰 인스턴스

## 생성

```javascript
new Vue();
```

# 컴포넌트

Vue.component('컴포넌트 이름', 컴포넌트 내용);

# 컴포넌트 통신방식

- 컴포넌트 간에 데이터를 주고 받기 위해선 규칙을 따라야함
- 상위에서 하위로 데이터를 내려줌 => 프롭스 속성
- 하위에서 상위로 이벤트를 올려줌 => 이벤트 발생

```javascript
<app-header v-bind:프롭스 속성 이름="상위 컴포넌트의 데이터 이름"></app-header>

<app-header v-on:하위 컴포넌트에서 발생한 이벤트 이름="상위 컴포넌트의 메서드 이름"></app-header>
```
