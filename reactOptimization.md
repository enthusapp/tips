### Controlled vs. Uncontrolled components
state 가 변경될때마다 랜더링이 발생한다.
반드시 필요할때가 아니면 input value 에 state 를 사용하는 controlled components 를 사용할 필요가 없다.
반드시 필요한 상황은 입력 변화에 기민하게 동작해야 하는 상황이다.
즉, submit 이전에 다른 UI 에 표시해야 하거나, UI 효과를 주거나, 실시간 validation 을 하는 경우가 대표적이다.

##### Reference
* https://goshakkk.name/controlled-vs-uncontrolled-inputs-react/

### 불변성, 깊은 값의 수정

##### Immuatable vs. Immer
* https://www.reddit.com/r/javascript/comments/96xqnu/immer_or_immutablejs/

### 랜더링 최적화
state, props 가 변경될때, 부모 컴포넌트가 리랜더링 될때, forceUpdate 가 실행될때 컴포넌트는 리랜더링 된다.
리랜더링은 컴포넌트 개수가 증가에 비례하여 늘어나게 되고, 가장 많은 성능 문제를 발생시킨다.

따라서 리랜더링 조건을 최소화하는 최적화 작업이 항상 필요하다.

##### React.memo
부모 컴포넌트가 리랜더링 되더라도 props 가 변경되지 않았으면 리랜더링 하지 않게 해준다.

##### 전달 props 의 최적화
자식 컴포넌트에 입력하는 props 들이 최대한 변경되지 않도록 해야 한다.
useCallback 등을 이용하여 props 로 전달되는 함수들이 리랜더링 시에 재생성 되지 않도록 해야 한다.
props 개수를 최소화해야 한다. 기본 구조 자체에 props 전달을 적게 할수 있는 방향으로 해야 한다.
redux 를 사용하는 방법도 있다.
