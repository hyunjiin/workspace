## Serializers

serializer는 <u>queryset과 모델 인스턴스</u>와 같은 **복잡한 데이터**를 JSON, XML 또는 다른 컨텐츠 유형으로 쉽게 변환 할 수 있음.  serializer는 받은 데이터의 유효성(validation)을 검사한 다음, 복잡한 타입으로 형 변환을 할 수 있또록 serialization을 제공한다. Restframework의 serializer는 Django의 형태와 ModelForm 클래스와 유사하게 동작. 

#### [Serialzers의 필드 타입 변경하기]



```python
class TestSerializer(serializers.ModelSerializer):
    원래의 필드명 = serializers.IntegerField(source="<바꾸고 싶은 필드명")
    
    class Meta:
        model = TestModel
        fields = ('원래의 필드명', ...)
    
```

나의 경우 

```python
#models.py
class Lec(models.Model):
    objects = models.Manager()
    lec_id = models.AutoField(primary_key=True)
    title = models.CharField(max_length=50)
    content = models.TextField()
    room = models.CharField(max_length=10)
    date = models.DateField()
    time = models.TimeField()
    level = models.IntegerField()
    email = models.ForeignKey(settings.AUTH_USER_MODEL, on_delete=models.CASCADE)
    number = models.IntegerField()
    status = models.IntegerField()

    def __str__(self):
        return self.title

```

email 필드가 ForeignKey로 연결되어 있어서 화면에 숫자 값으로 return 됨. 나는 본래의 text로 나타나게 하고 싶어서 

```python
#serializers.py
class LecSerializer(serializers.ModelSerializer):
    email = serializers.CharField(source="email.name")   

    class Meta:
        model = Lec
        fields = ['lec_id', 'title', 'content', 'room', 'date', 'time', 'level', 'email', 'number', 'status']

```

`email = serializers.CharField(source="email.name")   `를 추가.

`원래 필드명 = serializers. 나타내고 싶은 필드종류(source="새로운 필드명")`

참조: https://jinmay.github.io/2020/05/13/django/drf-how-to-change-field-name-of-serializer/