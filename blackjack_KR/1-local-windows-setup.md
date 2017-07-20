# 1 부 : 지역 개발 환경 설정

## 개요

이 문서는 학생들이 Java 설정 프로세스를 이해하도록 돕습니다. 
자신의 컴퓨터에서 개발 환경, &quot;Maven&quot;을 사용하여 프로젝트 만들기 
및 &quot;Netbeans&quot;을 선택하고 개발자 클라우드 서비스에 배포하십시오. 

여기에 학생들은 지역에 기존의 &quot;블랙 잭&quot;프로젝트를 배포합니다. 
Application Server, Oracle Application Cloud에 배포 
컨테이너 서비스에 액세스하고 마지막으로 HTML-5 클라이언트에서 액세스합니다. 

**중요 사항 :**ID 도메인 이름, 사용자와 같은 로그인 자격 증명 
개발자 클라우드 서비스를 사용하려면 이름과 비밀번호가 필요합니다. 
Oracle Application Container 클라우드 서비스. 이 정보 수집 
오라클로부터받은 이메일을 편리하게 보관하십시오. 

## 소프트웨어 다운로드 목록

|**이름 및 버전**|**다운로드 링크**| 
| ---------------------------- | -------------------- ------------------------------------------------- | 
| **JDK 8 or higher**        | <http://www.oracle.com/technetwork/java/javase/overview/index.html> |
| **Netbeans 8.1 or higher** | <https://netbeans.org/downloads/>                                   |
| **GIT 2.11.0.3 or higher** | <https://git-scm.com/downloads>                                     |
| **Maven 3.3.9 or higher**  | <http://maven.apache.org/download.cgi>                              |

**참고**: 위 표에 언급 된 소프트웨어 목록을 다운로드 할 수 있습니다. 
다운로드 저장을 시작하기 전에 컴퓨터에 저장 
시각. 

**또는**

연습과 함께 소프트웨어를 다운로드 할 수 있습니다. 마다 
운동에는 필요한 다운로드 및 설치를위한 세부 단계가 포함되어 있습니다. 
소프트웨어. 

64 비트 설정에서 작업하고 제공된 것으로 가정합니다. 
이에 따라 소프트웨어를 다운로드하고 설치하십시오. 당신이있는 경우 
64 비트 설정에서 작동하지 않는 다음 호환되는 소프트웨어를 다운로드하십시오. 
귀하의 설정. 

## JDK 설치

다음 지시 사항에 따라 Java를 다운로드, 설치 및 구성하십시오. 
컴퓨터의 개발 키트. 

**참고 : JDK-8U121**은 당시 사용 가능한 최신 버전의 JDK입니다. 
이 문서를 만드는 방법. 다운로드하는 것이 좋습니다. 
최신 버전의 JDK (사용 가능한 경우) 및이 랩 수행 
활동. 

이미 JDK 8 이상 버전이 설치되어있는 경우 
그런 다음**Install JDK**단계를 건너 뛰고**설정으로 진행하십시오. 
JAVA \ _HOME, PATH 및 CLASSPATH 환경 변수**설정 / 확인 
환경 변수. 

1. Firefox 브라우저에서 다음 위치로 이동하십시오. 
    <http://www.oracle.com/technetwork/java/javase/overview/index.html>

2.**다운로드**탭을 클릭하고 최신 버전을 다운로드하십시오. 
    JDK available. In this case, we are downloading JDK-8U121.

    <img src="images/1/image1.png" width="541" height="311" />

3. &quot;Java 용 Oracle 이진 코드 라이센스 계약&quot;에 동의해야합니다. 
    SE” to download the software. Click the **Accept License
    Agreement** button.

4.**jdk-8u121-windows-x64.exe**설치 프로그램 파일을 다음 위치로 다운로드하십시오. 
    your computer. The download may take some time. Wait for the
    download to complete before proceeding to the next step.

5. 시작하려면**jdk-8u121-windows-x64.exe**파일을 두 번 클릭하십시오. 
    the installation.

    **Note:** If you receive a security warning such as “Do you want to
    allow the following program to make changes to this computer?” click
    **Yes**.

6. 설치 프로그램이 열리면**다음**버튼을 클릭하십시오. 

7. 기본 설치 위치를 승인하고**다음**을 두 번 클릭하십시오. 

8. 설치 프로그램이 JDK를 성공적으로 설치하고 표시 할 때까지 기다립니다. 
    a “Java SE Development Kit 8 Update 121 (64-bit)” message. Click the
    **Close** button.

### Windows 7 - 환경 변수 설정

#### JAVA \ _HOME, PATH 및 CLASSPATH 환경 변수 설정 

**참고 :**관리자 권한으로 컴퓨터에 로그온해야합니다. 

1. Windows**시작**버튼을 클릭하십시오.**컴퓨터**를 마우스 오른쪽 버튼으로 클릭하고 
    select **Properties**. Click **Advanced system settings**.

2.**환경 변수**를 클릭하십시오. 

3. 환경 변수 창의**시스템 변수**아래에서, 
    click the **New** button.

4. 새 시스템 변수 창에서 변수 이름을 입력하십시오 
    **JAVA\_HOME**, enter the Variable value **C:\\Program
    Files\\Java\\jdk1.8.0\_121,** and then click the **OK** button.

    <img src="images/1/image2.png" width="303" height="131" />

5.**PATH**시스템 변수를 선택하고**Edit**버튼을 클릭하십시오 (If 
    PATH system variable is not available, click the **New** button to
    create PATH variable, enter the Variable value **C:\\Program
    Files\\Java\\jdk1.8.0\_121,** and then click the **OK** button).

6. 시스템 변수 편집 창의 변수 값 필드에서, 
    place the cursor at the starting position and enter **C:\\Program
    Files\\Java\\jdk1.8.0\_121\\bin**; Then click the **OK** button.

    <img src="images/1/image3.png" width="303" height="131" />

7.**새**단추를 클릭하여 다른 시스템 변수를 만듭니다. 

8. 새 시스템 변수 창에 변수 이름을 입력하십시오 
    **CLASSPATH**, enter the Variable value **C:\\Program
    Fles\\Java\\jdk1.8.0\_121\\lib\\tools.jar;.;** (this has a
    semicolon, a period, and a semicolon at the end), and then click the
    **OK** button.

    <img src="images/1/image4.png" width="314" height="136" />.

9. 세 개의 시스템 변수를 작성 / 갱신했습니다.**확인**을 클릭하십시오.**
    button to close the Environment Variables and System
    Properties windows. Close the Control Panel window.

### Windows 10 - 환경 변수 설정

#### JAVA \ _HOME, PATH 및 CLASSPATH 환경 변수 설정 

**참고 :**관리자 권한으로 컴퓨터에 로그온해야합니다. 

1. Windows 바탕 화면에서**이 PC**를 마우스 오른쪽 단추로 클릭하고 
    **Properties**. Click **Advanced system settings**.

2.**환경 변수**를 클릭하십시오. 

3. 환경 변수 창의**시스템 변수**아래에서, 
    click the **New** button.

4. 새 시스템 변수 창에서 변수 이름을 입력하십시오 
    **JAVA\_HOME**, enter the Variable value **C:\\Program
    Files\\Java\\jdk1.8.0\_121** and then click the **OK** button.

    <img src="images/1/image5.png" width="363" height="106" />

5.**PATH**시스템 변수를 선택하고**Edit**버튼을 클릭하십시오 (If 
    PATH system variable is not available, click the **New** button to
    create PATH variable, enter the Variable value **C:\\Program
    Files\\Java\\jdk1.8.0\_121;** and then click the **OK** button).

6. 환경 변수 편집 창에서**새로 작성**버튼을 클릭하고 
    enter **C:\\Program Files\\Java\\jdk1.8.0\_121\\bin** then click the
    **OK** button.

    <img src="images/1/image6.png" width="177" height="194" />

7.**새**단추를 클릭하여 다른 시스템 변수를 만듭니다. 

8. 새 시스템 변수 창에 변수 이름을 입력하십시오 
    **CLASSPATH**, enter the Variable value **C:\\Program
    Fles\\Java\\jdk1.8.0\_121\\lib\\tools.jar;.;** (this has a
    semicolon, a period, and a semicolon at the end), and then click the
    **OK** button.

    <img src="images/1/image7.png" width="326" height="95" />.

9. 세 개의 시스템 변수를 작성 / 갱신했습니다.**확인**을 클릭하십시오.**
    button to close the Environment Variables and System
    Properties windows.

### JDK 설치 확인

1.**Java 버전 확인 :**명령 프롬프트 창을 열고 실행하십시오. 
    the `java -version` command. This verifies that a JRE is installed but
    does not verify that the JDK is installed. Verify that the output of
    the `java –version` command shows “1.8.0\_121” or higher.

    <img src="images/1/image8.png" width="570" height="126" />

## Netbeans 설치

다음 지침에 따라 다운로드, 설치 및 구성하십시오. 
컴퓨터의 Netbeans IDE. 

**참고 : Netbeans 8.1**은 최신 버전입니다. 
이 문서를 만듭니다. 다운로드 할 것을 적극 권장합니다. 
최신 버전의 IDE (사용 가능한 경우) 및이 랩 수행 
활동. 

Netbeans 8.1 이상의 버전이 이미 설치되어있는 경우 
그런 다음**Netbeans 설치**단계를 건너 뛰고 계속 진행하십시오. 
**넷빈 설치 확인**단계. 

1. Firefox 브라우저에서 다음 위치로 이동하십시오. 
    <https://netbeans.org/downloads/>.

2.**All**기술을 지원하는 Netbeans 8.1 버전을 다운로드하십시오. 
    from the last column.

3.**netbeans-8.1-windows.exe**설치 프로그램 파일을 다음 위치로 다운로드하십시오. 
    your computer. The download may take some time. Wait for the
    download to complete before proceeding to the next step.

4.**netbeans-8.1-windows.exe**파일을 두 번 클릭하여 시작합니다. 
    the installation.

    **Note:** If you receive a security warning such as “Do you want to
    allow the following program to make changes to this computer?” click
    **Yes**.

5. 설치 프로그램이 열리면**사용자 정의**버튼을 클릭하고 
    check box to select **Apache Tomcat 8.0.27** under the **Runtimes**
    section, and click the **OK** button.

6. 시작 화면에서**다음**버튼을 클릭하여 계속 진행합니다 
    the installation.

7. 라이센스 계약의 조항에 동의하고 
    **Next** button.

8. 기본**NetBeans IDE 설치를 수락합니다.**경로 
    NetBeans, make sure the correct installation path of
    JDK (jdk1.8.0\_121) is selected in the **JDK for the NetBeans IDE:**
    field, and click the **Next** button.

9.**Glassfish**및**Apache의 기본 설치 경로를 그대로 사용합니다. 
    Tomcat** and click the **Next** button. Click the **Install**
    button on the Summary window.

10. 설치 프로그램이 넷빈을 설치하고 
    “**Setup Complete**” message. Click the **Finish** button.

### Netbeans 설치 확인

1. Netbeans 확인 :**Netbeans IDE를 시작하고 
    version number of the JDK used by the IDE, double-click the
    **Netbeans 8.1** shortcut on the desktop. Netbeans opens to a “Start
    Page.” Open the **Help** menu and select **About**. The Netbeans and
    Java versions should be **Netbeans IDE 8.1** and
    **Java 1.8.0\_121.** When done, **Close** the **About** window.

## GIT 설치

다음 지침에 따라 GIT를 다운로드, 설치 및 구성하십시오. 
컴퓨터의 도구. 

**참고 : GIT 2.11.0.3**은에서 사용할 수있는 최신 버전의 도구입니다. 
이 문서를 만들 때. 그것은 당신이 
이 도구의 최신 버전을 다운로드하십시오. 
(가능한 경우) 실험실 활동을 수행합니다. 

GIT 2.11.0.3 이상의 버전이 이미 설치되어있는 경우 
그런 다음**GIT 설치**단계를 건너 뛰고**확인하기로 진행하십시오. 
GIT 설치**단계. 

1.  In the Firefox browser, navigate to <https://git-scm.com/downloads>
    and click the **Downloads for Windows** button.

2.**Git-2.11.0.3-64-bit.exe**설치 프로그램 파일을 다음 위치로 다운로드하십시오. 
    your computer. The download may take some time. Wait for the
    download to complete before proceeding to the next step.

3. 시작하려면**Git-2.11.0.3-64-bit.exe**파일을 두 번 클릭하십시오. 
    the installation.

    **Note:** If you receive a security warning such as “Do you want to
    allow the following program to make changes to this computer?” click
    **Yes**.

4. 설치 프로그램이 열리면**다음**버튼을 클릭하십시오. 

5.**GIT**의 기본 설치 경로를 그대로 사용하고 
    **Next** button.

6.**구성 요소 선택 화면에서 기본 선택 사항을 수락하고 
    click the **Next** button.

7.**시작 메뉴 폴더 선택**화면에서 기본값을 승인하십시오 
    and click the **Next** button.

8.**Adjusting에서**Use Git Bash only**옵션을 선택하십시오 
    your PATH environment** screen and click the **Next** button.

    <img src="images/1/image9.png" width="324" height="252" />

9.**라인 결말 구성에서 기본 선택을 수락하십시오 
    conversions** screen and click the **Next** button.

10.**터미널 구성에서 기본 선택 사항을 수락하십시오 
    emulator to use with Git Bash** screen and click the
    **Next** button.

11.**추가 옵션 구성**에서 기본 선택 사항을 승인하십시오. 
    screen and click the **Next** button.

12.**실험 구성 중 기본 선택을 그대로 적용하십시오. 
    options** screen and click the **Install** button. Wait until the
    installer installs the **Git 2.11.0.3** and displays a “**Setup has
    finished installing Git on your computer**” message. Click the
    **Finish** button.

### GIT 설치 확인

1.**GIT 확인 :**Windows**시작**메뉴에서**Git Bash**열기 
    and run the `git --version` command. Verify that the output of the `git
    --version` command shows “git version 2.11.0.windows.3.”

    <img src="images/1/image10.png" width="574" height="133" />

## Maven 설치하기

Maven을 다운로드, 설치 및 구성하려면 다음 지시 사항을 따르십시오. 
귀하의 컴퓨터에. 

**참고 : Maven 3.3.9**는 최신 버전의 도구입니다. 
이 문서를 만드는 시간. 그것은 당신이 
이 도구의 최신 버전을 다운로드하고 (사용 가능한 경우)이 랩을 수행하십시오. 
활동. 

Maven 3.3.9 이상 버전이 이미 설치되어있는 경우 
그런 다음**Maven 설치**단계를 건너 뛰고**설정으로 진행하십시오. 
M2 \ _HOME, M2 및 PATH 환경 변수**단계에서 위로 
필요한 환경 변수를 설정 / 확인하십시오. 

1. Firefox 브라우저에서 다음 위치로 이동하십시오. 
    <http://maven.apache.org/download.cgi>.

2. 바이너리 ZIP 아카이브,**apache-maven-3.3.9-bin.zip**파일을 다운로드하십시오. 
    on to your computer. The download may take some time. Wait for the
    download to complete before proceeding to the next step.

    <img src="images/1/image11.png" width="501" height="292" />

3. C : \\에**Maven**이라는 디렉토리를 만들고 
    distribution archive to **C:\\Maven** directory.

    **Note:** You should achieve the directory structure highlighted in the screenshot

    <img src="images/1/image12.png" width="348" height="160" />

4. 전체 경로 (**C : \\ Maven \\ apache-maven-3.3.9**)를 복사하십시오. 
    extraction is completed; this is required to create
    environment variables.

### Windows 7 - 환경 변수 설정

#### M2 \ _HOME, M2 및 PATH 환경 변수 설정 

**참고 :**관리자 권한으로 컴퓨터에 로그온해야합니다. 

1. Windows**시작**버튼을 클릭하십시오.**컴퓨터**를 마우스 오른쪽 버튼으로 클릭하고 
    select **Properties**. Click **Advanced system settings**.

2.**환경 변수**를 클릭하십시오. 

3. 환경 변수 창의**시스템 변수**아래에서, 
    click the **New** button.

4. 새 시스템 변수 창에서 변수 이름을 입력하십시오 
    **M2\_HOME**, enter the Variable value
    **C:\\Maven\\apache-maven-3.3.9** , and then click the
    **OK** button.

    <img src="images/1/image13.png" width="341" height="147" />

5. 환경 변수 창의**시스템 변수**아래에서, 
    click the **New** button.

    In the New System Variable window, enter the Variable name **M2**,
    enter the Variable value **%M2\_HOME%\\bin** , and then click the
    **OK** button.

    <img src="images/1/image14.png" width="341" height="147" />

6.**PATH**시스템 변수를 선택하고**편집**버튼을 클릭하십시오. 

7. 시스템 변수 편집 창의 변수 값 필드에서, 
    place the cursor at the last position and enter **;%M2%** and then
    click the **OK** button.

    <img src="images/1/image15.png" width="347" height="149" />

8.**확인**버튼을 두 번 클릭하여 시스템 변수 편집을 닫고 
    System Property windows

### Windows 10 - 환경 변수 설정

#### M2 \ _HOME, M2 및 PATH 환경 변수 설정 

**참고 :**관리자 권한으로 컴퓨터에 로그온해야합니다. 

1. Windows 바탕 화면에서**이 PC**를 마우스 오른쪽 단추로 클릭하고 
    **Properties**. Click **Advanced system settings**.

2.**환경 변수**를 클릭하십시오. 

3. 환경 변수 창의**시스템 변수**아래에서, 
    click the **New** button.

4. 새 시스템 변수 창에서 변수 이름을 입력하십시오 
    **M2\_HOME**, enter the Variable value
    **C:\\Maven\\apache-maven-3.3.9** and then click the **OK** button.

    <img src="images/1/image16.png" width="372" height="110" />

5. 환경 변수 창의**시스템 변수**아래에서, 
    click the **New** button.

    In the New System Variable window, enter the Variable name **M2**,
    enter the Variable value **%M2\_HOME%\\bin** , and then click the
    **OK** button.

    <img src="images/1/image17.png" width="377" height="111" />

6.**PATH**시스템 변수를 선택하고**편집**버튼을 클릭하십시오. 

7. 시스템 변수 편집 창의 변수 값 필드에서, 
    place the cursor at the last position and enter **;%M2%** and then
    click the **OK** button.

    <img src="images/1/image18.png" width="228" height="251" />

8.**확인**버튼을 두 번 클릭하여 시스템 변수 편집을 닫고 
    System Property windows

### Maven 설치 확인

1. Maven 버전 확인 :**명령 프롬프트 창을 열고 실행 
    the `mvn --version` command. Verify that the output of the `mvn
    -–version` command matches with the following screenshot:

    <img src="images/1/image19.png" width="499" height="143" />
