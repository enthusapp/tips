### Controlled vs. Uncontrolled compoenents
state 가 변경될때마다 랜더링이 발생한다.
input value 에 state 를 사용하면 불필요한 랜더링이 발생하는 것은 아닐까?
value 를 React.memo 에서 제외하는 방법도 불필요한 코드를 증가시키는 것으로 보인다.

* https://goshakkk.name/controlled-vs-uncontrolled-inputs-react/
