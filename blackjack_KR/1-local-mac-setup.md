# 1 부 : 지역 개발 환경 설정


## 개요


이 문서는 수강생들이 컴퓨터에서 Java 개발 환경을 설정하고 &quot;Maven&quot;및 &quot;Netbeans&quot;을 사용하여 프로젝트를 만들고이를 개발자 클라우드 서비스에 배포하는 프로세스를 이해하도록 도와줍니다. 

여기에서 수강생들은 기존 &quot;Blackjack&quot;프로젝트를 로컬 Application Server에 배포 한 다음 Oracle Application Cloud Container Service에 배포하고 마지막으로 HTML-5 클라이언트에서 액세스합니다. 

**중요 사항 : 개발자 클라우드 서비스 및 Oracle Application Container 클라우드 서비스를 사용하려면 ID 도메인 이름, 사용자 이름 및 암호와 같은 로그인 자격 증명이 필요합니다. 오라클로부터받은 이메일에서이 정보를 수집하고 편리하게 사용하십시오. 

## 소프트웨어 다운로드 목록


| **Name and Version**       | **Download Link**                                                   |
|----------------------------|---------------------------------------------------------------------|
| **JDK 8 or higher**        | <http://www.oracle.com/technetwork/java/javase/overview/index.html> |
| **Netbeans 8.1 or higher** | <https://netbeans.org/downloads/>                                   |
| **GIT 2.10.1 or higher** | <https://git-scm.com/downloads>                                     |
| **Maven 3.3.9 or higher**  | <http://maven.apache.org/download.cgi>                              |


**참고**: 다운로드 시간을 저장하기 전에 위 표에 언급 된 소프트웨어 목록을 다운로드하여 컴퓨터에 저장할 수 있습니다. 

**또는**

연습과 함께 소프트웨어를 다운로드 할 수 있습니다. 각 연습에는 필수 소프트웨어를 다운로드하고 설치하는 자세한 단계가 포함되어 있습니다. 

64  비트 설정에서 작업하고 소프트웨어 다운로드 및 설치 지침을 제공한다고 가정합니다. 64 비트 설정에서 작업하지 않는 경우 설치 프로그램과 호환되는 소프트웨어를 다운로드하십시오. 

## JDK 설치


다음 지시 사항에 따라 컴퓨터에 Java Development Kit을 다운로드, 설치 및 구성하십시오. 

**참고 : JDK-8U121**은이 문서를 만들 때 사용할 수있는 최신 버전의 JDK입니다. 최신 버전의 JDK (사용 가능한 경우)를 다운로드하고 이러한 랩 활동을 수행하는 것이 좋습니다. 

컴퓨터에 JDK 8 이상의 버전이 이미 설치되어있는 경우**JDK 활동 설치**를 건너 뛰고**Java 환경 변수 설정**활동을 수행하여 환경 변수를 설정 / 검증하십시오. 

1. 브라우저를 열고    <http://www.oracle.com/technetwork/java/javase/overview/index.html>


2. **다운로드**탭을 클릭하고 사용 가능한 최신 버전의 JDK를 다운로드하십시오. 여기서는 JDK-8U121을 다운로드 중입니다. 

    <img src="images/1m/image1.png" width="504" height="258" />


3. 소프트웨어를 다운로드하려면 &quot;Java SE 용 Oracle 2 진 코드 라이센스 계약&quot;에 동의해야합니다.**Accept License Agreement**버튼을 클릭하십시오. 

4. **jdk-8u121-macosx-x64.dmg**설치 프로그램 파일을 컴퓨터에 다운로드하십시오. 다운로드에는 다소 시간이 걸릴 수 있습니다. 다음 단계로 진행하기 전에 다운로드가 완료 될 때까지 기다리십시오. 

5. **jdk-8u121-macosx-x64.dmg**파일을 두 번 클릭하여 설치를 시작합니다. 

6. **JDK 8 Update 121.pkg**아이콘을 두 번 클릭하여 JDK 8 업데이트에 Java Development Kit 설치 121 창을 엽니 다. 

7. 설치 프로그램이 열리면 소개 화면에서**계속**버튼을 클릭하십시오. 

8. 설치 유형 화면에서 설치 버튼을 클릭합니다. 메시지가 표시되면 관리자 사용자 이름과 암호를 입력하십시오. 

9. 설치 프로그램이 JDK를 성공적으로 설치하고 &quot;설치가 성공적으로 완료되었습니다&quot;라는 메시지가 나타날 때까지 기다리십시오.**닫기**버튼을 클릭하십시오. 

### Java 환경 변수 설정


#### JAVA \ _HOME, PATH 및 CLASSPATH 환경 변수 설정 

JAVA \ _HOME 및 PATH 환경 변수 설정에 대한 다음 지시 사항을 사용하십시오 

참고 : 컴퓨터에 관리자로 로그온해야합니다. 

1. 터미널 창을 열고`vim ~ / .bash_profile` 명령을 실행하십시오. 

2. ~ / .bash \ _profile 파일을 아래 명령으로 업데이트하십시오 

export JAVA_HOME = $ (/ usr / libexec / java_home) export PATH = $ PATH : $ JAVA_HOME / bin 

3. ~ / .bash \ _profile 파일을 저장하십시오. 

    <img src="images/1m/image2.png" width="490" height="317" />


### JDK 설치 확인


1. **Java 버전 확인 :** 터미널 창을 열고`java -version` 명령을 실행하십시오. 이것은 JRE가 설치되어 있는지 확인하지만 JDK가 설치되어 있는지 확인하지는 않습니다. `java -version` 명령의 출력이 &quot;1.8.0 \ _121&quot;이상인지 확인하십시오. 

    <img src="images/1m/image3.png" width="556" height="115" />


## Netbeans 설치


다음 지침에 따라 컴퓨터에 Netbeans IDE를 다운로드, 설치 및 구성하십시오. 

**참고 : Netbeans 8.1**은이 문서를 만들 때 사용할 수있는 최신 버전입니다. 최신 버전의 IDE (사용 가능한 경우)를 다운로드하고 이러한 랩 작업을 수행하는 것이 좋습니다. 

컴퓨터에 Netbeans 8.1 이상의 버전이 이미 설치되어있는 경우**Netbeans 설치**단계를 건너 뛰고**Netbeans 설치 확인**단계를 진행하십시오. 

1. Firefox 브라우저에서 다음 위치로 이동하십시오.    <https://netbeans.org/downloads/>.


2. 마지막 열에서**All**기술을 지원하는 Netbeans 8.1 버전을 다운로드하십시오. 

3. **netbeans-8.1-macosx.dmg**설치 프로그램 파일을 컴퓨터에 다운로드하십시오. 다운로드에는 시간이 걸릴 수 있습니다. 다음 단계로 진행하기 전에 다운로드가 완료 될 때까지 기다리십시오. 

4. **netbeans-8.1-macosx.dmg**파일을 두 번 클릭하여 설치 프로그램을 엽니 다. 

5. **Netbeans 8.1.pkg**를 두 번 눌러 설치를 시작하십시오. 

6. 보안 경고 창에서**계속**버튼을 클릭하십시오. 

7. 소개 화면에서**계속**버튼을 클릭하십시오. 

8. 소프트웨어 사용권 계약 창에서 조건에 동의하고**계속**버튼을 클릭하십시오. 

9. 기본 설치 위치를 채택하십시오. 

10. **사용자 정의**버튼을 클릭하고**Apache Tomcat 8.0.27**을 선택하고**설치**버튼을 클릭하십시오. 

11 . 프롬프트가 표시되면 관리자 사용자 이름과 암호를 입력하십시오. 

12 . 설치 프로그램이 Netbeans을 설치하고 &quot;**설치가 완료되었습니다.**&quot;메시지가 나타날 때까지 기다리십시오.**닫기**버튼을 클릭하십시오. 

### Netbeans 설치 확인


1. Netbeans 확인 :** Netbeans IDE를 시작하고 IDE에서 사용하는 JDK의 버전 번호를 확인하려면 응용 프로그램에서 Netbeans 8.1을 시작합니다. Netbeans이 &quot;시작 페이지&quot;로 열립니다. Netbeans 메뉴를 열고 Netbeans 정보를 선택하십시오. Netbeans 및 Java 버전은 Netbeans IDE 8.1 및 Java 1.8.0 \ _121이어야합니다. 완료되면 정보 창을 닫습니다. 

    <img src="images/1m/image4.png" width="402" height="471" />


## GIT 설치


다음 지침에 따라 컴퓨터에 GIT Tool을 다운로드하고 설치하십시오. 

**참고 : GIT 버전 2.10.1**은이 문서를 만들 때 사용할 수있는 최신 버전의 도구입니다. 이 도구의 최신 버전 (사용 가능한 경우)을 다운로드하고 이러한 Lab 활동을 수행 할 것을 적극 권장합니다. 

이미 컴퓨터에 GIT 2.10.1 이상 버전이 설치되어 있다면**GIT**활동 설치를 건너 뛰고**GIT 설치 확인 활동**을 진행하십시오. 

1. 터미널 창을 열고 git --version 명령을 실행하십시오. 

    <img src="images/1m/image5.png" width="568" height="111" />


**참고 :** 이 명령은 이미 설치되지 않은 경우 GIT 도구를 설치합니다. 

2. **설치**버튼을 클릭하십시오. 

    <img src="images/1m/image6.png" width="457" height="190" />


3. **Agree**버튼을 클릭하여 사용권 계약에 동의하십시오. 

4. 설치 프로그램이 GIT 도구를 다운로드하여 설치하고 &quot;**소프트웨어가 설치되었습니다.**&quot;메시지가 나타날 때까지 기다리십시오.**완료**버튼을 클릭하십시오. 

### GIT 설치 확인


1. **GIT Tool 확인 :** 터미널 창을 열고`git --version` 명령을 실행하십시오. `git --version` 명령의 출력에 &quot;git version 2.10.1 (Apple Git-78)&quot;이 표시되는지 확인하십시오. 

    <img src="images/1m/image7.png" width="570" height="80" />


## Maven 설치하기


다음 지침에 따라 컴퓨터에 Maven을 다운로드, 설치 및 구성하십시오. 

**참고 : Maven 3.3.9**는이 문서를 만들 때 사용할 수있는 최신 버전의 도구입니다. 이 도구의 최신 버전 (사용 가능한 경우)을 다운로드하고 이러한 Lab 활동을 수행 할 것을 적극 권장합니다. 

컴퓨터에 Maven 3.3.9 이상의 버전이 이미 설치되어 있다면**Maven**액티비티 설치를 건너 뛰고**Maven 환경 변수 설정**작업을 진행하여 필요한 환경 변수를 설정 / 확인하십시오. 

1. 브라우저를 열고    <http://maven.apache.org/download.cgi>.


2. 바이너리 ZIP 아카이브, 컴퓨터에**apache-maven-3.3.9-bin.tar.gz**파일을 다운로드하십시오. 다운로드에는 다소 시간이 걸릴 수 있습니다. 다음 단계로 진행하기 전에 다운로드가 완료 될 때까지 기다리십시오. 

    <img src="images/1m/image8.png" width="624" height="129" />


3. / Applications 디렉토리에 배포 아카이브의 압축을 풉니 다. 

4. 추출이 완료되면 전체 경로 (/Applications/apache-maven-3.3.9)를 복사하십시오. 이것은 환경 변수를 작성하는 데 필요합니다. 

### Maven 환경 변수 설정하기


M2 \ _HOME 및 PATH 환경 변수를 설정하려면 다음 지시 사항을 따르십시오. 

**참고 :** 관리자 권한으로 컴퓨터에 로그온해야합니다. 

1. 터미널 창을 열고`vim ~ / .bash_profile` 명령을 실행하십시오. 

2. **~ / .bash \ _profile**파일을 아래에 언급 된 명령으로 업데이트하십시오. 

export M2_HOME = / 응용 프로그램 / apache-maven-3.3.9 export PATH = $ PATH : $ M2_HOME / bin 

3. **~ / .bash \ _profile**파일을 저장하십시오. 

    <img src="images/1m/image9.png" width="469" height="295" />


### Maven 설치 확인


1. **Maven 버전 확인**: 터미널 창을 다시 시작하고`mvn --version` 명령을 실행하십시오. `mvn --version` 명령의 출력이 다음 스크린 샷과 일치하는지 확인하십시오 : 

    <img src="images/1m/image10.png" width="553" height="167" />
