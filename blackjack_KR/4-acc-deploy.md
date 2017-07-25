# IV 부 : Oracle Application Container Cloud에 BlackJack WebService 응용 프로그램 직접 배포


## Oracle Application Container 클라우드 서비스 (OACCS) 활성화


**중요 사항 :** 클라우드 로그인 자격 증명 및 링크는 랩을 수행하는 데 필요합니다. 오라클로부터 받은 이메일에서 확인하실 수 있습니다.

이 문서를 작성하기 위해 EMEA Local 데이터 센터의 클라우드 인스턴스가 사용되었습니다. NAMER Local 데이터 센터에서 클라우드 인스턴스를 얻을 수 있습니다. 이에 따라 데이터 센터를 선택하십시오. 

Oracle Application Container Cloud Service는 Java Platform, Standard Edition (Java SE) 및 Node.js 애플리케이션을 배포 및 실행할 수 있습니다. 이 액티비티에서는 이전 활동에서 작성한 애플리케이션 아카이브 파일을 사용하여 ACJ에 BlackJack 애플리케이션을 배포하는 방법을 배우게됩니다. 

다음 지침에 따라 BlackJack 응용 프로그램을 사용자 인터페이스에서 ACCS에 배포하십시오. 

1. Oracle Cloud 계정에 로그인하십시오 (로그인 방법에 대한 자세한 내용은 **개발자 클라우드 서비스 활성화**활동 참조) 

2. 로그인이 성공하면 시작 페이지에서**ID 도메인 이름**및**사용자 이름**을 볼 수 있습니다. 

    <img src="images/4/image1.png" width="360" height="145" />


3. 계정에 지정된 서비스가 대시 보드에 표시됩니다.**Application Container**서비스가 보이지 않으면 대시 보드에 **Application Container**의 **Show**버튼을 표시하여 **대시 보드 사용자 정의 **버튼과 **Show**버튼을 표시하십시오. 

    <img src="images/4/image2.png" width="360" height="174" />


4. 대시 보드에서**Application Container**를 클릭하여**Service Details : Oracle Application Container Cloud**페이지로 이동하십시오. 

    <img src="images/4/image3.png" width="324" height="111" />


## OACCS에 BlackJack 응용 프로그램 직접 배포


이 액티비티에서는 응용 프로그램 아카이브를 ACCS에 직접 배포하는 방법을 배우게됩니다. 우리는이 배포에도 동일한 샘플 응용 프로그램 인 BlackJack을 사용하고 있습니다. 

다음 지시 사항에 따라 BlackJack 응용 프로그램을 OACCS에 직접 배포하십시오. 

1. **서비스 콘솔 열기**버튼을 클릭하십시오. 

    <img src="images/4/image4.png" width="385" height="148" />


2. **응용 프로그램 만들기**및**Java SE**단추**를 클릭하십시오.**

    <img src="images/4/image5.png" width="261" height="170" />


3. **응용 프로그램 만들기 **대화 상자에서 응용 프로그램 이름으로 BlackJack-part3을 입력하고 구독 유형으로 **Monthly**을 선택하고 메모 필드에 **BlackJack 응용 프로그램 배포를 ACCS에 직접**로 입력하십시오. 응용 프로그램 아카이브 필드에 대해 **아카이브 업로드**를 선택하십시오. 

    <img src="images/4/image6.png" width="248" height="291" />


4. **target**디렉토리에서**blackjack-part2-1.0-dist.zip**파일을 찾아 선택하십시오. 

    <img src="images/4/image7.png" width="366" height="221" />


5. **응용 프로그램 생성 대화 상자에 선택한 파일이 표시됩니다. **인스턴스**에서 인스턴스 수와 메모리 크기를 검토하고 필요한 사항을 조정하십시오.**작성**을 클릭하여 애플리케이션을 Oracle Application Container Cloud에 배포하십시오. 

    <img src="images/4/image8.png" width="225" height="263" />


6. **아카이브 아카이브**임을 나타내는 상태 메시지가 나타납니다. 

    <img src="images/4/image9.png" width="295" height="207" />


7. 아카이브 된 응용 프로그램이 업로드되면 서비스는 아카이브가 제대로 구성되었는지 여부를 판별합니다. 일치하면 다음 대화 상자가 나타납니다. **확인**을 클릭하십시오. 

    <img src="images/4/image10.png" width="270" height="125" />


8. 응용 프로그램을 배포하는 데 몇 분이 걸립니다. 전개 상태는 진행중인 활동 섹션에서 볼 수 있습니다. 

    <img src="images/4/image11.png" width="348" height="228" />


9. 응용 프로그램이 성공적으로 배포되면 활동 섹션에 **Status : Succeeded**메시지가 표시됩니다. 

    <img src="images/4/image12.png" width="480" height="112" />


10. 응용 프로그램 URL을 복사하여 메모장에 붙여 넣습니다. 테스트 목적으로이 URL이 필요합니다. 

    <img src="images/4/image13.png" width="486" height="147" />


## OACCS에 배포 된 BlackJack 응용 프로그램 테스트


HTML-5 클라이언트 응용 프로그램이 개발되어 BlackJack 응용 프로그램과 함께 제공되면 로컬 / 원격 서버에 배포 된 기능을 테스트합니다. 

다음 지시 사항에 따라 BlackJack 응용 프로그램을 테스트하십시오. 

1. 그래픽 파일 탐색기를 열고**구름> BlackJack> html5-client**디렉토리로 이동하십시오. 

2. 브라우저로 index.html 파일을 엽니 다. 

3. 첫 번째 필드 인 **서비스**에 이전 Lab에서 복사한 URL인 <https://blackjack-part3-ouopc084.apaas.em2.oraclecloud.com/>를 넣으십시오.
두 번째 필드에 1에서 9 사이의 숫자를 입력 한 다음 연결을 클릭하십시오. 

    <img src="images/4/image14.png" width="520" height="141" />


4. 게임 콘솔에 연결되면**디버그 켜기 / 끄기**버튼을 클릭하여 디버그 콘솔을 표시합니다. 

    <img src="images/4/image15.png" width="513" height="247" />


**참고 :** UI에서 사용 가능한**Hit**및**Stand**버튼을 사용하여 게임을 할 수 있습니다. 

이 HTML5 클라이언트 애플리케이션은 클라우드의 OACCS에 배포 된 BlackJack 게임 애플리케이션과 상호 작용합니다. 

이를 통해 사용자 인터페이스 및 테스트를 사용하여 ACCS에 BlackJack 응용 프로그램을 직접 배포하는 작업을 성공적으로 마쳤습니다.