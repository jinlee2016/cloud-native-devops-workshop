# 1 부 : 지역 개발 환경 설정

## 개요

이 문서는 학생들이 Java 설정 프로세스를 이해하도록 돕습니다. 
자신의 컴퓨터에서 개발 환경, &quot;Maven&quot;을 사용하여 프로젝트 만들기 
및 &quot;Netbeans&quot;을 선택하고 개발자 클라우드 서비스에 배포하십시오. 

여기에 학생들은 지역에 기존의 &quot;블랙 잭&quot;프로젝트를 배포합니다. 
Application Server, Oracle Application Cloud에 배포 
컨테이너 서비스에 액세스하고 마지막으로 HTML-5 클라이언트에서 액세스합니다. 

**중요 사항 :**ID 도메인 이름, 사용자 이름과 같은 로그인 자격 증명 
및 암호는 개발자 클라우드 서비스 및 
Oracle Application Container 클라우드 서비스. 이 정보 수집 
오라클로부터받은 이메일을 편리하게 보관하십시오. 

## 소프트웨어 다운로드 목록

|**이름 및 버전**|**다운로드 링크**| 
| ---------------------------- | -------------------- ------------------------------------------------- | 
| **JDK 8 or higher**        | <http://www.oracle.com/technetwork/java/javase/overview/index.html> |
| **Netbeans 8.1 or higher** | <https://netbeans.org/downloads/>                                   |
| **GIT 2.10.1 or higher** | <https://git-scm.com/downloads>                                     |
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

**참고 : JDK-8U121**은 당시 사용 가능한 최신 JDK 버전입니다. 
이 문서를 만듭니다. 다운로드 할 것을 적극 권장합니다. 
최신 버전의 JDK (사용 가능한 경우) 및 이러한 랩 활동을 수행합니다. 

이미 JDK 8 이상 버전이 설치되어있는 경우 
그런 다음**JDK 활동 설치**를 건너 뛰고**Java 설정으로 진행하십시오. 
환경 변수**환경 변수를 설정 / 검증하는 활동. 

1. 브라우저를 열고 
    <http://www.oracle.com/technetwork/java/javase/overview/index.html>

2. **다운로드**탭을 클릭하고 최신 버전을 다운로드하십시오. 
    JDK available. In this case, we are downloading JDK-8U121.

    <img src="images/1m/image1.png" width="504" height="258" />

3. &quot;Java 용 Oracle 이진 코드 라이센스 계약&quot;에 동의해야합니다. 
    SE” to download the software. Click the **Accept License
    Agreement** button.

4.**jdk-8u121-macosx-x64.dmg**설치 프로그램 파일을 다음 위치로 다운로드하십시오. 
    your computer. The download may take some time. Wait for the
    download to complete before proceeding to the next step.

5.**jdk-8u121-macosx-x64.dmg**파일을 두 번 클릭하여 시작합니다. 
    the installation.

6.**JDK 8 Update 121.pkg**아이콘을 두 번 클릭하여 Java를 설치합니다. 
    Development Kit in JDK 8 updates 121 window.

7. 설치 프로그램이 열리면**계속**버튼을 클릭하십시오. 
    Introduction screen.

8. 설치 유형 화면에서 설치 버튼을 클릭합니다. 들어가다 
    administrator user name and password if prompted.

9. 설치 프로그램이 JDK를 성공적으로 설치하고 표시 할 때까지 기다립니다. 
    a “The installation was completed successfully” message. Click
    the **Close** button.

### Java 환경 변수 설정

#### JAVA \ _HOME, PATH 및 CLASSPATH 환경 변수 설정 

JAVA \ _HOME 및 PATH 설정에 대한 다음 지시 사항을 사용하십시오. 
환경 변수 

참고 : 컴퓨터에 관리자로 로그온해야합니다. 

1. 터미널 창을 열고`vim ~ / .bash_profile` 명령을 실행하십시오. 

2. ~ / .bash \ _profile 파일을 아래 명령으로 업데이트하십시오 

        export JAVA_HOME=$(/usr/libexec/java_home)
        export PATH=$PATH:$JAVA_HOME/bin

3. ~ / .bash \ _profile 파일을 저장하십시오. 

    <img src="images/1m/image2.png" width="490" height="317" />

### JDK 설치 확인

1.**Java 버전 확인 :**터미널 창을 열고 java 
    -version` command. This verifies that a JRE is installed but does not
    verify that the JDK is installed. Verify that the output of the `java
    –version` command shows “1.8.0\_121” or higher.

    <img src="images/1m/image3.png" width="556" height="115" />

## Netbeans 설치

다음 지침에 따라 다운로드, 설치 및 구성하십시오. 
컴퓨터의 Netbeans IDE. 

**참고 : Netbeans 8.1**은 최신 버전입니다. 
이 문서를 만듭니다. 다운로드 할 것을 적극 권장합니다. 
최신 버전의 IDE (사용 가능한 경우) 및이 랩 수행 
활동. 

Netbeans 8.1 이상의 버전이 이미 설치되어있는 경우 
그런 다음**Netbeans 설치**단계를 건너 뛰고**확인 진행 
Netbeans 설치**단계. 

1. Firefox 브라우저에서 다음 위치로 이동하십시오. 
    <https://netbeans.org/downloads/>.

2.**모든**기술을 지원하는 Netbeans 8.1 버전 다운로드 
    the last column.

3.**netbeans-8.1-macosx.dmg**설치 프로그램 파일을 다음 위치로 다운로드하십시오. 
    your computer. Download may take some time. Wait for the download to
    complete before proceeding to the next step.

4.**netbeans-8.1-macosx.dmg**파일을 두 번 클릭하여 설치 프로그램을 엽니 다. 

5.**Netbeans 8.1.pkg**를 두 번 눌러 설치를 시작하십시오. 

6. 보안 경고 창에서**계속**버튼을 클릭하십시오. 

7. 소개 화면에서**계속**버튼을 클릭하십시오. 

8. 소프트웨어 사용권 계약 창에서 조건에 동의하고 확인을 클릭합니다. 
    the **Continue** button.

9. 기본 설치 위치를 채택하십시오. 

10.**사용자 정의**버튼을 클릭하고**Apache Tomcat을 선택하려면 확인란을 클릭하십시오. 
    8.0.27**, and click **Install** button.

11. 프롬프트가 표시되면 관리자 사용자 이름과 암호를 입력하십시오. 

12. 설치 프로그램이 넷빈을 설치하고 &quot;**
    Install was Successful.**” message. Click the **Close** button.

### Netbeans 설치 확인

1. Netbeans 확인 :**Netbeans IDE를 시작하고 버전 확인 
    number of the JDK used by the IDE, launch Netbeans 8.1
    from Applications. Netbeans opens to a “Start Page.” Open the
    Netbeans menu and select About Netbeans. The Netbeans and Java
    versions should be Netbeans IDE 8.1 and Java 1.8.0\_121. When done,
    Close the About window.

    <img src="images/1m/image4.png" width="402" height="471" />

## GIT 설치

다음 지침에 따라 GIT Tool을 다운로드하여 설치하십시오. 
컴퓨터. 

**참고 : GIT 버전 2.10.1**은 최신 버전의 도구입니다. 
이 문서를 만들 때. 그것은 당신이 
이 도구의 최신 버전을 다운로드하십시오. 
(가능한 경우) 실험실 활동을 수행합니다. 

이미 GIT 2.10.1 이상 버전이 설치되어있는 경우 
그런 다음**GIT**활동 설치를 건너 뛰고**확인하기로 진행하십시오. 
GIT 설치**활동. 

1. 터미널 창을 열고 git --version 명령을 실행하십시오. 

    <img src="images/1m/image5.png" width="568" height="111" />

    **Note:** This command installs GIT tool if it is not installed already.

2.**설치**버튼을 클릭하십시오. 

    <img src="images/1m/image6.png" width="457" height="190" />

3.**Agree**버튼을 클릭하여 사용권 계약에 동의하십시오. 

4. 설치 프로그램이 GIT 도구를 다운로드하여 설치할 때까지 기다렸다가 
    displays a “**The Software was installed.**” message. Click the
    **Done** button.

### GIT 설치 확인

1.**GIT Tool 확인 :**터미널 창을 열고`git 
    --version` command. Verify that the output of the `git --version`
    command shows “git version 2.10.1 (Apple Git-78)”

    <img src="images/1m/image7.png" width="570" height="80" />

## Maven 설치하기

Maven을 다운로드, 설치 및 구성하려면 다음 지시 사항을 따르십시오. 
귀하의 컴퓨터에. 

**참고 : Maven 3.3.9**는 최신 버전의 도구입니다. 
이 문서를 만드는 시간. 그것은 당신이 
이 도구의 최신 버전을 다운로드하고 (사용 가능한 경우)이 랩을 수행하십시오. 
활동. 

Maven 3.3.9 이상 버전이 이미 설치되어있는 경우 
그런 다음**Maven**활동 설치를 건너 뛰고**설정으로 진행하십시오. 
Maven 환경 변수**필요한 설정 / 확인 작업 
환경 변수. 

1. 브라우저를 열고 
    <http://maven.apache.org/download.cgi>.

2. 바이너리 ZIP 아카이브,**apache-maven-3.3.9-bin.tar.gz**파일을 다운로드하십시오. 
    on to your computer. The download may take some time. Wait for the
    download to complete before proceeding to the next step.

    <img src="images/1m/image8.png" width="624" height="129" />

3. / Applications 디렉토리에 배포 아카이브의 압축을 풉니 다. 

4. 전체 경로 (/Applications/apache-maven-3.3.9)를 
    extraction is completed; this is required to create
    environment variables.

### Maven 환경 변수 설정하기

M2 \ _HOME 및 PATH 환경 설정에 대한 다음 지시 사항을 사용하십시오. 
변수. 

**참고 :**관리자 권한으로 컴퓨터에 로그온해야합니다. 

1. 터미널 창을 열고`vim ~ / .bash_profile` 명령을 실행하십시오. 

2.**~ / .bash \ _profile**파일을 명령으로 업데이트하십시오 
    mentioned below.

        export M2_HOME=/Applications/apache-maven-3.3.9
        export PATH=$PATH:$M2_HOME/bin

3.**~ / .bash \ _profile**파일을 저장하십시오. 

    <img src="images/1m/image9.png" width="469" height="295" />

### Maven 설치 확인

1. Maven 버전 확인**: 터미널 창을 다시 시작하고 
    `mvn --version` command. Verify that the output of the `mvn -–version`
    command matches with the following screenshot:

    <img src="images/1m/image10.png" width="553" height="167" />
