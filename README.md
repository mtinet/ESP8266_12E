# ESP8266_12E(NodeMCU 1.0)
---
* ESP8266_12E 사용 준비  
---
1. NodeMCU 1.0모듈을 usb케이블을 이용해 컴퓨터와 연결하면 잠시 후 장치관리자가 알아서 드라이버를 설치하고 포트를 잡는다. 포트가 안잡힐 경우 CP2102 usb driver를 검색해서 설치한다.  
2. 아두이노 IDE를 열고 파일 - 환경설정 - 추가적인 보드 매니저 URLs에 http://arduino.esp8266.com/stable/package_esp8266com_index.json 를 붙여 넣는다.  
3. 툴 - 보드매니저를 열고 'esp8266 by ESP8266 Community'를 클릭한다.   
4. '설치' 버튼을 눌러 해당 보드를 설치한다.   
5. 설치가 완료되면 파일 - 예제에 ESP8266관련 예제가 생성된다. 이 때 예제 옆의 ()안에 esp8266이라고 써 있는 예제는 기존의 아두이노에서 적용할 수 없게 된다.   
6. 툴에서 보드는 NodeMCU 1.0(ESP-12E Module), CPU Frequency는 80MHz, Flash Size는 4M(3M SPIFFS), Upload Speed는 115200으로 자동 세팅되는데, 그대로 사용하면 된다. 포트는 해당 모듈이 연결된 포트를 장치관리자 - 포트를 확인하여 선택한다.  

---
* 와이파이 웹서버 테스트  
---
1. 아두이노 IDE의 파일 - 예제 - ESP8266WiFi - WiFiWebServer를 선택한다.  
2. 와이파이 SSID와 PW를 수정한다.   
3. 업로드한다.   
4. 시리얼 모니터를 누르면 다음과 같이 ip주소가 나온다.   
Connecting to mtinet  
.....  
WiFi connected  
Server started  
192.168.43.***   

5. ESP8266_12E 모듈이 접속해 있는 공유기에 접속된 다른 모듈을 통해 해당IP/gpio/0으로 접속하면 자체 칩 LED가 켜지고 해당IP/gpio/1으로 접속하면 자체 칩 LED가 꺼진다.   
6. HTML 부분을 원하는대로 편집한다.(이미지 링크도 잘 됨.)  


//관련 동영상은 아래 사진을 클릭하세요.  
[![](https://raw.githubusercontent.com/mtinet/ESP8266_12E/master/image.png)](https://www.youtube.com/watch?v=vwJoXQwv7AI)
