# mongoDB Tips
## CreateIndex 안되는 경우
이미 입력되어 있는 데이터가 createIndex 조건에 맞지 않으면 index 동작이 수행되지 않는다.
이전 데이터를 수정하거나 drop 한뒤에 createIndex 를 해야 한다.

## 데이터 수동으로 수정
### mongoDB compass

### mongoDB CLI
* https://docs.mongodb.com/manual/reference/mongo-shell/
```
prompt> mongo
> show databases
...

> use <db>  // database 이름 선택
> show collections
...

> db.<collection>.find() // collection 의 data list 출력
...

> db.<collection>.drop() // collection 전체 데이터 삭제
 

> db.<collection>.remove({"sensorID": "1234"}) // sensorID 가 1234 인 데이터 전체 삭제
```

mLab 사용
