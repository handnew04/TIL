주소 / 뒤에 값만 같이 보내는 get request가 아닌 `baseUrl?key1=”key11”&key2=”key22”`와 같은 request를 보낼 경우 

전자의 경우는 Task를 `requestPlain`으로 설정하고 `Path에 직접 값`을 적어서 보낸다. 

후자의 경우(제목의 경우)는 Task를 `requestParameters`의 파라미터로 데이터를 전달하고, encoding을 URLEncoding.queryString으로 지정해야한다. 

→ Alamofire: Alamofire.parameterEncoding이 들어감

post와 달리 get은 JSONEncoding으로 데이터를 넘기는 것이 아니라 , `딕셔너리`로 보내야 한다

[”key1”: key11, “key2”: key22]
