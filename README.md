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

### 2022.4.04 ~ 2022.4.08
 * 운전자력 Service, Controller, Mapper 개발
    * Service, Controller, Mapper 연구 및 개발
 * 수송근무 공통코드 분석
 ![KakaoTalk_20220408_205550584](https://user-images.githubusercontent.com/82793713/162431156-db1be989-da65-45bc-bf9d-a535c497d682.jpg)
#### 느낀점:

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
