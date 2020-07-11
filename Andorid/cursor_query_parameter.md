
# Cursor, query paramater

```
Cursor cursor = context .getContentResolver() .query(uri, projection, selection, selectionArgs, sortOrder);
```

#### parameter

1.  uri
    
    -   content:// 주소 데이터들을 검색 할 수 있음
        
        ```
        Uri uri = ContactsContract.CommonDataKinds.Phone.CONTENT_URI;
        ```
        
2.  projection
    
    -   투사, 투영, 영사
        
    -   쿼리의 결과값에서 보여질 필드를 정하는 것
        
        ```
        String[] projection = new String[]{ ContactsContract.CommonDataKinds.Phone.NUMBER, ContactsContract.CommonDataKinds.Phone.DISPLAY_NAME, };
        ```
    
3.  selection
    
    -   SQL where 절
    -   쿼리의 결과를 찾을 행 조건
    -   null 일 경우 모든 데이터 반환
</br>
4.  selectionArgs
    -   selelction을 지정하였을 경우, where 절에 해당하는 값들을 배열로 넣어줌
</br>
5.  sortOrder
    
    -   결과 값의 정렬 조건
    
    ```
    String sortOrder = ContactsContract.CommonDataKinds.Phone.DISPLAY_NAME + " COLLATE LOCALIZED ASC";
    ```