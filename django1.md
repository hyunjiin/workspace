#### 웹 프로그램

---

- 웹 프로그램은 **클라이언트와 서버**로 이루어짐. 

#### 웹 프로그래밍

---

- 웹 프로그래밍이란? HTTP 프로토콜로 통신하는, **클라이언트와 서버를 개발**하는 것.
  - 보통 **웹 서버**를 개발하는 경우가 많아서 파이썬 프로그래밍이라고 하면 장고 같은 웹 프레임워크를 사용하여 웹 서버를 개발하는 것을 떠올린다.

##### [웹 클라이언트? 웹 서버?]

-> 웹은 서버 - 클라이언트 체계에서 동작함. 인터넷이 연결되어 있는 환경에서 동작하는 앱이나 웹, 게임 등은 모두 클라이언트 - 서버 체계에서 동작. 

- <u>웹 브라우저</u>를 실행해서 <u>네이버</u>에 접속하는 것도 웹 프로그램이 동작하는 것이다.
  - 여기서 **웹 브라우저는 클라이언트이고 웹 서버는 네이버 서버이다.** (즉,  **클라이언트가 요청하고  서버가 응답**하는 클라이언트 - 서버 프로그램이 동작하는 것  )
- 웹 브라우저를 켜서 주소를 입력하면 주소에 해당되는 서버에게 내가 알고 싶은 웹 페이지의 정보를 요청하는 것이다. 웹 서버가 그 요청을 받아서 하드디스크나 어딘가에 저장되어 있는 웹 페이지 문서를 읽어서 다시 클라이언트 컴퓨터에게 보내준다.(이를 응답이라고 함)

<mozilla>

![](C:\Users\guswl\OneDrive\바탕 화면\문법 정리\정리 사진 파일\image.png)

![](C:\Users\guswl\OneDrive\바탕 화면\문법 정리\정리 사진 파일\캡처8.PNG)

- **서버**: 클라이언트에게 네트워크를 통해 **정보나 서비스를 제공**하는 컴퓨터 시스템으로 컴퓨터 프로그램 또는 장치를 의미. 제공하는 서비스가 웹이면 웹 서버인 것이고, 서비스가 메일이라면 메일 서버가 된다.

- **웹서버** : 웹 브라우저와 같은 **클라이언트로부터** *HTTP 프로토콜로 **요청을 받아** HTML 문서 등과 같은 **정적 웹 페이지를 응답**해주는 **소프트 웨어** (서버 쪽에서 정보를 제공하는 소프트웨어를 의미)
  -  ex) apache, nginx 등 ( 둘 다 오픈소스)  
- 웹 브라우저 : 웹 클라이언트라고 해도 무방함. 

##### [웹 서버 동작]

<하드웨어 측면>

- 하드웨어 측면에서 **웹서버는 웹서버의 소프트웨어와 웹사이트의 컴포넌트 파일들을 저장하는 컴퓨터**.
- 컴포넌트 파일에는 HTML 문서, images, CSS stylesheets, 그리고 JavaScript files이 있음.
- 웹 서버는 인터넷에 연결되어 있고, 도메인 이름을 통해 접속 될 수 있음.

<소프트웨어 측면>

- 웹 사용자가 어떻게 호스트 파일들에 접근하는 지를 관리 
- HTTP 서버(웹 서버)는 URL과 HTTP의 소프트웨어 일부.

#### HTTP 프로토콜

---

- 웹 서버와 웹 클라이언트 사이에서 데이터를 주고받기 위해 사용하는 **통신 방식으**로, TCP/IP 프로토콜 위에서 동작.

  즉, 우리가 웹을 이용하려면 웹 서버와 웹 클라이언트는 각각 TCP/IP 동작에 필수적인 IP주소를 가져야 한다는 뜻.

- HTTP란 하이퍼텍스트 전송용 프토콜이지만 실제로 HTML, XML과 같은 하이퍼텍스트 뿐만 아니라 이미지 ,음성 ,자바스크립트 와 각종 도큐먼트 파일 등 컴퓨터에서 다룰 수 있는 데이터는 무엇이든 전송할 수 있음
  - ex) 웹 브라우저 창에 naver.com을 입력하고 엔터를 누르면 웹 클라이언트와 서버 사이에 http연결이 맺어지고, 웹 클라이언트는 웹 서버에 http 요청 메세지를 보낸다. 웹 서버는 요청에 따른 처리를 진행한 후, 그 결과를 웹 클라이언트에게 HTTP 응답 메세지를 보냄. 이런 방식으로 요청 메세지와 응답 메세지가 반복적으로 오가면서 웹을 사용. 

#### HTTP 메세지 구조

---

1) **요청 메세지** : 클라이언트 -> 서버
2) **응답 메세지** : 서버 -> 클라이언트 
   - 처리 결과를 상태라인에 표시
   - 바디에는 보통 HTML 테스트 표시

![](C:\Users\guswl\OneDrive\바탕 화면\문법 정리\정리 사진 파일\캡처9.PNG)

- 헤더와 바디는 빈 줄로 구분 / 헤더와 바디는 생략 가능
- HOST 항목은 필수

#### HTTP 처리 방식

---

- HTTP 메소드를 통해서 클라이언트가 원하는 처리방식을 서버에 알려줌.

##### [HTTP 메소드]

- HTTP 메소드는 데이터 조작의 기본이 되는 CRUD와 매핑되는 처리를 함.

1. GET 방식 (Read 조회) : 지정한 URL의 정보를 가져오는 방식
   - 웹 브라우저를 이용하여 서버로부터 웹 페이지, 이미지, 동영상 등을 가져오려고 할 때 수 많은 GET 방식의 요청 사용
2. POST (Creat 생성) : 리소스 생성
   - 블로그에 글을 등록하는 경우
3. PUT (Update 변경) : 리소스 변경
   - 블로그에서 글을 업로드한 작성자를 변경하거나 글의 내용을 업데이트 하는 경우
4. DELETE (Delete 삭제) : 리소스 삭제
   - 일반적으로 DELETE 요청에 대한 응답은 바디를 반환하지 않음.

#### GET, POST 메소드

---

- 가장 많이 사용되는 2가지 메소드 / HTML의 폼에서 지정할 수 있는 메소드
- 파라미터를 보내는 방식의 차이가 있음

1. GET : URL 부분의 **?** 뒤에 **"이름 = 값**" 쌍으로 이어붙여 보냄 
   - URL의 길이 제한이 있기 때문에 많은 양의 데이터를 보내기 어렵고
   - 전달되는 사용자의 데이터가 웹 브라우저의 주소창에 노출되는 단점이 있어 보안 측면에서 불리
2. POST : GET에서 URL에 포함시켰던 파라미터들을 요청 메세지의 바디에 넣음 (URL에 드러내지 않음)
   - 폼을 사용하거나 추가적인 파라미터를 서버로 보내는 경우 POST 방식을 많이 사용

#### 상태코드

---

- 서버에서의 처리 결과는 응답 메세지의 상태라인에 있는 상태 코드를 보고 파악 가능.

- 상태코드는 세 자리 숫자로 되어 있음

  ex) 404 , 500 , 502 등의 번호

#### URL 설계 

---

- 웹 어플리케이션을 개발 할 때, 고객의 요구사항이 정리되면 먼저 디자인 측면에서 **화면 UI**를 설계하고,

  프로그램 로직 측면에서는 **URL**을 설계함. 즉, URL의 설계는 웹 서버 로직 설계의 첫걸음이며, 사용자 또는 웹 클라이언트에게 웹 서버가 가지고 있는 기능을 명시해주는 중요한 단계.  전체 프로그램 로직을 생각하면서 차후 로직이 변경되더라도 URL 변경은 최소화 할 수 있도록 유연하게 설계하는 것이 중요.

  ex) **http://www.example.com:80/service?catregory=2&kind=patets#n10**

  - 포트번호 (80) : 웹 서버내의 서비스 포트번호. 생략시에는 디폴트 포트 번호로 http는 80, https는 443을 사용.

#### URL을 바라보는 측면 

---

- url은 웹 클라이언트에서 호출한다는 시점에서 보면, 웹 서버에 존재하는 애플리케이션에 대한 API라고 할 수 있다.
  - 이러한 API의 명명 규칙을 정하는 방법은 두가지로 분류가 가능한데, URL을 **RPC로 바라보는 방식과 REST로 바라보는 방식.**
- REST방식으로 URL 설계
  - REST 방식이란? **웹 서버에 존재하는 요소들을 모두 리소스라고 정의**하고, URL을 통해 웹 서버의 특정 리소스를 표현한다는 개념. 리소스는 시간이 지남에 따라 상태가 변할 수 있기 때문에 **클라이언트와 서버 간에 데이터 교환을 리소스 상태의 교환으로 간주**한다.
  - 중요한 것은 리소스에 대한 조작을 GET, POST, PUT, DELETE 등의 HTTP 메소드로 구분한다. 
  - 따라서, REST 방식으로 바라본다면 **웹 클라이언트에서 URL을 전송하는 것이 웹 서버에 있는 리소스 상태에 대한 정보를 주고 받는 것**으로 간주 될 수 있다. 
  - http://blog.example.com/search/test   <-- get 메소드를 사용한 REST 방식 형태

#### 간편 URL

---

- 쿼리스트링 없이 경로만 가진 간단한 구조의 URL

#### 파이썬의 우아한 URL

---

- 파이썬 프레임 워크에서는 처음부터 간편식 URL 체계를 도입하였고 그 외에도 정규표현식을 추가적으로 사용해 URL 정의 가능.

#### 웹 어플리케이션 서버 **

---

- 웹 클라이언트(보통은 웹 브라우저를 지칭)의 요청을 받아서 처리하는 서버를 통치하여 웹서버라고 부르지만, 좀 더 세분화 하면

  **웹 어플리케이션 서버 / 웹 서버**로 분류 가능. 

- **웹 서버** : 웹 클라이언트의 요청을 받아서 요청을 처리하고, 그 결과를 웹 클라이언트에게 응답. 주로 정적 페이지인 HTML, 자바스크립트 파일, CSS, 이미지를 웹 클라이언트에 제공할 때 웹 서버 사용. 만약 동적 페이지 처리가 필요하다면 웹 어플리케이션 서버에 처리를 넘김. ex) Apache, Nginx, lighttpd, IIS

- **웹 어플리케이션 서버** : 웹 서버로부터 동적 페이지 요청을 받아서 요청을 처리하고 그 결과를 웹 서버로 반환. 주로 동적 페이지 생성을 위한 프로그램 실행과 데이터베이스 연동 기능을 처리. ex) Apache Tomcat, mod_wsgi, Gunicorn

  ->  웹 서버 및 웹 어플리케이션 서버라는 용어는 **소프트웨어** 측면의 서버 프로그램을 의미. 

#### 정적 페이지 vs 동적 페이지 

---

1. **정적페이지** 	
   - 언제 요구하더라도 **항상 같은 내용**을 표시하는 웹 페이지. 	
   - 웹 서비스의 제공자가 사전에 준비하여 서버 측에 배치한 것
   - 동일한 리소스의 요청에 대해서는 항상 동일한 내용의 페이지를 반환
   - 주로 HTML, CSS, 자바스크립트, 이미지 만으로 이루어진 페이지가 해당

2. **동적 페이지**
   - 동일한 리소스의 요청이라도 누가, 언제 어떻게 요구했는지에 따라 **각각 다른 내용이 반환**되는 페이지.
   - ex) 현재 시각을 보여주는 페이지, 쇼핑 사이트에서 사용자마다 다른 카트 내용 보여주는 페이지

-> 정적, 동적이란 용어는 사용자가 페이지를 요청하는 시점에 페이지의 내용이 유지되는가, 변경되는가를 구분해주는 용어

 = 즉, 동적 페이지에는 프로그래밍 코드가 포함되어 있어서 페이지 요청 시점에 HTML 문장을 만들어 내는 것.



초창기 정적 페이지를 보여주는 것이 주된 웹 서버의 주된 역할이였으나 점차 동작 페이지에 대한 요구가 생기고 필요한 데이터를 저장하고 꺼내오는 등의 데이터베이스 처리에 대한 요구가 많아짐에 따라 웹 서버와는 별도의 프로그램이 필요하게 됨.

***CGI 규격**: 별도의 프로그램과 웹 서버 사이에 주고받는 규칙을 정의 한 것 (책 참고)

#### 애플리케이션 서버 방식

---

- 웹 서버가 직접 프로그램을 호출하기 보다 웹 애플리케이션 서버를 통해서 **간접적으**로 웹 애플리케이션 프로그램을 실행. 

  웹 애플리케이션 서버는 애플리케이션 프로그램의 실행 결과를 웹 서버에 전달해주며, 웹 애플리케이션 서버로부터 전달받은 응답 결과를 웹 클라이언트에 전송.

  ![](C:\Users\guswl\OneDrive\바탕 화면\문법 정리\정리 사진 파일\캡처 10.PNG)

- 웹 서버와 웹 애플리케이션 서버가 분리됨에 따라 서로의 역할도 구분하여 사용하는 것이 좋음

  정적 페이지를 처리하는 경우에 비해 동적 페이지를 처리하는 경우가 더 많은 메모리를 소비하기 때문.

  즉, 정적 페이지 처리에 특화된 웹 서버는 정적 페이지만 처리하고, 웹 애플리케이션 서버는 동작 페이지만 처리하도록

  역할을 분담하는 것이 훨씬 효율적.

- 웹 서버는 정적 페이지를 웹 클라이언트에게 제공하는 것이 주 역할 + 캐시 기능, 프록시 기능의 추가적이 기능 제공 등등
- 웹 애플리케이션 서버는 웹 서버와의 연동 규격만 잘 따르면 임의의 언어 플랫폼을 사용하여 애플리케이션 프로그램을 작성하고 실행시킬 수 있음.

#### 웹 서버와의 역할 구분 

---

https://developer.mozilla.org/ko/docs/Learn/Common_questions/What_is_a_web_server

#### 웹 서버 라이브러리

---

웹 프로그래밍의 클라이언트 쪽은 웹 브라우저라는 강력한 프로그램을 사용하기 때문에 웹 서버 프로그램을 작성할 때는 개발자가 직접 파이썬 라이브러리를 사용해서 웹 서버를 개발하기보다 웹 프레임워크를 사용해서 개발하는 경우가 대부분. 

***라이브러리** : 개발 시 활용 가능한 도구들을 모아서 모듈화 한 것

***프레임 워크**(뼈대) : 기본적인 뼈대가 이미 완성되어 있고 규칙이 존재하는 **개발환경** (개발자들이 따라야 할 가이드라인을 가지며 개발 범위가 정해져 있고 다양한 도구가 지원된다 -> 개발 편의성이 높아지며 오류의 폭을 좁힐 수 있으나 의존도가 높아져 개발 능력이 저하될 수 있고 자유도가 떨어짐.)

### CGI란?

---

- **공통 게이트웨이 인터페이스(Common Gateway Interface)**의 약어로, 웹서버와 외부 프로그램 사이에서 **정보를 주고받는** **방법이나 규약**

  -> 웹 서버도 종류가 여러가지일 것이고, 프로그램 또한 엄청나게 많은 프로그램이 존재하기 때문에 **서로 입출력을 주고 받을 표준이 필요** / 이 표준에 맞추어 만들어진 것이 CGI 스크립트. CGI 스크립트는 어떤 프로그래밍 언어로도 만들 수 있음. 

  *인터페이스 = **상호 간의 소통을 위해 만들어진 물리적 매개체나 프로토콜** 

- CGI를 구동하는 방법이 한가지는 아니지만 대표적인 방법이  Apache HTTPd.
- 웹 서버와 통신하기 위해 CGI를 사용하는 프로그램은 매 리퀘스트(요청)마다 서버를 재 시작해야 함. 모든 리퀘스트(요청)은 파이썬 인터프리터를 새롭게 구동하기 때문에 CGI는 부하가 적은 상황에서만 쓸모 있는듯. 

![](웹 프로그래밍, 웹서버.assets/캡처 13.png)


유저가 웹페이지를 요청했을 때 서버는 요청된 페이지를 보내준다. 하지만 유저가 웹페이지에서 **특정 form**을 채운 뒤 웹페이지를 보내면 이는 보통 애플리케이션에 의해 처리되어야 한다. 웹서버는 보통 form 정보를 처리해줄 애플리케이션 프로그램에 정보를 보내고, confirmation 메시지를 돌려준다. 예를 들어, 회원가입 정보라면 서버는 이 정보를 애플리케이션에 보내 회원가입 관련 로직이 수행되도록 할 것이고, 애플리케이션은 회원가입 로직을 수행한 뒤 결과를 서버에 다시 보내줄 것이다. 이렇게 서버와 애플리케이션이 소통할 때 CGI 기반으로 만들어진 프로그램이라면 CGI 스펙을 따라 소통이 이루어진다.

그러니까 **CGI도 그냥 인터페이스**인데, 무엇과 무엇 사이의 인터페이스냐면 **웹서버와 요청을 받아 처리해줄 로직을 담고 있는 애플리케이션 프로그램 사이의 인터페이스**인 것이다. 웹서버가 특정 언어로 쓰인 구체적인 프로그램이 아니라 **이 인터페이스에 의존하고 있기 때문에** **어떤 언어든 이 인터페이스를 구현하기만 한다면(CGI 스펙을 따른다면) 웹서버와 소통할 수 있다.**

즉, 웹 서버와 애플리케이션 간에 데이터를 주고받기 위한 규격을 CGI라고 함.

##### [CGI 장, 단점]

**CGI 장점**

- 언어, 플랫폼 독립적이다(스펙만 준수하면 된다).
- 매우 단순하고 다른 server-side 프로그래밍 언어에 비해 advanced task를 훨씬 쉽게 수행할 수 있다.
- 재사용할 수 있는 CGI 코드 라이브러리가 풍부하다.
- CGI가 웹서버에서 실행될 때 안전하다.
- CGI 코드를 수행하는데 특정 라이브러리가 필요하지 않기 때문에 매우 가볍다.

**CGI 단점**

- 느리다(요청이 올 때마다 DB connection을 새로 열어야 한다).
- **HTTP 요청마다 새로운 프로세스를 만들기 때문에** 서버 메모리를 많이 잡아먹는다.
  (servlet은 요청마다 스레드를 만든다.)
  - 서버의 부하가 높아져서 프로세스가 멈추거나 다운 도리 수도 있음.
- 페이지 로드 사이에 데이터가 메모리에 캐시될 수 없다.

#### WSGI

---

파이썬에서는 WSGI 규격이 정의. 파이썬애플리케이션을 실행하고자 하는 웹 서버는 이 규격을 준수해야 함. 

CGI의 단점을 해결하고 파이썬 언어로 애플리케이션을 좀 더 쉽게 작성할 수 있또록 웹 서버와 애플리케이션 간에 연동 규격을 정의한 것이 WSGI.

따라서 파이썬에서는 WSGI규격만 맞추면 어떠한 웹 서버에서도 파이썬 애플리케이션을 실행할 수 있다.

ex) 장고로 작성한 웹 애플리케이션은 아파치 웹서버/ Nginx 웹 서버에서도 실행할 수 있다. 아파치나 nginx는 일반 범용 웹 서버로 WSGI 처리 기능이 없다. 이런 **웹 서버와 파이썬 웹 애플리케이션 중간**에서 WSGI 통신 규격을 처리해주는 것이 mod_wsgi, Gunicorn과 같은 WSGI 서버.

#### 장고 Django

---

- 파이썬으로 만들어진 무료 오픈소스 웹 애플리케이션 프레임 워크. **(파이썬 웹 프레임 워크**) 쉽고 빠르게 웹 사이트를 개발할 수 있도록  돕는 구성요소로 이루어진 웹 프레임 워크.


#### 장고의 특징

---

##### [MVT 개발패턴 ]

장고는 MVC 를 기반으로 한 프레임 워크이지만 장고에서는 View를 Template, Controller를 View라고 부른다. 따라서 장고를 흔히 **MVT 프레임 워크**라고 함. (용어만 다를 뿐, 기능은 같음)

**Mode**l : 데이터베이스에 액세스하는 컴포넌트

**View**: 데이터를 가져오고 변형하는 컴포넌트 (=Controller)

**Template** : 데이터를 사용자에게 보여주는 컴포넌트(=View)

##### [객체 관계 매핑 ORM]

- ORM이란? Object Relation Mapping

- 객체(Object)와 관계형 데이터베이스(Relational)를 연결(Mapping)해주는 것을 의미.  즉, 데이터베이스의 테이블을 객체(Object)와 연결하여 테이블을 CRUD 할 때, SQL 쿼리를 사용하지 않고도  데이터베이스의 데이터를 다룰 수 있게 한다. 데이터베이스의 테이블을 객체지향 프로그래밍에서 흔히 사용하는 객체(Class)처럼 사용할 수 있도록 해주는 기술.

= 작성한 파이썬 코드를 관계형 DB의 SQL 쿼리로 자동 변환 시켜서 개발자가 따로 SQL 쿼리를 작성할 필요 없이 파이썬 코드 작성만으로 DB를 조작할 수 있게 해 주는 것

- 파이썬에서 모델을 작성하고 migration 하면 **장고가 ORM으로 쿼리를 생성해서 실행**했기 때문입에 테이블이 생김.

  클래스의 모양 그대로 DB 테이블을 구성할 수 있도록 SQL을 생성한 것.
  
  ##### [Django Model]
  
  - 데이터베이스 Table과 파이썬의 Calss는 1대 1로 매핑 
  
  ##### [쿼리셋]
  
  - 전달받은 모델의 **객체 목록**
  - 데이터베이스로부터 데이터를 읽고, 필터를 걸거나 정렬 가능 
  - 장고의 ORM인 장고 Mode

##### [자동으로 구성되는 관리자 화면]

장고는 웹 서버의 콘텐츠, 데이터베이스에 대한 관리 기능을 위하여 프로젝트를 시작하는 시점에 기본 기능으로 관리자 화면 제공. 관리자 화면을 통해 애플리케이션에서 사용하는 테이블과 데이터들을 쉽게 생성하거나 변경 가능.

##### [우아한 URL 설계]

장고는 우아한 URL 방식 채택 -> 직관적이고 쉽게 표현.

+정규표현식을 사용해 복잡한 URL도 표현 가능하며, 각 URL 형태를 파이썬 함수에 1:!로 연결하도록 되어 있음

##### [자체 템플릿 시스템]

장고는 내부적으로 확장 가능하고 디자인이 쉬운 강력한 템플릿 시스템이 있음. 화면 디자인과 로직에 대한 코딩을 분리하여 독립적인 개발 진행이 가능.템플릿 시스템은 HTML과 같은 텍스트 형 언어 쉽게 다룰 수 있음.
