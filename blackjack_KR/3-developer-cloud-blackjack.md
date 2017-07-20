# PART III : BlackJack 웹 서비스 응용 프로그램 테스트, 빌드 및 배포

## 리포지토리에서 BlackJack Project 다운로드

로컬 컴퓨터에 [blackjack.zip](BlackJack.zip) 파일 다운로드 

## 로컬 서버에 BlackJack 응용 프로그램 배포

다음 지침에 따라 BlackJack 응용 프로그램을 
Apache Tomcat Server가 프로젝트와 번들로 제공됩니다. 

1. 그래픽 파일 탐색기를 열고**cloud**디렉토리로 이동하십시오. 

2.**cloud**디렉토리 안에 이름이 지정된 디렉토리를 만듭니다. 
    **BlackJack** and copy the **BlackJack.zip** file that you
    downloaded in the earlier exercise.

3.**BlackJack.zip**파일을**클라우드****>**에 압축을 풉니 다. 
    **BlackJack** directory.

4. 바탕 화면의 바로 가기를 사용하여 넷빈을 실행합니다. 

5. Netbeans에서**blackjack-part2**프로젝트를 엽니 다. 

    <img src="images/3/image1.png" width="314" height="163" />

    **Note:** If you see a \[Unloaded\] tag against the project name then
    right-click on the project and select, **Resolve Project Problems**
    and then click on Resolve button. Please wait until Netbeans downloads
    the Maven related files then click on close button.

6. 프로젝트를 마우스 오른쪽 버튼으로 클릭하고**Clean 및**을 선택합니다. 
    **Build** option.

    <img src="images/3/image2.png" width="132" height="167" />

7. 프로젝트를 마우스 오른쪽 단추로 클릭하고**실행**을 선택하여 프로젝트를 배포합니다. 
    Tomcat Server.

    <img src="images/3/image3.png" width="138" height="173" />

8. Available에서**com.example.blackjack.rest.Application**을 선택하십시오. 
    Main Classes list and click the **Select Main Class** button.

    <img src="images/3/image4.png" width="252" height="245" />

9. &quot;시작 응용 프로그램&quot;을 받아야합니다. 
    &lt;&lt;seconds&gt;&gt; seconds (JVM running for 5.19)*” message in
    the Output window.

    <img src="images/3/image5.png" width="490" height="280" />

    **Note:** You may encounter a problem in running this project due to a
    port conflict issue. This application will be deployed to Apache Tomcat
    Server and it requires **8080** local port number to listen to the
    client request. Make sure you stop the services running on **8080**
    local port number.

    **TCPView** tool can be used to identify and terminate the process using
    this port number.

    AAAA

## 로컬에 배포 된 BlackJack 응용 프로그램 테스트

HTML-5 클라이언트 응용 프로그램이 개발되어 
BlackJack 응용 프로그램은 한번 배포 된 기능을 테스트합니다. 
로컬 / 원격 서버. 

다음 지시 사항에 따라 BlackJack 응용 프로그램을 테스트하십시오. 

1. 그래픽 파일 탐색기를 열고**구름> 
    BlackJack > html5-client** directory.

2. 브라우저로 index.html 파일을 엽니 다. 

3. 첫 x 째 필드 인**서비스**가 채워 졌는지 확인하십시오 
    **<http://127.0.0.1:8080/>** value, enter a number between 1 and 9
    in the second field, and then click Connect.

    <img src="images/3/image6.png" width="528" height="229" />

4. 게임 콘솔에 연결되면**디버그 켜기 / 끄기**를 클릭하십시오. 
    button to view the Debug console.

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
    opened already.

2. 프로젝트를 마우스 오른쪽 버튼으로 클릭하고**Clean**을 클릭하십시오. 

    <img src="images/3/image8.png" width="165" height="192" />

3. 그래픽 파일 탐색기를 열고**구름> BlackJack> 
    blackjack-part2**, and make a note of the directory structure and
    its contents.

    <img src="images/3/image9.png" width="444" height="102" />

    **Note:** The manifest.json file is required for all applications
    deployed to Oracle Application Container Cloud Service. If this file
    is not present in the root directory of the .zip, .tar, or .tar.gz
    file, deployment will fail. At a minimum, this file specifies the
    major version of the runtime environment and the launch command.

    **Content of manifest.json file in this example**:

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

5.**구름> BlackJack> Blackjack-part2**로 전환하십시오. 
    directory and notice that a new directory named **target**
    is created.

6.**target**디렉토리를 검사하십시오.**. zip 및 
    .tar.gz** distribution files have been generated. These are
    application archive files that we can use to deploy to OACCS.

    <img src="images/3/image11.png" width="466" height="178" />

## 개발자 클라우드 서비스에서 새 프로젝트 만들기

다음 지시 사항에 따라 개발자에게 빈 프로젝트를 만듭니다. 
클라우드 서비스 

1. oracle 클라우드 계정에 로그인하십시오. 

2. 대시 보드에서**개발자 클라우드 서비스**를 클릭하여 
    **ServiceDetails:developer85599 (Oracle Developer
    Cloud Service)** page.

    <img src="images/3/image12.png" width="466" height="137" />

3.**서비스 콘솔 열기**버튼을 클릭하십시오. 

    <img src="images/3/image13.png" width="460" height="225" />

4.**새 프로젝트**를 클릭하십시오. 

    <img src="images/3/image14.png" width="378" height="232" />

5. 다음과 같이 프로젝트 이름과 설명을 입력하십시오 
    screenshot and click **Next**.

    <img src="images/3/image15.png" width="378" height="268" />

6.**빈 프로젝트**템플릿 및**다음**을 클릭하십시오. 

    <img src="images/3/image16.png" width="378" height="271" />

7. Wiki Markup 드롭 다운 목록에서**MARKDOWN**을 선택하고 
    **Finish.**

    <img src="images/3/image17.png" width="388" height="280" />

8. Provisioning BlackJack-Part2 프로젝트는 몇 분이 걸릴 수 있습니다. 기다림 
    until all the modules are provisioned and redirected to the
    BlackJack-Part2 home screen.

    <img src="images/3/image18.png" width="444" height="161" />

## 개발자 클라우드 서비스에서 GIT 저장소 만들기

다음 지침에 따라 빈 GIT 저장소를 만듭니다. 
개발자 클라우드 서비스. 

1.**REPOSITORIES**섹션에서**New Repository**버튼을 클릭하십시오. 

    <img src="images/3/image19.png" width="426" height="154" />

2. 새 저장소 창에서 저장소 이름을 입력하고 
    description as shown in the following screenshot and click **Create**.

    <img src="images/3/image20.png" width="426" height="362" />

3. 저장소를 만드는 데 몇 분이 걸릴 수 있습니다. 때까지 기다리십시오. 
    BlackJack-Part2Repo repository is created and redirected to its
    home page.

    <img src="images/3/image21.png" width="426" height="112" />

4. BlackJack-Part2Repo 홈페이지에서 HTTP 탭을 클릭하고 복사하십시오. 
    the URL.

    <img src="images/3/image22.png" width="546" height="143" />

## GIT 저장소 복제

BlackJack-Part2 프로젝트를 복제하려면 다음 지침을 따르십시오. 
개발자 클라우드 서비스의 GIT 저장소. 

1. GIT 저장소를 복제하려면 먼저 클라우드 / 블랙 잭으로 변경하십시오 
    directory that is the root directory for your repository.

2.`git clone`을 실행합니다. https : //ora1@developer.em2.oraclecloud.com/developer85599-ouopc084/s/developer85599-ouopc084 \ _blackjack-part2 \ _4112 / scm / BlackJack-Part2Repo.git` 

    <img src="images/3/image23.png" width="507" height="166" />

    **Notes:**

    -   Enter your cloud account username and password, if you are prompted.
    -   If you are not prompted for user name and password and if this
        command fails with 403 error then mention the password explicitly
        the GIT repository URL. For example: `git clone https://ora1@developer.em2.oraclecloud.com/developer85599-ouopc084/s/developer85599-ouopc084\_blackjack-part2\_4112/scm/BlackJack-Part2Repo.git`
    -   The output of this command should be similar to the output in the
        above screenshot.

3.**BlackJack-Part2Repo**라는 새 디렉토리가 있습니다. 
    created inside **cloud/BlackJack** directory.

4.**blackjack-part2**프로젝트 디렉토리를 복사하여 붙여 넣기하십시오. 
    **cloud/BlackJack** directory to **BlackJack-Part2Repo** directory

    **Note:** Content of the **BlackJack-Part2Repo** directory should
    match with the contents listed below screenshot.

    <img src="images/3/image24.png" width="535" height="94" />

5.**BlackJack-Part2Repo**디렉토리로 변경하십시오. 

        cd BlackJack-Part2Repo

6. 프로젝트 루트 디렉토리에서 GIT에 소스 파일을 추가하십시오 

        git add .

7. 변경 사항 적용 

        git commit –m "commiting changes to BlackJack-Part2Repo repository"

8. 개발자 클라우드 서비스의 저장소로 파일을 푸시합니다. 

        git push origin master

    **Note:** Wait until all the files are pushed to repository

9. 개발자 클라우드 서비스로 전환하여 개발자 클라우드 서비스로 푸시 된 파일을 확인합니다. 
    repository

10.**BlackJack-Part2**홈 페이지에서**BlackJack-Part2Repo.git**을 클릭하십시오. 

    <img src="images/3/image25.png" width="474" height="178" />

11.**blackjack-part2**프로젝트 디렉토리가 푸시되었습니다. 
    repository on Developer Cloud Service. Click on it and verify
    its contents.

    <img src="images/3/image26.png" width="478" height="154" />

## 개발자 클라우드 서비스에 대한 프로젝트 빌드

다음 지침에 따라 BlackJack-Part2 프로젝트를 빌드하십시오. 
개발자 클라우드 서비스. 

1. 왼쪽 탐색 분할 창에서**빌드**를 누른 다음**새 작업**을 누르십시오. 

    <img src="images/3/image27.png" width="421" height="190" />

2. 새 작업 창에서**BlackJack-Part2BuildJob**을 입력하십시오 
    name field and click on **Save**.

    <img src="images/3/image28.png" width="421" height="147" />

3.**주**탭에서 다음 값을 입력하십시오. 

    -   Edit the job name if it needs adjusting.
    -   Enter a description.
    -   Set the **JDK** to **JDK 8.**

    <img src="images/3/image29.png" width="421" height="188" />

4.**소스 제어**탭을 클릭하십시오. 

    -   Select **Git** as your repository.
    -   For **URL**, select the URL to your Git repository.

    <img src="images/3/image30.png" width="391" height="203" />

5.**트리거**탭을 클릭하십시오. 

    -   Based on SCM polling schedule

    <img src="images/3/image31.png" width="391" height="178" />

    **Note:** This setting will enable auto-deploy feature of DevCS. After
    the application is modified and if the changes are committed to GIT
    repository on DevCS, it automatically picks up the updated code and
    deploys.

6.**빌드 단계**탭을 클릭하십시오. 

    -   Click Add Build Step and select Invoke Maven 3.
    -   Set the **Goals** to: clean package.
    -   Set the **POM File** location to: blackjack-part2/pom.xml

    <img src="images/3/image32.png" width="397" height="171" />
    <img src="images/3/image33.png" width="397" height="216" />

7.**Post Build**탭을 클릭하십시오. 

    -   Select Archive the artifacts.
    -   Set **Files To Archive** to: blackjack-part2/target/blackjack-part2-1.0.jar,
        blackjack-part2/target/blackjack-part2-1.0-dist.zip
    -   Set Compression Type to **NONE**.

    <img src="images/3/image34.png" width="451" height="186" />

8.**저장**을 클릭 한 다음**지금 빌드**를 클릭하십시오. 

    If the build was successful, you'll see two files in the **Artifacts of Last Successful Build** section:
    -   blackjack-part2/target/blackjack-part2-1.0.jar
    -   blackjack-part2/target/blackjack-part2-1.0-dist.zip

    You can download them by clicking the file name.

    If the build failed then go back to check the build job configuration
    or click **Git Logs** to see more information about the error.

    <img src="images/3/image35.png" width="451" height="181" />

## DevCS에서 ACCS로 프로젝트 배포

다음 지침에 따라 BlackJack-Part2를 
개발자 클라우드 서비스의 응용 프로그램 컨테이너 클라우드 서비스. 

1. 왼쪽 탐색 창에서**배포**를 클릭 한 다음**새로 만들기를 클릭하십시오. 
    Configuration**

    <img src="images/3/image36.png" width="436" height="171" />

2.**새 배포 구성**페이지에서 다음을 입력합니다. 
    the **Configuration Name** and **Application Name** as shown below

    <img src="images/3/image37.png" width="436" height="173" />

3.**Deployment Target**필드에서**New**를 클릭하고 
    select **Application Container Cloud**

    <img src="images/3/image38.png" width="233" height="119" />

4.**응용 프로그램 컨테이너 클라우드에 배포**창에서 다음을 입력합니다. 
    following values and click **Test connection**

    -   Data center
    -   Identity Domain
    -   Username
    -   Password

    <img src="images/3/image39.png" width="273" height="131" />

5.**성공**메시지가 표시되면**연결 사용**을 클릭하십시오. 

    <img src="images/3/image40.png" width="273" height="131" />

6. 다음 값을 입력하고**저장**을 클릭하십시오. 

    -   **Type**: Automatic (Select Deploy stable build only)
    -   **Job:** BlackJack-Part2BuildJob
    -   **Runtime**: Java
    -   **Subscription:** Monthly
    -   **Artifact:** blackjack-part2/target/blackjack-part2-1.0-dist.zip

    <img src="images/3/image41.png" width="393" height="137" />

7.  Click the gear icon <img src="images/3/image42.png" width="51" height="28" />
    and then select **Start** to deploy the application to Oracle
    Application Container Cloud Service.

8. 성공적인 배포 후 Blackjack-Part2를 마우스 오른쪽 단추로 클릭합니다. 
    project name and copy the URL

    <img src="images/3/image43.png" width="393" height="130" />

## DevCS에서 OACCS에 배포 된 BlackJack 응용 프로그램 테스트

HTML-5 클라이언트 응용 프로그램이 개발되어 
BlackJack 응용 프로그램은 한번 배포 된 기능을 테스트합니다. 
로컬 / 원격 서버. 

다음 지시 사항에 따라 BlackJack 응용 프로그램을 테스트하십시오. 

1. 그래픽 파일 탐색기를 열고**구름> 
    BlackJack > html5-client** directory.

2. 브라우저로 index.html 파일을 엽니 다. 

3. 첫 번째 필드**서비스**에 
    URL you copied in the previous exercise,
    <https://blackjack-part2-ouopc084.apaas.em2.oraclecloud.com/>. Enter a
    number between 1 and 9 in second field, and then click Connect.

    <img src="images/3/image44.png" width="513" height="230" />

4. 게임 콘솔에 연결되면**디버그 켜기 / 끄기**를 클릭하십시오. 
    button to view the Debug console.

    <img src="images/3/image45.png" width="513" height="247" />

    **Note:** You can use the **Hit** and **Stand** buttons available on the
    UI to play the game.

이 HTML5 클라이언트 애플리케이션은 BlackJack 게임과 상호 작용합니다. 
클라우드의 OACCS에 배포 된 응용 프로그램 
