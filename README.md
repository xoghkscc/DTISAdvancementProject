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

### 2021.12.20 ~ 2021.12.24
 * 데이터베이스 설계서 작성을 위한 TO-BE 테이블 관계 정리 및 컬럼 단어와 도메인 표준화
 * 데이터베이스 설계서 산출물 작성 수행

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
