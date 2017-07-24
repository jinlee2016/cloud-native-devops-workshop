# 2 부 : Oracle Developer Cloud Service를 사용하여 Helloworld App 테스트 및 사용




## Make-up



**중요 사항 :** 보안 네트워크 Maven을 선택하면 다음과 같은 경고 메시지가 표시됩니다. 그때는 건너 뛰기**GITistor 생성**로 이동 시도. 

### Netbeans의 Maven에 대한 설정



1. C : \\ Program Files \\ NetBeans 8. 1 \\ java \\ maven \\ conf \\ settings.xml 파일을 메모장에 놓습니다. 

**참고 :** Mac 설정 파일. / 응용 프로그램 / NetBeans / NetBeans 8. 1.app/Contents/Resources/Netbeans/java/maven/conf/settings.xml. 

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




3.  Replace **ENTER YOUR PROXY ADDRESS** within the <host> tag
임시 저장하고 파일을 저장합니다. 

**참고 :** settings.xml C : \\ Program Files \ \ NetBeans 8. 1 settings \\ java \\ maven \ settings.xml 파일의 설정을 저장하는 데 문제가있을 수 있습니다. \ conf \\ (Windows) 또는 / Applications / NetBeans / NetBeans 8. 1.app/Contents/Resources/Netbeans/java/maven/conf/ (Mac) 디렉토리입니다. 

### Maven의 프록시 설정



1. NotePad ++와 같은 텍스트 편집기 C : \\ Maven \\ apache-maven-3. 3.9  \\ conf \\ settings.xml 

**참고 :** Mac 설정 파일. /Applications/apache-maven-3. 3.9/ conf/settings.xml. 

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




3.  Replace **ENTER YOUR PROXY ADDRESS** within the <host> tag
임시 저장하고 파일을 저장합니다. 

## GIT res 만들기



이 활동의 ​​일환으로 사용자의 홈 아래에있는 GIT 저장소를 초기화하십시오. 

1. Windows**시작**메뉴에서 열심히 Mac을 사용하여 터미널 창을 사용하십시오. 

2. 홈 디렉토리에서**구름**디렉토리를 작성하십시오. 

        mkdir cloud



3. 디오를**구름**디렉토리로 변경하십시오. 

        cd cloud



4. 주어진 유형을 선택하십시오. 

        git init



5. 많은 사람들이 Git 저장소에 있습니다. `ls -a` 명령을 실행하면 당신이 확인해보세요. `ls -a` 명령의 출력은 스크린 샷의 결과와 일치합니다 : 

    <img src="images/2/image1.png" width="497" height="124" />



**참고 :** 지금은 .git 디렉토리가 생성 목록을 준비합니다. 

## GIT 저장소 구성



GIT 저장소는 전자 메일 주소를 변경하여 저장자를 식별 할 수 있습니다. 

1. 다음 명령을 실행하여 구성하십시오. 

        git config --global user.name "Your Name"



**예 :** `git config -global user.name &quot;John Doe&quot;` 

2. 다음 명령어를 전자 메일 주소로 구성하십시오. 

        git config --global user.email your-email@address




    **Example:** `git config –global user.email <john.doe@oracle.com>`



3. 다음 명령을 실행하십시오. 

        git config --global –l



이 명령의 출력은 스크린 샷의 출력과 유사합니다. 

<img src="images/2/image2.png" width="420" height="219" />



**참고 :** 
- 모든 GIT 프로젝트의 이름과 이메일 주소를 설정하십시오. 
- - 글로벌 옵션을 사용하여 프로젝트 레벨에서 전자 메일 주소를 설정할 수 있습니다. 

## Maven 프로젝트 유형을 사용하여 프로젝트 만들기



**Hello World! Example**Hello world! Example &quot;Hello World!&quot;를 인쇄하십시오. message to display. 이 프로그램은 GIT 저장소에 저장하고, DevCS에서 프로젝트를 만들고, DevCS의 GIT 저장소에서 다음 작업을 생성합니다. 

Archetypes가 Maven 프로젝트를 사용하여 지시 사항을 생성합니다. 

1. Windows 시작 메뉴에서 Git Bash를 열거 나 Mac을 사용하여 터미널 창을 엽니 다. 

2. 데이터 저장 공간을 변경합니다. 

        cd cloud



3. 헬로 월드를 만들면서 작성합니다. 

        mkdir helloworld



4. Helloworld 디렉토리로 변경하기. 

        cd helloworld



5. Maven-archetype-quickstart Maven 프로젝트에서 빈을 사용하십시오. 다음 명령어를 입력하십시오. 

        mvn archetype:generate -DgroupId=com.example -DartifactId=Helloworld-Example -DarchetypeArtifactId=maven-archetype-quickstart -DinteractiveMode=false



**참고 :** 명령의 출력은 스크린 샷의 출력과 유사합니다. 

<img src="images/2/image3.png" width="317" height="363" />



6. Helloworld-Example**은 Maven 프로젝트를 실행합니다. 디렉토리 구조에서 검사 클래스를 com.example.App에 설치하십시오. 이제 pom.xml 파일을 사용하여 플러그인을 구성하십시오. 

7. 넷빈즈를 사용 하시려면 여기를 클릭하십시오. 

8. Netbeans의**구름 / 헬로우 월드**헬프 월드 - 예**Maven 프로젝트를위한 연습. 

    <img src="images/2/image4.png" width="374" height="193" />



9. 프로젝트의 디렉토리 구조를 검사하고**com.example.App**실행 가능 클래스를 사용하여 전파를 조사하십시오. 

    <img src="images/2/image5.png" width="384" height="181" />



10. **Project Files> pom.xml**을 클릭하고 클릭하십시오. 

    <img src="images/2/image6.png" width="242" height="242" />



11 . dependency section in configuration. 프로젝트의 자바 버전을 설정합니다. 

```xml
    <properties>
      <java.version>1.8</java.version>
      <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    </properties>
```



12 . 의존성은 추가 구성 요소를 추가합니다. 

```xml
    <build>
      <plugins>
      <!-- Your plugins go here -->
      </plugins>
    </build>
```



13 . 플러그인의 구성을 추가하십시오. 

```xml
    <plugin>
      <groupId>org.apache.maven.plugins</groupId>
      <artifactId>maven-compiler-plugin</artifactId>
      <version>2.3.2</version>
      <configuration>
        <source>1.8</source>
        <target>1.8</target>
      </configuration>
    </plugin>
```



14 . pom.xml 파일에 임원 플러그인을 추가하십시오. 

```xml
    <plugin>
      <groupId>org.codehaus.mojo</groupId>
      <artifactId>exec-maven-plugin</artifactId>
      <version>1.4.0</version>
      <executions>
        <execution>
          <goals>
            <goal>exec</goal>
          </goals>
        </execution>
      </executions>
      <configuration>
        <mainClass>com.example.App</mainClass>
      </configuration>
    </plugin>
```



15 . pom.xml 파일에 JAR 플러그인을 추가하십시오. 

```xml
    <plugin>
      <groupId>org.apache.maven.plugins</groupId>
      <artifactId>maven-jar-plugin</artifactId>
      <version>2.6</version>
      <configuration>
        <archive>
          <manifest>
            <mainClass>com.example.App</mainClass>
          </manifest>
        </archive>
      </configuration>
    </plugin>
```



16 . 소스 창에서**파일을 클릭하고 파일을 선택하여 파일을 복사하십시오. 

<img src="images/2/image7.png" width="276" height="227" />



17. **pom.xml**파일을 저장합니다. 

18. **Helloworld - 예제**프로젝트를 클릭하고**깨끗하게하고 빌드하십시오.**를 클릭하십시오.**

19. **Helloworld - 예제**실행을 클릭하고**실행**을 클릭하십시오.**

    <img src="images/2/image8.png" width="231" height="196" />



20 . 사용 가능한 기본 클래스 목록에서**com.example.App**선택하고**주 클래스 선택**버튼을 클릭하십시오. 

<img src="images/2/image9.png" width="231" height="225" />



21 . 성공하기 메시지**Hello World!**가 나와. 

<img src="images/2/image10.png" width="406" height="152" />



22 . Git Bash (Windows) 또는 Terminal 창 (Mac)과 Helloworld-Example로 변경하십시오. 

        cd Helloworld-Example




<img src="images/2/image11.png" width="395" height="100" />



23 . mvn clean 컴파일 명령을 실행하고 프로젝트를 완성하십시오. 

<img src="images/2/image12.png" width="363" height="387" />



24 . mvn exec : java 명령을 실행하고 응용 프로그램을 실행합니다. 

<img src="images/2/image13.png" width="360" height="297" />



25 . mvn 패키지 명령어를 실행하고 응용 프로그램을 패키지화합니다. 

<img src="images/2/image14.png" width="435" height="235" />



**참고****구름 / 헬로우 월드 / 헬로우 월드 - 예 / 목표**홀트 제작**Helloworld-Example-1. 0-SNAPSHOT.jar**파일을 검사하십시오. 

26. `java -jar target / Helloworld-Example-1. 0-SNAPSHOT.jar` 명령을 실행하여 응용 프로그램을 실행하십시오. 

    <img src="images/2/image15.png" width="454" height="120" />




## GIT 저장소를 사용하는 Helloworld-Example 프로젝트



다음 Helloworld-Example 프로젝트에 GIT 저장하기 

1. cloud / helloworld 디렉토리로 바꾸기. 

2. `git add -n .` 명령을 실행하여 추가 준비가 된 파일의 목록을보십시오. 

    <img src="images/2/image16.png" width="408" height="102" />



**참고 사항 :** 감사의 말**.**가 포함되어 있습니다. 

3. &#39; git add&#39; . 명령을 실행하고 파일을 추가하십시오. 

    <img src="images/2/image17.png" width="408" height="102" />



4. `git status` 명령을 실행하여 추가 파일을 확인하십시오. 

    <img src="images/2/image18.png" width="408" height="106" />



5. Helloworld-Example Project &quot;에 대한 명령을 실행하고 파일을 저장하고 버전 추적을 시작하십시오. 

    <img src="images/2/image19.png" width="415" height="108" />



6. 지금은 파일이 없습니다. 

7. `git status 명령 &#39; 을 실행하여 상태를 확인하십시오. 

    <img src="images/2/image20.png" width="415" height="84" />



**참고 :** 스크린 샷에 대해서도 대등 한 응답을 받아 들일 수 있습니다. 

## 개발자 클라우드 서비스 프로젝트 만들기



이 액티비티는 기본 데이터 센터에서 정보를 정의하고 데이터를 지우면 데이터를 복제하거나 복제 할 수 있습니다. 

(HelloworldProjectRepo) HelloworldProject (HelloworldProject)를 사용하여 응용 프로그램을 다운로드 할 수 있습니다. 

**참고 :** 연습의 부분은 돈돈 자격 증명 및 링크가 필요합니다. 그곳에서 정보를 수집하고 즐기십시오. 

## storage layer configuration




### Oracle Cloud 계정에 로그인하십시오.




1. From any browser, go to the URL: <https://cloud.oracle.com>



2. 브라우저의 오른쪽 상단 모서리에**로그인**을 클릭하십시오. 

    <img src="images/2/Picture100-1.png" width="429" height="119" />



3. ****중요**- 내 서비스에서 드롭 다운 목록에서 올바른 데이터 센터를 선택하고**내 서비스**를 클릭하십시오. 직접 선택 데이터 센터에서 알 수없는 경우 개인 훈련 이벤트입니다.***강좌**에**Local**에있는 드롭 다운 목록에서 선택하십시오. 평가판을 사용하여 평가판을 작성하십시오 로컬에서 사전 선택하는 URL을 제공하십시오. 

    <img src="images/2/Picture100-2.png" />



4. ID 도메인을 선택하고**이동**을 클릭하십시오. 

**참고 :** **ID ID, 사용자 이름**및**비밀번호**값 또는 강좌 또는 시험판 확인 이메일이 있습니다. 

5. 로그인을 클릭하고 로그인하십시오. 

    <img src="images/2/Picture100-3.5.png" />



6. 고객 서비스는 대용량이됩니다. 

    <img src="images/2/Picture100-4.png" />



7. 모든**스토리지**클라우드 서비스는 보이지 않는 폴더**대시 보드 사용자 정의****************************************응용 프로그램 컨테이너, 개발자 및 저장 장치. 특별한 서비스를 받으려면 클릭하십시오. 

    <img src="images/2/Picture100-5.png" />




### 스토리지 계층화 정책 확인 / 설정



이전 버전의 복제 정책을 사용하면 복제 정책을 사용하지 않을 수 있습니다. 스토리지 클라우드 서비스가 복제 정책의 상태를 확인하십시오. 

1. **스토리지**클라우드 서비스를 클릭하십시오.    <img src="images/2/Picture-01.png" />



2. 아이콘 상단의**아이콘을 클릭하십시오. 

    <img src="images/2/Picture-01.5.png" />



3. 대화 상자는 복제 정책을 사용하여 복제 정책을 설명합니다. 기본값을 사용하고 정책 설정**버튼을 클릭하십시오. 이 정책은 워크샵에 준비가되었습니다. 

    <img src="images/2/Picture-02.5.png" />



4. 지금까지 복제 정책을 설정하고 실행 창을 닫으십시오. 



### 내 서비스 포털을 사용하여 복제 정책 확인



Oracle Storage Cloud Service에서 대시 보드**페이지에서**스토리지**링크를 클릭하십시오. 결과 페이지에서**서비스 내용 : Oracle Storage Cloud Service를 확장하십시오.**Oracle Storage Cloud Service 인스턴스의 세부 사항이 표시됩니다. 다음으로 스크린 샷을 펼치기 복제 정책 필드를 찾으십시오. 

<img src="images/2/image30.png" width="348" height="116" />




## 학생 클라우드 서비스 활성화 및 새 프로젝트 만들기



DevCS에서 새 프로젝트를 개발하고, DevCS에서 GIT 저장소를 생성하고, DevCS GIT 저장소를 사용하여 로컬 빌드 프로젝트를 생성하고 생성합니다. 

다음 지시 사항에 따라 DevCS를 활성화하고 새 프로젝트를 수행하십시오. 

1. 개발자 서비스는 보이지 않습니다.**개발자**서비스**버튼을 클릭하고**앱 컨테이너**에 대한**표지**버튼을 클릭하십시오. 대시 보드에 표시됩니다. 

    <img src="images/2/image31.png" width="378" height="237" />



2. 대시 보드에서**개발자 클라우드 서비스**를 클릭하면**ServiceDetails : developer85599  (Oracle Developer Cloud Service)**페이지로 이동하십시오. 

    <img src="images/2/image32.png" width="454" height="134" />



3. 서비스를 다시 클릭하십시오.**버튼을 클릭하십시오. 

    <img src="images/2/image33.png" width="399" height="195" />



4. **새 프로젝트**를 클릭하십시오. 

    <img src="images/2/image34.png" width="399" height="245" />



5. 다음 화면을 클릭하고**다음을 클릭하십시오**. 

    <img src="images/2/image35.png" width="399" height="288" />



6. 프로젝트를 클릭하고**다음을 클릭하십시오.**

    <img src="images/2/image36.png" width="378" height="271" />



7. Wiki Markup 토론 목록에서**MARKDOWN**을 선택하고**Finish**를 클릭하십시오. 

    <img src="images/2/image37.png" width="384" height="277" />



8. 프로비저닝 HelloworldProject는 분분하면됩니다. HelloworldProject 홈 화면으로 돌아 가기 

    <img src="images/2/image38.png" width="388" height="141" />




## GITector에서 제공하는 패키지 배송 서비스



다음 길라잡이 안내 서비스에 GIT 저장소가 있습니다. 

1. **REPOSITORIES**섹션에서**New Repository**버튼을 클릭하십시오. 

    <img src="images/2/image39.png" width="360" height="130" />



2. New Repository (새 저장소) 다음을 클릭하십시오.****을 (를) 작성하십시오. 

    <img src="images/2/image40.png" width="351" height="282" />



3. 저장소를 생성합니다. HelloworldProjectRepo 저장소 HelloworldProjectRepo 홈 페이지에서 새로 고침. 

    <img src="images/2/image41.png" width="384" height="103" />



4. HelloworldProjectRepo 홈 페이지에서 HTTP를 클릭하고 URL을 복사하십시오. 

    <img src="images/2/image42.png" width="384" height="106" />




## GIT 저장소



다음 지침에 따라 Helloworld-Example 프로젝트 호스팅 패키지를 Ghost에 저장하십시오. 

1. GIT 스토리지를 사용하여 클라우드 / helloworld를 변경하십시오. 

2. `git clone`을 실행하십시오. https / ora1  @ developer.em2. oraclecloud.com / developer85599- ouopc084  / s / developer85599- ouopc084_ helloworldproject_3753  / scm / HelloworldProjectRepo.git` 

    <img src="images/2/image43.png" width="427" height="111" />



**참고 :** 
- 사용자가 암호를 입력하면 암호를 입력하십시오. 
명령이 403  오류로 실패하고 명시 적으로 암호를 언급합니다        the GIT repository URL. For example: `git clone https://ora1:e1Car030@developer.em2.oraclecloud.com/developer85599-ouopc084/s/developer85599-ouopc084\_helloworlsprojectrepo\_4070/scm/HelloworldProjectRepo.git`


- 명령의 출력은 명령의 출력과 유사합니다. 위의 스크린 샷. 


3. **helloworldProjectRepo**클라우드 / helloworld**를 생성합니다. 

4. **helloworld - 예제**프로젝트 디렉토리에서**cloud / helloworld**디렉토리에서**HelloworldProjectRepo**디렉토리로 복사를 시도하십시오. 

**참고 :** HelloworldProjectRepo**디렉토리의 내용은 스크린 샷과 일치합니다. 

<img src="images/2/image44.png" width="441" height="89" />



5. **HelloworldProjectRepo**디렉토리로 변경하십시오. 

        cd HelloworldProjectRepo



6. 프로젝트 디렉토리에서 GIT에 소스 파일을 추가하십시오 

        git add .



7. 변경 사항 적용 

        git commit –m "commiting changes to HelloworldProjectRepo repository"



8. 자선 서비스의 저장고를 푸시합니다. 

        git push origin master



9. 차량 대여 서비스를 푸시 한 파일을 확인하십시오. 

10. **HelloworldProject**홈 페이지에서**HelloworldProjectRepo.git**를 클릭하십시오. 

    <img src="images/2/image45.png" width="378" height="150" />



11. **Helloworld - 예**프로젝트의 길잡이는 자원 봉사자의 수퍼 스타가됩니다. 클릭하고 내용을 확인하십시오. 

    <img src="images/2/image46.png" width="385" height="153" />




    <img src="images/2/image47.png" width="385" height="158" />




## 개발자 클라우드 서비스에 대한 프로젝트 빌드



다음 지침 Helloworld-Example project 개발자 Cloud Service를 빌드합니다. 

1. 왼쪽 탐색 창에서 다음을 클릭하십시오**새 작업**을 클릭하십시오. 

    <img src="images/2/image48.png" width="457" height="201" />



2. 새 작업 창에서**HelloworldProjectBJ**작업 이름 입력 및 저장**을 클릭하십시오. 

    <img src="images/2/image49.png" width="457" height="167" />



3. **주**탭에서 다음 값을 입력하십시오. 

- 조정. 
- 설명을 입력하십시오. 
- **JDK**를**JDK 8로 설정하십시오.**

    <img src="images/2/image50.png" width="433" height="204" />



4. **소스 제어**탭을 클릭하십시오. 

- **Git**을 보유하고 선택하십시오. 
- **URL**의 사례 URL은 선택합니다. 

<img src="images/2/image51.png" width="433" height="211" />



5. **설치 단계**탭을 클릭하십시오. 

- Maven 3를 선택하고 빌드를 선택하십시오. 
- **목표**를 클린턴으로 설정하십시오. 
- **POM 파일**위치 Helloworld-Example / pom.xml로 설정하십시오. 

    <img src="images/2/image52.png" width="441" height="189" />




    <img src="images/2/image53.png" width="441" height="235" />



6. **게시물 작성**탭을 클릭하십시오. 

- 아티팩트 아크를 선택하십시오. 
- Helloworld-Example / target / Helloworld-Example-1. 0-SNAPSHOT.jar 
- 압축 유형을 선택하지 않으면 설정합니다. 

    <img src="images/2/image54.png" width="443" height="184" />



7. 저장**다음을 클릭하십시오**지금 클릭하십시오.**

Helloworld-Example / target / Helloworld-Example-1. 0-SNAPSHOT.jar에 대한 요약을 참고하십시오. 파일 이름을 클릭하면 다운로드 할 수 있습니다. 

더 많은 정보를 얻으려면 로그인하십시오**더 많이 읽음 로그인 더 이상 선택하지 않으셨습니까? 

<img src="images/2/image55.png" width="453" height="183" />



Maven 프로젝트 생성, Maven 프로젝트 저장, DevCS 활성화, DevCS에서의 프로젝트 생성, GIT 저장소 생성, DevCode 생성, 생성하기.