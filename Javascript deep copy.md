### stackoverflow
* https://stackoverflow.com/questions/122102/what-is-the-most-efficient-way-to-deep-clone-an-object-in-javascript/10916838#10916838

##### JSON.parse(JSON.stringify(object))
* 간단하고 쉽지만 제일 느림

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
