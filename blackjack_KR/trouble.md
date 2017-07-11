# 문제 해결 팁

다음은 수행하는 동안 발생할 수있는 몇 가지 문제입니다. 
이 연습 및 아래 문제 해결 팁과 절차가 있습니다. 
당신이 그들을 해결할 수 있습니다. 

## 프록시 문제

Maven 및 Netbeans에 프록시 문제가 발생할 수 있습니다. 
보안 된 네트워크와 방화벽 뒤에. 이것은 주로 
Maven에서 새 프로젝트를 만들거나 기존 프로젝트를 실행할 때 
Maven 프로젝트에서는 여러 설정 파일을 다운로드하는 경향이 있습니다. 
프록시 설정이 완료되지 않으면 다운로드가 실패합니다. 

**참고 :**프록시에 대해서는 이벤트 관리자 또는 네트워크 관리자에게 문의하십시오. 
주소 

### Maven에서 프록시 문제 해결 :

1. C : \\ Maven \\ apache-maven-3.3.9 \\ conf \\ settings.xml 파일을 다음과 같이 엽니 다. 
    a text editor like Notepad++.

2.  Add the following lines under the `<proxies>` tag:

    ```xml
    <proxy>
      <id>Oracle</id>
      <active>true</active>
      <protocol>http</protocol>
      <host>**ENTER YOUR PROXY ADDRESS**</host>
      <port>80</port>
      <nonProxyHosts>localhost|oracle.com</nonProxyHosts>
    </proxy>
    ```

3.  Replace **ENTER YOUR PROXY ADDRESS** within the `<host>` tag
    with your proxy and save the file.

### Netbeans에서 프록시 문제 해결 :

1. C : \\ Program Files \\ NetBeans를 엽니 다. 
    8.1\\java\\maven\\conf\\settings.xml file with a text editor
    like Notepad++.

2.  Add the following lines under the <proxies> tag:

    ```xml
    <proxy>
      <id>Oracle</id>
      <active>true</active>
      <protocol>http</protocol>
      <host>**ENTER YOUR PROXY ADDRESS**</host>
      <port>80</port>
      <nonProxyHosts>localhost|oracle.com</nonProxyHosts>
    </proxy>
    ```

1.  Replace **ENTER YOUR PROXY ADDRESS** within the `<host>` tag
    with your proxy and save the file.

## 항만 충돌 문제

포트로 인해이 프로젝트를 실행할 때 문제가 발생할 수 있습니다. 
갈등 문제. 이 응용 프로그램은 Apache Tomcat에 배포됩니다. 
서버와 그것을 듣기 위해서는**8080**로컬 포트 ​​번호가 필요합니다. 
클라이언트 요청.**8080**에서 실행중인 서비스를 중지하십시오. 
로컬 포트 ​​번호. 

**TCPView**도구를 사용하여 프로세스를 식별하고 종료 할 수 있습니다. 
이 포트 번호. 

[**다운로드 링크**] (https://technet.microsoft.com/en-us/sysinternals/bb897437) 

## 403 상태 코드로 GIT 복제 오류 발생

`git clone` 명령은 사용자 이름과 
암호 (클라우드 계정 로그인 자격 증명). 당신이 요청하지 않으면 
사용자 이름과 암호 그리고이 명령이 403 오류로 실패하면 
비밀 번호를 명시 적으로 GIT 저장소 URL을 언급하십시오. 

다음은 암호가있는 업데이트 된 git clone 명령입니다. 

    git clone https://ora1:e1Car030@developer.em2.oraclecloud.com/developer85599-ouopc084/s/developer85599-ouopc084\_helloworlsprojectrepo\_4070/scm/HelloworldProjectRepo.git

참조 용 스크린 샷은 다음과 같습니다. 

<img src="images/t/image1.png" width="335" height="228" />
