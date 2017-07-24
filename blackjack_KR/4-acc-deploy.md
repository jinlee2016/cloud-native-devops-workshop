# IV 부 : Oracle Application Container Cloud에 BlackJack WebService 응용 프로그램 직접 배포

## Oracle Application Container 클라우드 서비스 (OACCS) 활성화

**중요 사항 :** 클라우드 로그인 자격 증명 및 링크는 
실험실 활동의이 부분을 수행하십시오. 이 정보를 
귀하가 오라클로부터받은 이메일을 편리하게 보관하십시오. 

이 문서를 작성하기 위해 
EMEA 지역 데이터 센터가 사용되었습니다. 에서 클라우드 인스턴스를 가져옵니다. 
NAMER 지역 데이터 센터; 이에 따라 데이터 센터를 선택하십시오. 

Oracle Application Container Cloud Service는 Java를 배포 및 실행할 수 있습니다. 
Platform, Standard Edition (Java SE) 및 Node.js 응용 프로그램을 지원합니다. 이 
액티비티를 사용하여 BlackJack 애플리케이션을 ACCS에 
이전 활동에서 작성한 애플리케이션 아카이브 파일 

다음 지침에 따라 BlackJack 응용 프로그램을 ACCS에 배포하십시오. 
사용자 인터페이스에서. 

1. Oracle Cloud 계정에 로그인하십시오 (**개발자 활성화 참조). 
클라우드 서비스**활동 (로그인 방법에 대한 자세한 지침 참조) 

2. 로그인에 성공하면**ID 도메인 이름**및 
시작 페이지의**사용자 이름**. 

    <img src="images/4/image1.png" width="360" height="145" />

3. 귀하의 계정에 지정된 서비스가에 표시됩니다. 
대시 보드.**응용 프로그램 컨테이너**서비스가 아닌 경우 
표시하려면**대시 보드 사용자 정의**버튼을 클릭하고**표시**
**응용 프로그램 컨테이너**에 대한 버튼 
대시 보드. 

    <img src="images/4/image2.png" width="360" height="174" />

4. 대시 보드에서**Application Container**를 클릭하여 
**서비스 세부 정보 : Oracle Application Container Cloud**페이지. 

    <img src="images/4/image3.png" width="324" height="111" />

## OACCS에 BlackJack 응용 프로그램 직접 배포

이 액티비티에서는 응용 프로그램 아카이브를 다음 위치에 배포하는 방법을 배우게됩니다. 
ACCS에 직접. 우리는 동일한 샘플 애플리케이션 인 BlackJack for 
이 배포 역시 마찬가지입니다. 

다음 지침에 따라 BlackJack 응용 프로그램을 
OACCS에 직접. 

1. **서비스 콘솔 열기**버튼을 클릭하십시오. 

    <img src="images/4/image4.png" width="385" height="148" />

2. **응용 프로그램 만들기**및**Java SE**단추**를 클릭하십시오.**

    <img src="images/4/image5.png" width="261" height="170" />

3. **응용 프로그램 만들기**대화 상자에서 BlackJack-part3 for를 입력하십시오. 
응용 프로그램 이름, 구독 유형으로****매월**을 선택하고, 
**BlackJack 응용 프로그램을 ACCS에 직접 배포**에 입력하십시오. 
메모 필드 응용 프로그램 아카이브 필드에서**업로드를 선택하십시오. 
자료실**. 

    <img src="images/4/image6.png" width="248" height="291" />

4. 찾아보기에서**blackjack-part2-1.0-dist.zip**파일을 선택하십시오. 
**target**디렉토리. 

    <img src="images/4/image7.png" width="366" height="221" />

5. **응용 프로그램 생성 대화 상자에 선택한 파일이 표시됩니다. 
**인스턴스**에서 인스턴스 수와 메모리를 검토합니다. 
크기를 조정하고 필요한 조정을하십시오. 배치하려면**작성**을 클릭하십시오. 
귀하의 애플리케이션을 Oracle Application Container Cloud로 마이그레이션하십시오. 

    <img src="images/4/image8.png" width="225" height="263" />

6. **아카이브 아카이브**임을 나타내는 상태 메시지가 나타납니다. 

    <img src="images/4/image9.png" width="295" height="207" />

7. 보관 된 응용 프로그램이 업로드 된 후 서비스가 다음을 결정합니다. 
아카이브가 제대로 구성되었는지 여부 그렇다면 다음과 같습니다. 
대화 상자가 나타납니다.**확인**을 클릭하십시오. 

    <img src="images/4/image10.png" width="270" height="125" />

8. 응용 프로그램을 배포하는 데 몇 분이 걸립니다. 그만큼 
진행 상태는 진행중인 상태에서 볼 수 있습니다. 
활동 섹션. 

    <img src="images/4/image11.png" width="348" height="228" />

9. 활동에**Status : Succeeded**메시지가 나타납니다. 
섹션을 참조하십시오. 

    <img src="images/4/image12.png" width="480" height="112" />

10 . 응용 프로그램 URL을 복사하여 메모장에 붙여 넣습니다. 우리는 필요할 것이다. 
이 URL은 테스트 용입니다. 

<img src="images/4/image13.png" width="486" height="147" />

## OACCS에 배포 된 BlackJack 응용 프로그램 테스트

HTML-5 클라이언트 응용 프로그램이 개발되어 
BlackJack 응용 프로그램은 한번 배포 된 기능을 테스트합니다. 
로컬 / 원격 서버. 

다음 지시 사항에 따라 BlackJack 응용 프로그램을 테스트하십시오. 

1. 그래픽 파일 탐색기를 열고**구름> 
BlackJack> html5-client**디렉토리에 있습니다. 

2. 브라우저로 index.html 파일을 엽니 다. 

3. 첫 번째 필드 인**서비스**에 
    URL you copied in the previous exercise, <https://blackjack-part3-ouopc084.apaas.em2.oraclecloud.com/> .
두 번째 입력란에 1에서 9 사이의 숫자를 입력하고 
연결을 클릭하십시오. 

    <img src="images/4/image14.png" width="520" height="141" />

4. 게임 콘솔에 연결되면**디버그 켜기 / 끄기**를 클릭하십시오. 
버튼을 클릭하여 디버그 콘솔을 봅니다. 

    <img src="images/4/image15.png" width="513" height="247" />

**참고 :** **히트**및**스탠드**버튼을 사용할 수 있습니다 
게임을하기위한 UI. 

이 HTML5 클라이언트 애플리케이션은 BlackJack 게임과 상호 작용합니다. 
클라우드의 OACCS에 배포 된 응용 프로그램 

이를 통해 BlackJack 배포가 성공적으로 완료되었습니다. 
사용자 인터페이스 및 테스트를 사용하여 ACCS에 직접 적용 할 수 있습니다. 
