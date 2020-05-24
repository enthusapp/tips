# mongoDB 의 데이터를 수동으로 수정하고 싶을때
### mongoDB compass 사용

### mongoDB CLI 사용
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
```

mLab 사용
