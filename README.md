# DTISAdvancementProject(국방수송정보체계 고도화 프로젝트)
* 2021.09 ~ 2023. 04

## 0_개요
국방수송정보체계 고도화 프로젝트를 참여한 저의 개발일기입니다. 국방 CBD방법론에 따라 분석-설계-개발-테스트-전력화 단계에 따라 개발이 진행됩니다. 
저는 설계단계부터 참여를 하였습니다. 각 단계에 필요한 산출물 및 개발 과정에 대한 내용을 작성하며, 느낀 점과 어려움에 대해 작성해 나갈 것입니다.

## 1_개발환경
  * OS : window 10
  * 개발언어 : java, JavaScript
  * DB : 티베로(Tibero)
  * 프레임워크 : Spring, Mybatis
  * 형상관리 툴 : SVN(SubVersioN)
  * UI : 넥사크로
  * 배치프로그램 : JOB-PASS
  * 품질 : Sparrow
  * 기타 : 잡패스(JOB-PASS)

## 2_개발일지

#### 연동통제문서(ICD) 
 * KB손해보험정보체계
 * KTX특송정보체계
 * 국방군수통합정보체계
 * 국방수송정보체계
 * 국방인사정보체계
 * 국방증명서통합발급체계
 * 국방통합재정정보체계
 * 수서고속철도통합정보체계
 * 제주항공정보체계
 * 티웨이항공정보체계
 * 하이에어정보체계
 * 한진택배정보체계

  ### 2022.12.26 ~ 2022.12.30
  * TRR(Test Readiness Review-시험 준비 검토) 2차 평가 준비
 #### 느낀점: 2023.01.04부터 TRR 2차 평가 일정이 잡혔다. TRR을 준비했던 사항은 다음과 같다. 첫째. 시나리오 수정이다. TRR 1차 평가 결과 반영에 따라 기능이 수정 및 추가가 되었으므로 이에 따라 시나리오 수정을 하였다. 둘째. TRR 1차 때 나온 오류사항 재검토이다. TRR 1차 평가때 나온 오류 및 버그 사항을 다시 테스트 해봄으로써 같은 사항이 2차때 걸리지 않도록 점검하였다. 셋째. 요구사항 반영 점검이다. 사용자가 요구했던 요구사항 중 일부 건들이 제대로 반영되어 있는지 체크하였다. 이 외에도 계속 내부 테스트를 진행하면서 점검을 하였다. 무사히 TRR 2차 평가를 무사히 마쳤으면 좋겠다.

  ### 2022.12.05 ~ 2022.12.23
  * TRR(Test Readiness Review-시험 준비 검토) 1차 검토 결과 반영 
 #### 느낀점: TRR 1차 테스트가 끝이났다. 생각치도 못한 오류가 많이 발견되었으며 오류는 아니지만 수많은 요구사항들이 나왔다. 오류에 대해서는 큰 건은 없어서 금방 수정할 수 있었지만 문제는 요구사항이다. 전력과까지 얼마남지 않았기 때문에 모든 요구사항을 수용한다면 일정에 차질이 생기기 때문이다. 그래서 각 업무에서 나온 요구사항들을 정리해서 나, 차장님, TF담당자 3명이 모여서 요구사항에 대해 수용여부를 결정하였다. 나 역시 요구사항을 최대한 들어주고 싶지만 시스템 구조를 뒤바꿔야하는 요구사항과 이러한 요구사항이 요구사항정의서에 없었던 내용이라면 수용하기 어렵다는 의견을 밝혔다. 하지만 대부분의 요구사항은 큰 어려움이 없는 것들이었고 간단한 내용들이라 대부분은 수용하였다. 그래서 이 기간동안 오류에 대해서는 수정을 하고 수정 결과를 증적으로 남겼고, 요구사항 반영건에 대해서는 최대한 반영을 하고 반영된 결과를 증적으로 남겼다. 그리고 결함수정과 요구사항이 반영된 결과를 TF담당자에게 보여주었고 모두 처리가 되었음을 확인받았다. 이렇게 해서 TRR1차가 끝이 났다. 아직 다른 팀들은 곗곡 수정 중이라 아마 모든 팀들이 다 끝나면 TRR2차가 진행될 것 같다.
 
   ### 2022.11.07 ~ 2022.12.02
  * TRR(Test Readiness Review-시험 준비 검토) 1차 테스트 준비 및 진행
 #### 느낀점: TRR 1차 테스트를 진행하였다. 각군에서 실제로 업무를 사용하는 담당자들을 초대해서 테스트를 진행하였다. 나의 경우는 운전자력과 군전세객차를 실제로 담당하는 담당자는 총 10명이였다다. 담당자들이 테스트를 하니까 생각치도 못한 문제와 요구사항들이 나왔다. 예를 들어 운전자력 업무 중 교육생 교육 성과 정보를 조회/입력하는 화면이 있다다. 기존에는 교육생을 한명씩 일일이 눌러서 교육 성과(교육시간, 교육거리, 교육등급)를 입력해야 했으나 담당자 의견으로는 교육 성과 정보는 대부분 같으므로 일괄로 입력해달라는 요구사항을 확인하였다. 그래서 일괄입력하고자 하는 교육생들을 체크하고 [성과 일괄 입력]버튼을 클릭하면 팝업창이 나타나 성과를 입력하고 [적용]버튼을 누르면 체크된 교육생들에게 성과가 일괄 적용되는 기능을 추가로 개발하였다. 비록 이러한 점은 분석단계에서 조사하였던 요구사항정의서에서는 포함되지 않았지만 실제 업무에서 꼭 필요한 기능이나 편의기능을 요구한다면 사용자의 니즈의 맞춰서 최대한 맞추고자 노력을 했다.

   ### 2022.10.31 ~ 2022.11.04
  * 상호운영 평가, 통합 테스트 
 #### 느낀점: 타 체계와의 연동을 위해 테스트를 하였다. 예를 들어 KB보험정보체계와 송신 8건 수신 3건을 해야하는데 잡패스를 통해 매일 10시, 16시에 배치가 돌아가면서 WAS서버 지정된 경로에 배치 결과 파일을 떨궈준다. 그 이후 보험체계에서 떨궈준 파일을 읽고 수송정보체계에 송신을 하는 방식이다. 송신은 성공적으로 끝냈으나 수신을 테스트 하던 중 한글에 깨져서 수신이 되었다. 이유를 살펴보니 보험체계에서는 EUC-KR 방식으로 보내주었으나 우리 체계는 UTF-8방식으로 글자를 읽어 한글이 깨진 채로 수신이 되었다. 그래서 수신 방법을 EUC-KR 방식으로 수정하고 빌드요청을 드려 해결하였다. 그리고 통합 테스트가 진행되었다. 외부 인원이 오기 전 TF에서 전체적인 기능을 테스트하고 수정사항을 정리하여 보내주었다. 분명 내가 테스트를 진행할 때는 오류가 안났었는데 남이 테스트를 할때 오류가 나는 것 보니까 테스트를 좀 더 꼼꼼히 해야겠다는 생각이 들었다.
 
  ### 2022.10.10 ~ 2022.10.28
  * 운전자력, 군전세객차 연동, 내외부, 배치프로그램 개발, 군전세객차 배정 프로그램 개발
 #### 느낀점: 드디어 군전세객차의 핵심 기능은 배정 프로그램 개발을 하였다. 배정 프로그램이란 신청자들이 열차에 출발역, 도착역을 입력하고 예약신청을 하면 배치프로그램을 통해 각 신청자들의 우선순위 점수를 매겨서 좌석을 배치하는 프로그램이다. 이때 점수에 영향을 주는 항목이 계급, 별거간부, 신청일시분초, 탑승점수, 위규점수가 있으며 이러한 점수를 다 따져가면서 좌석을 배치해야하는 프로그램이다. 이러한 프로그램에서 오류가 난다면 사용자들이 군전세객차를 이용하는데에 큰 불편함이 있기 때문에 개발을 하는데 심혈을 기울여 개발을 하였다. 예를 들어 A는 총점이 150점이고 B의 총점은 145점인데 A는 배정을 못받고 B가 배정을 받으면 안되기 때문이다. 사용자들이 배정결과를 볼 수 있기 때문에 오류가 나면 항의가 많이 들어온다고도 하였다. 개발이 끝나고도 오류를 찾아내기 위해 어려가지 상황을 놓고 다양하게 테스트를 진행하였다.
 
   ### 2022.9.26 ~ 2022.10.07
  * 운전자력, 군전세객차 연동, 내외부, 배치프로그램 개발
 #### 느낀점: 외부 체계와의 연동을 위한 프로그램을 개발했다. 연동방법은 DB TO DB 방법과 FILE TO FILE 방법으로 나뉜다. 수신방법은 다음과 같다. 3분 간격으로 잡패스를 통해 배치 프로그램을 돌려 인터페이스 테이블에 데이터를 확인하거나 지정된 경로에 파일을 확인하여 데이터를 INSERT 한 뒤 인터페이스 테이블의 수신확인을 Y로 바꾸거나 확인된 파일을 old 파일로 이동시키는 방법이다. 송신방법은 다음과 같다. 예를 들어 증명서체계에서 들어온 경력확인서 신청건을 DTIS 내부 체계에서 결재승인이 이루어 지면 해당 데이터를 인터페이스 테이블에 INSERT 하거나 지정된 경로에 파일을 만드는 방식으로 개발했다. 앞으로 해야할 일은 개발된 연동프로그램을 지정된 날짜에 외부 체계와의 연동 테스트를 성공적으로 마쳐야 한다.
  
   ### 2022.9.19 ~ 2022.9.23
  * 운전자력, 군전세객차 연동, 내외부, 인터페이스 테이블 업무, 배치프로그램 개발
 #### 느낀점: DTIS체계에서 사용하던 DB를 외부와 연동하거나 혹은 외부에서 INSET된 DB를 DTIS체계로 불러와야 했다. 또한 DTIS체계에 있는 DB를 인터넷 DB와 연동을 해야했다. 방법은 다음과 같다. 1. 송신방법: DTIS체게에 있는 테이블을 인터페이스 테이블의 형식에 맞게 INSERT를 한다 이때 연동관련 컬럼이 존재해서 외부에서 송신된 데이터를 가져가면 송신여부가 Y로 바뀌게 된다. 2. 수신방법: 외부 혹은 인터넷 체계에서 인터페이스 테이블의 형식에 맞게  INSERT를 하면 DTIS에서 인터페이스 테이블 데이터를 가져가는 방법이다. 이때 송/수신을 주기적으로 했어야 했다. 예를 들어 인터넷의 운전경력확인서 신청을 DTIS체계로 송신하면 DTIS체계에서 결재하고 승인을 하게 되면 인터넷 체계에서 경력확인서를 인쇄할 수 있다. 그런데 이러한 송/수신 주기는 매일했어야 했으므로 송/수신 코드를 잡패스에 올려서 매일 0시에 코드가 돌아가도록 개발을 하였다. 
 
  ### 2022.8.29 ~ 2022.9.16
  * 운전자력, 군전세객차 모바일 화면 개발 및 통합테스트 진행
 #### 느낀점: DTIS체계에서 개발분량이 완료되었다. 그러나 추가적으로 모바일 개발이 필요했다. 운전자력의 군운전경력확인서와 군전세객차의 군전세객차 신청 화면이였다. DTIS는 국방망 인트라넷에서만 접속이 가능하지만 모바일은 외부 인터넷에서도 접속이 가능하다. 개발하면서 어려웠던 점은 DTIS는 넥사크로 UI툴이 있었지만 모바일은 UI툴이 따로 없고 HTML/CSS/JS로만 개발을 해야했다. 그래서 오랜만에 내가 개발한 일기를 보거나 검색을 하면서 개발을 했다. 또한 DB와의 연결은 새로 개발해야했기 때문에 JQuery와 ajax를 활용하여 오퍼레이션을 불러와 개발을 하였다. 확실히 UI툴을 사용하다가 순수 HTML/CSS/JS로 화면을 개발하려다 보니 코드도 조금 복잡해지고 까다로웠다. 
 
 ```C
 http://www.dtis.mil.kr/internet/m/index.public.jsp
 ```
![Image 1](https://user-images.githubusercontent.com/82793713/192143277-29507dbd-598a-49c3-bb3a-9fd3083c0713.png)
![Image 2](https://user-images.githubusercontent.com/82793713/192143349-49519bad-1105-41da-a4e7-12d793fd6776.png)
![Image 3](https://user-images.githubusercontent.com/82793713/192143377-d937e42d-1ebc-4191-afb2-de2b57e3f6f5.png)
 
 ### 2022.8.8 ~ 2022.8.26
 * 운전자력, 군전세객차 단위테스트, 시나리오 작성
#### 느낀점: 나에게 주어진 1차적인 개발 분량이 어느정도 끝이 나간다. 솔직히 말해서 나의 개발속도가 조금 빨라서 나의 분량을 미리 끝내고 다른 팀원들의 부족한 개발부분을 내가 개발을 하였다. 그래서 차장님이 매달 상여금 50만원을 나에게 주셨고 나는 이에 힘을 입어 다른 팀원들의 개발분량도 열심히 도왔다. 그러단 와중 구현단계에서의 산출물을 해야했다. 단위테스트와 시나리오 작성이였다. 설계단계에서 작성했던 컴포넌트명세서에 따라서 실제로 오퍼레이션이 테스트 된 적이 있는지, 단위 기능들이 정상적으로 작동하고 있는지 등 스스로 테스트를 해서 산출물에 반영을 해야했다. 실제로 개발을 하다보니 설계단계에서 설계했던 것과 구현단계에서 구현했던 결과물이 많이 달랐다. 그래서 구현물에 맞춰 설계단계의 산출물들을 조금씩 수정을 해가며 산출물들을 작성했다. 물론 설계를 할 때에 추후에 구현이 끝나면 작성한 산출물들을 수정을 하겠지라는 생각은 하였지만 나의 예상보다 너무 많은 수정.. 아니 거의 새로 산출물들을 다시 만들어야 하는 수준이다. 예를 들어 면허시험을 신청할 때에 단순히 신청서만 저장할 줄 알았지만 실제 결과물은 신청서 저장과 함께 신청서 정보를 토대로 운전자력기록부를 생성 혹은 수정을 하는 기능이 필요했다. 그래서 이를 반영해 산출물을 수정해야했고, 기존에 기획했던 화면과는 너무 달라져서 분석단계의 사용자인터페이서명세서를 새롭게 작성을 해야했다. 




### 2022.7.18 ~ 2022.8.5
 * 운전자력 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
#### 느낀점: 운전교육생 관련 기능을 개발하였다. AS-IS에는 없던 TO-BE 체계에서 새로 생겨난 기능이라 DB구조부터 시작해서 처음부터 끝까지 새롭게 구현해야했던 기능중 하나이다. 처음 계획하였을 때에는 분석단계의 요구사항에 맞게 심플하게 구현계획을 하였고 이를 실제로 사용하는 교육단에 보여주었다. 그러더니 교육단에서는 이렇게 계획하면 개발을 하나마나라면서 쓸 수가 없을 뿐더러 교육단에서 일을 두 번 하게 될 수 있다고 하였다. 분석 단계에서 사용자의 요구사항이 잘 반영되었어야 했으나 그 당시의 사용자들도 어떤 기능이 있어야 하는지 정확하게 정립을 하지 못하였다고 한다. 예를 들어 기존 개발 계획에서는 단순히 교육 계획을 CRUD하는 수준에 그쳤지만 교육단에서는 교육계획에 교육생들을 등록하여 해당 수업에 어떤 교육생들이 수업을 들었는지 알 수 있게 해야한다고 하였다. 그래서 교육단의 의견을 들어 처음부터 다시 DB를 설계하고 화면구성을 변경하여 새롭게 개발을 하였다. 이를 통해 어떤 기능을 개발할 때에는 사용자의 의견을 정확하게 이해를 하고 반영을 해야겠다고 생각했다.


### 2022.7.4 ~ 2022.7.15
#### 개발화면 (92/109), Service(45(+6)/51), Controller(45(+6)/51), Report(0/21), 개발해야할 Operation: 314개
 * 운전자력 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
#### 느낀점: 사진을 업로드하고 올린 사진을 웹에서 볼수 있는 공통기능을 개발하였다. 물론 파일을 업로드 하는 기능은 공통쪽에서 개발을 하였으나 올린 사진을 웹에서 보는 기능은 아직 개발되어 있지 않아서 내가 개발을 하였다. 개발 방법은 다음과 같다. 첫째. 리눅스 서버에 사진 파일이 올라간 경로를 쿼리를 통해 얻는다. 둘째.해당 경로를 서버로 보내 해당 파일을 base64형태로 받는다. 셋째.base64의 데이터를 사진으로 변환하여 화면에 표현해준다. 이러한 기능은 수송근무 뿐만이 아니라 다른 업무쪽에서 많이 쓰일 것 같아서 다같이 공통으로 쓸 수 있도록 코드를 작성하였다.

### 2022.6.27 ~ 2022.7.1
#### 개발화면 (92/109), Service(39(+3)/51), Controller(39(+3)/51), Report(0/21), 개발해야할 Operation: 314개
 * 운전자력 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
#### 느낀점: SELECT 쿼리문을 불러오는 데에 너무 오래 걸리는 이슈가 발생하였다. TO-BE기준 SELECT문은 3초안에 불러들어와야 하는데 데이터양이 방대하거나 조인하는 테이블이 많은 경우 오래 걸릴 수 있다 이러한 문제를 해결하기 위해 DBA분에게 찾아갔고 플랜을 해야한다고 하였다. 플랜이란 어떤 경로로 테이블을 접근하는지, 어떤 방식으로 조인하는지, 어떤 인덱스 자원을 사용하는지 등에 대한 최적화한 계획을 알려주는 것이다. 그러면서 내가 짠 쿼리를 살펴보니 크게 몇 가지의 문제점이 있었다. 첫째.서브쿼리에 대해 알리아스를 제대로 하지 않았다는 점이다. 예를 들어 메인 테이블은 A테이블이 있고 B테이블을 군번과 군구분을 통해 서브쿼리로 불러와야 하는데 이때 서브쿼리 조건에 알리아스 A를 하지 않아 서브쿼리에서 B에 대해 전체를 뒤지고 있었다는 점이다. 둘째. 인덱스를 활용하지 않았다. PK로 조인해오면 참 좋겠지만 어떤 경우는 일반 컬럼을 통해 조인을 해와야 할 경우가 많다 이럴 경우 데이터의 양이 너무 방대하다면 DBA분께 요청에 조인에 필요한 컬럼에 인덱스를 달아달라고 요청을 해야한다는 것이다. 셋째. 효율적으로 테이블을 조인하는 방법이다. 예를 들어 컬럼 2개를 조인할 때 만약 1개는 인덱스가 걸려있고 다른 1개는 인덱스가 걸려있지 않다면 인덱스가 걸려있는 컬럼을 먼저 찾은 다음에 나머지 인덱스가 걸려있지 않은 컬럼을 찾게 하는 방식과 테이블 2개를 조인해 올 경우 두 테이블의 데이터 양을 비교해보고 데이터가 적은 테이블 먼저 조인 후 남은 테이블을 조인하는 식으로 쿼리문을 짜라고 하셨다. 이때까지 결과만 잘 나오면 되겠지라는 생각에 쿼리문을 짰지만 지금 당장에는 상관없을지 모르나 추후에 데이터가 방대해질 경우를 생각한다면 DBA분께서 말씀하신대로 DB가 빠르게 원하는 결과물을 가지고 올 수 있도록 플랜을 보고 쿼리문을 짜야겠다고 생각했다.

### 2022.6.6 ~ 2022.6.24
#### 개발화면 (92/109), Service(36(+6)/51), Controller(36(+6)/51), Report(0/21), 개발해야할 Operation: 314개
 * 운전자력 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
#### 느낀점: 상황관리 장비취급이라는 새로운 기능을 개발하였다. 운전자력 기록부 중 장비취급경력이라는 기능이 있는데 이 기능은 해당 운전자가 차종 및 차종번호별로 매달 운전기록을 기록하는 기능이다. 그런데 보통 운전자들은 여러 차종을 운전하기 때문에 매달 운전했던 차종들을 기입하기가 번거로워서 그냥 한 차종으로 합산하여 기입하고 있는 상황이였다. 그래서 상황관리에서 차종별로 운행기록을 합산하여 저장하는 기능을 만들어달라는 요구사항이 있었다. 그래서 배차쪽 담당자와 협의를 하여 배차를 내서 운전자가 해당 배차를 운전을 하고 주파거리를 기록한다면 월 단위로 배차기록을 받아와서 차종, 차종번호 별로 GROUP를 지어 주파거리를 합산하여 자동으로 저장하게끔 개발을 하였다. 배차쪽 데이터를 가져오기 위해서는 배차쪽 테이블들을 알고 있어야하는데 난 모르는 상황이여서 테이블들을 분석하는 데에 시간이 걸렸다. 그래서 배차쪽 테이블들 5개정도 JOIN을 해와서 내가 원하는 상황관리 데이터를 불러오는 데에 성공을 하였다.

### 2022.5.30 ~ 2022.6.3
#### 개발화면 (92/109), Service(30(+3)/51), Controller(30(+3)/51), Report(0/21), 개발해야할 Operation: 314개
 * 운전자력 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
 * 화면검토회
#### 느낀점: 화면검토회를 하였다. 아직 개발일정이 완료되지 않았지만 중간점검의 성격으로 전군에서 DTIS이용자들이 모였다. 현재까지의 진행상황을 설명하고 개발된 부분에 대해서 화면을 시연해주었다. 아무래도 실제 사용자들이다보니 디테일한 부분까지도 질문사항이 많았다. 특히 군 관련 정책에 대해서 질문이 들어왔을 때는 아직 1년차밖에 되지 않다보니까 기술적인 부분은 설명이 가능했지만 정책과 관려된 부분은 아직 미흡하다보니까 원활하게 대응하지 못하였다. 또한 내가 개발하는 프로그램이 육군, 공군, 해군, 해병대 각 군 모두가 사용하는 프로그램이다보니까 각군마다 정책이 달라 개발하는데에 약간 이슈가 있었다. 예를 들면 육군에서는 직접운전을 신청할 때에 운전병 신상을 생성하도록 하게하는 지침이 육군본부로 부터 내려왔다고 하나 우리팀은 그런 지침을 들은 바가 없었고 타 군에서도 그런 지침은 받은 적이 없다면서 각 군마다 지침이 달라서 애로사항이 생기기도 하였다. 무엇보다도 가장 중요한 점은 내가 군 관련 정책을 제대로 파악하지 못해 기술적으로 구현은 하였으나 왜 그렇게 개발되는지에 대해 제대로 설명을 못하였다는 것이다. 개발을 함에 있어서 기능을 구현하는 것에 그치는 게 아니라 이러한 기능에 필요성과 그에 관련된 정책, 히스토리 등을 파악하는 것도 중요하다고 생각하였다.

### 2022.5.23 ~ 2022.5.27
#### 개발화면 (92/109), Service(27(+3)/51), Controller(27(+3)/51), Report(0/21), 개발해야할 Operation: 314개
 * 운전자력 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
 * 취약점 점검
    * Sparrow를 통한 코드 익스펙션
#### 느낀점: Sparrow를 통한 코드 익스펙션을 하였다. 코드 익스펙션이란 소프트웨어에 대한 품질을 점검하는 것이며 작성한 개발소스 코드를 분석하여 개발 표준에 위배되었거나 잘못 작성된 부분을 수정하는 작업을 뜻한다. 내가 작성한 개발소스에 대해서도 몇가지의 취약점이 발견되었다. 첫째. 디버깅을 위한 console.log 및 System.out.prinln 등이였다. 디버깅을 위해 작성하였으나 개발이 완료되었으면 해당 코드는 제거해야하나 미쳐 제거하지 못하고 남겨두어서 취약점이 발견되었다. 물론 해당 코드를 제거함으로써 이를 해결하였다. 둘째. MyBatis에서 ${}을 사용한 점이다. 이러한 코드가 왜 취약하냐면 #{}은 내부적으로 PreparedStatement(값을 바인딩하는 시점에서 전달된 값에 대한 특수문자, 쿼리 등을 필터링)를 사용하지 때문에 SQLInjection 공격에 안전한데 ${}는 입력받은 파라미터를 쿼리에 직접 치환해주기 때문이다. 그래서 ${}로 작성된 매퍼를 #{}로 수정함으로써 문제를 해결하였다. 코드를 작성함에 있어서 취약점에 대한 부분도 고려하면서 개발을 해야겠다고 생각하였다.

### 2022.5.16 ~ 2022.5.20
#### 개발화면 (92/109), Service(24(+3)/51), Controller(24(+3)/51), Report(0/21), 개발해야할 Operation: 314개
 * 운전자력 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
#### 느낀점: 직접운전 관련 기능을 개발하였다. 직접운전이란 크게 두가지로 나뉜다. 첫째는 군 간부들이 본인 차량을 군부대에서 운전할 수 있게 하는 자격과 운전병 없이 본인이 군 차량을 운전할 수 있게 하는 자격이다. 이때 간부가 차량을 운전하다가 교통법규를 어기게 되면 면허정지기간이 부여된다 AS-IS에서는 배차를 내는 담당자가 정지기간을 확인하여 배차를 내는 방식이였으나 기술적으로는 배차를 낼 수 있게 되어 있었다. 이를 TO-BE체계에서는 정지기간 내에는 배차가 나지 않도록 기술적으로 개발해야했다. 근데 배차관련 기능은 다른 팀에서 담당하는 기능이기 때문에 다른 팀과의 협업을 통해서 구현을 해야했다. 그래서 해결한 방식은 교통법규 관리 화면에서 해당 운전자에 대해 정지기간이 주어지면 배차를 할때에는 SYSDATE가 정지기간 내에 포함되면 배차가 안되도록 설정을 하며 정지기간이 끝나지 않더라도 면허를 해제할 수 있기 때문에 직접운전자의 면허상태에 정상상태 코드를 기입하여 면허정지기간과 면허상태코드를 확인하여 배차여부를 파악할 수 있도록 개발하였다. 이러한 경험을 통해 개발을 하면서 다른 팀과의 협업이 반드시 필요하다는 것을 알게 되었다.

### 2022.5.9 ~ 2022.5.13
#### 개발화면 (92/109), Service(21(+3)/51), Controller(21(+3)/51), Report(0/21), 개발해야할 Operation: 314개
 * 운전자력 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
#### 느낀점: 이번주에는 개발 이외의 이야기를 하려고 한다. 5.10 윤석열대통령이 취임을 하여 국방부에 오셨다. 마침 시간대가 점심시간 때라 본관 근처에서 구경하였다. 방송국도 많이 왔고 경호도 삼엄했다. 처음 보는 광경이라 신기했다. 하지만 좋은 점보단 안좋은 점이 더 많은 것 같다. 첫째로는 본관에 있던 지하식당이 영업을 못하게 되어 내가 자주 이용하던 별관 식당으로 몰리게 되어 식당을 이용하기가 어렵게 되었다. 둘째는 시위로 인해 소음이 생겼다는 점이다. 국방부 정문 앞에서 매일 시위하는 사람들도 인해 소음이 발생하였고 이러한 소음으로 인해 코딩을 하는데 조금 신경이 쓰였다. 그래도 지금이 가장 중요한 시기이기 때문에 얼른 신경끄고 내 업무에 집중하려고 한다.

### 2022.5.2 ~ 2022.5.6
#### 개발화면 (92/109), Service(18(+3)/51), Controller(18(+3)/51), Report(0/21), 개발해야할 Operation: 314개
 * 운전자력 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
#### 느낀점: PM님께서 내가 개발한 화면들을 검증하였다. 분명 내가 테스트 할때는 오류가 없었는데 PM님께서 점검을 하니 오류가 발생하였고 생각지도 못한 부분에서 에러가 발생하였다. 예를 들어 군운전면허시험 신청 화면에서 성명을 기입하는 부분이 있었다. 성명을 저장하는 컬럼은 VARCHAR(100)이였는데 길이에 대한 밸리데이션(Validation)체크를 할 때 그 부분을 신경쓰지 못해 에러가 나고 만것이다. 또한 수정을 해야하는데 특정한 상황에서는 수정이 이루어지지 않는 등 자잘한 오류들을 발견하셨다. 그러고는 PM님께서 디테일한 부분을 신경쓰면서 개발해야한다고 조언을 하셨다. 물론 맞는 말이다. 나도 이러한 디테일한 부분을 신경써가며 개발을 하고 싶다. 하지만 나한텐 정해진 일정이 있고 일정 내에 기능들이 동작이 되도록 개발을 해야하는데 이런 디테일한 부분을 다 신경써가며 개발하고 일정을 맞출려면 어떻게 해야하나 고민을 했고 이러한 점을 차장님께 털어놓았다. 차장님께서는 일단 기본적인 기능은 동작하게 만들되 디테일한 부분은 추후 QA를 할 때에 수정을 하자고 하셨다. 그렇지만 기본적인 기능이라는게 말 그대로 CRUD만 돌아가면 되는 것인지 아니면 어느정도 선까지 디테일한 부분을 생각하며 개발해야하는 지에 대해서는 감이 오지 않았다. 그래도 일단은 기한을 우선적으로 맞추되 디테일한 부분을 최대한 맞춰보도록 노력을 해야겠다고 생각했다.

#### 우리팀원들 중에 매달 개발을 가장 잘하는 인원을 뽑아 상금을 주기로 하였는데 4월달에는 내가 가장 개발을 잘해서 상금 50만원을 받았다. 나의 개발분량도 성실하게 해냈지만 아픈 동료나 일정을 맞추지 못한 동료들을 적극적으로 도와주었고 이러한 점을 알아주신게 아닐까 싶다. 나의 담당이 아닌 업무였기에 테이블들의 구조, 화면, 스크립트 등 익숙하지 않았지만 계속 개발하고 연구하다보니 다른 업무에 대한 이해도도 올라간것 같다. 나의 개발일정도 중요하지만 전체적인 팀의 개발일정이 더 중요하기 때문에 앞으로도 나의 일정이 여유롭다면 팀 개발일정에 맞춰 유연하게 대처해야겠다.

### 2022.4.25 ~ 2022.4.29
#### 개발화면 (92/109), Service(15(+3)/51), Controller(15(+3)/51), Report(0/21), 개발해야할 Operation: 314개
 * 군전세객차 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
#### 느낀점:군전세객차에 대해 잔여좌석을 신청하는 화면을 개발할 때에 일이다. AS-IS를 분석해보니 신청하기 전 이것저것 확인하는 게 많았다. 예를 들어 USER_ID를 통해 해당 신청자가 동일 열차를 신청하지 않았는지, 조회할 때는 이미 신청된 좌석은 안나오지만 신청하는 인원이 많다보니 신청하는 동안에도 누군가가 신청을 하기 때문에 다른 사람이 신청하진 않았는지 등등 체크를 해야했다. AS-IS는 프로시저로 개발되어있었지만 이를 Spring에 맞춰 개발을 해야했다. 그래서 다음과 같은 방식으로 개발하였다.
```C

<mapper namespace = "mapper경로"
  <select id="select체크오퍼레이션" resultType="map">
   SELECT
    COUNT(USER_ID) AS COUNT
   FROM
    군전세객차 신청서 관련 테이블
   .....비밀..
  </select>
</mapper>

@Service
public class 비밀 implements I비밀(인터페이스){

 @Autowired
 CommonDao commonDao
 
 public String save오퍼레이션 (List<Map> list)
{
   for(Map map : list){
     Map<Object, String> chk = commonDao.selectOne(mapper경로.select체크오퍼레이션);
     
     //조회하였을 때 count가 0이 아니라면 해당 신청서에 존재하기 때문에 String 타입을 반환함
     if(!(String.valueOf(map.get("COUNT"))).equals("0")){
       return "다른 신청자가 이미 신청한 좌석입니다."
     }
     
     //조회하는 오퍼레이션이 4개(구조는 위와 동일)
     
     //체크를 끝냈다면 insert를 실행
     commonDao.insert(mapper경로.insert오퍼레이션);
   }
}
```
위와 같이 코드를 작성하여 문제가 되는 건이 발생한다면 insert를 하지 않고 위험 문구를 반환하도록 작성을 하였다. 개발을 할때 프로시저로 되어있는 개발소스들을 어떻게 하면 TO-BE 체계로 개발할 수 있는지 더 고민해야 겠다고 생각했다.
![KakaoTalk_20220510_224530016](https://user-images.githubusercontent.com/82793713/167644539-7cca84ae-6f69-480b-b09b-f6eb25aea31d.jpg)


### 2022.4.18 ~ 2022.4.22
#### 개발화면 (92/109), Service(12(+3)/51), Controller(12(+3)/51), Report(0/21), 개발해야할 Operation: 314개
 * 군전세객차 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
#### 느낀점: 개발해놓은 화면들을 테스트를 하던 중 에러가 발생하였다. 에러메세지를 살펴보니 SELECT문에서 해당 컬럼이 테이블에 존재하지 않는 다는 것이였다. 그래서 살펴보니까 테이블의 컬럼구조가 변경된 것이였다. 예를 들어 신청 관련 테이블에 신청자의 군번과 군구분을 기입하여 신청서 작성자의 신상을 불러올때 군번과 군구분을 통해 신상 테이블과 조인 및 서브쿼리를 통해 불러왔지만 바뀐 구조는 군번과 군구분 대신 USER_ID를 통해 해당 신상을 불러오고 저장하도록 구조가 바뀌었다. 그래서 그 즉시 관련 코드들을 모두 수정하였다. 수정은 하였지만 수정된 이슈에 해당하는 쿼리문들이 수정해야할 것들을 찾는 데에 시간이 너무 걸렸다. 테이블을 설계할 때 이러한 점이 반영되었다면 수정을 하지 않고 시간을 아낄 수 있었을 텐데라는 생각이 들며 역시 개발도 중요하지만 설계 또한 그에 못지않게 중요하다는 점을 깨닫게 되었다. 
PS. 코로나의 거리두기가 풀려서 우리 프로젝트 인원들끼리 오랜만에 회식도 하고 기분이 좋았다. 곧 야외 마스크도 벗는다는데 얼른 코로나도 풀리고 마스크를 벗는 날이 왔으면 좋겠다.
(서울 올라온지가 3년 넘었는데 2년 넘게 마스크 썼네..)

### 2022.4.11 ~ 2022.4.15
#### 개발화면 (92/109), Service(9(+1)/51), Controller(9(+1)/51), Report(0/21), 개발해야할 Operation: 314개
 * 운전자력 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
#### 느낀점: 군운전면허시험 신청/조회 화면 및 기능을 개발하였다. 컴포넌트 명세서상으로는 면허시험을 신청하면 신청서 관련 테이블에 INSERT되는 개발 방법이였다. 그러나 AS-IS를 분석해보니 신청서를 신청할때 신청하는 사람의 군구분 및 군번을 통해 운전자 신상 테이블에 데이터가 있는지 확인하여 존재한다면 해당 정보를 UPDATE를 하고 없으면 INSERT 후에 신청서 관련 테이블에 INSERT하는 방식이였다. 설계단계때는 산출물 기한으로 인해 AS-IS를 자세하게 분석하지 못해 그 부분까지 파악하지 못한 것이였다 그래서 AS-IS대로 운전자 신상 테이블에 해당 정보의 유무를 파악해서 데이터를 처리하고 하였으나 그러면 설계단게에서 계획하지 못한 컴포넌트가 늘어나고 개발해야하는 양이 크게 늘어날 것 같았다. 그래서 구글에 검색을 하여 MERGE INTO 문을 찾아내었다.
```C
MERGE INTO 운전자신상 테이블 S
    USING DUAL
       ON (S.군번 = #{찾고자하는 군번} AND S.군구분 = #{찾고자하는 군구분})
    WHEN MATCHED THEN
        UPDATE SET 업데이트하고자 하는 컬럼 = 업데이트하고자하는 값
    WHEN NOT MATCHED THEN
        INSERT (INSERT하고자 하는 컬럼)
        VALUES (INSERT하고자 하는 값)
```
이런식으로 쿼리문을 작성하여 운전자 신상 테이블에 데이터가 있으면 UPDATE, 없으면 INSERT 되도록 개발하였다. AS-IS 방식 그대로 따르는 것이 아닌 더 나은 개발 방법이 떠오른다면 더 나은 코드로 개선해나가는 것이 중요하다고 생각했다.

### 2022.4.04 ~ 2022.4.08
#### 개발화면 (92/109), Service(8(+1)/51), Controller(8(+1)/51), Report(0/21), 개발해야할 Operation: 314개
 * 운전자력 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
 * 수송근무 공통코드 분석
 ![KakaoTalk_20220408_205550584](https://user-images.githubusercontent.com/82793713/162431156-db1be989-da65-45bc-bf9d-a535c497d682.jpg)
#### 느낀점: 철도 연간운행계획관리 화면 및 기능을 개발하였다. 이를 위해 철도공사로부터 열차에 관련된 데이터를 전달받았다. 이 과정에서 이해가 되지 않는 부분이 있었다. 예를 들어 신규 작성을 할 때에는 해당 철도에 관한 정보(노선에 관한 정보들)은 철도공사로부터 가져오나 저장할 때는 수송근무 테이블에 저장하여 관리를 한다는 것이었다. 이렇게 되면 만약 철도공사측에서 철도에 관한 정보를 수정해야할 때 자동으로 수정되는 것이 아닌 우리가 관리하는 테이블에서 수정을 해야했다. 그래서 이러한 점을 얘기하였으나 일단 일정에 맞춰서 개발을 해야하니 AS-IS대로 개발을 하자고 하셨다. 그리고 추후에 철도공사측과 연동회의를 할때 잘 기억해뒀다가 이러한 이슈를 공론화해야 할 것 같다. 그리고 차장님께 들은 이야기인데 철도 예약과 관련된 기능에서 건의사항이 많이 나온다고 한다. 왜냐하면 군인들이 휴가 혹은 출장 갈때마다 열차를 전세하기 때문에 자주 쓰이는 기능이라고 하셨다. 그래서 이번에 개발할때 이 부분들 만큼은 실수없이 잘 개발하라고 하셨다. 내가 만든 기능들을 군인들이 자주 사용한다고 생각하니까 개발이 되어도 테스트는 자주 해봐야 겠다는 생각이 들었다. 수송근무 공통코드 분석할 때에 일이다. AS-IS에서는 공통코드를 테이블에 둬서 관리를 하였는데 공통코드를 불러오는 방법이 일정하지 않았다. 예를 들어 테이블의 컬럼이 MAINCD, SUBCD, CODE1, CODE2 이런식으로 있고 MAINCD='열차역명과 관련된 코드를 불러오는 명', SUBCD='열차역명(서울, 부산 대구...)', CODE1='A(서울), B(부산), ...', CODE2='001(서울), 002(부산), ...' 이런식으로 존재하여서 어떤 경우에는 A를 통해 열차역명을 불러오는 경우가 있고 어떤 경우에는 001를 통해 열차역명을 불러오는 경우가 있었다. 그래서 이를 공통코드로 바꿀려고 하니 이러한 이슈때문에 문제가 생겨 조사를 하게 되었다. 왜 이런식으로 쓰이냐고 차장님께 어쭤봤더니 옛날 10년전부터 여러사람들이 공통코드를 쓰다보니 불러오는 방식이 점점 늘어나서 이렇게 되었다고 한다. 이번 기회에 조사를 하여서 이러한 문제들을 해결해서 하나의 방법으로만 코드를 불러오도록 해야할 것 같다.

### 2022.3.28 ~ 2022.4.01
 * 운전자력 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
#### 느낀점: 군전세객차 관련쪽 저장 관련 기능을 개발하다가 문제가 생겼다. 오류 메세지를 살펴보니 저장을 할때 보내는 파라메터의 길이가 너무 길다는 것이였다. 내가 보내려던 데이터는 열차의 좌석과 관련된 것이다. 예를 들어 열차 1대에 최대 25량까지 있으며 1량에는 최대 88좌석까지 지정할 수 있다. 또한 저장하는 데이터의 형식은 한 좌석당 1ROW로 관리되고 있었던 것이였다. 즉 한 좌석당 열차명, 열차번호, 좌석번호, 노선번호 등등이 저장되어있어 많은 좌석을 저장하기 위해 보낸 파라메터이 최대 제한 수를 넘기고 말았던 것이였다. DBA과 그 테이블을 관리하던 체계지원 쪽 개발자분과 상의를 해봤는데 길이를 늘릴 순 있으나 파라메터가 커지는 케이스가 다수라면 수정해야하나 이러한 경우가 드물기 때문에 수정하기는 힘들다고 하셨다. 그래서 생각해낸 방법이 파라메터 1줄에 배열을 보내는 방법을 생각하였다. 예를 들어 A열차명에 1번 차량번호에 1A, 2A, .... 16A, 1B, ....16D까지 좌석이 있다면 기존에는 총 64ROW(16X4)만큼의 파라메터를 보냈어야 하나 1ROW에 좌석을 배열로 담아 보낸 뒤(사실상 배열의 형식으로 하고 있는 String이다) 서비스단에서  "," 단위로 Split을 하여 String[]로 바꾼 다음 for문으로 1줄씩 DB에 전달하는 방식을 생각해 내였고 그 결과 성공적으로 데이터가 저장 및 수정할 수 있게 되었다. 이러한 어려움을 해결하면서 아쉬운 점은 AS-IS에서의 테이블 구조를 따라하다보니 어쩔 수 없이 이런 방식을 택할 수 밖에 없었는데 애초에 테이블 구조를 잘 짰으면 조금 더 수월하지 않았을 까라는 생각을 하게 되었다. 예를 들어 테이블 1Column에 배열 형식의 데이터를 저장하여 관리한다면 데이터 크기 측면에서나 관리 측면에서나 좀 더 수월 했을 것 같다라는 생각이 들었다.


### 2022.3.21 ~ 2022.3.25
 * 운전자력 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
    * AS-IS 개발 소스 및 쿼리문 분석
    * myBatis를 기반으로 한 개발
#### 느낀점: 이번주부터 본격적으로 일정을 맞추기 위해 개발에 박차를 가하였다. 시간이 부족하여 야근을 하였으나 다행히도 생각보다 개발이 잘 진행되어서 나의 개발 일정은 1~2일 정도 여유가 있어졌다. 개발을 하면서 다른 업무 영역의 테이블을 불러와야 하는 경우가 생겼다. 예를 들어 군 부대와 관련된 테이블을 관리하는 업무 팀이 있는데 부대코드와 매핑되는 부대정보를 불러올 일이 생겨 담당자에게 필요한 테이블에 대한 설명을 듣고 업무를 진행하였다. 일을 너무 집중해서 손목이 아팠다. 그래서 집 가는 길에 버티컬 마우스를 주문해서 그 마우스로 업무를 진행하였다. 사원 중 1명이 개발하면서 막히는 부분이 있어 확인해보니 내가 겪은 부분이랑 비슷했다. 그래서 내 해결방법을 알려주어 해결해주었다.

### 2022.3.11 ~ 2022.3.18
 * 운전자력 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
    * AS-IS 개발 소스 및 쿼리문 분석
    * myBatis를 기반으로 한 개발
#### 느낀점: 군면허시험 신청 화면을 개발을 하였다. 하던 와중 주민등록번호 데이터를 불러올 상황이 생겨 DB에서 불렀으나 암호화가 되어 있었다. 그래서 복호화하는 방법을 찾아보니 크게 2가지 방법이 있었다. 첫째. DB에서 복호화하는 방법 둘째. AP에서 복호화하는 방법 DBA분께 어쭤보니 DB에서 복호화하게 되면 DB에 부담이 갈 수 있으므로 AP에서 복호화하는 방법으로 개발하라고 하셨다. 이를 통해 개발을 할 때에는 다른 개발자와의 의사소통이 중요하다고 다시 한번 더 느끼게 되었다. 또한 이곳에 작성하기는 힘들지만 엄청 복잡한 DB를 불러와야 하는 경우가 생겼다. 그럴때 차장님이 AS-IS 쿼리문을 분석해서 TO-BE에 맞게 수정해서 사용하라고 말씀하셨다. 분석해보니 AS-IS에서는 프로시저로 불러오고 있었지만 TO-BE에 맞게 적절하게 수정하여 해결할 수 있었다. 이러한 경험을 통해 기존에 개발된 소스나 쿼리문들을 활용하는 것이 시간 단축과 정확한 개발을 할 수 있을 것 같다는 생각이 들었다.

### 2022.3.7 ~ 2022.3.11
 * 화면 개발
    * 넥사크로를 이용하여 화면 개발
 * 운전자력 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
    * myBatis를 기반으로 한 개발
 * 수송근무 설계단계 감리시정조치
    * 개략설계, 상세설계 감리시정 조치 작업
 #### 느낀점: 처음으로 서비스단과 컨트롤단을 개발하여 매퍼과 sql문을 작성하여 DB(티베로)로 연결하였다. AS-IS SQL문을 보면서 개발하고는 있으나 생각보다 조인해야할 테이블들이 너무 많은 것 같다. 기존의 sql문에 대해 연구를 해야겠다는 것을 깨달았다. 또한 mybatis sql문을 연구하던 중 #{}과 ${}을 보게 되었다. 검색해보니 ${}는 파라메터가 바로 출력되는 형식으로 해당 컬럼의 자료형에 맞추어서 파라매터의 자료형이 변경되는 방식이고 #{}는 파라매터가 String 형태로 들어오는 방식임을 알게 되었다. 국비학원을 다니면서 myBatis에 대해 공부를 하였으나 개발을 하게 되면서 새로운 지식을 알게 되는 것 같아서 역시 개발은 끝없는 공부라는 것을 깨닫게 되었다.

### 2022.2.28 ~ 2022.3.4
 * 화면 개발
    * 넥사크로를 이용하여 화면 개발
 * ICD 국방통계정보체계 수정
    * 코드성 컬럼 및 데이터 조사 및 수정
 #### 느낀점: 수송근무 팀원 2명이 코로나 양성판정이 나왔다. 1주일간 출근을 할 수가 없기에 개발 일정에 차질이 생겼다. 남은 4명이서 이번주 개발 일정을 맞추기 위해 대책 회의를 하였고 다행히 나의 분량인 운전자력과 군전세객차에 대한 화면 개발이 거의 진행된 상태라서 마무리를 짓고 차질이 생긴 분량에 대해 화면 개발을 하기로 했다. 그렇게 야근을 하여 겨우 개발 일정을 맞출 수가 있었다. 만약 2명이 아니라 그 이상의 인원이 프로젝트 참여에 차질이 생기게 된다면 개발 일정에 큰 차질이 생길 것 같다. 코로나는 어쩔 수 없는 상황이긴 하지만 그래도 나의 몸은 내가 관리하지 않으면 다른 팀원에게 더 부담이 가고 일정에 큰 차질이 생긴다. 그렇기 때문에 일을 함에 있어서 건강 관리 또한 중요한 요소임을 알게 되었다. 

### 2022.2.21 ~ 2022.2.25
 * 화면 개발
    * 넥사크로를 이용하여 화면 개발
 * 수송근무 상세설계 산출물 수정
    * 컴포넌트 설계서(패키지정의, 배포정의), 사용자인터페이스 설계서 물리경로에 따른 경로 수정 등을 수정
 * 수송근무 암호화 적용
    * 주민등록번호, 계좌번호, 운전면허번호 등 컬럼에 대한 암호화 적용 작업

### 2022.2.14 ~ 2022.2.18
 * 화면 개발
    * 넥사크로를 이용하여 화면 개발
 * 수송근무 내외부간 연동통제문서(ICD) 수정 작업
    * TO-BE 테이블 및 컬럼 수정에 따른 내외부간 연동통제문서(ICD) 수정
 * 수송자산 개략, 상세설계 산출물 수정
    * 수송자산 측 요청에 의해 산출물 수정 작업 도움

### 2022.2.7 ~ 2022.2.11
 * 화면 개발
    * 넥사크로를 이용하여 화면 개발
 * 수송근무 연동통제문서(ICD) 수정 작업
    * TO-BE 테이블 및 컬럼 수정에 따른 연동통제문서(ICD) 수정
 #### 느낀점: 수송근무의 운전자력 부분의 화면을 개발하였다. 이번 프로젝트의 형상관리 툴은 SVN을 사용였다. 개발한 화면 소스를 퇴근 전 매일 커밋을 해야합니다. 평소와 같이 커밋을 하는데 보통 프로젝트를 전체를 업데이트 한 후에 개발한 부분만 커밋을 하는데 실수로 프로젝트 전체를 커밋을 해버렸습니다. 그래서 공통소스가 수정되버렸습니다. 그래서 곧바로 차장님께 보고드린뒤 차장님과 함께 AA(Application Architect)를 찾아가서 실수한 부분을 말씀드렸습니다. 그리고는 제가 커밋하기 직전으로 롤백을 하면 안되냐고 어쭤보았지만 롤백의 권한은 TF팀에 있다면서 롤백을 하려면 절차를 거쳐서 보고를 해야한다고 하였습니다. AA분께서는 롤백보다는 Synchronize를 통해서 공통부분이 수정된 소스를 찾아 그부분을 Override and Commit을 하자고 하였습니다. 그렇게 해서 문제를 해결하였습니다. 이러한 실수를 통해 느낀 점은 여러 명이서 함께 하는 프로젝트에서는 업데이트와 커밋을 신중하게 해야겠다고 반성하게 되었다.

### 2022.1.31 ~ 2022.2.4
 * 설날

### 2022.1.24 ~ 2022.1.28
 * 수송근무 PMO 기술지원인원 점검결과 반영
    * 개략설계 산출물 수정 작업
 * 수송근무 테이블, 컬럼 매핑 표준화 작업
    * 코드설계서에 따른 컬럼 매핑화
 * 상세설계 산출물 수정 작업
    * 개략설계 산출물 수정에 따른 상세설계 산출물 수정
 * 화면 개발
    * 넥사크로를 이용하여 화면 개발(이때 화면 규칙에 따라 개발해야함)

### 2022.1.17 ~ 2022.1.21
 * 수송근무 PMO 기술지원인원 점검결과 반영
    * 개략설계 산출물 수정 작업
 * 수송근무 테이블, 컬럼 매핑 표준화 작업
    * 테이블, 컬럼 매핑 표준화 작업
    * 컬럼 데이터타입 및 데이터길이 매핑 작업
 * 넥사크로 공통 교육
    *  UI 공통 기능 설명 및 적용방법 등
 * 개발환경 교육
    *  개발환경 세팅, 개발소스 구조, 서버환경 가이트 교육
 * 상세설계 CDR 산출물 PMO 검토의견 반영
    *  상세설계 산출물 검토의견 반영 작업
 #### 느낀점: 넥사크로 교육과 개발환경 교육을 하였다. UI 같은 경우 컴포넌트의 디자인 규칙이 확정된 상태라서 규칙에 어긋나는 컴포넌트를 사용할 경우 다른 화면들과의 이질감이 들 수도 있을 것이다. 예를 들어 넥사크로의 기본 달력 컴포넌트가 있지만 이번 프로젝트에서는 달력 컴포넌트를 커스텀한 달력 컴포넌트를 사용하기 때문에 반드시 이를 유의해야 합니다. 

### 2022.1.10 ~ 2022.1.14
 * 수송근무 PMO 기술지원인원 점검결과 반영
    * 개략설계 산출물 점검결과 반영
    * 상세설계 산출물 점검결과 반영
 * 수송근무 구현 사전 준비
    * 메뉴구조도 작업
    * 프로그램 개발 목록 작업
 * 수송근무 테이블, 컬럼 매핑 표준화 작업
 * 설계단계 검토회(PDR/CDR)
 #### 느낀점: 개략설계 단계 산출물 중 일부 수정할 사항이 점검 기술지원인원 점검 중 발견이 되어서 수정하였다. 예를 들어 정기공수 탑승/신청과 부정기공수 탑승/신청의 컨트롤 클래스 및 인터페이스가 탑승/신청으로 명명되어 있다. 이름이 중복되어 설계가 된 것이다. 그래서 이를 수정하는데 상세설계 산출물이 개략설계 산출물을 기반으로 작성하다보니 상세설계 산출물 또한 수정을 하게 되었다. 만약 구현 단계에서 이러한 사항이 발견되었다면 더 많은 수정작업이 이루어졌을거라 생각한다. 최대한 완벽하게 설계를 해야 그 이후 작성될 산출물이나 구현단계에서 구현될 코드들의 수정이 최소화 될 것 같다라는 생각이 들어 이 이후에는 산출물을 좀 더 꼼꼼히 봐야겠다고 다짐했다.
 
### 2022.1.3 ~ 2022.1.7
 * 연동통제문서(ICD) 현행화 작업
 * TO-BE 테이블 ERD 작성 및 DB 반영
 * AS-IS와 TO-BE 테이블 및 컬럼 이전을 위한 데이터 타입 및 길이 일치화
#### 느낀점: 테이블 및 컬럼 매핑을 거의 완료하였으나 연동통제문서에서 도메인이 변경되는 바람에 연동과 관련된 테이블의 컬럼 도메인을 수정해야하는 상황이 생겼다. 예를 들어 한국철도공사에서 철도번호를 기존에서는 30BYTE로 수신해주기로 하여 이에 맞춰 도메인 길이를 30BYTE로 매핑하였으나 32BYTE로 변경되는 바람에 기존에 테이블 설계 문서들을 수정하는 상황이 발생하였다. 또한 우리가 송신하는 데이터들에 대해서 도메인이 변경하게 되어 관련 업체와의 협의가 필요하게 되었다. 예를 들어 KB손해보험정보체계에 송신하는 데이터들 중 사건발생일시가 기존에는 DATE타입이였으나 VARCHAR2(14)로 변경되어서 KB손해보험 측과 협의를 하여 변경하기로 하였다. 단순히 데이터타입이나 길이를 바꾸는 것이 결코 쉽지 않은 일이라는 것을 알게 되었다.

### 2021.12.27 ~ 2021.12.31
 * AS-IS 프로시저 및 쿼리 분석작업 수행
 * 데이터베이스 설계서 산출물 작성 작업 

### 2021.12.20 ~ 2021.12.24
 * AS-IS 프로시저 및 쿼리 분석작업 수행
 * 데이터베이스 설계서 작성을 위한 TO-BE 테이블 관계 정리 및 컬럼 단어와 도메인 표준화
 * 외부 연동항목테이블매핑설계서 작성
#### 느낀점: AS-IS와 TO-BE 테이블 및 컬럼을 매핑하는데 테이블이 달라도 같은 이름의 컬럼이라면 도메인 길이를 통일해야 하는데 그렇지 못하고 AS-IS에 맞춰서 도메인 길이를 정하다 보니까 같은 이름의 컬럼인데도 불구하고 도메인 길이가 다르게 매핑되는 문서를 작성하게 되었다. 그래서 길이가 가장 긴 도메인 길이를 기준으로 통일해 수정하였다. 단순히 데이터 타입 및 길이만을 맞춰 매핑하기 보단 전체적인 테이블 및 컬럼과의 통일성도 신경을 써야겠다고 생각했다.

### 2021.12.13 ~ 2021.12.17
 * AS-IS 프로시저 및 쿼리 분석작업 수행
 * 데이터베이스 설계서 작성을 위한 TO-BE 테이블 관계 정리 및 컬럼 단어와 도메인 표준화
 * 외부 연동항목테이블매핑설계서 작성
#### 느낀점: AS-IS 테이블 및 컬럼을 TO-BE 테이블 및 컬럼에 매핑을 해야하는 작업을 하였다. 매핑을 하려면 기존 AS-IS 데이터의 타입 및 길이를 분석하여 TO-BE 체계 도메인에 맞게 매핑을 해야했다. 이때 사용된 쿼리문은 아래와 같다. 이때 크나큰 실수를 하게 되었다. 가장 길이가 긴 LENGTH기준으로 도메인 길이를 정하여 매핑하였는데 한글은 3BYTE라는 사실을 인지하지 못한 채 예를 들어 '서울시'라는 데이터의 LENGTH는 3이나 9BYTE이므로 최소 9BYTE 이상의 도메인 길이를 매핑해야했으나 3BYTE 도메인과 매핑을 해서 다시 조사해서 매핑을 하였다. 이러한 데이터 길이를 확실히 인지하고 매핑을 해야겠다고 생각했다.
```C
 SELECT 컬럼, LENGTH(컬럼), COUNT(*) FROM AS테이블 GROUP BY 컬럼 ORDER BY LENGTH(컬럼) DESC;
```

### 2021.12.06 ~ 2021.12.10
 * 사용자인터페이스설계서 산출물 작업
 * 상세설계 품질검토 반영작업 수행
 * AS-IS 프로시저 및 쿼리 분석작업 수행

### 2021.11.29 ~ 2021.12.3
 * 트랜잭션설계서 산출물 작업

### 2021.11.22 ~ 2021.11.26
 * 컴포넌트 설계서 산출물 작업
 * 패키지정의, 배포정의 작업

### 2021.11.15 ~ 2021.11.19
 * 분석단계 산출물 감리 반영 및 시정조치

## 3_개략설계 산출물
### 2021.09 ~ 2021.11

### 3.1. 컴포넌트아키텍처명세서
#### 3.1.1 목적
 * 본 컴포넌트아키텍처명세서는 시스템아키텍처정의서에서 정의한 컴포넌트 아키텍처 정의에 따라 각 레이어별 컴포넌트를 식별하고 컴포넌트 아키텍처를 설계하는데 목적이 있다.
#### 3.1.2 표준 컴포넌트 아키텍처 다이어그램
 * 컴포넌트간의 상호작용은 시스템 아키텍처 정의서의 소프트웨어 아키텍처를 준수, 다음의 표준에 따라 단방향의 호출 관계로 실행 아키텍처가 정의되어 있음. 또한, 구성요소(WebUI, Controller, Interface, Interfacelmpl) 간의 호출관계 식별이 용이하도록 명명규칙을 정의, 컴포넌트 아키텍처 다이어그램은 호출관계 표준 도식화로 대체함

### 3.2. 인터페이스상호작용명세서
#### 3.2.1 목적
 * 본 인터페이스상호작용명세서는 식별된 컴포넌트 인터페이스 간의 상호작용 분석을 통해 컴포넌트 인터페이스를 정제하는데 목적이 있다.

### 3.3. 컴포넌트명세서
#### 3.3.1 목적
 * 본 컴포넌트명세서는 각각의 컴포넌트에 대해 컴포넌트 내부를 모델링 하고 컴포넌트와 인터페이스를 설계하는데 목적이 있다.
#### 3.3.2 컴포넌트내부 클래스 다이어그램
 * 컴포넌트 내부 클래스 구성요소 및 상호작용은 시스템 아키텍처 정의서의 소프트웨어 아키텍처를 준수하여 다음의 표준에 따라 정의되어 작성함
 * 본 국방수송체계 고도화 사업의 구현 플랫폼은 전자정보 프레임웍을 정의하고 있어 업무영역 컴포넌트별 내부 클래스인 구현 클래스로 설계하여 작업함

### 3.4. 사용자인터페이스명세서
#### 3.4.1 목적
 * 본 사용자인터페이스명세서는 사용자 인터페이스 정의 결과를 바탕으로 웹 페이지와 사용자 인터페이스 제어 역할을 담당하는 클래스를 설계하고, 웹 페이지 및 웹 클래스간의 관계를 정의하는데 목적이 있다.
 #### 3.4.2 표준 웹 구성 다이어그램
  * 웹페이지 및 웹클래스 간의 호출관계는 시스템 아키텍처 정의서의 소프트웨어 아키텍처를 준수하여 다음의 표준에 따라 정의되어 있음. 표준 웹 구성 다이어그램 작성을 통해 호출관계를 도식화하고 그 외 호출관계는 업무영역별로 작성된 사용자 인터페이스명세서(웹페이지명세) 부분의 관련 페이지 정보로 확인 할 수 있음\

### 3.5. 데이터명세서
#### 3.4.1 목적
 * 본 데이터명세서는 시스템에서 지속적으로 관리되어야 하는 데이터와 그 특성을 식별하여 개발자 간 공유하기 위해 데이터 모영을 모델링하는데 그 목적이 있다.
#### 3.4.2 표준 웹 구성 다이어그램
 * 본 무서를 구성하는 데이터 모영은 Data Modeling, Tool(ERWin)을 이용하여 작성은 ERD(Entity Relationship Diagram)로 각 업무영역별 PDF 문서로 제출함

## 4_개략설계 산출물
  * 2021.11 ~ 2022.01

### 4.1. 컴포넌트설계서
#### 4.1.1 목적
 * 컴포넌트설계서는 각각의 컴포넌트에 대해 컴포넌트 내부를 모델링 하고 컴포넌트와 인터페이스를 구현 플랫폼에 맞게 적용하여 설계하는데 목적이 있다.

### 4.2. 트랜잭션설계서
#### 4.2.1 목적
 * 본 트랜잭션설계서는 유스케이스별로 명시된 트랜잭션이 어떤 인터페이스의 오퍼레이션으로 구현되는지 설계하는데 목적이 있다.

### 4.3. 사용자인터페이스설계서
#### 4.3.1 목적
 * 본 사용자인터페이스설계서는 사용자 화면을 플랫폼에 맞게 구현할 수 있도록 웹페이지 및 사용자 인터페이스 제어 역할을 하는 웹 클래스 등의 경로와 물리적 위치를 정의하여, 웹 클래스 및 웹 페이지를 구성하는 페이지를 구성하는 페이지 목록을 설계하는데 목적이 있다.

### 4.4. 데이터베이스설계서
#### 4.4.1 목적
 * 본 데이터베이스설계서는 확정된 데이터 모델링 결과를 바탕으로 개발 대상 시스템에서 사용될 DBMS의 환경에 맞는 물리적 스키마와 DBMS 내장 프로그램, 세부 코드를 설계하는데 목적이 있다.
