항상 Deep copy 만을 사용한다면 편하지만 성능을 저하시키는 습관이 된다.

최적의 Deep copy 를 찾는 것보다, Shallow copy 을 써도 문제 없는 구조를 만드는 것이 더 좋은 습관이다.

##### 구상중인 더 좋은 방법
* 초기값을 선언할때, 객체 리터럴보다 함수를 통해 객체를 전달하기, 초기값 오염을 방지할수 있다.

### stackoverflow
* https://stackoverflow.com/questions/122102/what-is-the-most-efficient-way-to-deep-clone-an-object-in-javascript/10916838#10916838

##### Object.assign
* Shallow copy
* setter 를 호출
* property 복사 x
* 빠름

##### Object spread
* `{ ...obj }`
* property 복사 x
* 빠름

##### JSON.parse(JSON.stringify(object))
* 간단하고 쉬운 Deep Copy
* 제일 느림

##### v8.deserialize(v8.serialize(obj))
* Node 에서만 동작하는 Native 함수
```
const v8 = require('v8');

const structuredClone = obj => {
  return v8.deserialize(v8.serialize(obj));
};
```

### velog
* https://velog.io/@ddalpange/%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EA%B0%9D%EC%B2%B4-%EB%B3%B5%EC%82%AC%ED%95%98%EA%B8%B0

##### Immutable.js 사용
```
import { Map } from 'immutable';

const map = Map({a : 1});
const newMap = map;
newMap.set('a', 2);
console.log(map.get('a'));
console.log(newMap.get('a'));
```
