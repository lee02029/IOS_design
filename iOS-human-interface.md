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
  + 손가락으로 가리지 않도록 충분한 큰 미리보기 제공
  + 일부에만 적용하지 말고 통일되게 최대한 모든 곳에서 제공
  + 사용자에게 혼동을 주지 않도록 항목을 구성
  + 작업 버튼을 제공하는 것이 좋음
  + 미리보기 메뉴를 제공 금지 -> Deep press 등 일반적인 사용방식
+ Audio
  + Silence
  + Volume
  + Headphones
+ Designing a Great Audio Experience
  + 필요한 경우 자동으로 조절 가능/ 단,전체 볼륨은 조정 금지
  + 적절한 경우 오디오의 경로 변경을 허용
  + 시스템 제공 볼륨보기를 사용하여 오디오 조정 허용
  + 짧은 사운드와 진동에는 시스템의 사운드 서비스 사용
  + 사운드가 앱에 필수라면 오디오를 분류
  + 중단이 발생하면 오디오 재생을 다시 시작
  + 앱이 임시 오디오 재생을 마칠 때 다른 앱에 알림
  + 필요한 경우에만 오디오 컨트롤에 응답 
  + 오디오 컨트롤을 용도 변경 금지

 
  <img width="586" alt="스크린샷 2022-01-03 오후 8 37 53" src="https://user-images.githubusercontent.com/80015108/147926509-182231b4-5b3a-49be-9dd8-a260992e9644.png">
  
  
+ Authentication
  + 최대한 늦게 표시
  + 어떤 권한을 필요하는지 설명
  + 최소 입력으로 해결
  + Passcode 라는 용어 사용 금지
  + 가능하면 Biometiric Authentication를 지원

![image](https://user-images.githubusercontent.com/80015108/147926776-2542d065-4027-41b9-b47d-f8c1d7cdcfbc.png)

+ Drag and Drop
  + Drag 동작시 목적지가 될 수 있는 것과 아닌것을 구분해서 보여주자(Drag and Drop in UIKit)
  + 같은 Context에서 이동(예: 텍스트 내)과 다른 Context로의 이동(예: Reminder의 목록을 리스트간 이동)
  + 가능하다면 이동 중에 프리뷰를 볼 수 있도록 하자
  + 가능하다면 표현방식의 다양성을 
+ Feedback
  + 사용자가 확인할 수 있도록 유용한 피드백 제공(예: 업데이트 진행률, 완료 확인 등)
  + 불필요한 알림은 제공 금지
  + Haptic Feedback을 제공(Animation and Haptics)
+ File Handling
  + 파일을 주기적으로, 키고 끌때, 이동할 때 자동으로 저장
  + 디바이스에 파일을 저장 금지 -> 클라우드 환경에 저장
  + 관리화면을 효과적으로 표현(예:ibook)
  + App을 벗어나지 말고 Preview를 할 수 있도록 하기
  + 필요하다면 다른앱과의 공유기능을 제공(Document Picker Programming Guide 활용)
+ Gestures
  + 게임이 아닐 경우엔 항상 표준 Gestures를 사용해야 혼용X
  + HomeScreen, Control Center, Notification Center등 systemvide screen-edge 재스쳐를 막지 않아야 한다.
  + 가능하다면 Shortcut Gestures를 지원(예:Swipe Back 기능)
  + UIGsetureRecognizer를 활용하여 사용자에게 Multifinger Gestures를 지원하는 것을 추천
  + Standard Gestures
    + Tap : 선









