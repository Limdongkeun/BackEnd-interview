# Backend-Interview-Question

## CS

<details>
<summary>TCP와 UDP 방식의 차이점을 설명해주세요.</summary>
<div markdown="1">

  + tcp는 연결 지향형 프로토콜이고 udp는 데이터를 데이터그램단위로 전송하는 프로토콜입니다. tcp는 가상 회선을 만들어 신뢰성을 보장하도록하는 프로토콜로 따로 신뢰성을 보장하기
    위한 절차가 없는 udp에 비해 속도가 느린편입니다
  + TCP는 그래서 파일전송과 같은 신뢰성이 중요한 서비스에 사용되고, UDP는 스트리밍과 같이 연속성이 더 중요한 서비스에 사용됩니다

</div>
</details>
<details>
<summary>Client Side Rendering 과 Server Side Rendering 의 차이점에 대해서 설명해주세요.</summary>
<div markdown="1">

+ ssr이란 서버로부터 완전하게 만들어진 html 파일을 받아와 페이지 전체를 렌더링 하는 방식이고, csr은 사용자의 요청에 따라 필요한 부분만 응답 받아 렌더링하는 방식입니다 
  + SSR
  
    장점 : seo 검색엔진의 최적화 되어있다 , 빠른 초기 로딩시간 이 있습니다
    
    단점 : 요청시마다 전체 페이지가 새로고침되고, 새로운 요청이 있을때마다 바뀌지 않아도 되는 부분까지 렌더링 되기 때문에 서버에 부하를 줍니다
    
  + CSR
  
    장점 : 속도가 빠르며 서버의 부화가 적습니다, 새로운 요청을 할때 페이지 전체가 렌더링되지 않고 필요한 부분만 되기 때문에 사용자 친화적입니다
    
    단점 : 자바스크립트를 사용하여 사용자와 상호작용 후에 페이지 내용을 로드하기 때문에 seo에 불리합니다 또한 모든 파일을 서버에서 받아와야 하기 때문에 초기로딩 속도가 느립니다
    

</div>
</details>
<details>
<summary>URL과 URI의 차이점이 무엇인가요?</summary>
<div markdown="1">

  + URI는 특정 리소스를 식별하는 통합 자원 식별자를 의미하고 URL은 흔히 웹주소를 나타내며 리소스가 어디에 있는지 알려주기 위한 규약입니다
  
  + 실세계에 빗대어 보면 “임동근”은 제 이름이며 식별자입니다 하지만 제 위치, 연락처 등을 알 수 없기 때문에 URL이 될 수 없고, “서울시 송파구 석촌동”은 주소로 특정 위치를 알려주는 것 입니다
</div>
</details>
<details>
<summary>REST API란 무엇인가요?</summary>
<div markdown="1">
  
  -   REST의 원리를 따르는 API입니다
  
    1. URI는 동사보다 명사, 대문자보다 소문자 사용
    2. 마지막에 슬래시를 포함하지 않는다
    3.언더바 대신 하이픈을 사용한다
    4.파일확장자는 포함하지 않는다
    5.행위는 포함하지 않는다

  + REST란 REST(Representational State Transfer)의 약자로 자원을 이름으로 구분하여 해당 자원의 상태를 주고받는 모든 것을 의미합니다
    즉 URI를 통해 자원을 명시하고, HTTP Method를 이용하여 자원에 대한 CRUD를 적용하는것 입니다 

  + RestFul REST의 원리를 따르는 시스템을 의미하고, REST API의 설계 규칙을 올바르게 지킨 시스템을 RESTful하다 말할 수 있습니다
  
  + HTTP 표준 프로토콜에 따르는 모든 플랫폼에서 사용이 가능하며, REST API 메세지가 의도하는 바를 명확하게 나타내므로 의도하는 바를 쉽게 파악 할 수 있어 프런트엔드와 백엔드의 소통이 원활합니다
</div>
</details>
<details>
<summary>CORS에 대해 설명해주세요.</summary>
<div markdown="1">
  
  -   교차 출처 리소스 공유로 동일한 출처가 아닌 다른 출처에서 데이터를 주고받는 것을 제한하기 때문에 이러한 문제를 해결하기 위한 정책입니다
      방법으로는 예비요청과, 단순요청이 있습니다
      동일한 출처는 URL 중에서도 프로토콜, 도메인 주소, 포트 번호가 같은 것을 의미합니다
</div>
</details>
<details>
<summary>Session과 Cookie 그리고 Token 인증방식에 대해 설명해주세요.</summary>
<div markdown="1">
  
  -   세션은 사용자의 정보를 서버에 저장하여 활용하는 방식이고, 서버에서 발급된 세션ID를 쿠키에 담아 클라이언트에게 인증정보를 넘겨주는 것이 쿠키 방식입니다
  -   토큰은 엑세스토큰을 http헤더에 담아 클라이언트에게 넘겨주고 요청을 할때 토큰을 이용하여 서버에 넘겨줍니다 토큰은 시간 제약이 있어 엑세스 토큰이 만료되면 
      서버에 저장된 리프래시 토큰을 이용하여 재발급 받습니다
</div>
</details>
<details>
<summary>CORS가 무엇이고, CORS 정책을 Spring Security에 설정하는 방법에 대해서 설명해 주세요.</summary>
<div markdown="1">
  
  -   교차 출처 리소스 공유로 동일한 출처가 아닌 다른 출처에서 데이터를 주고받는 것을 제한하기 때문에 이러한 문제를 해결하기 위한 정책입니다
      방법으로는 예비요청과, 단순요청이 있습니다 동일한 출처는 URL 중에서도 프로토콜, 도메인 주소, 포트 번호가 같은 것을 의미합니다
  -   corsConfigurationSource로 허용되는 URL,header,method를 설정하는 방법이 있습니다
</div>
</details>
<details>
<summary>인증(Authentication)과 인가(권한 부여, Authorization)의 차이에 대해 설명해 주세요.</summary>
<div markdown="1">
  
  -   인증은 사용자가 누구인지 확인하는 절차이며, 회원가입이나 로그인 입니다 
  -   인가는 사용자에게 서비스 접근에 대한 권한을 허용해 주는것 입니다
</div>
</details>
<details>
<summary>세션과 쿠키 그리고 토큰 인증 방식에 대해 설명해 주세요.</summary>
<div markdown="1">
  
  -   세션은 사용자의 정보를 서버에 저장하여 활용하는 방식이고, 서버에서 발급된 세션ID를 쿠키에 담아 클라이언트에게 인증정보를 넘겨주는 것이 쿠키 방식입니다
  -   토큰은 엑세스토큰을 http헤더에 담아 클라이언트에게 넘겨주고 요청을 할때 토큰을 이용하여 서버에 넘겨줍니다 토큰은 시간 제약이 있어 엑세스 토큰이 만료되면 서버에 저장된 리프래시 토큰을 이용하여 
      재발급 받습니다
</div>
</details>
<details>
<summary>패스워드를 암호화 하는 단방향 암호화에 대해서 설명해 주세요.</summary>
<div markdown="1">
  
  -   한쪽 방향으로만 암호화를 한다는 의미합니다 즉 암호화만 가능하고 복호화는 할 수 없습니다그렇기 때문에 비밀번호를 관리할 때 유용하게 사용됩니다 비밀번호를 단방향 암호화 방식으로 저장하는 경우에는 
      비밀번호 DB가 노출되어도 안전합니다 비밀번호를 검증할 때에는 사용자로부터 입력받은 비밀번호를 똑같은 방식으로 암호화하여 암호화된 비밀번호끼리 비교를 하면 됩니다 대표적으로 많이 사용하고 있는 
      알고리즘은 SHA-256 암호화 알고리즘 입니다
</div>
</details>
<details>
<summary>캐시란 무엇인가요? 캐시의 일반적인 작동원리를 설명해주세요.</summary>
<div markdown="1">
  
  -   캐시란 자주 사용하는 데이터나 값을 미리 복사해두는 임시 저장소 입니다 저장공간이 작고 비용이 비싼대신 빠른 성능을 제공합니다
  -   원래 데이터에 접근하는 시간이 오래걸리는 경우나 반복적으로 동일한 결과를 돌려주는 경우 사용을 고려합니다
  -   사용자가 정보를 서버에 요청했을 경우 서버에서 응답을 해주면서 브라우저 캐시에 저장을하고 동일한 요청을 하면 캐시에 있는 정보를 제공해주며 시간이 지나 캐시에 있는 정보가 만료될경우 다시 서버로 
      요청하여 정보를 받아 브라우져 캐시에 저장해둡니다
</div>
</details>
<details>
<summary>가비지 컬렉션은 무엇이며, 가비지 컬렉션 기능을 가진 언어는 무엇인가요?</summary>
<div markdown="1">
  
  -   자바의 메모리 관리 방법 중 하나로 JVM의 Heap영역에서 동적으로 할당했던 메모리 영역 중 필요 없게 된 메모리 영역을 주기적으로 삭제하는 프로세스 입니다
</div>
</details>
<details>
<summary>트랜잭션에 대해 설명해주세요.</summary>
<div markdown="1">
  
  -   데이터베이스의 상태를 변화시키기 위해서 수행하는 작업의 단위 입니다 
  -   원자성,일관성,독립성,지속성 4가지 특징을 가지고 있습니다
</div>
</details>
<details>
<summary>OAuth 2 인증 시스템과 JWT를 이용한 인증 및 권한 부여 처리 흐름에 대해서 설명해 주세요.</summary>
<div markdown="1">
  
  -   OAuth2의 흐름은 먼저 Resource Owner가 Client 즉, 웹 사이트나 앱등에 로그인 요청을 하게 되면 Client는 Resource Server에 인가 코드를 요청하게 되고 코드를 받으면 다시 코드를 이용해 Access Token과 Refresh Token을 요청하게 됩니다 그럼 Resource Server는 인가 코드를 확인하고 일치하면 토큰을 발급해 줍니다. Client는 Access Token을 Resource Owner에게 넘겨주게 되고 토큰을 이용하여 Resource Server에 있는 Resource Owner의 정보에 접근이 가능하게 됩니다 JWT는 토큰기반 인증 시스템으로 클라이언트가 서버에 접속을 하면 서버에서는 DB와 조회해서 가입된 회원인지를 확인하고 서버측에서 Access Token을 발급해주고 사용자는 서버에 매 요청마다 header에 Access Token을 넣어 요청하게 됩니다 그럼 서버에서는 Token을 검증하고 올바르다면 요청에 응답합니다
</div>
</details>



## Java

<details>
<summary>자바 객체지향 프로그래밍(OOP에 대해 설명해 주세요).</summary>
<div markdown="1">
  
  -   OOP(Object Oriented Programming)이란 문제를 여러 개의 객체 단위로 나워 작업하는 방식으로, 객체들이 서로 유기적으로 상호작용하는 프로그래밍 이론입니다.
      프로그래밍에서 객체란 데이터의 분실을 막기위해 데이터와 기능을 하나로 묶은 그룹을 말합니다 장점으로는 미리 만들어둔 코드를 활용할 수 있기 때문에 재사용성이 증가하고
      생산성 향상이 있습니다. 단점으로는 객체지향적이게 코드를 짜는것이 어려워 코드를 쓰는데 난이도가 높으며 그것에 따라 개발속도가 느립니다.
</div>
</details>
<details>
<summary>클래스와 객체에 대해 설명해주세요.</summary>
<div markdown="1">
  
  -   클래스는 객체를 생성하기 위한 필드와 메소드를 정의하는 것입니다
  -   객체는 클래스로부터 만들어진 글래스의 인스턴스라고 합니다. 클래스로부터 객체를 만드는 과정을 인스턴스화 한다고 합니다
</div>
</details>
<details>
<summary>자바 데이터 타입 중 기본형과 참조형의 차이에 대해 설명해주세요.</summary>
<div markdown="1">
  
  -   boolean, char, byte, short, int, long, float, double 실제 연산에 사용되는 것은 모두 기본형 변수이고 기본형 8가지를 제외한 나머지 타입이 참조형 변수 입니다
</div>
</details>
<details>
<summary>클래스와 객체에 대해 설명해주세요.</summary>
<div markdown="1">
  
  -   클래스는 객체를 생성하기 위한 필드와 메소드를 정의하는 것입니다
  -   객체는 클래스로부터 만들어진 글래스의 인스턴스라고 합니다. 클래스로부터 객체를 만드는 과정을 인스턴스화 한다고 합니다
</div>
</details>
<details>
<summary>메서드 오버라이딩과 메서드 오버로딩의 차이는 무엇인가요?</summary>
<div markdown="1">
  
  -   오버로딩은 자바의 클래스 내에 이미 사용하려는 이름과 같은 이름을 가진 메소드가 있더라도 매개변수의 개수 또는 타입이 다르면 같은 이름의 메소드를 정의할 수 있는 것이고,
  -   오버라이딩은 부모클래스의 메소드를 재정의 하는 것이므로 자식클래스에서 메소드의 이름, 매개변수,리턴값이 모두 같아야 합니다
</div>
</details>
<details>
<summary>static 키워드에 대해 설명하고, static를 언제 사용해야 하는 지 설명해주세요.</summary>
<div markdown="1">
  
  -   오버로딩은 자바의 클래스 내에 이미 사용하려는 이름과 같은 이름을 가진 메소드가 있더라도 매개변수의 개수 또는 타입이 다르면 같은 이름의 메소드를 정의할 수 있는 것이고,
  -   오버라이딩은 부모클래스의 메소드를 재정의 하는 것이므로 자식클래스에서 메소드의 이름, 매개변수,리턴값이 모두 같아야 합니다
</div>
</details>
<details>
<summary>제네릭에 대해서 설명하고, 컬렉션 클래스에서 왜 제네릭을 사용하는 지 설명해주세요.</summary>
<div markdown="1">
  
  -   제네릭은 클래스,인터페이스,메소드 등의 타입을 파라미터로 사용할 수 있게 해주는 역할을 합니다 
      비제네릭 타입의 코드에서 발생하는 불필요한 타입 변환으로 인한 프로그램의 성능의 저하를 감소시킬 수 있습니다. 사용하는 이유는 컴파일 시 타입 체크를 할 수 있습니다 또 타입변환을 제거합니다 

</div>
</details>
<details>
<summary>추상 클래스와 인터페이스의 차이는 무엇인가요?</summary>
<div markdown="1">
  
  -   자바의 특성상 한개의 클래스만 상속이 가능하여 해당 클래스의 구분을 추상클래스 상속을 통해 해결하고, 할 수 있는 기능들을 인터페이스로 구현합니다 인터페이스를 사용해서 기본 틀을 구성한다면 공통으로
      필요한 기능들도 모든 클래스에서 오버라이딩 하여 재정의 해야하는 번거로움이 있습니다 이렇게 공통된 기능이 필요하다면 추상클래스를 이용해서 일반 메서드를 작성하여 자식 클래스에서 사용할 수 있도록 
      하면 된다.  만약 각각 다른 추상클래스를 상속하는데 공통된 기능이 필요하다면 해당 기능을 인터페이스로 작성해서 구현하는게 효율적입니다
</div>
</details>


## Spring

<details>
<summary>DI(Dependency Injection)에 대한 설명과 해당 기술의 장점에 대해 설명해주세요.</summary>
<div markdown="1">
  
  -   DI란 객체를 직접 생성하는게 아니라 외부에서 생성한 후 주입 시켜주는 방식입니다 생성자주입, 필드주입, 수정자주입 등이 있습니다 
      두 객체 간의 관계라는 관심사의 분리를 할 수 있고 객체간의 결합도를 낮춥니다
</div>
</details>
<details>
<summary>Spring MVC에서 REST API 엔드포인트를 구현하기 위해 사용되는 애너테이션들에 대해서 설명해 주세요.</summary>
<div markdown="1">
  
  -   MVC는 Model, View, Controller로 나뉘는데 Model에 사용되는 어노테이션에는 @Entity가 있으며 Controller에는 @Controller나 @RestController 어노테이션을 사용하며 Service 
      계층에는 @Service 어노테이션을, 데이터 엑세스 계층에는 @Repository 어노테이션을 사용합니다
</div>
</details>
<details>
<summary>Controller에서 응답 객체로 사용하는 ResponseEntity에 대해서 설명해 주세요.</summary>
<div markdown="1">
  
  -   httpEntity를 상속받는, 결과 데이터와 HTTP 상태 코드를 직접 제어할 수 있는 클래스입니다 사용자의 HttpRequest에 대한 응답 데이터가 포함 됩니다 httpStatus, httpHeader, httpBody가
      포함되어 있습니다
</div>
</details>
<details>
<summary>DTO가 무엇인지 설명해 주세요.</summary>
<div markdown="1">
  
  -   계층간 데이터 교환을 하기 위해 사용하는 객체로, 로직을 가지지 않는 순수한 데이터 객체입니다
</div>
</details>
<details>
<summary>Spring JDBC, Spring Data JDBC, Spring Data JPA의 차이점을 설명해 주세요</summary>
<div markdown="1">
  
  -   Spring JDBC는 자바로 데이터를 데이터베이스에 CRUD 기능을 해주는 표준 API이고 
  -   Spring Data JDBC는 주로 DDD에 사용됩니다 단방향 매핑만 지원이 되며 미리 작성된 DDL이 필요합니다
  -   Spring Data JPA는 쿼리를 자동으로 생성해주며 테이블과 객체를 매핑하여 사용할 수 있습니다
</div>
</details>
<details>
<summary>Spring에서 트랜잭션을 설정하는 방법에 대해서 설명해 주세요.</summary>
<div markdown="1">
  
  -   @Transactional 어노테이션을 사용합니다. 메소드뿐만 아니라, 인터페이스, 클래스 선언에도 사용할수 있다
</div>
</details>
<details>
<summary>JUnit의 Assertion이 무엇을 의미하는지 설명해 주세요.</summary>
<div markdown="1">
  
  -   테스트가 원하는 결과를 제대로 리턴하는지 에러는 발생하지 않는지 확인할 때 사용하는 메소드를 말합니다 
  -   예를 들면 assertEquals(expected, actual)  -  expected와 actual이 동일하면 True, assertSame동일한 Object면 True 등이 있습니다
</div>
</details>
<details>
<summary>(아직)Spring Boot 기반 애플리케이션 빌드 시, 주로 사용하는 프로파일(Profile)에 대해서 설명해 주세요.</summary>
<div markdown="1">
  
  -   
</div>
</details>
<details>
<summary>(아직)static 키워드에 대해 설명하고, static를 언제 사용해야 하는 지 설명해주세요.</summary>
<div markdown="1">
  
  -   
</div>
</details>
<details>
<summary>스프링MVC에서 예외처리 기법에 대해 설명해주세요</summary>
<div markdown="1">
  
  -   스프링 MVC에서 각 컨트롤러마다 @ExceptionHandler 어노테이션을 이용하여 예외처리를 하고 @ResponseStatus로 응답 상태를 지정해 줄 수 있습니다  하지만 각 컨트롤러마다 똑같은 작업을 반복해야 하는 번거로움과 코드중복이 발생하므로 AOP기법을 이용하여 @RestControllerAdvice, @ControllerAdvice 를 이용하여 공통된 예외처리를 한 번에 수행할 수 있습니다. 또  @ExceptionHandler 에 등록된 예외 클래스와 파라미터로 받는 예외 클래스가 동일해야 합니다 그렇지 않으면 런타임 시점에 에러가 발생할 수 있습니다
</div>
</details>
<details>
<summary>영속성 컨텍스트에 대해 설명해주세요.</summary>
<div markdown="1">
  
  -   영속성 컨텍스트란 엔티티를 영구 저장하는 환경이라는 뜻으로, 애플리케이션과 데이터베이스 사이에서 객체를 보관하는 가상의 데이터베이스 같은 역할을 합니다. 엔티티 매니저를 통해 엔티티를 저장하거나 조회하면서 영속성컨텍스트에 엔티티를 보관하고 관리합니다
</div>
</details>
