# Human Interface Guidelines 번역본
------------
### 순서
1. Overview
2. App Architecture
3. User Interaction
------------

### 1.Overview
#### themes
#### ios Design의 차별성
1. Clarity(명확함)
+ 텍스트,아이콘,장식들을 보기 좋게 만들다. 
+ 기능이 명확하게 드러나고 중요한 요소는 강조하자.

2. Deference(컨텐츠 존중): 좋은 화면 구성을 통해 사용자들이 컨탠츠들을 이해하기 쉽게 하기.
+ 전체화면 활용
+ 컨텐츠를 부각
+ 베젤, 그라데이션, 그림자등을 최소화 하여 화면이 밝고 가볍게 느끼게 한다.

3. Depth(깊이) 
+ 레이어와 모션을 통해 계층구조를 표현.
+ 특정한 동작에 의해 컨텐츠가 손실 방지.
+ 보고 있거나 이동하려는 화면의 깊이감을 느끼게 하기.

#### Design Principles(디자인 원칙)
+ Aesthstic Integrity(미적인 통일성)
+ Consistency(일관성)
+ Direct Manipulation(직접조작)
+ Feedback(피드백) - 그래픽,사운드 활용
+ Metaphors(비유) - 이해을 위한 친숙한 비유
+ User Control(사용자 통제) - 중요한 작업으 사용자가 직접 통제

#### Uikit
+ Bars(탭이나 내비게이션 등)
+ Views(화면 표현되는 표현
+ Controls(버튼, 스위치 등)

### 2. App Architecture

+ Accessibilty
  + Reduce transparency
  + VoiceOver
  + Button Shapes
+ Loading

  ![image](https://user-images.githubusercontent.com/80015108/147924369-10540d95-4ea1-427d-a250-55fb681c843a.png)
+ Modality

  ![image](https://user-images.githubusercontent.com/80015108/147924032-840c9281-7593-4dd2-b537-00f822287a2f.png)
+ Navigation

  ![image](https://user-images.githubusercontent.com/80015108/147924389-6037cf72-4753-4483-9599-44c704f861a5.png)
+ Onboarding
  + 실행 화면 제공
  + 앱의 방향을 일치
  + 빠르게 동작
  + 기다리는 동안 유용한 팁을 제공
  + 필수 튜토리얼을 삽입
  + 흥미를 유발
  + 처음에는 셋업을 위한 정보르 제공하지 않음
  + 라이센스 동의 등을 앱 안에 넣지 않는 것이 좋다.(앱 스토어에서 확인)
  + 앱을 다시 실행 했을때 예전 상태 저장
  + 사용자 리뷰를 너무 자주 요청 금지
  + 재부팅 강요 금지
+ Requesting Permission
  + 확실히 필요할 때만 요구
  + 왜 필요한지 명시
  + 처음 실행할때 요구
  + 불필요하게 정보 수집 금지
+ Settings
  + 어떤 것을 설정변경 할수있는지 언급
  + 우선순위를 정해서 배치
  + 설정들을 세팅앱을 통해 설정
  + Settings 앱으로 가는 단축 아이콘을 포함

### 3. User Interaction
+ 3D Touch
  + Home Screen Interaction
  + Peek and Pop
  + Live Photos
  + 미리보기 사용
