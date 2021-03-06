Session 과 Cookie 사용 이유
: 현재 우리가 인터넷에서 사용하고 있는 HTTP프로토콜은 연결 지향적인 성격을 버렸기 때문에 새로운 페이지를 요청할 때마다 새로운 접속이 이루어지며 이전 페이지와 현재 페이지 간의 관계가 지속되지 않는다. 이에 따라 HTTP 프로토콜을 이용하게 되는 웹 사이트에서 웹페이지에 특정 방문자가 머무르고 있는 동안에 그 방문자의 상태를 지속시키기 위해 쿠키와 세션을 이용한다.

- Session
  * 특정 웹사이트에서 사용자가 머무리는 기간 또는 한명의 사용자의 한번의 방문을 의미한다.
  * Session 에 관련된 데이터는 Server에 저장된다.
  * 웹 브라우저의 캐시에 저장되어 브라우저가 닫히거나 서버에서 삭제시 사라진다.
  * Cookie에 비해 보안성이 좋다.

- Cookie
  * 사용자 정보를 유지할 수 없다는 HTTP의 한계를 극복할 수 있는 방법
  * 인터넷 웹 사이트의 방문 기록을 남겨 사용자와 웹 사이트 사이를 매개해 주는 정보이다.
  * Cookie는 인터넷 사용자가 특정 웹서버에 접속할 때, 생성되는 개인 아이디와 비밀번호, 방문한 사이트의 정보를 담은 임시 파일로써, Server가 아닌 Client에 텍스트 파일로 저장되어 다음에 해당 웹서버를 찾을 경우 웹서버에서는 그가 누구인지 어떤 정보를 주로 찾았는지 등을 파악할 때 사용된다.
  * Cookie는 Client PC에 저장되는 정보기 때문에, 다른 사용자에 의해서 임의로 변경이 가능하다.

Q! 보안성이 낮은 Cookie 대신 Session을 사용하면 되는데 안하는 이유?
 - 모든 정보를 Session에 저장하면 Server의 메모리를 과도하게 사용하게 되어 Server에 무리가 간다. 