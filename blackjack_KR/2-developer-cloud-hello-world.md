# 2 부 : Oracle Developer Cloud Service를 사용하여 Helloworld App 테스트 및 구축

## 메이븐을위한 프록시 설정

**중요 사항 :** 프록시를 변경하려면 다음 지침을 따르십시오. 
보안 네트워크의 일부인 경우 Maven의 설정 
방화벽**전용**이 활동을 건너 뛰고 
다음 활동,**GIT 저장소 만들기**. 

### Netbeans의 Maven에 대한 프록시 설정

1. C : \\ Program Files \\ NetBeans를 엽니 다. 
8. 1 \\ java \\ maven \\ conf \\ settings.xml 파일과 텍스트 편집기 
메모장 + +처럼. 

**참고 :** Mac에서는 settings.xml 파일을 다음 위치에서 찾을 수 있습니다. 
/ Applications / NetBeans / NetBeans 8.1.app/Contents/Resources/Netbeans/java/maven/conf/settings.xml 

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
프록시로 저장하고 파일을 저장하십시오. 

**참고 :** settings.xml 파일을 편집 할 때 문제가 발생하면, 
settings.xml 파일의 복사본을 다른 위치에 저장하고 수정 한 다음, 
C : \\ Program Files \\ NetBeans에 다시 넣습니다. 
8. 1 \\ java \\ maven \\ conf \\ (Windows) 또는 / Applications / NetBeans / NetBeans 8.1.app/Contents/Resources/Netbeans/java/maven/conf/ (Mac) 디렉토리에 있습니다. 

### Maven의 프록시 설정

1. C : \\ Maven \\ apache-maven-3.3.9 \\ conf \\ settings.xml 파일을 다음과 같이 엽니 다. 
메모장 ++와 같은 텍스트 편집기. 

**참고 :** Mac의 경우 settings.xml 파일은 /Applications/apache-maven-3.3.9/conf/settings.xml에서 찾을 수 있습니다. 

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
프록시로 저장하고 파일을 저장하십시오. 

## GIT 저장소 만들기

이 액티비티의 일환으로 다음을 작성하고 초기화하는 방법을 배웁니다. 
사용자의 홈 디렉토리 아래 로컬 GIT 저장소. 

1. Windows**시작**메뉴에서 Git Bash를 열거 나 Mac을 사용하는 경우 터미널 창을여십시오. 

2. 홈 디렉토리에서**cloud**디렉토리를 작성하십시오. 

mkdir cloud 

3. 디렉토리를**cloud**디렉토리로 변경하십시오. 

cd cloud 

4. Git 저장소 유형을 만듭니다. 

자식 init 

5. 이제 클라우드 디렉토리가 Git 저장소가됩니다. `ls -a`를 실행하십시오. 
명령은 동일한 것을 확인합니다. `ls -a` 명령의 출력은 반드시 
다음 스크린 샷의 결과와 일치시킵니다. 

    <img src="images/2/image1.png" width="497" height="124" />

**참고 :** .git 디렉토리가 생성 된 것을 볼 수 있습니다. 
클라우드 디렉토리에 저장되고 저장소가 준비됩니다. 

## GIT 저장소 구성

GIT 저장소에 변경 사항을 적용하기 전에 
이름 및 전자 메일 주소를 사용하여 저장소의 커밋을 식별합니다. 

1. 다음 명령을 실행하여 이름을 구성하십시오. 

자식 설정 - 글로벌 user.name &quot;귀하의 이름&quot; 

**예 :** `git config -global user.name &quot;John Doe&quot;` 

2. 다음 명령을 실행하여 전자 메일 주소를 구성합니다. 

자식 구성 - 전역 user.email - 이메일 @ 주소 

    **Example:** `git config –global user.email <john.doe@oracle.com>`

3. 값이 설정되었는지 확인하려면 다음을 실행하십시오. 
명령: 

자식 설정 - 글로벌 - 난 

이 명령의 출력은 다음 명령의 출력과 유사해야합니다. 
다음 스크린 샷 : 

<img src="images/2/image2.png" width="420" height="219" />

**노트:** 
- 모든 GIT 프로젝트의 이름과 이메일 주소를 설정합니다. 
- - global 옵션을 사용하여 이름과 이메일 주소를 설정하지 마십시오. 
프로젝트 수준. 

## Maven 아키 타입을 사용하여 프로젝트 만들기

이 액티비티의 일환으로 간단한 Maven을 만드는 방법을 배웁니다. 
**Hello World!를 인쇄하는**Helloworld-Example**
메시지를 콘솔에 표시합니다. 이 응용 프로그램은 다음 
로컬 GIT 저장소에 저장하는 활동, 프로젝트를 만드는 활동 
DevCS, DevCS의 GIT 저장소로 복제 한 다음 Build를 만듭니다. 
배포 작업. 

Archetypes를 사용하여 Maven 프로젝트를 생성하려면 다음 지시 사항을 따르십시오. 

1. Windows 시작 메뉴에서 Git Bash를 열거 나 Mac을 사용하는 경우 터미널 창을여십시오. 

2. Git 저장소가 저장된 클라우드 디렉토리로 변경한다. 

cd cloud 

3. helloworld라는 디렉토리를 작성하십시오. 

mkdir helloworld 

4. Helloworld 디렉토리로 변경하십시오. 

cd helloworld 

5. 다음을 사용하여 빈 Maven 프로젝트를 만듭니다. 
maven-archetype-quickstart archetype. 다음 명령을 입력하십시오. 

mvn archetype : 생성 -DgroupId = com.example -DartifactId = Helloworld-Example -DarchetypeArtifactId = maven-archetype-quickstart -DinteractiveMode = false 

**참고 :** 이 명령의 출력은 다음 스크린 샷의 출력과 유사해야합니다. 

<img src="images/2/image3.png" width="317" height="363" />

6. 이 명령은 이름이 지정된 빈 Maven 프로젝트를 만듭니다. 
**Helloworld - 예**. 디렉토리 구조를 검사하고 기록하십시오. 
실행 가능한 클래스는 com.example.App에 있습니다. 이제 
pom.xml 파일을 구성해야합니다. 
플러그인. 

7. 바탕 화면의 바로 가기를 사용하여 Netbeans을 시작합니다. 

8. 아래에서 생성 된**Helloworld-Example**Maven 프로젝트를 엽니 다. 
**구름 / helloworld**디렉토리에 Netbeans. 

    <img src="images/2/image4.png" width="374" height="193" />

9. 프로젝트의 디렉토리 구조를 검사하고, open 
**com.example.App**실행 가능한 클래스를 만들고 코드를 검토하십시오. 

    <img src="images/2/image5.png" width="384" height="181" />

10. **Project Files> pom.xml**파일을 마우스 오른쪽 버튼으로 클릭하고 열기를 클릭합니다. 

    <img src="images/2/image6.png" width="242" height="242" />

11. 파일 앞에 다음 속성 설정을 추가합니다. 
의존성 섹션. 자바 버전과 인코딩을 설정합니다. 
프로젝트. 

    ```xml
    <properties>
      <java.version>1.8</java.version>
      <project.build.sourceEncoding>UTF-8</project.build.sourceEncoding>
    </properties>
    ```

12 . dependencies 요소 뒤에 빌드 및 플러그 인에 대한 요소를 추가하십시오. 

    ```xml
    <build>
      <plugins>
      <!-- Your plugins go here -->
      </plugins>
    </build>
    ```

13 . 컴파일러 플러그인의 구성을 
플러그인 섹션. 

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

14 . pom.xml 파일에 exec 플러그인을 추가하십시오. 

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

16 . 소스 창에서**pom.xml**파일을 마우스 오른쪽 단추로 클릭하고**서식**을 선택하여 파일의 들여 쓰기를 수정하십시오. 

<img src="images/2/image7.png" width="276" height="227" />

17 .**pom.xml**파일을 저장하십시오. 

18 .**Helloworld-Example**프로젝트를 마우스 오른쪽 버튼으로 클릭하고**Clean을 클릭하십시오. 
및 빌드.**

19 .**Helloworld-Example**프로젝트를 마우스 오른쪽 버튼으로 클릭하고**Run을 클릭하십시오.**

<img src="images/2/image8.png" width="231" height="196" />

20 . 사용 가능한 기본 클래스 목록에서**com.example.App**를 선택하고 
**Select Main Class**버튼을 클릭하십시오. 

<img src="images/2/image9.png" width="231" height="225" />

21 . 당신은**Hello World!를보아야합니다!**BUILD SUCCESS 메시지를 출력하십시오. 

<img src="images/2/image10.png" width="406" height="152" />

22 . Git Bash (Windows) 또는 터미널 창 (Mac)으로 전환하고 
디렉토리에서 Helloworld-Example으로 이동하십시오. 

cd Helloworld - 예 

<img src="images/2/image11.png" width="395" height="100" />

23 .`mvn clean compile` 명령을 실행하여 정리하고 컴파일하십시오. 
프로젝트. 

<img src="images/2/image12.png" width="363" height="387" />

24 . mvn exec : java` 명령을 실행하여 응용 프로그램을 실행합니다. 

<img src="images/2/image13.png" width="360" height="297" />

25 . mvn 패키지 명령을 실행하여 응용 프로그램을 패키지화하십시오. 

<img src="images/2/image14.png" width="435" height="235" />

**참고 :** **Helloworld-Example-1.0-SNAPSHOT.jar**파일을 검사하십시오. 
**구름 / 헬로우 월드 / 헬로우 월드 - 예 / 타겟**내부에서 생성되었습니다. 
예배 규칙서. 

26 .`java -jar target / Helloworld-Example-1.0-SNAPSHOT.jar`을 실행하십시오. 
명령을 사용하여 패키지 된 응용 프로그램을 실행하십시오. 

<img src="images/2/image15.png" width="454" height="120" />

## Helloworld-Example 프로젝트를 GIT 저장소로 확인하기

다음 지침에 따라 Helloworld-Example 프로젝트를 저장하십시오. 
로컬 GIT 저장소에 있습니다. 

1. cloud / helloworld 디렉토리로 변경하십시오. 

2. `git add -n .` 명령을 실행하여 파일 목록을 봅니다. 
저장소에 추가 할 준비가되었습니다. 

    <img src="images/2/image16.png" width="408" height="102" />

**참고 :** 명령 끝에**.**가 있음에 유의하십시오. 

3. `git add .` 명령을 실행하여 파일을 저장소에 추가하십시오. 

    <img src="images/2/image17.png" width="408" height="102" />

4. `git status` 명령을 실행하여 추가 된 파일을 확인하십시오. 

    <img src="images/2/image18.png" width="408" height="106" />

5. Helloworld를위한`git commit -m &#39;초기 커밋을 실행한다. 
파일을 리포지토리에 커밋하고 시작하는 &quot;Project&quot;프로젝트 
버전 추적. 

    <img src="images/2/image19.png" width="415" height="108" />

6. 이제 파일이 버전 추적을 위해 체크인됩니다. 

7. `git status 명령`을 실행하여 저장소의 상태를 확인하십시오. 

    <img src="images/2/image20.png" width="415" height="84" />

**참고 :** 귀하는 
스크린 샷. 

## 개발자 클라우드 서비스 프로젝트 만들기

이 작업의 일부로 복제 정책을 선택합니다 (복제 정책을 선택하면 
Identity Domain 관리자가 아직 수행하지 않은) 
기본 데이터 센터는 또한 데이터가 있어야하는지 여부를 지정합니다. 
지리적으로 멀리 떨어져있는 (보조) 데이터 센터에 복제됩니다. 

개발자 클라우드 서비스를 활성화하여 빈 프로젝트 만들기 
(HelloworldProject)와 푸시 할 저장소 (HelloworldProjectRepo) 
Helloworld-Example**응용 프로그램**
이전**활동**에서 개발자 클라우드 서비스. 

**참고 :** 수행하려면 클라우드 로그인 자격 증명 및 링크가 필요합니다. 
운동의이 부분. 전자 메일에서이 정보를 수집하십시오. 
오라클에서 제공하여 편리하게 사용하십시오. 

## 저장소 복제 정책 구성

### Oracle Cloud 계정에 로그인하십시오.

1. From any browser, go to the URL: <https://cloud.oracle.com>

2. 브라우저의 오른쪽 상단 모서리에있는**로그인**을 클릭하십시오. 

    <img src="images/2/Picture100-1.png" width="429" height="119" />

3. ****중요**- 내 서비스에서 드롭 다운 목록에서 올바른 데이터 센터를 선택하고**내 서비스**를 클릭하십시오. 직접 선택해야하는 데이터 센터를 알지 못하는 경우 이것은 개인 훈련 이벤트입니다.***강사**에게**Region**에 드롭 다운 목록에서 선택하도록 요청하십시오. 오라클 평가판을 통해 계정을받은 경우 평가판 확인 이메일에 해당 지역을 사전 선택하는 URL이 제공되어야합니다. 

    <img src="images/2/Picture100-2.png" />

4. ID 도메인을 선택하고**이동**을 클릭하십시오. 

**참고 :** **ID 도메인, 사용자 이름**및**비밀번호**값은 강사 또는 시험판 확인 이메일에서 제공됩니다. 

5. 신원 도메인이 설정되면 사용자 이름과 암호를 입력하고**로그인**을 클릭하십시오. 

    <img src="images/2/Picture100-3.5.png" />

6. 이 계정에서 사용할 수있는 다양한 클라우드 서비스가 표시된 대시 보드가 표시됩니다. 

    <img src="images/2/Picture100-4.png" />

7. 모든**스토리지**클라우드 서비스가 보이지 않으면**대시 보드 사용자 정의**에서**를 클릭하고**보기를 클릭하여 대시 보드에 서비스를 추가 할 수 있습니다**이 워크샵의 경우**응용 프로그램 컨테이너, 개발자 및 저장소**클라우드 서비스를 최소한 표시하고 싶습니다. 특정 서비스를 보지 않으려면**숨기기**를 클릭하십시오. 

    <img src="images/2/Picture100-5.png" />

### 저장소 복제 정책 확인 / 설정

클라우드 계정의 상태에 따라 이전에 복제 정책을 설정하지 않은 경우 복제 정책을 설정해야 할 수 있습니다. 이 단계에서는 Storage Cloud Service를 통해 복제 정책의 상태를 확인합니다. 

1. **스토리지**클라우드 서비스를 클릭하십시오. 
    <img src="images/2/Picture-01.png" />

2. 화면 상단의**서비스 콘솔 열기**아이콘을 클릭하십시오. 

    <img src="images/2/Picture-01.5.png" />

3. 다음 대화 상자가 표시되면 복제 정책을 변경할 때 변경할 수 없으므로 복제 정책을 설정할 때주의해야합니다. 기본값을 가져 와서**정책 설정**버튼을 클릭하십시오. 메시지가 표시되지 않으면 복제 정책이 이미 설정되고 클라우드 계정이 Workshop에 대한 준비가되었습니다. 

    <img src="images/2/Picture-02.5.png" />

4. 이제 복제 정책이 설정되고 브라우저 창을 닫을 수 있습니다. 



### 내 서비스 포털을 통해 서비스 인스턴스에 대해 선택된 복제 정책 확인

Oracle 용으로 선택된 복제 정책을 찾으려면 
스토리지 클라우드 서비스 인스턴스에서**스토리지**링크를 클릭하십시오. 
**대시 보드**페이지. 결과 페이지에서**서비스 세부 정보를 확장합니다. 
Oracle Storage Cloud Service,**Oracle Storage Cloud의 세부 정보 
서비스 인스턴스가 표시됩니다. 복제 정책 필드를 찾으십시오. 
다음 스크린 샷에 강조 표시되어 있습니다. 

<img src="images/2/image30.png" width="348" height="116" />

## 개발자 클라우드 서비스 활성화 및 새 프로젝트 만들기

이 액티비티에서는 개발자 클라우드 서비스를 활성화하고, 
DevCS에서 새 프로젝트를 만들고, DevCS에서 GIT 저장소를 만들고, 복제합니다. 
DevCS GIT 저장소가있는 로컬 빌드 프로젝트 및 빌드 작성 
배치를위한 직업. 

다음 지시 사항을 사용하여 DevCS를 활성화하고 새로운 
계획. 

1. 귀하의 계정에 지정된 서비스가에 표시됩니다. 
대시 보드.**개발자**서비스가 보이지 않으면를 클릭하십시오. 
**대시 보드 사용자 정의**버튼 및**표시 버튼**
**응용 프로그램 컨테이너**는 대시 보드에 표시합니다. 

    <img src="images/2/image31.png" width="378" height="237" />

2. 대시 보드에서**개발자 클라우드 서비스**를 클릭하여 
**ServiceDetails : developer85599 (Oracle Developer 
클라우드 서비스)**페이지. 

    <img src="images/2/image32.png" width="454" height="134" />

3. **서비스 콘솔 열기**버튼을 클릭하십시오. 

    <img src="images/2/image33.png" width="399" height="195" />

4. **새 프로젝트**를 클릭하십시오. 

    <img src="images/2/image34.png" width="399" height="245" />

5. 다음과 같이 프로젝트 이름과 설명을 입력하십시오 
스크린 샷을 클릭하고**다음**을 클릭하십시오. 

    <img src="images/2/image35.png" width="399" height="288" />

6. **빈 프로젝트**템플릿을 클릭하고**다음을 클릭하십시오.**

    <img src="images/2/image36.png" width="378" height="271" />

7. Wiki Markup 드롭 다운 목록에서**MARKDOWN**을 선택하고 
**끝**. 

    <img src="images/2/image37.png" width="384" height="277" />

8. 프로비저닝 HelloworldProject는 몇 분이 걸릴 수 있습니다. 기다릴 때까지 
모든 모듈이 프로비저닝되고 
HelloworldProject 홈 화면. 

    <img src="images/2/image38.png" width="388" height="141" />

## 개발자 클라우드 서비스에서 GIT 저장소 만들기

다음 지시 사항에 따라 개발자에게 GIT 저장소를 만드십시오. 
클라우드 서비스. 

1. **REPOSITORIES**섹션에서**New Repository**버튼을 클릭하십시오. 

    <img src="images/2/image39.png" width="360" height="130" />

2. 새 저장소 창에서 저장소 이름을 입력하고 
설명을 클릭하고**만들기**를 클릭하십시오. 

    <img src="images/2/image40.png" width="351" height="282" />

3. 저장소를 만드는 데 몇 분이 걸릴 수 있습니다. 때까지 기다리십시오. 
HelloworldProjectRepo 저장소가 생성되고 
HelloworldProjectRepo 홈페이지. 

    <img src="images/2/image41.png" width="384" height="103" />

4. HelloworldProjectRepo 홈 페이지에서 HTTP 탭을 클릭하고 복사하십시오. 
URL. 

    <img src="images/2/image42.png" width="384" height="106" />

## GIT 저장소 복제

다음 지침에 따라 Helloworld-Example 프로젝트를 복제하십시오 
개발자 클라우드 서비스의 GIT 저장소로 이동합니다. 

1. GIT 저장소를 복제하려면 먼저 cloud / helloworld로 변경하십시오 
디렉토리는 저장소의 루트 디렉토리입니다. 

2. `git clone`을 실행하십시오. https : // ora1 @ developer.em2.oraclecloud.com / developer85599-ouopc084 / s / developer85599-ouopc084_helloworldproject_3753 / scm / HelloworldProjectRepo.git` 

    <img src="images/2/image43.png" width="427" height="111" />

**노트:** 
- 메시지가 나타나면 클라우드 계정 사용자 이름과 암호를 입력하십시오. 
- 사용자 이름과 암호를 입력하라는 메시지가 표시되지 않고 
명령이 403 오류와 함께 실패하면 명시 적으로 암호를 언급합니다. 
GIT 저장소 URL 예를 들면 :`git clonehttps : // ora1 : e1Car030@developer.em2.oraclecloud.com/developer85599-ouopc084/s/developer85599-ouopc084 \ _helloworlsprojectrepo \ _4070 / scm / HelloworldProjectRepo.git` 
-이 명령의 출력은 다음 명령의 출력과 유사해야합니다. 
위의 스크린 샷. 

3. **HelloworldProjectRepo**라는 새 디렉토리가 있습니다. 
**cloud / helloworld**디렉토리에 생성됩니다. 

4. Helloworld-Example**프로젝트 디렉토리를 복사하여 붙여 넣기하십시오. 
**구름 / helloworld**디렉토리**HelloworldProjectRepo**
예배 규칙서 

**참고 :** **HelloworldProjectRepo**디렉토리의 내용은 
아래 스크린 샷의 내용과 일치해야합니다. 

<img src="images/2/image44.png" width="441" height="89" />

5. **HelloworldProjectRepo**디렉토리로 변경하십시오. 

cd HelloworldProjectRepo 

6. 프로젝트 루트 디렉토리에서 GIT에 소스 파일을 추가하십시오 

자식 추가. 

7. 변경 사항 적용 

git commit -m &quot;HelloworldProjectRepo 저장소에 커밋 변경&quot; 

8. 개발자 클라우드 서비스의 저장소로 파일을 푸시합니다. 

git push origin master 

9. 개발자 클라우드 서비스로 전환하여 개발자 클라우드 서비스로 푸시 된 파일을 확인합니다. 
저장소 

10. **HelloworldProject**홈 페이지에서**HelloworldProjectRepo.git**를 클릭하십시오. 

    <img src="images/2/image45.png" width="378" height="150" />

11. **Helloworld-Example**프로젝트 디렉토리가 푸시되었습니다. 
개발자 클라우드 서비스의 저장소에 저장합니다. 그것을 클릭하고 확인하십시오. 
그것의 내용. 

    <img src="images/2/image46.png" width="385" height="153" />

    <img src="images/2/image47.png" width="385" height="158" />

## 개발자 클라우드 서비스에 대한 프로젝트 빌드

다음 지침에 따라 Helloworld-Example 프로젝트를 작성하십시오. 
개발자 클라우드 서비스. 

1. 왼쪽 탐색 창에서**빌드**를 클릭 한 다음**새 작업**을 클릭하십시오. 

    <img src="images/2/image48.png" width="457" height="201" />

2. 새 작업 창에서**HelloworldProjectBJ**작업 이름을 입력하십시오. 
필드를 클릭하고**저장**을 클릭하십시오. 

    <img src="images/2/image49.png" width="457" height="167" />

3. **주**탭에서 다음 값을 입력하십시오. 

- 조정이 필요한 경우 작업 이름을 편집하십시오. 
- 설명을 입력하십시오. 
-**JDK**를**JDK 8로 설정하십시오.**

    <img src="images/2/image50.png" width="433" height="204" />

4. **소스 제어**탭을 클릭하십시오. 

- **Git**를 저장소로 선택하십시오. 
- **URL**의 경우 Git 저장소의 URL을 선택하십시오. 

<img src="images/2/image51.png" width="433" height="211" />

5. **빌드 단계**탭을 클릭하십시오. 

- 빌드 단계 추가를 클릭하고 Maven 3 호출을 선택하십시오. 
-**목표**를 클린 패키지로 설정하십시오. 
-**POM 파일**위치를 Helloworld-Example / pom.xml로 설정하십시오. 

    <img src="images/2/image52.png" width="441" height="189" />

    <img src="images/2/image53.png" width="441" height="235" />

6. **Post Build**탭을 클릭하십시오. 

- 아티팩트 아카이브를 선택하십시오. 
-**보관할 파일**을 다음으로 설정 : Helloworld-Example / target / Helloworld-Example-1.0-SNAPSHOT.jar 
- Compression Type을 NONE으로 설정하십시오. 

    <img src="images/2/image54.png" width="443" height="184" />

7. **저장**을 클릭 한 다음**지금 빌드를 클릭하십시오.**

빌드가 성공적으로 완료되면 파일이 표시됩니다. 
Helloworld-Example / target / Helloworld-Example-1.0-SNAPSHOT.jar in 
**마지막 성공적인 건축물의**인공물. 다운로드 할 수 있습니다. 
파일 이름을 클릭하면됩니다. 

빌드가 실패한 경우 다시 빌드 작업 구성을 확인하십시오. 
또는**Git Logs**를 클릭하여 오류에 대한 추가 정보를 확인하십시오. 

<img src="images/2/image55.png" width="453" height="183" />

이를 통해 로컬 GIT 생성을 성공적으로 마쳤습니다. 
저장소, Maven 프로젝트 생성하기, Maven 프로젝트를 로컬에 저장하기 
GIT 저장소, DevCS 활성화, 프로젝트 및 GIT 작성 
DevCS의 저장소, 프로젝트를 DevCS에 복제 한 다음 
배포 작업을 구축하십시오. 
