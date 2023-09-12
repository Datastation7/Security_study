# 애플리케이션 보안
- 프로토콜 110번 포트
  - 와이어샤크(WireShake) 프로그램을 이용하여 POP3 트래픽을 점검할 때 프로토콜 110번 포트를 검색한다.
  - POP3는 Mail Box에서 자신의 메일을 읽어오는 프로토콜로 110번 포트를 사용한다.
  - 메일을 읽은 후 Mail Box에서 해당 메일은 삭제된다.

- 프로토콜 143번 포트
  - IMAP이 사용하고 IMAP은 Mail Box에서 메일을 읽어도 삭제되지 않는다.

- 프로토콜 25번 포트
  - SMTP가 메일을 발송할 때 사용하는 포트 번호

- `버퍼 오버플로 취약점 대비`
  - `경계값을 검사하는 API를 사용해야 한다.`
  - `strncat, snprintf, strncpy 함수는 길이 값을 검사한다.`

- 웹쉘(WebSehell)
  - <% eval request("cmd") %> 문장이 포함된 ASP 스트립트가 존재하는 것
  - ASP의 eval 함수는 코드를 동적으로 구성하여 실행할 수 있는 함수
  - cmd로 입력되는 스크립트를 실행
  
- SET(Secure Electronic Transaction) 프로토콜
  - SET은 이중서명을 지원하기 때문에 구매자 정보와 판매자 정보를 분리해서 전자서명한다.
  - 따라서 상인에게 지불정보(카드번호)가 노출되지 않는다.

- SET(Secure Electronic Transaction) 프로토콜 단점
  - 암호 프로토콜이 너무 복잡하다.
  - RSA 동작은 프로토콜의 속도를 저하시킨다.
  - 지불 게이트웨이에 거래를 전자적으로 처리하기 위한 별도의 하드웨어와 소프트웨어를 요구한다.

- SSO(Single Sign On)
  - 일회 인증만으로 추가 인증없이 여러 시스템과 서비스를 이용할 수 있게 하는 인증 서비스

- 데이터베이스 보안 유형
  - 접근 제어, 허가 규칙, 가상 테이블은 보안 기법에 해당
  - 가상 테이블은 특정 칼럼만을 보여주게 하기 때문에 보안 유형에 해당

- DRM(Digital Rights Management)의 구성요소 - 콘텐츠(Contents)
  - 지적재산권으로 보호되어야 할 정보의 단위로 일반적으로 패키저를 통해 패키징 되기 이전의 원본을 의미
  - 원본 저작권자가 만든 디지털 산출물로 패키저를 통해서 패키징하여 배포된다.

- `CSRF 토큰`
  - `웹 브라우저(HTML)에 Hidden필드에 세션 이외의 추가 인증인 CSRF토큰을 저장하고 서버 호출 시에 CSRF토큰을 전달하여 추가 인증한다.`
  - 웹은 URL 기반으로 요청을 처리하는 구조
  - 해당 요청이 특정 사용자의 정상적인 요청인지를 구분하기 위해 사용자가 작업 페이지를 요청할 때마다 hidden값으로 클라이언트에게 토큰을 전달한 뒤 해당 클라이언트의 데이터 처리 요청 시 전달되는 값과 세션에 저장된 값을 비교하여 유효성을 검사한다.

- CAPTCHA 
  - 정상적인 사용자 호출인지 프로그램(Agent)에 의한 호출인지를 구별하기 위한 것

- NGFW(Next Generation Firewall)
    - UTM, DLP, SLL, Inspection, SSL VPN, Anti APT 등 다양한 기능을 통합해 지원하며 Layer 7까지 제어하고 암호화 트래픽 제어 가능한 보안 시스템
    - 포트, 포로토콜뿐만 아니라 애플리케이션 레벨까지 검사를 수행

- DRM(Digital Rights Management)
    - 디지털 콘텐츠의 무단 복제 및 사용을 막고 원자자의 권리와 이익을 보호해 주는 기술과 서비스를 의미

- HTTP Request Message(HTTP 요청 메시지)를 구성하는 순서
  - Request Line -> Header -> Black Line -> Body

- FTP Bounce Attack
  - 익명 FTP 서버를 이용해 그 FTP 서버를 경유해서 호스트를 스캔
  - FTP PORT 명령을 이용
  - FTP 서버를 통해 임의의 네트워크 접속을 릴레이한다.
  - 네트워크를 포트 스캐닝하는데 사용하는 공격
  - FTP가 명령 전송 포트와 데이터 전송 포트가 분리된 약점을 이용한다.

- `소프트웨어 보안 취약점 중 입력 값 검증 및 표현하는 것`
  - `SQL 인잭션, 경로 조작 및 자원 삽입, 위험한 형식의 파일 업로드`

- DNS 서비스를 위해 BIND 설치 시 관련이 있는 것
  -  /etc/named.conf, /etc/named.iscdlv.key, /etc/named.rfc1912.zones
  -  DNS 서버의 설정 파일은 named.conf 파일
  -  관련 프로세스의 이름은 named

- XML 디지털 서명의 유형

|유형|설명|
|:----|:----|
|Enveloping Signature|데이터가 Signature 구조 내에 존재한다.|
|Enveloped Signature|데이터가 밖에서 Signature 구조를 포함한다.|
|Detached Signature|데이터가 밖에서 있으며 Signature 구조를 포함하지 않는다.|

- 전자투표 시스템이 가져야 할 암호 기법
  - 공개키/개인키를 이용한 암호화 및 복호화
  - 전자서명(Digital Signature)
  - 은닉암호

- DB 보안 통제 방법
  - 흐름 통제, 추론 통제, 추론 통제, 접근 통제, 허가 규칙, 가상 테이블, 암호화가 있다. 

- 흐름 통제
  - 높은 수준의 권한을 가진 사용자들만이 접근할 수 있는 정보를 낮은 수준의 권한을 가진 사용자들이 접근할 수 있는 객체에 저장되어 있을 경우 DB보안의 흐름통제를 위반하는 것
  - 접근 가능한 객체 간의 정보 흐름을 조정하는 것

-  추론 통제
   -  간접 접근을 추론을 통제한다.

- 웹 응용 프로그램에서 운영체제 명령어 삽입 취약점이 존재할 경우 사용할 수 있는 특수문자를 사용한 명령어 조합
  - pwd;ls -al
    - pwd명령과 ls명령이 순차적으로 실행된다.

  - pwd | ls -al
    - pwd명령이 실패해야 ls -al명령이 실행된다.

  - ls -al | more
    - ls명령의 결과값을 more명령의 입력 값으로 사용한다.

- SMTP 서버의 릴레이 기능 제한 여부 점검
  - vi편집기를 이용하여 sendmail.cf 설정 파일을 열어 아래와 같이 주석을 제거한다.
    - RS $%error $@ 5.7.1 $ : "550 Relaying denied"
  - /etc/mail/access에 특정 IP, Domain, Email Address 및 네트워크에 대한 Sendmail 접근 제한을 확인한다.
    - localhost.localdomain RELAY
    - localhost RELAY
    - 127.0.0.1 RELAY
    - Spam.com REJECT
  - 수정했거나 생성했을 경우 makemap 명령으로 DB파일을 생성한다.
    - #makemap hash /etc/mail/access.db < /etc/mail/access

  - 메일 서버로 접근하는 호스트나 도메인의 접근을 통제하는 파일로 허가할 호스트나 도메인은 통과(RELAY)하고 거부하려면 REJECT 혹은 DISCARD를 한다.
    - /etc/mail/access  

- 포렌식의 기본 원칙
  - 정당성의 원칙
    - 모든 증거는 적법한 절차를 거쳐서 획득한 것이어야 한다.
    - 위범한 절차를 거쳐 획득한 증거는 증거 능력이 없다.
  - 재현의 원칙
    - 법정에 증거를 제출하려면 똑같은 환경에서 같은 결과가 나오도록 재현할 수 있어야 한다.
  - 신속성의 원칙
    - 컴퓨터 내부의 정보는 휘발성을 가진 것이 많아서 신속하게 이루어져야 한다.
  - 무결성 원칙
    - 수집된 증거가 위변조됮 않았는지?
    - 일반적으로 해시 값을 이용하여 수집 당시 저장 매체의 해시 값과 법정 제출 시 저장 매체의 해시 값을 비교하여 무결성을 입증해야 한다.


