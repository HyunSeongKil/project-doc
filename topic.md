# 토픽

## 공간정보

### 지구의 형상
* ![그림](https://mblogthumb-phinf.pstatic.net/20150727_245/kcscpr_1437962883446JUsza_PNG/1_%281%29.png?type=w2)


### 지오이드(Geoid)
* 측지학에서 정립한 각종 작업의 기준이 되는 새로운 지구의 수학적 모델
* 평균해수면을 육지까지 연장하여 지구 전체를 둘러쌌다고 가정한 곡면
* 지구를 물로 덮었다고 가정했을 때의 지구의 형태를 나타내고 있는 측지학, 지구물리학의 용어
* 항상 중력 중심에 수직(등포텔션면)
* 높이는 항상 0m (해발고도는 평균해수면을 기준으로 하기 때문)
* 물리적 지표면보다 단순하고, 준거타원체보다 더 실제 지구에 가까움
* 지오이드고
    * 지오이드와 지구타원쳬 사이의 높이 차
* ![그림](http://www.biz-gis.com/files/attach/images/5130/754/065/ac14475f22500f4e1d843edb62d1e881.jpg)


### 지구 타원체(Earth Ellipsoid)
* 지구를 근사하는 수학적 모델
* 측지학과 천문학, 지구과학에 쓰이는 기준틀


### 준거 타원체(Reference Ellipsoid)
* 지구의 일정 지역의 측지측량의 기준이 되는 타원체
* 측량기술, 측지 대상지역의 범위, 정치, 군사적인 문제등에 따라 달리 정의될 수 있음
* 특정지역 또는 국가마다 채택한 준거타원체가 다르기 때문에 국제 표준 타원체와 다를 수 있음
* 우리나라는 베셀(Bessel) 타원체를 사용
* ![그림](https://t1.daumcdn.net/cfile/tistory/230ECB4A5689DDBA29)
* ![준거타원체 종류](https://t1.daumcdn.net/cfile/tistory/22398A4A5689DDBD07)


### 좌표계(Coordinate Reference System, CRS)
* 둥근 지구를 2차원 평면에 투영(projection)하는 다양한 방법
* 지리 좌표계(Geographic Coordinate System, GCS)
    * 지구상에 위치를 정의하는데 3차원의 구면을 이용하는 좌표계
    * 지리 좌표계에서 한 지점은 경도(longitude)와 위도(latitude)값으로 지정됨
* 투영 좌표계(Projected Coordinate System, PCS)
    * 지리좌표를 평면상에 투영한 좌표계



### WGS84(World Geodetic System 1984)
* 미국이 군사 및 GPS 운용을 목적으로 구축한 지구 타원체
* GPS의 기준이 됨
* 국제표준타원체

### GRS80(Geodetic Reference System 1980)
* 국제측지학협회(IAG)와 국제측지학 및 지구물리학연합(IUGG)에서 채택한 지구 타원체
* 국제표준타원체





### EPSG(European Petroleum Survey Group, 유럽석유조사그룹)
* EPSG 코드에 대한 상세 정의는 prj4와 wkt라는 문자열로 정의
* EPSG:4326 - WGS84 타원체의 경위도 좌표계
* EPSG:3857 - GOOGLE, VWORLD의 좌표계
* EPSG:5174 - 경도 10.405초 보정된 Bessel 타원체의 TM 중부원점
* EPSG:5179 - GRS80 타원체의 UTM-K 좌표계


### TM(Transverse Meractor, 횡단원통등각투영법) 좌표계
* 평면 직각 좌표계의 하나
* 측량 범위가 넓지 않은 지역의 측량을 위해 주로 사용

### UTM(Universal Transverse Meractor, 국제 횡축 메르카토르) 좌표계
* 지구를 경도 6º간격으로 세로 띄로 나누어 횡측 메르카토르 도법으로 그린 뒤, 위도8º 간격으로 총 60x20개의 격자로 나누어 각 세로 구역마다 설정된 원점에 대한 종.횡 좌표로 위치를 표시
* ![사진](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Ft1.daumcdn.net%2Fcfile%2Fblog%2F1374DC445140DC9F1B)



### DEM(Digital Elevation Model)
* 수치 표고 모델
* 지형의 고도값을 수치로 저장함으로써 지형의 형상을 나타내는 지도
* [위키피디아](https://en.wikipedia.org/wiki/Digital_elevation_model)
* Ground
    * the solid surface of the earch
    * a solid base or foundation
    * a surface of the earch
    * bottom of the sea
* Height
    * measurement from base to top
    * elevation above the ground or recognized level
    * especially that of the sea
    * distance upwards
* Elevation
    * height above a given level
    * especially that of sea
    * height above the horizon
* Terrain
    * tract of country considered with regarded to its natural features, etc
    * an extent of ground, region, territory
* ![DEM,DTM,DSM](https://mblogthumb-phinf.pstatic.net/20150914_184/rsmilee_1442204373263asXhu_JPEG/smilee_DEM%252C_DSM%252C_DTM%252C_%25EC%2588%2598%25EC%25B9%2598%25ED%2591%259C%25EA%25B3%25A0%25EB%25AA%25A8%25EB%258D%25B8%252C%25EC%25B0%25A8%25EC%259D%25B4%252C%25EC%2584%25A4%25EB%25AA%2585.jpg?type=w800)

### DTM(Digital Terrian Model)

### DSM(Digital Surface Model)

### OSM(Open Street Map)
* 오픈소스 방식의 참여형 무료 지도 서비스
* https://www.openstreetmap.org
* [위키피디아](https://ko.wikipedia.org/wiki/%EC%98%A4%ED%94%88%EC%8A%A4%ED%8A%B8%EB%A6%AC%ED%8A%B8%EB%A7%B5)

### Point Cloud
* Lidar센서, RGB-D센서 등으로 수집되는 데이터
* 3차원 공간상에 퍼져 있는 여러 포인트의 집합
* [위키피디아](https://ko.wikipedia.org/wiki/%EC%A0%90%EA%B5%AC%EB%A6%84)

### PCL(Point Cloud Library)
* 포인트 클라우드 및 3차원 지오메트리 처리를 위한 오픈소스 라이브러리
* [위키피디아](https://en.wikipedia.org/wiki/Point_Cloud_Library)

### Trimble
### 3차원 레이저 스케너
### 건축한계선
* 도로의 개방감 확보를 위해 건축물을 도로에서 일정거리 후퇴시켜 그 선의 수직면을 넘어서 건축물 및 부대시설의 지상 부분이 돌출하여서는 안되는 선
### 건축지정선
* 건축물의 전층 또는 저층부의 외벽면이 일정 비율이상 접해야 하는 선

### degree
* 각도를 나타내는 단위
* 원 한바퀴를 360도로 표현하는 방법
* 반원은 180도, 직각은 90도

### radian
* 각도를 나타내는 단위
* 1라디안은 원주 호의 길이가 반지름과 같은 길이가 될 때의 각도
* 수학에서 사용하기에 편리한 단위
* 삼각함수에서 사용하기 편함
* 1라디안 = 57.2958...도
* 1파이(3.141592...) 라디안 = 180도
* 2파이(3.141592...) 라디안 = 360도
* ![radian](https://t1.daumcdn.net/cfile/tistory/23455B33510626C325)

### 본초 자오선(prime meridian)
* 영국 그리니치의 그리니치 천문대를 지나는 자오선으로, 경도의 기준이 됨
* 자오선이란 12간지중 자(밤12시)와 오(낮12시)에 해당
* 결과적으로, 본초자오선이란 '밤12시와 낮12시가 근본적으로 시작되는 선'이란 의미
* 그리니치 천문대는 낮12시(오선)을 구분짓는 경계
* [위키피디아](https://ko.wikipedia.org/wiki/%EB%B3%B8%EC%B4%88_%EC%9E%90%EC%98%A4%EC%84%A0)
* ![본초자오선](https://t1.daumcdn.net/cfile/blog/997BAC375BAF754B32?original)

### 경도(경선, 날줄, longitude)
* 지구상에서 본초 자오선을 기준으로 동쪽 또는 서쪽으로 얼마나 떨어져 있는지 나타내는 위치
* 단위 : 도(º)
* 범위 : 180ºE(동경 180도) ~ 180ºW(서경 180도)
* 한반도는 동경124 ~ 동경132
* [위키피디아](https://ko.wikipedia.org/wiki/%EA%B2%BD%EB%8F%84)
* ![경도](https://lh3.googleusercontent.com/proxy/iHaZLOHPe8ybyJRVznOXTTVS4_SffYd3gg-BgTQHa7MBmYNtOsEthQklaabQ3QwfU8vcQNNW2intjdX4lB48KoToSsVtH0-z5ZjVmdtVEVL7kp9HIswthjd1x_SRABKj7nVLM4smhTIC8AdErlzskuP5LPGhaNUPmrY-nx1bXcCZ5x2ZLhE_L7hVmFuEfb_TQCYCEVGLcMaCygVEp6CmLNqXamsayMdVX2zKF1rtC7OWGpDLhhI0Z8MyKAdpmpWJtQYk8SH9IZ-kWYQipuGG_alnym_GqnjYKa3R69UTE05_djq8vdxM9BV60wfrZtR_J82CoV6Kfliw7unOZ6KIp6RV)

### 위도(위선, 씨줄, latitude)
* 지구상에서 적도를 기준으로 북쪽 또는 남쪽으로 얼마나 떨어져 있는지 나타내는 위치
* 단위 : 도(º)
* 범위 : 적도(0º) ~ 북극점(90ºN), 적도(0º) ~ 남극점(90ºS)
* 한반도 : 32º ~ 43º
* [위키피디아](https://ko.wikipedia.org/wiki/%EC%9C%84%EB%8F%84)
* ![위도](https://t1.daumcdn.net/cfile/tistory/2756813C5865C7D116)


### GNSS(Global Navigation Satellite System, (범지구) 위성 항법 시스템)
* 인공위성을 이용해 위치를 결정할 수 있게 하는 체계
* GPS : 미국의 글로벌 포지션 시스템
* GLONASS : 러시아의 글로벌 궤도 항법 위성 시스템
* BeiDou-2 : 중국이 개발한 시스템
* Galileo : 유럽 연합(EU)에 의해 개발된 시스템
* QZSS(Quasi-Zenith Satellite System) : 일본
* NAVIC(Navigation Indian Constellation) : 인도
* ![그림](https://www.oxts.com/wp-content/uploads/2017/11/DifferentGNSS.jpg)


## IT
### API Gateway
* MSA에서 언급되는 컴포넌트중 하나이며, 모든 client 요청에 대한 end point를 통합하는 서버
* client interface를 backend 구현 환경에서 분리할 수 있는 방법
* 인증, 라우팅,  속도제한, 과금, 모니터링, 분석, 정책, 알림, 보안, 캐싱, 공통로직, 프로토콜 변환
* [참고](https://www.redhat.com/ko/topics/api/what-does-an-api-gateway-do)

### 서버리스(Serverless)
* [참고](https://tecadmin.net/delete-commit-history-in-github/)

### git의 특정 history 삭제하기
* [참고](https://rtyley.github.io/bfg-repo-cleaner/)

### SPA(Single Page Application)
* 기본적으로 단일 페이지로 구성
* 처음 접근시 필요한 모든 정적 리소스 다운로드, 이후 새로운 페이지 요청 시, 필요한 데이터만 서버에 요청
* 장점 
    * 간단한 배포
    * 적은 트래픽량
    * 반응성 향상(네이티브 앱과 유사한 사용자 경험 제공)
* 단점
    * 느린 초기 구동 속도
    * SEO(검색엔진 최적화) 문제
* [위키피디아](https://ko.wikipedia.org/wiki/%EC%8B%B1%EA%B8%80_%ED%8E%98%EC%9D%B4%EC%A7%80_%EC%95%A0%ED%94%8C%EB%A6%AC%EC%BC%80%EC%9D%B4%EC%85%98)

### CSR(Client Side Rendering)
* Angular vs React vs Vue

### SSR(Server Side Rendering)
* 

### WebAssembly
* 이진 명령어 포맷


### Throughput(처리량)
* 지정된 시간내에 처리된 정보량/처리량
* 이상적인 값은 band-width이나 이런저런 이유로 실제 처리되는 값은 throughput임
* ![그림](![image](https://user-images.githubusercontent.com/38479834/110746907-e4253300-8280-11eb-9234-ca47debdf174.png)


### Latency(지연시간)
* 각 처리의 시작~종료의 처리 시간
* throughput과 latency는 반비례함
* ![그림](![image](https://user-images.githubusercontent.com/38479834/110747406-ab398e00-8281-11eb-9f85-61a4722077b1.png)


### band-width
* 이상적인 처리량

### 미디어 쿼리(Media Query)
* 사이트에 접속하는 장치에 따라 특정한 CSS 스타일을 사용하도록 도와주는 소프트웨어 모듈
* 반응형 웹 디자인의 핵심
* 웹사이트를 콘텐츠를 화면 크기에 맞게 조정하는 역할을 수행함
* @media 속성을 사용해 특정 미디어에서 어떤 CSS를 적용할 것인지 지정해줌
```
CSS파일 사용 예시
    @media screen and (min-width:200px) and (max-width:360px) { /* 스타일 정의 */ }
```
```
<link>사용 예시
    <link href="cssfile.css" media="screen and (min-width:200px) and (max-width:360px)" rel="stylesheet">
```
```
<style>사용 예시
<style type="text/css" media="screen and (min-width:200px) and (max-width:360px)">
    /* style */
</style>
```
```
<style>-@import 사용 예시
<style>
    @import url(cssfile.css) screen and (min-width:200px) and (max-width:360px)
</style>
```


### 오픈 그래프(Open Graph Protocol)
* html문서의 메타정보를 쉽게 표시하기 위해서 메타정보에 해당하는 다양한 요소들에 대해서 사람들이 통일해서 쓸 수 있도록 정의해 놓은 프로토콜
* 페이스북에 만듦
```
    <meta property="og:title" content="콘텐츠 제목">
    <meta property="og:url" content="웹페이지 url">
    <meta property="og:type" content="웹페이지 타입(blog,website,...)">
    <meta property="og:image" content="표시되는 이미지">
    <meta property="og:site_name" content="웹사이트 이름">
    <meta property="og:description" content="설명">
```