# 개발 가이드
* 작성자 : vaiv
* 작성일 : 2021-03-xx

## * 공통
#### 개발 원칙 및 철학
* [SOLID(SRP, OCP, LSP, ISP, DIP)](https://ko.wikipedia.org/wiki/SOLID_(%EA%B0%9D%EC%B2%B4_%EC%A7%80%ED%96%A5_%EC%84%A4%EA%B3%84))
* [DRY(Don't repeat yourself)](https://ko.wikipedia.org/wiki/%EC%A4%91%EB%B3%B5%EB%B0%B0%EC%A0%9C)
* [KISS(Keep it small and simple)](https://ko.wikipedia.org/wiki/KISS_%EC%9B%90%EC%B9%99)
* [SoC(Separation of Concerns)](https://ko.wikipedia.org/wiki/%EA%B4%80%EC%8B%AC%EC%82%AC_%EB%B6%84%EB%A6%AC)
* [POLA(Principle Of Least Astonishment)](https://ko.wikipedia.org/wiki/%EB%86%80%EB%9E%8C_%EC%B5%9C%EC%86%8C%ED%99%94_%EC%9B%90%EC%B9%99)
* [YAGNI(You Aren't Gonna Need It)](https://ko.wikipedia.org/wiki/YAGNI)
* [방어적 프로그래밍](https://ko.wikipedia.org/wiki/%EB%B0%A9%EC%96%B4%EC%A0%81_%ED%94%84%EB%A1%9C%EA%B7%B8%EB%9E%98%EB%B0%8D)
* [java 코딩 규칙](https://myeonguni.tistory.com/1596)
* [javascript 코딩 규칙](https://www.crockford.com/code.html)


#### 로직 구현 공통
* 부정 조건문 지양
* 전역 변수 지양
* 메소드(함수)의 인자는 3개 이하가 적당함
* 타입-검사 피하기
    * 타입 검사하는것 자체가 어떤 타입의 변수가 사용되는지 모른다의 의미


#### 공통 환경
* 들여쓰기(indent)
    * 공백(space) 사용
    * 탭(tab) 사용하지 않음
* 공백
    * 4칸
* 인코딩
    * UTF-8

#### 사용 기술
###### 공통
* 통합개발환경(IDE) 택1
    * [Eclipse 2020-09+](https://www.eclipse.org)
    * [IntelliJ IDEA](https://www.jetbrains.com/idea/)
    * [Visual Studio Code 1.54+](https://code.visualstudio.com/)
* 형상(소스)관리
    * Git, [GitHub](https://github.com/)
    * [sourceTree](https://www.sourcetreeapp.com/)
* 빌드
    * [Gradle 6.5](https://gradle.org/)
* 데이터베이스
    * [PostgreSQL 1*5](https://www.postgresql.org/)
* ER(Entity Relationship) 모델링 택1
    * [ERWin](https://erwin.com/products/erwin-data-modeler)
    * [DA#](https://www.en-core.com/solution/solution2)
* 기타
    * [Docker 20.10](https://www.docker.com/)
    * [geoserver *16](http://geoserver.org)
    * [RabbitMQ](https://www.rabbitmq.com/)
    4. [QGIS 3.16](https://www.qgis.org)

###### BACK END
* 언어
    * [java 11+](http://openjdk.java.net/)
* 프레임워크
    * [string boot *0+](https://spring.io/projects/spring-boot)
* SQL mapper
    * [mybatis](https://blog.mybatis.org/)
* ORM(Object Relational Mapping)
    * [JPA](https://spring.io/projects/spring-data-jpa)
* 기타
    * [Lombok](https://projectlombok.org/)

###### FRONT END
* html
* css
* javascript
    * [vanilla javascript](http://vanilla-js.com/)
    * [jquery](https://jquery.com/)
    * [Handlebar](https://handlebarsjs.com/)
    4. ajax
    5. json
* 맵(map) 엔진
    * [CesiumJS](https://cesium.com/)
    * [Mago3D](https://github.com/Gaia3D/mago3djs)
* 템플릿 엔진
    * [thymeleaf](https://www.thymeleaf.org/)
* 기타
    * [bootstrap](https://getbootstrap.com/)


## * BACK END 개발 방법
#### 프로젝트 구조
```
src/main
        /java
                /프로젝트구분
                    /cmmn
                        /config
                        /interceptor
                        /utils
                        ...
                    /업무
                        /controller
                            /rest
                            /view
                        /service
                            /impl
                        /persistence
                    ...
        /resources
                /messages
                /mybatis
                    /디비명
                        /업무
                            /파일.xml
                        ...
                /statis
                    /css
                    /images
                    /js
                /templates
                    /업무
                        /파일.html
                    ...
```
#### java
* 공통
    * spring boot를 이용하여 구현
    * java config 이용 지향(환경 설정을 위한 xml 사용 지양)
    * 공통 라이브리러 사용
    (참조) https://github.com/HyunSeongKil/performance-platform/tree/master/pp-core
* 패키지 
    * 패키지명은 소문자만 사용
        ```
        ex) kr.vaiv.lhdt
        ```    
* 파일명명
    * 업무명 + RestController.java (rest api 서비스의 경우)
        ```
        ex) UserRestController.java
        ```
    * 업무명 + Controller.java (view 서비스의 경우)
        ```
        ex) UserController.java
        ```
    * 업무명 + Service.java
        ```
        ex) UserService.java
        ```
    4. 업무명 + ServiceImpl.java
        ```
        ex) UserServiceImpl.java
        ```
    5. 업무명 + Repository.java (JPA의 경우)
        ```
        ex) UserRepository.java
        ```
    6. 업무명 + Mapper.java (mybatis의 경우)
        ```
        ex) UserMapper.java
        ```
* 메소드
    * 등록 add + 구분명
        ```
        ex) addUser()
        ```
    * 수정 update + 구분명
        ```
        ex) updateUser()
        ```
    * 삭제 delete + 구분명
        ```
        ex) deleteUser()
        ```
    4. 조회 get + 구분명
        ```
        ex) getUser()
        ```
    5. 목록 list + 구분명
        ```
        ex) listUser()
        ```
* 메소드 상세
    * RestController
        리턴 타입   ResponseEntity<Map>
        ```
        ex)
        public ResponseEntity<Map> getUser(){
            ...
            return new ResponseEntity<Map>(map, HttpStatus.OK);
        }
        ```
    * Controller
        리턴 타입   String
        ```
        ex)
        public String getUser(){
            ...
            return "/user/userView";
        }
        ```
    * 메소드의 파라미터 갯수
        3개 이하 추천
        ```
        ex) addUser(userId, userName, tel)
        ```
        3개 초과하는 경우 Model 객체에 담아서 전달
        ```
        ex) addUser(UserModel)
        ```
* 주석
    * 가능하면 주석이 없어도 로직을 이해할 수 있도록 구현
    * 주석이 필요한 경우 java 코딩 규칙에 맞게 작성
* 변수
    * 의미있는 변수명 사용
        ```
        ex)
        (좋음) String userId;
        (나쁨) String a;
        ```
    * 단, 반복문에는 i,j,k,...사용 가능
        ```ex)
        for(int i=0; i<10; i++){ ... }
        ```
* 기타
    * Lombok 이용
    * Model 클래스는 Lombok을 이용하여 @Getter, @Setter, @Builder등 사용

#### sql
※ mybatis를 사용하는 경우에만 해당
* 파일명명
    * 업무 + _mapper.xml
        ```
        ex) user_mapper.xml person_mapper.xml ...
        ```
* sql 문(statement)
    * 콤마를 문장의 맨앞에 사용
        ```
        ex) select aaa
                ,bbb
            from table
        ```
    * n개 컬럼 사용시 한줄에 하나의 컬럼 사용
        ```
        ex) update table set
                aaa = #{aaa}
                ,bbb = #{bbb}
        ```
* sql id
    * 낙타(Camel)법 사용
    * 입력    insert + 업무
        ```
        ex) <insert id="insertUser" ...></insert>
        ```
    * 수정    update + 업무
        ```
        ex) <update id="updateUser" ...></update>
        ```
    * 삭제    delete + 업무
        ```
        ex) <delete id="deleteUser" ...></delete>
        ```
    * 조회    select + 업무
        ```
        ex) <select id="selectUser" ...></select>
        ```
    * 목록    select + 업무 + List  
        ```
        ex) <select id="selectUserList" ...></select>
        ```

## * FRONT END 개발 방법
#### javascript
* 공통
    * html과 js파일 분리
        ```
        ex)
        user.html
        user.js
        ```
    * OOP(Object Oriented Programming) 지향
    * TODO callback vs promise
    * TODO ES6+
    * 공통 js파일 사용
        * 공통 [pp-0.9-es6.js](https://github.com/HyunSeongKil/performance-platform/blob/master/pp-js/src/js/pp-2021.03-es6.js) or [pp-0.9-legacy.js](https://github.com/HyunSeongKil/performance-platform/blob/master/pp-js/dist/js/pp-2021.03-legacy.js)
        
* 변수 선언
    * var 사용 지양
        ```
        ex) 
        (좋음) const name = ''; or let name = '';
        (나쁨) var name = '';
        ```
    * 전역 변수 지양
* 파일 명명
    * 업무 + .js
        ```
        ex) user.js person.js ...
        ```
* 함수 명명
    * 함수명만으로도 동작을 유추할 수 있도록 의미있는 명칭 사용
    * 동사 + 기능
        ```
        ex) addUser(), viewUser(), renderHtml(), getData() ...
        ```
* 변수 명명
    * 의미있는 변수명 사용
        ```
        ex)
        (좋음) userId, userName, ...
        (나쁨) a, b, ...
        ```
    * 단, 반복문의 변수는 i, j, k,...사용 가능
        ```
        ex) for(let i=0; i<10; i++) { ... } 
        ```
* 주석
    * 가능하면 주석이 없어도 로직이 이해되는 코드 작성
    * 주석이 필요한 경우 함수, 파라미터, 리턴값의 주석 작성
        ```
        ex)
        /**
        * 사용자 정보 조회
        * @param {string} userId 사용자 아이디
        * @returns {User} 사용자 정보
        */
        function getUser(userId){
            ...(중략)
        }
        ```
* 기타        
    * 값 비교시 === 사용 지향 ( == 사용 지양)
        ```
        ex) 
        (좋음) userNum === 1
        (나쁨) userNum == 1
        ```
        (참조)    https://developer.mozilla.org/ko/docs/conflicting/Web/JavaScript/Reference/Operators_310dc67549939233c3d18a8fa2cdbb23
#### html
* 공통
    * MPA(Multi Page Application) vs SPA(Single Page Application)
    * CSR(Client Side Rendering) vs SSR(Server Side Rendering)
* 파일명명
    * 업무 + .html
        ```
        ex)user.html
        ```
* 템플릿 엔진
    * thymeleaf 사용

* js 선언
    * defer 속성 사용
    * 백그라운드에서 js를 다운로드 함 (dom파싱이 멈추지 않음)
    * dom 파싱 완료 후 js 실행됨
    ```
        <script type="text/javascript" src="..." defer ></script>
    ```
    * cf. async 속성
        * 백그라운드에서 js를 다운로드 함(dom파싱이 멈추지 않음)
        * 그러나, 다운로드가 완료되면 dom 파싱과 무관하게 스크립트 실행됨(dom 파싱전에 dom에 접근하려는 로직 존재시 스크립트 오류 발생)

#### css
* 클래스 명명
    * 구분자로 하이픈(-) 사용
        ```
        ex) <button type="button" class="add-user-button">추가</button>
        ```

## 4. 기타
### 유용한 Visual Studio Code Extension
* Auto Close Tag
* Auto Rename Tag
* Debugger for Java
* Java Extension Pack
* Language Support for Java
* Project Manager for Java
* Lombok Annotation Support for VS code
* Spring Boot Dashboard
* Spring Boot extension
* Spring Boot Tools
* Spring Initializr Java Support
* ESLint
* Javascript Debugger
* GitLens
* Gradle Tasks
* Prettier
* Rainbow Brackets
* Visual Studio IntelliCode 

### 유용한 Eclipse Plug-in
TODO

### 유용한 IntelliJ IDEA Plug-in
TODO
