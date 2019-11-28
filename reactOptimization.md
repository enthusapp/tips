### Controlled vs. Uncontrolled components
state 가 변경될때마다 랜더링이 발생한다.
반드시 필요할때가 아니면 input value 에 state 를 사용하는 controlled components 를 사용할 필요가 없다.
반드시 필요한 상황은 입력 변화에 기민하게 동작해야 하는 상황이다.
즉, submit 이전에 다른 UI 에 표시해야 하거나, UI 효과를 주거나, 실시간 validation 을 하는 경우가 대표적이다.

##### Reference
* https://goshakkk.name/controlled-vs-uncontrolled-inputs-react/
