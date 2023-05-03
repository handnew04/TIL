주소 / 뒤에 하나의 값만 보내는(path parameter) get request가 아닌 `baseUrl?key1=”key11”&key2=”key22”`와 같은 query string request를 보낼 경우 

Path parameter의 경우는 Task를 `requestPlain`으로 설정하고 `Path에 직접 값`을 적어서 보낸다. 

Query string의 경우(제목의 경우)는 Task를 `requestParameters`의 파라미터로 데이터를 전달하고, encoding을 URLEncoding.queryString으로 지정해야한다. 

→ Alamofire: Alamofire.parameterEncoding이 들어감

post와 달리 get은 JSONEncoding으로 데이터를 넘기는 것이 아니라 , `딕셔너리`로 보내야 한다

[”key1”: key11, “key2”: key22]

또는 URLEncoding으로 보내면 된다. 

```swift
URLEncoding() => [
  "param1" : param1,
  "param2" : param2
]
```
