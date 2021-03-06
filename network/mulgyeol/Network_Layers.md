# OSI 7 Layers & TCP/IP 4 Layers
><br>
>
> OSI(Open Systems Interconnection) 7 Layers와
> TCP/IP 4 Layers 에 대해 알아보자.
><br>


#### Reference
- [[10분 테코톡] 히히의 OSI 7 Layers](https://youtu.be/1pfTxp25MA8)
- [후니의 쉽게 쓴 CISCO 네트워크](http://www.yes24.com/Product/Goods/89520426)
- [hidaehyunlee velog, "데이터가 전달되는 원리" OSI 7계층 모델과 TCP/IP 모델자](https://velog.io/@hidaehyunlee/%EB%8D%B0%EC%9D%B4%ED%84%B0%EA%B0%80-%EC%A0%84%EB%8B%AC%EB%90%98%EB%8A%94-%EC%9B%90%EB%A6%AC-OSI-7%EA%B3%84%EC%B8%B5-%EB%AA%A8%EB%8D%B8%EA%B3%BC-TCPIP-%EB%AA%A8%EB%8D%B84)
- [네트워크의 기본 'OSI 7계층'](https://daystudy.tistory.com/733)

---

### OSI 7 Layers는 왜 만들어 졌을까?
- 통신에 관한 국제 표준기구 ISO는 통신이 일어나는 과정을 7개로 나누었다.
- 이는 통신을 단계별로 표준화 해서 그 효율성을 높이기 위해 사용되었다.

### 어떻게 효율적이길래?
1. __데이터의 흐름이 한 눈에 보인다.__
    - 우리가 사용하는 애플리케이션 계층부터 제일 하단인 피지컬 계즐까지를 나누어 놓아 어떻게 데이터가 전달되는지 보기 쉽다.
2. __문제를 해결하기 편하다.__
    - 커다란 문제를 한 번에 해결하려고 하다가 오류가 발생한 경우, 우리는 그 오류가 어디서 발생했는지 찾아야 한다. 또, 이 오류를 해결하려고 할 경우 다른 부분과 맞물려 또 다른 오류가 생길지도 모른다. 
    - 그런데 만약 이 커다란 문제를 작은 문제들로 나누어 해결하려고 했다면 오류가 어디서 발생했는지 발견하기도 편하고, 문제를 해결하는 것도 수월할 것이다.
    - 마찬가지로 네트워크 계층을 7개로 나누어 표준화를 하면, 문제를 해결하기가 쉬워진다.
3. __네트워크 장비간 통신이 쉬워진다.__
    - 계층을 나누어 표준화를 하니, 규격에 맞다면 다른 회사의 통신 장비 간에도 데이터의 전달이 원활하게 이루어진다.

---

### 각 계층은 어떤 의미를 지니는가?
><br>
>
> 계층을 나누어 통신이 효율적으로 이루어진다는 것은 이해했다.
> 이제 각 계층이 어떤 역할을 하는지 알아보도록 하자.
><br>

### OSI 7 Layer
<p align="center"><img src="./img/Network_Model/OSI7Layers.png" width = "800px"></p><br>

|계층|역할|
|----|----|
|7. 응용 계층|최종 사용자가 실제로 상호 작용하는 계층이다. 이 계층은 네트워크 리소스에 대한 액세스를 허용한다.|
|6. 표현 계층|데이터로 작동하는 계층이다. 이 계층의 주요 기능에는 데이터 변환, 암호화 및 압축이 포함된다. 기본적으로 사용자는 응용 계층과 상호 작용하여 데이터를 표현 계층으로 보낸다.|
|5. 세션 계층|두 컴퓨터 간의 세션을 설정, 관리 및 종료하여 적절한 통신을 유지하는 역할을 하는 계층이다.|
|4. 전송 계층| 이 계층은 메시지 전달 및 오류 복구를 처리하는 안정적인 프로세스를 제공한다.|
|3. 네트워크 계층|이 계층은 라우터가 작동하는 계층이다. 라우터는 네트워크 수준에서 작동하므로 IP주소가 네트워크 레벨이라고 말할 수 있다.|
|2. 데이터 링크 계층|이 계층은 비트를 프레임으로 구성하는, 스위치가 작동하는 계층이다. 특정 네트워크의 모든 컴퓨터는 서로 통신 할 수 있도록 스위치에 연결된다.|
|1. 물리 계층|이 계층은 데이터 비트의 실제 전송이 매체를 통해 발생된다. 이름에서 알 수 있듯이 컴퓨터를 함께 연결하는 모든 물리적 요소이다.|

### TCP/IP 모델
> OSI 참조 모델은 현재 TCP/IP 모델에게 시장점유율을 빼앗겻고, 
> 현재 실제 사용되는 인터넷 프로토콜은 TCP/IP 모델이다.

### TCP/IP
- TCP/IP는 인터넷 프로토콜 중 가장 중요한 역할을 하는 TCP와 IP의 합성어로 데이터의 흐름 관리, 정확성 확인, 패킷의 목적지 보장을 담당한다. 
- 데이터의 정확성 확인은 TCP가, 패킷을 목적지까지 전송하는 일은 IP가 담당한다.

#### TCP/IP의 4계층
<p align="center"><img src="./img/Network_Model/model.png" width = "800px"></p><br>

TCP/IP는 OSI 참조 모델과 달리 표현계층, 세션계층을 응용계층에 다 포함시키고 있지만, 사실상 TCP/IP Model의 Application 계층 하나에서 Application, Presentatiom, Session 계층의 구현을 하고있다.

### TCP/IP의 계층간 데이터 전달
- 데이터는 아래 그림과 같이 단계 별로 헤더(Data → Segment → Datagram → Frame)를 붙여 전송한다.
<p align="center"><img src="./img/Network_Model/TCP_IP_4Layers.gif" width = "800px"></p><br>

### TCP/IP 4계층의 계층 간 역할
|계층|역할|데이터 단위|
|----|----|----|
|4. 응용 계층|응용프로그램 간의 데이터 송수신|Data/Message|
|3. 전송 계층|호스트 간의 자료 송수신|Segment|
|2. 인터넷 계층|데이터 전송을 위한 논리적 주소 지정 및 경로 지정|패킷|
|1. 네트워크 연결 계층|실제 데이터 프레임을 송수신|MAC|

### 결론
- TCP/IP 프로토콜은 OSI 모델보다 먼저 개발되었다. 그러므로 TCP/IP 프로토콜의 계층은 OSI 모델의 계층과 정확하게 일치하지 않는다.
- 두 모델 모두 계층형 이라는 공통점을 가지고 있으며 TCP/IP는 인터넷 개발 이후 계속 표준화되어 신뢰성이 우수인 반면, OSI 7 Layer는 표준이 되기는 하지만 실제적으로 구현되는 예가 거의 없어 신뢰성이 저하되어있다.
- OSI 7 Layer는 장비 개발과 통신 자체를 어떻게 표준으로 잡을지 사용되는 반면에 실 질적인 통신 자체는 TCP/IP 프로토콜을 사용한다.