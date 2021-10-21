### Django 파라미터 전달 ***

---

#### <url 변수>   

url path형식으로  파라미터를 전달하면 

```python
urlpatters = [
	path('lec/<ink:pk>.') views.lec_detail, name="lec_detail")
]
```

<int: pk> 가 views.py의 인자값이 됨. 즉, 엔드포인트가 되는 것.

ex ) localhost:8000/lec/<int: pk> <-- 이런 식  

특히 어떤 자원의 위치를 특정할 때 사용. ex) 특정 상품의 상세 페이지 

#### <쿼리 파라미터>

파이썬 request 객체의 get은 파라미터를 자동으로 딕셔너리로 변환하여 저장.

만약, url/info?product=2&price=3 의 형식으로 파라미터를 보내면,

{'product' : 2, 'price': 3}의 형태로 저장.

? 뒤에 있는 값을 저장해 백엔드로 전달(정보 요청)

쿼리 파라미터는  key:value 쌍을 가진 쿼리 



쿼리 파라미터 & url 파리미터 정리를 잘 해놓은 것 참고! 

https://velog.io/@swhybein/django-queryurl-%ED%8C%8C%EB%9D%BC%EB%AF%B8%ED%84%B0