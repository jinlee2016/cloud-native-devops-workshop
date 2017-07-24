# 1 부 : 지역 개발 환경 설정

## 개요

이 문서는 자바 설정을 처리하는 데 도움이됩니다. 
자신의 컴퓨터에서 개발 환경, &quot;Maven&quot;을 사용하여 프로젝트 만들기 
및 &quot;Netbeans&quot;을 선택하고 프로그램을 컴퓨터에 설치하십시오. 

현재 지역의 &quot;블랙 잭&quot;프로젝트를 배포합니다. 
애플리케이션 서버, 프로비저닝 기능을 갖춘 Oracle Application Cloud 
컨테이너 서비스에 액세스하고 마지막으로 HTML-5 클라이언트에서 액세스합니다. 

**중요 사항 :**ID 도메인 이름, 사용자 이름 및 위의 로그인 자격 증명 
그리고 암호는 서비스입니다. 
Oracle Application Container 클라우드 서비스. 현장 수집 
오클랜드에서 이메일을 수 있습니다. 

## 소프트웨어 다운로드 목록

|**이름 및 버전**|**다운로드 링크**| 
|----------------------------|---------------------------------------------------------------------|
| **JDK 8 or higher**        | <http://www.oracle.com/technetwork/java/javase/overview/index.html> |
| **Netbeans 8.1 or higher** | <https://netbeans.org/downloads/>                                   |
| **GIT 2.10.1 or higher** | <https://git-scm.com/downloads>                                     |
| **Maven 3.3.9 or higher**  | <http://maven.apache.org/download.cgi>                              |

**참고**: 위 목록에있는 소프트웨어 목록을 다운로드하십시오. 
다운로드 저장을 시작하고 저장하기 
시각. 

**또는**

다운로드와 수련 
다운로드 및 설치 정보를 포함합니다. 
소프트웨어. 

64 비트 설정 및 작동. 
이 소프트웨어를 다운로드하고 설치하십시오. 너는 그렇다. 
64 비트 설정에서 작동하지 않습니다. 
귀하의 설정. 

## JDK 설치

다음 지시 사항에 자바 다운로드, 설치 및 구성. 
컴퓨터 개발 키트. 

**참고 : JDK-8U121**최신 업데이트 JDK 버전입니다. 
이 문서를 참조하십시오. 다운로드 사용하지 못한다. 
최신 버전의 JDK (사용법) 및 운영 활동을 처리합니다. 

이미 JDK 8 이상 버전 설치 
그런 다음**JDK 활동 설치**를 건너 뛰고**Java 설정으로 진행하십시오. 
환경 변수**환경 변수를 설정 / 검증 활동. 

1. 실행 
    <http://www.oracle.com/technetwork/java/javase/overview/index.html>

2. **다운로드**탭을 클릭하고 최신 버전을 다운로드하십시오. 
JDK를 수 있습니다. JDK-8U121을 다운로드 중입니다. 

    <img src="images/1m/image1.png" width="504" height="258" />

3. &quot;Java 용 Oracle 이진 교류 계약&quot;을 
SE &quot;를 클릭하면 다운로드 할 수 있습니다.**수락을 클릭하십시오. 
**버튼을 클릭하십시오. 

4. **jdk-8u121-macosx-x64.dmg**설치 프로그램 파일을 다음 위치로 다운로드하십시오. 
너의 시스템 야. 다운로드 긴 시간이 걸린 수 있습니다. 기다려라. 
다운로드에서 다음 단계로 진행하십시오. 

5. **jdk-8u121-macosx-x64.dmg**파일을 클릭하십시오. 
설치. 

6. **JDK 8 업데이트 121.pkg**아이콘을 클릭하면 설치가됩니다. 
JDK 8 업데이트 키트의 개발 키트. 

7. 설치 프로그램을 클릭하십시오. 
소개 화면. 

8. 설치를 클릭하고 설치를 클릭하십시오. 들어가다 
사용자 권한과 암호. 

9. JDK를 설치하고 표시하는 중입니다. 
&quot;설치가 완료되었습니다.&quot; 해리스 소리 
**닫기**버튼. 

### Java 환경 변수 설정

#### JAVA \ _HOME, PATH 및 CLASSPATH 환경 변수 설정 

JAVA \ _HOME 및 PATH 설정을 참고하십시오. 
환경 변수 

참고 : 컴퓨터에 관리자가 없습니다. 

1. 터미널 창을 &#39;vim ~ / .bash_profile` 명령을 실행하십시오. 

2. ~ / .bash \ _profile 파일을 제어하십시오. 

export JAVA_HOME = $ (/ usr / libexec / java_home) 
export PATH = $ PATH : $ JAVA_HOME / bin 

3. ~ / .bash \ _profile 파일을 저장하십시오. 

    <img src="images/1m/image2.png" width="490" height="317" />

### JDK 설치 확인

1. **자바 버전 확인 :**터미널 창을 자바 
-version`을 사용하면됩니다. JRE가 선택하지 않는 메시지. 
JDK가 설치 가능합니다. 자바의 출력 
-version` 명령은 &quot;1.8.0 \ _121&quot;이상을 표시합니다. 

    <img src="images/1m/image3.png" width="556" height="115" />

## Netbeans 설치

다음 지침 설치, 설치 및 구성. 
컴퓨터의 Netbeans IDE. 

**참고 : Netbeans 8.1**은 최신 버전입니다. 
이 문서를 참조하십시오. 다운로드 사용하지 못한다. 
최신 버전의 IDE (사용) 및 이서 유용 
활동. 

Netbeans 8.1이 버전의 새로운 기능 
그런 다음**Netbeans 설치**단계를 건너 뛰고**확인 진행 
Netbeans 설치**단계. 

1. Firefox에서 다음 위치로. 
    <https://netbeans.org/downloads/>.

2. **모든 기술 지원 Netbeans 8.1 버전 다운로드 
마지막 열. 

3. **netbeans-8.1-macosx.dmg**설치 프로그램 파일을 다음 위치로 다운로드하십시오. 
너의 시스템 야. 다운로드 시간은 걸린 수 있습니다. 다운로드를 기다리십시오. 
다음 단계로 진행합니다. 

4. **netbeans-8.1-macosx.dmg**설치 프로그램을 선택하고 파일을 선택하십시오. 

5. **Netbeans 8.1.pkg**설치를 시작합니다. 

6. 보안 경고창에서**보기를 클릭하십시오. 

7. 소개 화면에서**여기를 클릭하십시오. 

8. 소프트웨어 사용권 조건을 동의하고 확인하십시오. 
**진행**버튼. 

9. 기본 설치 위치. 

10 **아파치 Tomcat을 클릭하십시오. 
8. 0.27**선택하고**설치**버튼을 클릭하십시오. 

11 . 사용자 요구를 입력하십시오. 

12 . 설치 프로그램 설치 및 &quot;**
설치가이게 수리.**&quot;메시지.**닫기**버튼을 클릭하십시오. 

### Netbeans 설치 확인

1. Netbeans 확인 :**Netbeans IDE를 시작하고 버전 확인 
IDE에서 JDK 번호 사용하기, Netbeans 8.1 시작하기 
응용 프로그램. Netbeans은 &quot;시작 페이지&quot;를 탐색합니다. 
넷빈즈에서 넷빈즈 정보를 선택하십시오. Netbeans 및 Java 
버전은 Netbeans IDE 8.1 및 Java 1.8.0 \ _121에 있습니다. 완료되면, 
정보 창을 닫습니다. 

    <img src="images/1m/image4.png" width="402" height="471" />

## GIT 설치

GIT 툴을 설치하고 설치하기 
컴퓨터. 

**참고 : GIT 버전 2.10.1**최신 버전의 도구입니다. 
이 문서 작성 카테고리. 너는 이겼다. 
이 도구의 최신 버전을 다운로드하십시오. 
실습 활동을 수행합니다. 

이미 GIT 2.10.1 이상 버전 설치 
그런 다음**GIT**활동 설치를 건너 뛰고**확인을 진행하십시오. 
GIT 설치**활동. 

1. 터미널 창을 지우고 - 버젼 전환 명령을합니다. 

    <img src="images/1m/image5.png" width="568" height="111" />

**참고 :**이 명령은 GIT 도구를 설치하지 마십시오. 

2. **설치**버튼을 클릭하십시오. 

    <img src="images/1m/image6.png" width="457" height="190" />

3. **동의 함**버튼을 사용권 계약을 클릭하십시오. 

4. 설치 프로그램을 실행할 때 GIT 확장 프로그램이 자동 설치됩니다. 
&quot;**소프트웨어가 설치되었습니다.**&quot;메시지가 있습니다. 클릭 
**완료**버튼. 

### GIT 설치 확인

1. **GIT 연장 확인 :** 터미널 창에서 &#39;자녀 
--version 명령. `git --version`의 결과가 나옵니까? 
명령 &quot;git version 2.10.1 (Apple Git-78)&quot; 

    <img src="images/1m/image7.png" width="570" height="80" />

## Maven 설치하기

Maven을 다운로드하고 설치하고 구성하십시오. 
귀하의 컴퓨터. 

**참고 : Maven 3.3.9**는 최신 버전의 도구입니다. 
이 문서를 작성하는 것. 너는 이겼다. 
이 도구의 최신 버전을 다운로드하고 사용하십시오. 
활동. 

Maven 3.3.9 이전 버전 설치 
그런 다음**Maven**활동 설치를 건너 뛰기로 설정하십시오. 
Maven 환경 변수**필요 설정 / 해제 작업 
환경 변수. 

1. 실행 
    <http://maven.apache.org/download.cgi>.

2. 바이너리 ZIP 아카이브,**apache-maven-3.3.9-bin.tar.gz**파일을 다운로드하십시오. 
컴퓨터에 연결합니다. 다운로드 긴 시간이 걸린 수 있습니다. 기다려라. 
다운로드에서 다음 단계로 진행하십시오. 

    <img src="images/1m/image8.png" width="624" height="129" />

3. / 응용 프로그램 / 응용 프로그램. 

4. 전체 경로 (/Applications/apache-maven-3.3.9)를 
결정 성공. 생산이 필요합니다. 
환경 변수. 

### Maven 환경 변수 설정하기

M2 \ _HOME 및 PATH 환경 설정 다음 지시 사항을 따르십시오. 
변수. 

**참고 :**관리자 권한이 시스템을 사용하십시오. 

1. 터미널 창을 &#39;vim ~ / .bash_profile` 명령을 실행하십시오. 

2. **~ / .bash \ _profile**파일을 사용합니다. 
. 

export M2_HOME = / 응용 프로그램 / apache-maven-3.3.9 
export PATH = $ PATH : $ M2_HOME / bin 

3. **~ / .bash \ _profile**파일을 저장하십시오. 

    <img src="images/1m/image9.png" width="469" height="295" />

### 메이 벤 설치 확인

1. Maven 버전 확인**: 터미널 창을 다시 시작하고 
`mvn --version` 명령. `mvn --version` 명령의 출력이 &quot; 
다음 스크린 샷과 일치하는 항목 확인. 

    <img src="images/1m/image10.png" width="553" height="167" />
