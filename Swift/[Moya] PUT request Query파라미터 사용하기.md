기존의 GET request에서 URLEncoding으로 파라미터를 인코딩 했다면 
PUT에서의 Query로 들어가는 파라미터는 `URLEncoding.queryString`으로 인코딩해주어야 한다. 

Get의 파라미터가 pram1, pram2라면

```swift
URLEncoding() => ["param1" : param1, "param2": param2]
```

PUT의 경우
```swift
URLEncoding.queryString => ["param1" : param1, "param2": param2]
```
