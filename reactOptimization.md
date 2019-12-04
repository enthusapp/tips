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

### Redux
##### updater 전달
reducer 소스 내부에 입력 데이터 가공에 대한 코드가 들어가 있는 것보다 해당 입력 컴포넌트에 데이터 가공에 대한 코드가 있는 것이 낫다.
입력 형태에 따라 데이터 가공 형태도 달라지기 때문에 연관된 수정을 두 개의 소스에서 진행하는 것보다 한 개의 소스에서 진행하는 것이 편리하다.
dispatch 할때 데이터를 전달하지 않고 updater 함수를 전달하여 reducer 에서 해당 함수를 실행하게 한다.
각 소스간의 결합성은 줄어들고 reducer 및 상위 컴포넌트들의 형태는 입력 형태의 변화와 상관없이 그대로 유지하게 된다.

##### useStore.getState vs. useSelector
useSelector 를 사용하면 state 가 바뀔때마다 rendering 을 하고, useStore.getState 를 사용하면 rendering 없이 state 만 읽어올수 있다.
state 가 UI 를 구성하는데 쓰이지 않았다면, useStore 를 사용하는 것이 낫다.
