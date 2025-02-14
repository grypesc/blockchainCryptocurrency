# 블록체인 기반 학교 재정장부 자동 관리 시스템

**기존시스템의 문제점:** 학생회비의 사용내역이 실시간으로 확인이 불가능하여 부정부패의 위험이 있으며, 회비 관리자의 인계 과정이 번거롭다는 문제점이 있다.

**시스템의 목표:** 블록체인 기반 재정 관리 시스템의 목표는 학생회비가 어떤 방식으로 관리되고 있는지 추적이 가능한 것이다. 
학생들이 모든 사용내역을 확인하기 쉬워야하며, 데이터 관리에 있어서 보안성이 뛰어나야 한다.


**1. 블록체인**


각각의 블록은 하나의 트랜잭션에 대한 정보로 구성된다: <br>
  -회비 사용자<br>
  -거래 번호<br>
  -거래 일자<br>
  -거래 금액<br>
  -잔고<br>
  -거래 장소<br>
  -거래 유형<br>
  -다음 블록<br>
  -이전 블록의 해쉬<br><br>
  
**2. 웹 어플리케이션**


 우리는 두가지의 웹 어플리케이션을 개발한다.<br><br>
 - 트랜젝션을 일으키는 어플리케이션(코인을 전송)
 - 거래 내역을 확인할 수 있는 어플리케이션
 
**2-1. 트랜젝션 프로세스**


  개인 사용자는 각자의 지갑을 가지고 있다. 개인이 트랜젝션을 발생시키고 싶다면, 코인을 받는 수신자(이하 수신자)가 스마트폰으로 QR 코드를 생성한다. 그리고 그것을 코인을 보내는 송신자(이하 송신자)에게 보낸다. 송신자가 QR 코드를 스캔하면, 수신자의 지갑 주소를 받을 수 있고 동시에 웹 어플리케이션으로 연결된다. 전송 버튼을 누르면 트랜젝션이 발생한다.
  
  
**2-2. 트랜젝션 기록 조회**


 웹 어플리케이션에서 web3를 통해 트랜젝션 기록을 조회할 수 있다. 우리는 학생회비를 사용하는 특정 공인들의 지갑 주소(학생회 임원)를 그들의 이름과 맵핑하여 모든 코인 트랜젝션 기록중에 학생회비 사용 내역만 따로 불러올 수 있다.
 
 
**3. 노드 구성**


**3.웹 어플리케이션**

거래 완료 후, 학생회는 서버에 영수증 스캔본을 업로드한다. 웹 어플리케이션은 블록체인으로부터 정보를 받아 모든 학생들이 거래내역을 조회할 수 있도록 한다. 새 블록이 생기면 모든 이전 블록들을 증명해야하며, 증명을 성공하면 새 블록체인이 완성되며 학생들은 이를 웹 어플리케이션에서 조회 가능하다.<br><br>

 
 
 
**4.학생의 웹 어플리케이션**


블록 체인을 저장하고 새 블록을 확인한 다음 다운로드한다. 새로운 블록 체인과 저장된 블록간에 차이가 있을 경우 웹 어플리케이션은 사용자에게 경고를 표시하고 학생회에 연락할 수 있도록 해야한다. 또한, 학생회의 거래 내역에 대한 불만이 있을 경우 게시판에 이의제기를 할 수 있도록 한다.<br><br>

