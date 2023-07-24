# OCA 과제 Azure Extension

한 것들을 정리해서 올릴 수 있도록 한다.

### 문제 1 : 설치된 닷넷 패키지 버전이 맞지 않아 다시 설치를 해주어야 한다.

해결 되지 않으면 func start 시에 무한로딩이 걸려 페이지가 나오지 않는다.

## 해결 1 : 
dotnet add package Microsoft.Azure.Functions.Worker
dotnet add package Microsoft.Azure.Functions.Worker.Sdk

### 문제 2 : 실습시 따라했던 패키지를 모두 깔면 안된다.

모두 깔면 빌드가 되지 않는다.

## 해결 2 : 
dotnet add package Microsoft.NET.Sdk.Functions 를 했다면
dotnet remove package Microsoft.NET.Sdk.Functions로 패키지 삭제

### 문제 3 : local.settings.json이 없어서 받은 사람이 실행이 되지 않는다.

## 해결 3 : 
.gitignore 파일에 local.settings.json 앞에 #을 붙여서 주석처리 한다.