# TCP socket :rocket:

파이썬에서 TCP(Transmission Control Protocol)를 사용하려면 소켓타입을 `socket.SOCK_STREAM`으로 지정하고 `socket.socket` 함수로 소켓 객체를 생성하면 된다.

### TCP란?
한쿡말로 전송제어 프로토콜

- 서버와 클라이언트간에 데이터를 신뢰성있게 전달하기 위해 만들어진 프로토콜
- 데이터를 전송하기 전에 전송을 위한 연결을 해주는 것에 focus!
- 네트워크선로를 통해 전해지는 데이터들의 손실을 TCP에서 잡아내어, 교정하고 순서를 다시 맞춰줌
    - 수신자가 전달 받지 못한 패킷을 감지하여 재전송해줌!
    - 발신자가 전송한 순서대로 수신가능!



<img src="https://lh3.googleusercontent.com/v8W3gqDs1Dq00WqAjs9DjXOBul8qmn1X3jAL0TA4dcX9SsRg_6s2tQX1RGOm3pAvH6vJtF5_hxKGVRuzl8zzRNHdPOQB7EH10GbUVHc4u9FCrqz0_UR8x1wNgr3NVkIKs1k7LDlF" align="center">

### 소켓통신 순서
socket() 
bind()
listen()
accept()
순으로 함수들을 호출하여 리스닝 소켓을 생성

리스닝 소켓은 클라이언트의 접속을 대기하는 역할을 수행

---

클라이언트가 연결되면 accept()에서 새로운 소켓을 리턴하여 클라이언트와 통신시 사용 

---

클라이언트는 connect 함수를 호출하여 서버에 연결을 시도합니다. 

이때부터 3-way 핸드세이크를 시작합니다. 

핸드 세이크는 네트워크를 통해 양쪽이 연결되는 것을 보장하므로 중요합니다. 클라이언트가 서버에 도달할 수 있으며 그 반대도 마찬가지입니다. 

* `3-way 핸드세이크`
    - 목적 : 순번을 동기화, 연결의 양측에서 순번을 확인하고 TCP윈도우의 크기를 교환하고 최대 세그먼트 크기와 같은 기타 TCP옵션을 교환하는 것

--- 

연결이 완료된 후, 서버와 클라이언트는 send 함수와 recv 함수를 호출하여 데이터를 주고 받습니다. 

---

클라이언트가 연결 종료 메시지를 전송하거나 소켓을 닫으면 서버는 클라이언트와 통신을 위해 사용한 소켓을 닫습니다.





