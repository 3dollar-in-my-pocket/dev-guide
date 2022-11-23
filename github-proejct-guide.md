# 깃허브 Projects 사용 가이드
Jira의 티켓 관리 시스템을 가져와 Proejcts에서 진행합니다.  
가슴속 3천원에서는 백엔드, Android, iOS 공동으로 Projects를 사용해 협업을 합니다.  

## 1. Projects
최상위 레벨의 단위를 의미하며 `피처`를 기준으로 나누었습니다.  
새로운 피처를 시작하면 Proejcts를 생성하고, 해당 피처가 릴리즈되면 프로젝트를 close합니다.

![image](https://user-images.githubusercontent.com/7058293/203571368-0895ccc0-0407-49aa-8d56-0bf7837551c3.png)


## 2. 새로운 피처를 시작하는 경우
1. 새로운 Proejcts를 생성합니다.   
    - Projects 이름은 기능 이름으로 설정합니다. ex.) 즐겨찾기 기능
    - Proejcts의 형태는 Board 형태로 생성합니다. (보는 방식의 차이라 테이블 뷰도 상관 없지만 칸반보드가 진행 상태를 확인 편하다고 생각합니다.)  
![image](https://user-images.githubusercontent.com/7058293/203572985-b6d8b738-5ac3-4b7e-8f48-bf6050f8521f.png)  


2. 플랫폼에 해당하는 레포의 Issues 탭에서 milestone을 생성합니다.
    - milestone은 이번에 업데이트 될 앱 버전의 개념으로 정의하고 작성합니다. ex.) v3.1.0
![image](https://user-images.githubusercontent.com/7058293/203573601-8bab4c9f-0a85-43e0-b5e0-d40688933311.png)  

3. Proejcts로 돌아와 해야할 일들을 Todo 버킷에 이슈 형태로 생성합니다.
    - 이슈의 이름은 **`[{Platform}]{티켓 내용}`** 형태로 생성해주세요! ex.) [iOS] 마이 페이지 > 즐겨찾기 리스트 화면 뷰 그리기
    - 3개의 플랫폼이 같이 사용하기 때문에 접두사에 플랫폼을 넣습니다.
    - 이슈의 내용의 크기는 작을 수록 좋습니다. (1티켓 -> 1PR)크기가 제일 이상적입니다.
    - iOS의 경우에는 하나의 화면에 대해서 4개의 티켓을 구성할 예정입니다. (View그리기, 서비스 구현, ViewModel 구현, 데이터 바인딩)
    - 피처에 대하여 티켓들을 모두 생성하고 `convert to issue`를 눌러서 이슈로 변경합니다. (이슈 변경시 플랫폼에 맞는 레포로 설정하여 변경합니다.)
![image](https://user-images.githubusercontent.com/7058293/203575232-3681fcf1-e5c4-4cb9-8eef-7df7f55679e7.png)  

4. 생성한 이슈들에 내용과 속성을 설정합니다.
    - 이슈에 대한 배경, 설명이 필요하다면 설명을 작성합니다. (제목으로도 설명이 가능한 상황이라면 설명을 적지 않아도 좋습니다.)
    - 담당자를 설정합니다.
    - Milestone에 2번에서 만든 milestone으로 설정해줍니다.
![image](https://user-images.githubusercontent.com/7058293/203576149-bbcf8a13-56f6-4271-bac2-40677a2f7af9.png)

5. 각 이슈를 하나씩 처리하며 상태에 맞게 이슈의 버킷을 옮겨줍니다. (진행중, 완료)
    - `Todo`: 아직 시작하지 않은 해야할 일의 상태
    - `In Progress`: 진행중인 상태
    - `In Code Review`: PR을 만들고 코드리뷰를 받고 있는 상태 (플랫폼 상황에 따라 해당 버킷을 사용하지 않아도 됩니다.)
    - `Done`: 코드리뷰까지 완료된 상황

## 3. 피처가 릴리즈된 경우
1. 플랫폼별 레포에서 milstone을 close 시켜주세요. (milestone에 해당하는 모든 이슈가 merged된 상태여야합니다.)
2. 모든 플랫폼이 릴리즈 된 경우, Projects를 close 시켜주세요.

## 4. 피처가 아닌 버그 수정의 경우
1. 기존에 만들어진 Proejcts에서 버그수정 Project를 사용해주세요.
2. 나머지 이슈 생성 및 처리는 [2. 새로운 피처를 시작하는 경우](https://github.com/3dollar-in-my-pocket/dev-guide/new/main#2-%EC%83%88%EB%A1%9C%EC%9A%B4-%ED%94%BC%EC%B2%98%EB%A5%BC-%EC%8B%9C%EC%9E%91%ED%95%98%EB%8A%94-%EA%B2%BD%EC%9A%B0)와 같은 방식으로 진행합니다.
3. 버그 수정의 경우 지속적으로 발생하기 때문에 해당 Proejcts는 close되지 않습니다.


