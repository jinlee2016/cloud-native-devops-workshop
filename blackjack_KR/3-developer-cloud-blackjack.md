# PART III : BlackJack 웹 서비스 응용 프로그램 테스트, 빌드 및 배포

## 리포지토리에서 BlackJack Project 다운로드

로컬 컴퓨터에 [blackjack.zip](BlackJack.zip) 파일 다운로드 

## 로컬 서버에 BlackJack 응용 프로그램 배포

다음 지침에 따라 BlackJack 응용 프로그램을 
Apache Tomcat Server가 프로젝트와 번들로 제공됩니다. 

1. 그래픽 파일 탐색기를 열고**cloud**디렉토리로 이동하십시오. 

2. **cloud**디렉토리 안에 이름이 지정된 디렉토리를 만듭니다. 
**BlackJack**및**BlackJack.zip**파일을 복사하여 
이전 연습에서 다운로드했습니다. 

3. **BlackJack.zip**파일을**클라우드****>**에 압축을 풉니 다. 
**BlackJack**디렉토리. 

4. 바탕 화면의 바로 가기를 사용하여 Netbeans을 시작합니다. 

5. Netbeans에서**blackjack-part2**프로젝트를 엽니 다. 

    <img src="images/3/image1.png" width="314" height="163" />

**참고 :** 프로젝트 이름에 대해 \ [언로드] 태그가 표시되면 
프로젝트를 마우스 오른쪽 버튼으로 클릭하고**프로젝트 문제 해결**을 선택하십시오. 
Resolve 버튼을 클릭하십시오. Netbeans 다운로드가 완료 될 때까지 기다려주세요. 
Maven 관련 파일을 클릭 한 다음 닫기 버튼을 클릭하십시오. 

6. 프로젝트를 마우스 오른쪽 버튼으로 클릭하고**Clean 및**을 선택합니다. 
**빌드**옵션. 

    <img src="images/3/image2.png" width="132" height="167" />

7. 프로젝트를 마우스 오른쪽 단추로 클릭하고**실행**을 선택하여 프로젝트를 배포합니다. 
톰캣 서버. 

    <img src="images/3/image3.png" width="138" height="173" />

8. Available에서**com.example.blackjack.rest.Application**을 선택하십시오. 
Main Classes 목록에서**Select Main Class**버튼을 클릭하십시오. 

    <img src="images/3/image4.png" width="252" height="245" />

9. &quot;시작 응용 프로그램&quot;을 받아야합니다. 
&lt;&lt; 초 >> 초 (5.19 용 JVM 실행)*&quot;에서 메시지 
출력 윈도우. 

    <img src="images/3/image5.png" width="490" height="280" />

**참고 :** 이 프로젝트를 실행하는 데 문제가 발생할 수 있습니다. 
포트 충돌 문제. 이 응용 프로그램은 Apache Tomcat에 배포됩니다. 
서버와 그것을 듣기 위해서는**8080**로컬 포트 ​​번호가 필요합니다. 
클라이언트 요청.**8080**에서 실행중인 서비스를 중지하십시오. 
로컬 포트 ​​번호. 

**TCPView**도구를 사용하여 프로세스를 식별하고 종료 할 수 있습니다. 
이 포트 번호. 

[**Download Link**](https://technet.microsoft.com/en-us/sysinternals/bb897437) 

## 로컬에 배포 된 BlackJack 응용 프로그램 테스트

HTML-5 클라이언트 응용 프로그램이 개발되어 
BlackJack 응용 프로그램은 한번 배포 된 기능을 테스트합니다. 
로컬 / 원격 서버. 

다음 지시 사항에 따라 BlackJack 응용 프로그램을 테스트하십시오. 

1. 그래픽 파일 탐색기를 열고**구름> 
BlackJack> html5-client**디렉토리에 있습니다. 

2. 브라우저로 index.html 파일을 엽니 다. 

3. 첫 x 째 필드 인**서비스**가 채워 졌는지 확인하십시오 
    **<http://127.0.0.1:8080/>** value, enter a number between 1 and 9
두 번째 필드에 입력 한 다음 연결을 클릭하십시오. 

    <img src="images/3/image6.png" width="528" height="229" />

4. 게임 콘솔에 연결되면**디버그 켜기 / 끄기**를 클릭하십시오. 
버튼을 클릭하여 디버그 콘솔을 봅니다. 

    <img src="images/3/image7.png" width="535" height="251" />

UI에서 사용할 수있는**Hit**및**Stand**버튼을 사용하여 
게임하자. 

이 HTML5 클라이언트 애플리케이션은 BlackJack 게임과 상호 작용합니다. 
컴퓨터에서 로컬로 실행되는 Tomcat Server에 배포 된 응용 프로그램입니다. 
완료되면이 HTML5 클라이언트 애플리케이션을 닫습니다. 

## BlackJack 응용 프로그램을위한 응용 프로그램 아카이브 파일 생성

Oracle Application Container Cloud는 Java Platform을 배포하고 실행할 수 있으며, 
Standard Edition (Java SE) 및 Node.js 응용 프로그램을 지원합니다. 첫째, 배포 
응용 프로그램을**압축**압축**응용 프로그램 압축 
Tar (TGZ)**아카이브 파일 (필요한 구성 포함) 
정보. 

다음 지시 사항에 따라 응용 프로그램 아카이브를 작성하십시오. 

1. Netbeans에서 blackjack-part2 애플리케이션을 엽니 다 (그렇지 않은 경우). 
이미 열렸습니다. 

2. 프로젝트를 마우스 오른쪽 버튼으로 클릭하고**Clean**을 클릭하십시오. 

    <img src="images/3/image8.png" width="165" height="192" />

3. 그래픽 파일 탐색기를 열고**구름> BlackJack> 
blackjack-part2**를 만들고 디렉토리 구조를 기록하고 
그것의 내용. 

    <img src="images/3/image9.png" width="444" height="102" />

**참고 :** manifest.json 파일은 모든 응용 프로그램에 필요합니다. 
Oracle Application Container Cloud Service에 배포됩니다. 이 파일 
.zip, .tar 또는 .tar.gz의 루트 디렉토리에 존재하지 않습니다. 
파일, 배포가 실패합니다. 최소한이 파일은 
런타임 환경의 주 버전 및 실행 명령. 

**이 예제에서 manifest.json 파일의 내용**: 

    ```json
    {
      "runtime": {
        "majorVersion": "8"
      },
      "command": "java -jar blackjack-part2-1.0.jar",
      "release": {
        "version": "1.0",
        "build": "1",
        "commit": "1A2B345"
      },
      "notes": "Blackjack Web Service"
    }
    ```

4. Netbeans로 전환하고 프로젝트를 마우스 오른쪽 단추로 클릭 한 다음**Build를 클릭하십시오.**

    <img src="images/3/image10.png" width="184" height="237" />

5. **구름> BlackJack> Blackjack-part2**로 전환하십시오. 
디렉토리에 복사하여**target**이라는 새 디렉토리 
생성됩니다. 

6. **target**디렉토리를 검사하십시오.**. zip 및 
.tar.gz**배포 파일이 생성되었습니다. 이것들은 
OACCS에 배포하는 데 사용할 수있는 응용 프로그램 아카이브 파일 

    <img src="images/3/image11.png" width="466" height="178" />

## 개발자 클라우드 서비스에서 새 프로젝트 만들기

다음 지시 사항에 따라 개발자에게 빈 프로젝트를 만듭니다. 
클라우드 서비스 

1. oracle 클라우드 계정에 로그인하십시오. 

2. 대시 보드에서**개발자 클라우드 서비스**를 클릭하여 
**ServiceDetails : developer85599 (Oracle Developer 
클라우드 서비스)**페이지. 

    <img src="images/3/image12.png" width="466" height="137" />

3. **서비스 콘솔 열기**버튼을 클릭하십시오. 

    <img src="images/3/image13.png" width="460" height="225" />

4. **새 프로젝트**를 클릭하십시오. 

    <img src="images/3/image14.png" width="378" height="232" />

5. 다음과 같이 프로젝트 이름과 설명을 입력하십시오 
스크린 샷을 클릭하고**다음**을 클릭하십시오. 

    <img src="images/3/image15.png" width="378" height="268" />

6. **빈 프로젝트**템플릿 및**다음**을 클릭하십시오. 

    <img src="images/3/image16.png" width="378" height="271" />

7. Wiki Markup 드롭 다운 목록에서**MARKDOWN**을 선택하고 
**끝.**

    <img src="images/3/image17.png" width="388" height="280" />

8. Provisioning BlackJack-Part2 프로젝트는 몇 분이 걸릴 수 있습니다. 기다림 
모든 모듈이 프로비저닝되고 모듈로 리디렉션 될 때까지 
블랙 잭 - 파트 2 홈 스크린. 

    <img src="images/3/image18.png" width="444" height="161" />

## 개발자 클라우드 서비스에서 GIT 저장소 만들기

다음 지침에 따라 빈 GIT 저장소를 만듭니다. 
개발자 클라우드 서비스. 

1. **REPOSITORIES**섹션에서**New Repository**버튼을 클릭하십시오. 

    <img src="images/3/image19.png" width="426" height="154" />

2. 새 저장소 창에서 저장소 이름을 입력하고 
설명을 클릭하고**만들기**를 클릭하십시오. 

    <img src="images/3/image20.png" width="426" height="362" />

3. 저장소를 만드는 데 몇 분이 걸릴 수 있습니다. 때까지 기다리십시오. 
BlackJack-Part2Repo 저장소가 생성되고 해당 저장소로 리디렉션됩니다. 
홈페이지. 

    <img src="images/3/image21.png" width="426" height="112" />

4. BlackJack-Part2Repo 홈페이지에서 HTTP 탭을 클릭하고 복사하십시오. 
URL. 

    <img src="images/3/image22.png" width="546" height="143" />

## GIT 저장소 복제

BlackJack-Part2 프로젝트를 복제하려면 다음 지침을 따르십시오. 
개발자 클라우드 서비스의 GIT 저장소. 

1. GIT 저장소를 복제하려면 먼저 클라우드 / 블랙 잭으로 변경하십시오 
디렉토리는 저장소의 루트 디렉토리입니다. 

2. `git clone`을 실행합니다. https : //ora1@developer.em2.oraclecloud.com/developer85599-ouopc084/s/developer85599-ouopc084 \ _blackjack-part2 \ _4112 / scm / BlackJack-Part2Repo.git` 

    <img src="images/3/image23.png" width="507" height="166" />

**노트:** 

- 메시지가 나타나면 클라우드 계정 사용자 이름과 암호를 입력하십시오. 
- 사용자 이름과 암호를 입력하라는 메시지가 표시되지 않고 
명령이 403 오류와 함께 실패하면 명시 적으로 암호를 언급합니다. 
GIT 저장소 URL 예를 들면 :`git clonehttps : //ora1@developer.em2.oraclecloud.com/developer85599-ouopc084/s/developer85599-ouopc084 \ _blackjack-part2 \ _4112 / scm / BlackJack-Part2Repo.git` 
-이 명령의 출력은 다음 명령의 출력과 유사해야합니다. 
위의 스크린 샷. 

3. **BlackJack-Part2Repo**라는 새 디렉토리가 있습니다. 
**cloud / BlackJack**디렉토리에 생성됩니다. 

4. **blackjack-part2**프로젝트 디렉토리를 복사하여 붙여 넣기하십시오. 
**cloud / BlackJack**디렉토리**BlackJack-Part2Repo**디렉토리 

**참고 :** **BlackJack-Part2Repo**디렉토리의 내용은 
아래 스크린 샷의 내용과 일치해야합니다. 

    <img src="images/3/image24.png" width="535" height="94" />

5. **BlackJack-Part2Repo**디렉토리로 변경하십시오. 

cd 블랙 잭 -Part2Repo 

6. 프로젝트 루트 디렉토리에서 GIT에 소스 파일을 추가하십시오 

자식 추가. 

7. 변경 사항 적용 

git commit -m &quot;BlackJack-Part2Repo 저장소 변경 커밋&quot; 

8. 개발자 클라우드 서비스의 저장소로 파일을 푸시합니다. 

git push origin master 

**참고 :** 모든 파일이 저장소로 푸시 될 때까지 기다리십시오. 

9. 개발자 클라우드 서비스로 전환하여 개발자 클라우드 서비스로 푸시 된 파일을 확인합니다. 
저장소 

10 .**BlackJack-Part2**홈 페이지에서**BlackJack-Part2Repo.git**을 클릭하십시오. 

    <img src="images/3/image25.png" width="474" height="178" />

11 .**blackjack-part2**프로젝트 디렉토리가 푸시되었습니다. 
개발자 클라우드 서비스의 저장소 그것을 클릭하고 확인하십시오. 
그것의 내용. 

    <img src="images/3/image26.png" width="478" height="154" />

## 개발자 클라우드 서비스에 대한 프로젝트 빌드

다음 지침에 따라 BlackJack-Part2 프로젝트를 빌드하십시오. 
개발자 클라우드 서비스. 

1. 왼쪽 탐색 분할 창에서**빌드**를 누른 다음**새 작업**을 누르십시오. 

    <img src="images/3/image27.png" width="421" height="190" />

2. 새 작업 창에서**BlackJack-Part2BuildJob**을 입력하십시오 
이름 입력란을 클릭하고**저장**을 클릭하십시오. 

    <img src="images/3/image28.png" width="421" height="147" />

3. **주**탭에서 다음 값을 입력하십시오. 

- 조정이 필요한 경우 작업 이름을 편집하십시오. 
- 설명을 입력하십시오. 
-**JDK**를**JDK 8로 설정하십시오.**

    <img src="images/3/image29.png" width="421" height="188" />

4. **소스 제어**탭을 클릭하십시오. 

-**Git**를 저장소로 선택하십시오. 
-**URL**의 경우 Git 저장소의 URL을 선택하십시오. 

    <img src="images/3/image30.png" width="391" height="203" />

5. **트리거**탭을 클릭하십시오. 

- SCM 폴링 일정에 기반 

    <img src="images/3/image31.png" width="391" height="178" />

**참고 :** 이 설정은 DevCS의 자동 배포 기능을 활성화합니다. 후 
응용 프로그램이 수정되고 변경 사항이 GIT에 위임 된 경우 
DevCS의 저장소에서 업데이트 된 코드를 자동으로 선택하고 
배치. 

6. **빌드 단계**탭을 클릭하십시오. 

- 빌드 단계 추가를 클릭하고 Maven 3 호출을 선택하십시오. 
-**목표**를 클린 패키지로 설정하십시오. 
-**POM 파일**위치를 blackjack-part2 / pom.xml로 설정하십시오. 

    <img src="images/3/image32.png" width="397" height="171" />
    <img src="images/3/image33.png" width="397" height="216" />

7. **Post Build**탭을 클릭하십시오. 

- 아티팩트 아카이브를 선택하십시오. 
-**보관할 파일**을 blackjack-part2 / target / blackjack-part2-1.0.jar로 설정합니다. 
blackjack-part2 / target / blackjack-part2-1.0-dist.zip 
- 압축 유형을**NONE**으로 설정하십시오. 

    <img src="images/3/image34.png" width="451" height="186" />

8. **저장**을 클릭 한 다음**지금 빌드**를 클릭하십시오. 

빌드가 성공적으로 완료되면**마지막 성공 빌드의 아티팩트**섹션에 두 개의 파일이 표시됩니다. 
- blackjack-part2 / target / blackjack-part2-1.0.jar 
- blackjack-part2 / target / blackjack-part2-1.0-dist.zip 

파일 이름을 클릭하여 다운로드 할 수 있습니다. 

빌드가 실패한 경우 다시 빌드 작업 구성을 확인하십시오. 
또는**Git Logs**를 클릭하여 오류에 대한 추가 정보를 확인하십시오. 

    <img src="images/3/image35.png" width="451" height="181" />

## DevCS에서 ACCS로 프로젝트 배포

다음 지침에 따라 BlackJack-Part2를 
개발자 클라우드 서비스의 응용 프로그램 컨테이너 클라우드 서비스. 

1. 왼쪽 탐색 창에서**배포**를 클릭 한 다음**새로 만들기를 클릭하십시오. 
구성**

    <img src="images/3/image36.png" width="436" height="171" />

2. **새 배포 구성**페이지에서 다음을 입력합니다. 
**구성 이름**및**응용 프로그램 이름**

    <img src="images/3/image37.png" width="436" height="173" />

3. **Deployment Target**필드에서**New**를 클릭하고 
**응용 프로그램 컨테이너 클라우드**를 선택하십시오. 

    <img src="images/3/image38.png" width="233" height="119" />

4. **응용 프로그램 컨테이너 클라우드에 배포**창에서 다음을 입력합니다. 
값을 클릭하고**연결 테스트**를 클릭하십시오. 

- 데이터 센터 
- ID 도메인 
- 사용자 이름 
- 비밀번호 

    <img src="images/3/image39.png" width="273" height="131" />

5. **성공**메시지가 표시되면**연결 사용**을 클릭하십시오. 

    <img src="images/3/image40.png" width="273" height="131" />

6. 다음 값을 입력하고**저장**을 클릭하십시오. 

-**유형**: 자동 (선택 : 안정된 빌드 만 배포) 
-**Job :** BlackJack - Part2BuildJob 
-**런타임**: Java 
-**구독 :** 월간 
-**아티팩트 :** 블랙 잭 - 파트 2 / 타겟 / 블랙 잭 - 파트 2 - 1.0-리스트 .zip 

    <img src="images/3/image41.png" width="393" height="137" />

7.  Click the gear icon <img src="images/3/image42.png" width="51" height="28" />
**시작**을 선택하여 Oracle에 응용 프로그램을 배포하십시오 
응용 프로그램 컨테이너 클라우드 서비스. 

8. 성공적인 배포 후 Blackjack-Part2를 마우스 오른쪽 단추로 클릭합니다. 
프로젝트 이름 및 URL 복사 

    <img src="images/3/image43.png" width="393" height="130" />

## DevCS에서 OACCS에 배포 된 BlackJack 응용 프로그램 테스트

HTML-5 클라이언트 응용 프로그램이 개발되어 
BlackJack 응용 프로그램은 한번 배포 된 기능을 테스트합니다. 
로컬 / 원격 서버. 

다음 지시 사항에 따라 BlackJack 응용 프로그램을 테스트하십시오. 

1. 그래픽 파일 탐색기를 열고**구름> 
BlackJack> html5-client**디렉토리에 있습니다. 

2. 브라우저로 index.html 파일을 엽니 다. 

3. 첫 번째 필드**서비스**에 
이전 연습에서 복사 한 URL, 
    <https://blackjack-part2-ouopc084.apaas.em2.oraclecloud.com/>. Enter a
두 번째 필드에서 1과 9 사이의 숫자를 입력 한 다음 연결을 클릭하십시오. 

    <img src="images/3/image44.png" width="513" height="230" />

4. 게임 콘솔에 연결되면**디버그 켜기 / 끄기**를 클릭하십시오. 
버튼을 클릭하여 디버그 콘솔을 봅니다. 

    <img src="images/3/image45.png" width="513" height="247" />

**참고 :** **히트**및**스탠드**버튼을 사용할 수 있습니다 
게임을하기위한 UI. 

이 HTML5 클라이언트 애플리케이션은 BlackJack 게임과 상호 작용합니다. 
클라우드의 OACCS에 배포 된 응용 프로그램 
