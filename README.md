# OCA 과제 Azure Extension

과제시 발생한 문제와 해결 방법을 제시한다.

## 문제 1 : 설치된 닷넷 패키지 버전이 맞지 않아 다시 설치를 해주어야 한다.
해결 되지 않으면 func start 시에 무한로딩이 걸려 페이지가 나오지 않는다.

### 해결 1 : 
dotnet add package Microsoft.Azure.Functions.Worker<br>
dotnet add package Microsoft.Azure.Functions.Worker.Sdk

## 문제 2 : 실습시 따라했던 패키지를 모두 깔면 안된다.
모두 깔면 빌드가 되지 않는다.

### 해결 2 : 
dotnet add package Microsoft.NET.Sdk.Functions 를 했다면<br>
dotnet remove package Microsoft.NET.Sdk.Functions로 패키지 삭제

## 문제 3 : local.settings.json이 없으면 프로젝트를 받은 사람이 실행하기 어렵다.
파일이 없으면 멘토가 프로젝트를 받아서 빌드 해볼 수 없다.

### 해결 3 : 
.gitignore 파일에 local.settings.json 앞에 #을 붙여서 주석처리 한다.

## 문제 4 : 터미널에서 한글이 깨지는 현상이 발생한다.
프로젝트에 지장을 주지 않지만 글씨가 깨진다.

### 해결 4 : 
검색 - 국가 또는 지역 변경 - 우측 "추가 날짜, 시간 및 국가별 설정" - 국가 또는 지역 - 관리자 옵션 - 시스템 로캘 변경 - Beta: 세계 언어 지원을 위해 Unicode UTF-8 사용 - 확인<br>
이후 재부팅 하면 글씨가 정상적으로 출력 된다.

## 문제 5 : VsCode 터미널에서 func init가 되지 않는다.
어떤 이유인지 터미널에서 init이 되지 않는 이슈가 있다.

### 해결 5 : 
프로젝트 폴더에 가서 경로를 쓸 수 있는 곳에 cmd.을 치면 해당 폴더의 명령 프롬프트 창을 열 수 있다.<br>
명령 프롬프트 창에서는 func init이 정상적으로 실행 된다.