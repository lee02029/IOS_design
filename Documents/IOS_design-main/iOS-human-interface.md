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
  + 가능하다면 표현방식의 다양성을 구현
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
    + Tap : 선택, 컨트롤
    + Drag: 이동(item, 화면 등)
    + Flick: 스크롤이나 전환을 빠르게 하기
    + Swipe: 한 손가락 - 이전 화면으로 이동 split view controller에서 뒤에 화면 보이게 하기, 삭제등 액션 버튼 보이기 하기 / 네 손가락(Pad)- 다른 앱으로 전환
    + Double-tap: Zoom-in, Zoom-out
    + Pinch: Zoom-in, Zoom-out
    + Touch and hold: 텍스트(편집을 위한 메뉴),Certain View(item 재조정을 위한 모드로 진입)
    + Shake: Redo and Undo 
+ Near Field Communication
  + NFC
    + 물리적으로 접촉할 필요가 없기 때문에 용어를 잘 선택
      + "touch", "tap" 대신 "scan", "hold near" 등
    + "NFC tag"등 전문적인 용어를 사용하지 말고 친근한 언어 사용
    + 최대한 직관적이고 간단한 언어 사용, 단계가 여러개일 경우 중복되는 문구 제거
+ Undo and redo
  + 간단하고 정확한 단어로 실행할 것과 취소할 것을 명시
  + Shake Gestures를 사용할 경우에 다른 action을 중첩시키지 말것.
  + Redo와 Undo는 분리 시켜서 명확하게 한가지씩 동작하도록 할 것

### System Capability

#### Multitasking
+ OverView
  + 실행중인 앱에서 다른 앱으로 언제든 빠르게 전환할 수 있게 해주고, 특히 iPad에서 gesture로 전환가능하게 함.
  + iPad에서 두가지 앱을 한화면에 띄울 수 있는걸 가능하게 한다.
  <img width="585" alt="image" src="https://user-images.githubusercontent.com/80015108/147928921-a722b5d2-7e7f-471b-8050-9ea667ef35c8.png">
  
+ Contents
  + 앱 디자인 철칙& 앱개발시 명심해야할 사향
    + 멀티태스팅 환경에 맞게 앱을 디자인하기
    + 앱 사용 중단 -> 현재 상태 저장 -> 중단 상황이 끝남 -> 자연스럽게 동작
    + a double high status bar 상태를 지원
    + 앱에서 다른앱으로 이동할때, 사용자가 특별한 활동을 하지 않아도(저장) 그상태를 그대로 유지
    + 다른앱에서의 audio 소리에 적당히 반응
    + 앱이 Background상황이 되면 종료상황이라 인식 -> 그에 적절한 조치를 취함
    + 알림을 적절히 사용

#### Notifications
+OverView
  + 앱의 알림은 디바이스가 잠겨있어도, 중요한 정보는 어느때나 알림을 만들기
  + 각각의 알림은 앱 이름, small아이콘, 메세지를 포함
  
#### Notifications Behavior
+ Contents
  + 알림의 동작은 Setting에서 앱 하나하나 정해줄 수 있다.
  + 알림의 종류
    + Banner: 디바이스를 사용중일때 몇초간 화면 top부분에 보여짐
    + Alert: 디바이스를 사용중일때 수동으로 없애기 전까지 사라지지 않음
  + 잠금화면에서 Tapping, Swiping 하면 알림은 사라지고 알맞는 정보가 주어짐
  + 혹은 Swiping Up하거나 disappear을 선택하면 알림만 사라진다.
  + 잠금 해제화면에서 3D Touch를 사용하거나, Swiping Doen하면 Detail하게 볼 수 있다.
  + Customizable 가능
  + 4가지버튼의 액션을 정할 수 있다
  + Note: 알림의 설정의 여부는 앱이 처음 실행될떄 정해짐 -> Setting에서 정할 수 있음. 
  
#### Designing a Great Notification Experience
+ Provide useful, informative notifications
  + 완벽한 문장, 문장케이스, 적절한 구두점, 끊기지 않는 메세지(필요하면 시스템은 자동으로 문장을 자르기도 함)
  + 앱을 실행하라는 메세지는 피함
  + 특정한 화면으로의 전환, 특정한 버튼을 이용한 전환, 다른 테스크로의 전환하라는 말은 피하기(주의!!! 알림은 일단 dismissed됨)
  + 같은 정보에 대한 알림을 여러번 보내지 않는다.
  + 앱이름, 아이콘을 넣지 않는다.(자동으로 넣어줌)
  + 알림 미리보기가 숨겨진 경우 서술하는 문구를 제공
  + 알림과 함께 알림 소리도 정해준다.
  + 디테일 뷰를 고려
  + 직관적이고 유익한 액션을 제공 -> 적절한 4가지의 버튼액션으로 앱 사용 태스크를 중일 수 있다.
  + 디테일 뷰에서 알람을 없애는 액션을 신중히 사용 -> 만약 사용한다면 사용자에게 충분히 경고를 알려야한다.

#### Badging
+ Contents

  <img width="315" alt="image" src="https://user-images.githubusercontent.com/80015108/147931670-dbee68c5-836f-4063-9fff-2109e3fdf34e.png">
  + 알림을 쌓기위해 Badging을 이용 -> 특정한 정보를 표시 금지
  + Badging은 오직 알림에만 사용
  + Badging업데이트에 항상 신경쓰기 -> 사용자는 알림이 확인이 되면 Badging이 업데이트가 되길 바람

#### Printing
+ Overview
  + Air-print 기술을 사용하여 무선으로 여러 문서를 프린팅 할수 있다.
  + 만약 Air-Print를 사용하는 앱에서 프린트가 가능할때 유저들은 Navigation bar의 Print버튼이나, toolbar의 Print버튼을 이용
+ Contents
  + 프린트 시스템 버튼을 누른다면 사용자에게 다음과 같은 모습으로 버튼을 보여 준다.

  <img width="315" alt="image" src="https://user-images.githubusercontent.com/80015108/147932237-3d0d2c61-4dc3-491c-8a44-9c331bbb0ce1.png">
  + 프린트가 가능할때만 프린트기능을 활성화 -> 가능하지 않으면 표시X
  + 프린트하면 생각나는 기능들을 제공
    + 인쇄 범위
    + 인쇄 장수
    + 첫장부터 인쇄,뒷장부터 인쇄 등등

#### Quick Look
+ Overview
  + 미리보기는 다양한 포멧을 지원 -> keynote, Numbers, Pages, and PDF doucuments, images. types of files, 지원하지 않는 파일의 포맷포함
  + 보통 메일에서 다운로드한 파일을 미리보기에 사용
+ Contents
  + 현재 보고있는 화면에서 적절하게 뷰를 보여준다
    + 아이폰의 경우 네비게이션 바가 있다면 화면을 옆으로 밀어서 보여준다. -> 다른 뷰가 켜지는 것처럼
    + 아이패드에서 네비게이션바가 없다면 model뷰안에 네비게이션 바를 포함

#### Ratings and Reviews
+ Overview
  + 별점과 평가는 사용자들의 앱 선택에 도움을 준다 -> 긍정적인 별점과 평가는 더욱 사람들의 이목을 끌 수 있다.
  + 좋은 별점과 평점을 얻기위해 적절한 시점에 사용자에게 피드백을 요구하는게 중요
  + 나의 앱과 사용자가 입증괸 계약이 되어있을때 별점을 요구 -> 앱을 실행하자마자 요구 금지!
  + 유저를 방해하는 시점 요구 금지!
  
#### System Rating and Review Prompts
+ Contents
  + 시스템은 거슬리지않는 적절한 시점에 별점과 리뷰를 요청
  + 최근 별점을 주었다면, 당분간 알람을 띄어선 안됨
  + 시스템은 자동적으로 365일안에 별점 요청을 3번으로 제한
  + 되도록이면 시스템이 제공하는 별점창을 사용
  + 피드백을 위한 다른 버튼을 만들지 않기

#### Screenshots
+OverView
  + 유저는 현재화면을 캡쳐할 수 있다. ios11부터 화면 하단에 짧게 캡쳐한 화면이 보임
  + 되도록이면 시스템 스크린샷 인터페이스를 그대로 유지

#### Siri
+ OverView
  + 개발자의 앱에 Siri를 함께 이식해 음성으로 상호 작용 가능
+ Contents
  + 음성으로만 동작하게 처리(잠금해제없이 유저들은 시리를 사용하기를 원한다.)
  + Siri를 가장한 다른 Siri를 만들거나, Siri를 직접 다루지 않는다.(만약 그러면 애플에서 직접적으로 조치가 옴)
  + 공격적인 내용 금지!!
  + Siri를 광고에 사용 금지!!

#### Responding to People
+ 최소한의 개입으로, 반응 빠르게
+ 중간과정없이 Siri로 받은 명령은 직접 실행(Siri를 통해 앱을 실행할깨 중간 단계(Screen)없이 연결)
+ 정확한 행동화 믿을 수 있는 반응(Message 보내하고 했는데 전화 금지)
+ Siri를 통한 명령이 금전적인 요구가 있다면 안정하게 그리고 최소한의 금액을 요구하는 옵션을 제공(구매항목이 여러개 있는데 제일 비싼걸 디폴트 금지!!)

#### Designing a Custom Interface
+ 개발자의 앱에 Siri를 커스텀하려면, Siri의 모양을 최대한 살림
+ 인터페이스를 정의할때, 최소한의 여유 간격을 둠
+ 최소한의 높이를 갖는 인터페이스 마련
+ 대화형 인터페이스를 만들기 금지(탭, 제스터로 동일하게)
+ 인터페이스에 앱이름, 아이콘을 포함(자동으로 만들어줌)
#### Increasing Accuracy
+ 커스텀 단어를 정의해서 사용(Siri가 더많은 액션을 위해 단어를 정의, 단 기본적인 단어는 중복 정의X)
+ 다양한 앱 이름을 정의(UnicornChat -> Unicorn)
+ Siri 사용의 예제를 만들어줌
#### Tv Providers
+ TV App Intergration: 사용자들에세 장비를 상관하지 않고 좋아하는 영화, TV Show를 보여줄수 있다.
  + 화면 전환의 부드러운 연속성을 유지 -> TV App이 실행될 때 검은 화면을 먼저 표시 -> 끝날때도 동일
  + TV App을 실행할때, 내용을 우선해서 먼저 보여줌 -> 중간에 splash화면이나 다른 것들이 오면 좋지 않음
  + 영상을 시작할땐 사용자에게 재생할것이지 묻지 않기
  + 올바른 사용자에게 내용이 보여지는지 확실하게 하기 -> 앱이 여러 프로필을 지원하면 TV App은 재생 요청할때 지정 가능
+ Loading Content: 2초이상 로딩이 지연되는 경우 화면 중앙에 Activity spinner을 위치
  + 가능하면 로딩화면은 피하기
  + 가능하면 재생을 빠르게 하기 -> 로딩화면이 필요하면, 재생에 필요한 만큼 로딩
  + 로딩 화면은 검정으로 하기 -> TV App의 하얀 화면과 대비가 잘된다.
  + 로딩 화면시 컨텐츠는 최소한으로 보여줌
+ Exiting Playback: 유저는 영상을 재생완료 후 TV App으로 이동하는게 아니하 나의 앱으로 남긴다 -> 유저에게 혼동 방지
  + 상황에 맞는 화면을 보여줌
    + 컨텐츠를 종료할때, 방금까지 보았던 내용을 표시
    + 다른 시작하는 버튼도 옵션으로 넣기
    + 콘텐프가 포함된 메뉴를 보여주거나, 앱의 메뉴를 보여줌
  + 사용자가 언제든 종료가능 -> 그것을 위한 대비하기
#### TV Providers
+ Single sign-On: TV Provides가 사용자 계정 인증을 요구 -> 그럴때 사용

<img width="315" alt="image" src="https://user-images.githubusercontent.com/80015108/147936044-7baf28f0-cc8c-4e48-bbab-bd49d66e139c.png">
  + 유저가 system Level에서 인증을 했다면, 또다시 인증을 요청하지 않기
  + Privacy controls에서 로그아웃을 하지 않기

### Visual Design

#### Adaptivity and Layout
+ OverView
  + 사용자들은 다양한 디바이스에서 동일한 앱을 사용하길 원함
  + ios는 자동으로 화면의 크기에 맞게 모양을 바꿔줌

<img width="525" alt="image" src="https://user-images.githubusercontent.com/80015108/147936530-8dcf3a25-8adb-47fb-9d6e-27b52c664b40.png">
+ Auto Layout
  + Auto Layout을 이용해 화면상의 규칙을 정할 수 있다.
  + 자동으로 레이아웃을 Constraints를 통해 줄 수 있다.
  + Auto layout including
    + 다른 크기의 스크린과 다른 색상들(sRGB/P3)
    + 다른 디바이스의 회전화면들(portratit/landscape)
    + iPad Split view
    + Multitasking mode(iPad)
    + Dynamic Type(사이즈 조절)
    + 국제화적인 특징을 가질 수 있다.(왼쪽 오른쪽 레이아웃 방향, 시간등)
+ Layout Guides and Safe Area
  + 레이아웃 가이드는 실제 화면에선 보이지않는 정사각형의 레이아웃을 정의
  + safe 영역과 layout margins(UIKit)을 고수하기

  <img width="398" alt="image" src="https://user-images.githubusercontent.com/80015108/147937042-502094eb-561d-4885-8796-bf7e30f06c19.png">
+ Adaptivity and Layout
  + Size Classes: 디바이스마다 슽크린 사이즈를 불러오는 클래스
    + regular
    + compact

<img width="607" alt="image" src="https://user-images.githubusercontent.com/80015108/147937286-a4477ffe-c14c-4dcf-8973-60b5304ee900.png">

<img width="609" alt="image" src="https://user-images.githubusercontent.com/80015108/147937328-50cedeae-5b9b-4bd4-9a11-98cb6db6c93b.png">

<img width="579" alt="image" src="https://user-images.githubusercontent.com/80015108/147937355-3ce54e15-e25b-422e-9228-018d334307fc.png">

<img width="462" alt="image" src="https://user-images.githubusercontent.com/80015108/147937374-c813ac5c-8469-45b6-b5bf-723b14e63cc4.png">
+ Layout Considerations
  + Context가 바뀌는동안, 현재의 콘텐츠에 집중할 수 있게한다.
  + 중요한 내용이면 한가지 화면에 다 담도록 노력
  + 화면이 바뀔 때 통일
  + 중요한것을 전달하기위해 시각적인 균형을 잘맞추기
  + 화면을 가득 채우기
  + 적절한 빈공간과 주변을 콘텐츠로 채우기
  + 큰화면의 디바이스에서 읽기좋은 화면 간격을 유지
  + 충분한 터치가 가능한 버튼, 아이콘을 넣기

  <img width="483" alt="image" src="https://user-images.githubusercontent.com/80015108/147937746-3396fc87-93f7-43df-a089-839c7775acd8.png">
  + 불필요한 layout 변경은 피하기
  + 가능하면 가로, 세로 모드를 지원
  + 만약 필요하면 하나의 모드를 지원
  + 앱의 내용에 따라 화면 전환을 커스텀하기
  + 폰트크기에 변화에 대응할 준비하기

#### Animation
+ IOS는 미묘한 애니메이션을 이용해서 GOOD
+ 적절한 사용은 유저들의 행동에 도움을 준다
+ 현명하게 애니메이션 효과를 사용
+ 현실성있게, 신뢰성있게 되려고 노력(사람들은 생각한대로 안움직이면 혼란스러워함)
+ 일관된 애니메이션을 사용
+ 애니메이션을 만드는것을 선택적으로 한다.

#### Branding
+ OverView
  + 훌륭한 앱은 독특한 브랜드의 특성을 가지고있다.(폰트,색상,이미지)
  + 정교하고 깔끔한 브랜딩을 만들기
  + 브랜딩이 앱디자인을 방해 금지(브랜딩보다 ios앱 답게 만드는게 중요)
  + 만든 앱의 모든곳에 나의 로고를 넣고싶은 유혹을 뿌리치기
  + 애플 가이드라인을 고수하기

#### Color
+ Overview
  + 색상은 유저와의 상호작용에 큰 도움이 된다
  + App tint 색상을 고를 때는 색상 설계 가이드를 보고 선택하기
  
    <img width="496" alt="image" src="https://user-images.githubusercontent.com/80015108/147938809-4023e7b2-7e9f-457b-8ebb-2055e10c4a33.png">
  + 의사소통을 위해 색상을 신중히 사용(경고의 경우 빨간색)
  + 상호보완적인 색을 앱에 사용
  + 앱로고와 일백상통하는 색상을 사용. 브랜딩에 도움
  + 하나의 대표 색상을 정해서 앱에 적용
  + 활성화, 배활성화 색상은 같은 색을 사용 금지
  + artwork와 반투명사이의 색상을 고려

    <img width="426" alt="image" src="https://user-images.githubusercontent.com/80015108/147939051-fbfbb90a-1a9b-4d36-af00-6fde61d7a98b.png">
  + 다양한 환경에서 색상을 테스트(실내,실외에 따라 다르게 보일수 있다.)
  + True Tone 효과(자동밝기조절)가 색상에 영향을 미치는걸 고려
  + 색맹에 대해 알고 있어야한다.
  + 문화권, 나라마다 다른 색상에 대한 의미를 고려
  + 충분한 색상 대비 비율을 사용(4.5:1)
  + 5%가 사람들에게 주제 색상을 인식 시켜준다.
  + 마법의 비율 70:25:5
  
    <img width="441" alt="image" src="https://user-images.githubusercontent.com/80015108/147939557-2332c4b9-f379-4784-9c11-e6a0b1562c45.png">

    <img width="345" alt="image" src="https://user-images.githubusercontent.com/80015108/147939612-0b87e7be-f695-4e05-a8f1-71cfe20d8e7b.png">
    
#### Color Management
+ ios standard RGB(sRGB)에 맞는 이미지를 사용
+ 호환 가능한 색상을 최대한 사용(Display P3) 픽셀당 16비트 P3프로파일 .png

  <img width="281" alt="image" src="https://user-images.githubusercontent.com/80015108/147939858-d6c0796e-fcfa-4bd8-921f-837e67c7008b.png">
+ iphone 7 최초의 DCI-P3 color space 사용제품

   <img width="431" alt="image" src="https://user-images.githubusercontent.com/80015108/147939949-bb8c2a12-3d17-4a74-a865-112c16a40342.png">

#### Terminology
+ OverView
  + 유저화의 소통을 위해 소통법이 편안함을 주는지 알아본다
  + San Francisno(SF)는 IOS의 기본 폰트!!
  + 한글 서체인 애플SD 고딕 네오와의 조합도 굿
+ Contents
  + 친숙하고 이해하기 쉬운 용어와 문장을 사용(일반적으로 모든사람이 사용하는 앱에는 기술적인 용어는 필요X)
  + 인터페이스 텍스트를 간결하고 명확하게 보여준다.(사람들은 읽는것을 강요받는걸 싫어한다.)
  + 사람과 대화하는 느낌의 Label문장과 Button을 만든다.(요소를 한눈에 알아야 한다.)
  + 공손한 말투 사용
  + 비공식적이고, 친숙한 언어를 사용하게 노력
  + 유머를 사용할때는 조심해서 사용(다른 문화권에서는 안 통할수 있기 때문)
  + 관련성있고 일관된 이미지와 텍스트를 사용(iPad사용자가 iPhone 정보나 이미지를 보여주지 말기)
  + 날짜를 정확하게 사용
    + 앱을 사용하는 사람의 시간대에 맞추어서 날짜정보를 보여주어야한다.
    + 비행일정표를 보여주는 앱, 비행의 출발과 도착 시간을 명시적으로 표현
  + 중요한 내용으 강조
  + 가능하 한가지 서체를 사용
  + 가능하면 기본으로 제공하는 text style을 사용
  + Custom fonts가 잘보이는지 확인
  + Custom fonts가 사용자 지정 크기변화에도 적용이 잘되어야함
+ Typography
  + SF느 유동적인 크기변화에도 잘 작동됨
  + xSmall,Samll,Medium,Large,xLarge,xxLarge,xxxLarge
  + Larger Accessibility Type Sizes -> 추가적으로 더 큰 사이즈의 타입을 지원
+ Font Usage and Tracking
  + 인터페이스의 실물 크기로 올바른 글꼴을 사용
    + Button, Label, 표준 컨트롤러 라이브러리는 사용자 설정으로 자동으로 폰트가 변경됨

#### Icons and Images
+ OverView
  + ios는 이미지를 배피할떄 사용하는 기본 좌표는 Point Display에서는 Pixel이다.
  + Standard-Resolution screen에선 Point == Pixel
  + 고생도에서는 Pixel의 수가 더 많아진다. Point != Pixel
+ Contents
  + 앱이 지원하는 모든 장피에 대해 고해상도 이미지가 있어야한다.
    + 표준 해상도 이미지의 비율 -> 1.0, @1x -> 10px * 10px
    + 2.0 -> @2x -> 20px * 20px
    + 3.0 -> @3x -> 30px * 30px
+ Designing High-Resolution Artwork
  + 8px-by-8px grid를 사용
    + 깔끔하고 날카롭게하는 다듬기 작업이 수월
    + 이미지 경계를 그리드로 맞추면, 이미지 축소시 발생하는 이미지 손실을 최소한으로 막을수있다.
  + 적절한 포맷 이미지 사용 권장
    + 무손실이미지
    + 사진 -> JPEG 사용 , 사이즈를 줄여주지만, Artwork보다 손실된 이미지를 구분하기가 어려움
  + 24-bit가 다 필요없다면, 8-bit color palette를 사용
+ Designing High-Resolution Artwork
  + JPEG를 사용하면 사이즈와 quality의 균형 맞추기
  + 이미지 및 아이콘에 대한 텍스트 정보를 제공 -> VoicOver

#### App Icon
+ Overview
  + 모든 앱은 앱스토어나 홈화면에서 이목을 끌고, 기억에 남는 아름다운 아이콘을 가짐
  + 아이콘은 앱의 목적과 어떤 앱인지 짧게 보여줄 기회
  + 아이콘은 시스템 전반에서 어디든지 보여줌
+ Contents
  + 단순하게!
  + 한가지 포인트 정하기
  + 알아보기 쉬운 디자인 하기
  + 배경은 단순, 투명은 X
  + 로고일 경우에만 단어 사용
  + 사진, 스크린샷, 인터페이스 요소는 X
  + 애플껀 사용 X
  + 인터페이스에 사용된걸 사용 X
  + 여러 배경에서 테스트
  + 아이콘의 모서리는 정사각형으로 유지

+ App Icon Attributes
  <img width="550" alt="스크린샷 2022-02-17 오후 3 12 13" src="https://user-images.githubusercontent.com/80015108/154416280-e435e343-5edc-41d9-8511-c74f32020807.png">
+ App Icon Sizes
  + 모든 앱은 반드시 Small아이콘이 있어야합니다. 큰아이콘은 App Store에서 사용
  + 다양한 디바이스에서 아이콘이 멋지게 보이는지 확인
  + 작은 아이콘을 앱스토어에 사용X -> 앱스토엔 좀더 상세한 묘사를 할 수 있다.
+ Spotlight, Setting, and Notification Icons
  + 모든 앱은 반드시 Small 아이콘이 있야합니다. 검색할떄, 세팅에서, 알림에서 쓰인다.
  + 세팅아이콘에 중첩이나 테두리를 사용X

#### Custon Icons
+ Overview
  + 우리가 만든 앱이 시스템 아이콘으로 다 표현할 수 없다면, 새롭게 만들 수 있다.
+ Contents
  + 알아보기 쉽게, 간단히 디자인하기
  + Glyph처럼 아이콘은 디자인하기
  + Glyphs는 @2X와 PHD로 저장
  + 아이콘에 일관성을 유지하기
  + 읽기 쉬운 아이콘이어야함
  + 아이콘이 선택되었을떄와 그렇지 않을때를 color로 나뉘어 사용
  + 아이콘에 텍스트를 사용X
  + 애플기본 아이콘을 사용X
  + 아이콘과 마찬가지로 VoiceOver 기능에 대응하기
+ Cutom Ico Sices
  + 아이콘은 동일한 사이즈를 가짐
  
  <img width="424" alt="스크린샷 2022-02-17 오후 3 25 32" src="https://user-images.githubusercontent.com/80015108/154418001-c9042c36-a34f-4141-9105-00a97778cea8.png">

+ Tab Bar Icon Size
  + Portrait 방향일때, Landscape 방향일때 아이콘의 크기를 정하기
  + Regular tab bar 일때와 Compact tab ber
  
  <img width="489" alt="스크린샷 2022-02-17 오후 3 26 17" src="https://user-images.githubusercontent.com/80015108/154418071-57ce43f5-c6af-4700-be62-5183c9245179.png">
  
#### Launch Screen
+ Overview
  + 앱이 실행되기 전의 화면 -> 실행되면 빠르게 실행화면으로 전환 -> 예술적으로 보여줄 기회X
  + 모든 앱은 Launch Screen이 있다.
  + Launch Screen은 디바이스마다 다르기 때문에, Xcode에서 storyboard를 사용하기를 권장
+ Contents
  + 앱의 첫번쨰 화면이디 깨문에 정체성을 보여 줄수 있는 화면으로 만들기
  + 텍스트를 피하기 -> 정해진 화면이기 때문에 국제화를 대응할수 없다.
  + 사용자들이 앱을 자주 바꿔서 실행하기 때문에, 이목을 쓰는 launch Screen 사용 X
  + 광고에 사용X
  
#### System Icons
+ Overview
  + IOS에서 제공해주는 아이콘을 사용 -> 사람들에게 친숙함을 느끼게함
    + Navigation Bar and Toolbar Icons
    + Tab Bar Icons
    + Home Screen Quick Action Icons
  + 의도에 맞는 아이콘을 사용
  + 아이콘에 대체 text-Label을 제공
  + 필요하면 커스텀아이콘을 사용

  <img width="509" alt="스크린샷 2022-02-17 오후 3 34 52" src="https://user-images.githubusercontent.com/80015108/154419178-916fdfd6-822d-4596-a5e0-961f60d35ba9.png">


### Bars(UI Elements)
+ Navigation Bars
  + 계층구조로 구성된 연속적인 페이지를 차레로 조회 가능
    + 위치: 화면 상단의 상태바 아래
    + 좌측: 보통 뒤로가기 버튼 삽입, 보통 이전 페이지 제목으로 표시
    + 우측: 기타 컨트롤 요소 삽입, 보통 수정 또는 완료 버튼 표시
  + 숨김 처리
    + 제스처 발생, 키보트 노출, 뷰 사이즈 변경등의 상황에 바를 숨긴다.
    + 콘텐츠를 전체화면으로 보여주는 경우, 바를 숨기는 편이 좋다
  + 타이틀 배치 시 권유사항
    + 현재 보여지는 뷰의 제목을 표시하는 편이 좋다
    + 종류: Stardard title, Large title
    + 기본적으로 Large title로 표시한 후, 스크롤 등의 이벤트가 발생 시 Standard title로 변경하는 것이 좋다.
  + 바 내부에 컨트롤 요소 배치 시 권유 사항
    + 컨트롤 요소를 너무 많이 넣지 않는다.
    + 버튼 사이 간격을 넓게 한다.
    + 뒤로가기 버튼은 Standard Back Button 사용, 항상 직전 화면을 표시하는 액션만 취해야 한다.
    + 세그먼트 컨트롤을 사용하면 페이지들의 계층 구조를 단순하게 보여줄 수 있다
    + 세그먼트 컨트롤을 넣을 깬 타이틀을 제외한다: 보통 3~5개의 탭을 쓴다.
    + 탭은 항상 활성화 상태로 둔다: 탭 내부 콘텐츠가 사용할 수 없더라도 탭 내부에서 이를 표시한다.
    + 특정 탭에 업데이트된 정보가 있으면 배지를 달아서 표시할 수 있다.


+ Tab Bars
  + 앱 내에서 다른 섹션으로 스위칭 가능
    + 앱 구조를 단순하게 표시 할 수 있다. 앱 레벨에서 사용한다.
    + 위치: 화면 하단
    + 탭바 버튼은 액션을 수행하는 데 사용하지 않는다. 현재 뷰에서 특정 액션을 취해야 하는 경우, Tool Bar를 사용한다.
    + 너무 많은 탭을 쓰지 않는다.

<img width="622" alt="스크린샷 2022-02-17 오후 3 45 56" src="https://user-images.githubusercontent.com/80015108/154420738-3715f300-577e-4e9c-8d8f-796d3b22a7f1.png">

+ Tool Bars
  + 현재 뷰에서 수행가능한 기능 표시
    + 위치: 화면 하단
    + 현재 화면과 관련된 버튼만 표시
    + 툴바 위에 세그먼트 컨트롤은 사용하지 않는 편이 좋다
    + 택스트 버튼들은 간격을 넓게 한다.

+ Search Bars
  + 단독으로 배치되거나 네비게이션 바 등의 뷰 내부에 배치
  + Text Field 말고 Search Bar 요소를 이용한다.
  + Clear 버튼 사용
  + Cancel 버튼을 만들어 검색을 중단할 수 있도록 한다.
  + 검색 중 하단에 연관검색어를 보여주면 좋다.
  + 힌트 문구를 넣어 검색 가능한 범위를 알 수 있도록 한다.
  + Scope Bar
    + 검색 바에 붙이면 검색 범위를 좁힐 수 있다.

+ Status Bars
  + 현재 시간, 네트워크 상태, 배터리 등 기기의 현재 상태를 표시
    + 시스템 제공 바를 사용
    + 앱 디자인에 따라 바 색상을 변경 할 수 있자: Light/Dark
    + 기본적으로 투명해서 콘텐츠가 비쳐보인다: 상태바 내용이 잘 보일 수 있도록 상태바 뒷부분에 UIBlurEffect를 적용하여 흐리게 만든다.
    + 전체화면으로 미디어를 보여줄 때는 상태바를 잠시 숨긴다.
    
### Views(UI Elements)
+ Tables
  + 컬럼 1개인 리스트로, 여러 줄의 데이터를 스크롤 조회 가능
    + 주로 텍스트 기반의 콘텐츠나 Split View에서 내비게이션을 표시할 때 사용됨
    + 테이블 너비를 고려
    + 이미지 들의 추가적인 데이터를 보여주기 위해 기다리지 않는디: 텍스트 데이터부터 빠르게 보여준다.
    + 콘텐츠가 로드될 때까지 Progress Indicator를 보여준다.
    + 테이블 콘텐츠를 정기적으로 업데이트하는 방법을 고려한다. 단, 업데이트될 때 현재 스크롤 위치는 유지한다.
+ Plain
  + 행이 라벨이 있는 섹션 단위로 묶일 수 있다.
  + Header와 Front를 가질 수 있다.
  + 우측에는 색인(index)을 세로로 삽입할 수 있다.
  + 단, 우측에 Disclosure Indicator 등의 요소가 있으면 색인은 넣지 않는다.
+ Grouped
  + 행이 그룹 단위로 묶일 수 있다.
  + Header와 Footer를 가질 수 있다.
  + 항상 1개 이상의 그룹을 가지며, 각 그룹은 1개 이상의 행을 가진다.
  + 색인은 삽입 X
  
  <img width="511" alt="스크린샷 2022-02-17 오후 10 57 20" src="https://user-images.githubusercontent.com/80015108/154496473-c18041fc-c024-4dc8-93ae-39d80d5806ad.png">
  
+ Collections
  + 정렬된 콘텐츠 모음을 관리하고 시각적인 레이아웃으로 표시
    + 업격한 선형구조를 요구하지 않기 때문에, 여러 사이즈로 콘텐츠들을 보여주는 데 적합하다.
    + 콘텐츠 주위에 패딩 사용: 레이아웃을 깨끗하게 유지하고 콘텐츠가 겹치는 것을 방지할 수 있다.
    + 텍스트 콘텐츠 배치 시, 컬렉션보다 테이블 사용
    
+ Split Views
  + 스크린을 두 화면으로 나누어 관리
  + 주 화면(왼쪽): 변하지 않는 내용 표시
    + 보통 카테고리(네비게이션) 표시
    + 사용하지 않을 떈 숨겨둔다
  + 보조 화면(오른쪽): 관련 콘텐츠 표시
  + 화면 분할은 콘텐츠 균형에 맞게 한다.
    + 기본적으로 주 화면은 1/3, 보조 화면은 2/3을 차지한다.
    + 보조 화면이 주 화면보다 더 작아지면 안된다.
  + 숨겨져 있는 주 화면 노출 시, 여러 방법 제공
    + 스와이핑, 버튼 클릭 등

+ Scroll Views
  + 사용자와 상호작용 시, 일시적인 스크롤 인디케이터 노출
    + Tap,flick,drag,pinch,swipe 제스처를 따른다.
    + 사용자 제스처의 적정선을 설정한다: 예를 들어, 줌인 시 너무 커지거나 작아지지 않도록 최대 스케일, 최소 스케일 값을 설정한다.
    + 페이징 모드로 설정 시: 스크롤 시 새 페이지로 전환 기능
    + 스크롤 뷰 안에 스크롤 뷰를 중첩해서 넣지 않는다.
    + 스크롤 뷰는 한 화면에 1개만 보여준다.
      + 만약 2개의 스크롤 뷰를 넣어야 한다면, 다른 방향으로 스크롤 하도록 만든다. 제스처가 다른 뷰에 영향을 주지 않기 때문
      
+ Pages
  + 문서, 책, 메모장, 달력 등에 사용되며, 여러 장의 콘텐츠를 차례대로 접근 가능
    + 화면 전환 방법: Scrolling or page-curl
    + 연속되지 않는 특정 페이지에 바로 접근할 수 있도록 구현하면 좋다.

+ Text Views
  + 텍스트 뷰는 어떤 높이도 될 수 있으며, 콘텐츠가 뷰보다 길어질 때 스크롤 가능하다.
  + 텍스트는 읽기 쉽게 쓴다.
    + 여러 글꼴, 색 등을 입혀 창의적인 방법을 사용할 수 있지만, 콘텐츠 가독성을 유지하는 것이 중요하다.
    + Dynamic Type을 사용하면 기기에서 텍스트 크기가 변경되어도 여전히 좋게 보인다.
    + 만약 텍스트뷰가 수정 가능하면(editable), 탭 시 키보드가 올라온다.
    + 적절한 키보드를 보여준다: 효율적인 텍스트 입력을 위해서는 필드에 들어갈 콘텐츠 타입에 맞는 키보드를 노출해야 한다.(UIKeyboardType)
    
+ Image Views
  + 한 장의 이미지나 여러 장의 연결된 이미지들을 표시
    + 이미지는 이미지뷰 안에서 늘어나거나 커지거나 작아지거나 딱 맞춰지거나 특정 위치에 고정될 수 있다.
    + 이미지뷰는 기본적으로 사용자 상호작용이 불가능하다.
    + 연속되는 이미지들을 통해 애니메이션 형태로 보여줄 때 최대 한 같은 사이즈의 이미지를 사용한다: 시스템이 스케일링을 해주긴 하지만, 미리 이미지들이 뷰 사이즈에 맞게 처리돼있는 것이 좋은 결과듣 보여준다.
    + 템플릿 이미지로 설정된 이미지: color 값이 제거되고 이미지 뷰의 틴트값을 사용한다.
      + 이미지를 항상 템플릿 이미지로 그리는 옵션:UIImageRenderingMideAlwaysTemplate
    + 템플릿 이미지란?
      + 단색 이미지로, 마스크를 사용하여 모양을 정의함
      + 투명도가 있고, 안티앨리어싱 기능이 있으며 명암이 없다.
      + 이는 자동으로 상황이나 상호작용에 따라 적절한 색상 지정, 강조 표시 등을 받아 사용한다.

+ Map Views
  + 지형정보를 보여주고 빌트인 맵 앱에서 제공하는 기능을 지원
    + 표준지도, 위성이미지 표시 가능
    + pin,overlay,zooming, panning 기능 제공
    + 이동루트 표시 가능 
    + 예측 가능한 pin 색상을 사용: 사용자는 표준 pin 색상에 익숙하다. 목적지는 빨간색, 출발지는 녹색, 사용자 선택 지점은 보라색으로 표시한다.

+ Web Views
  + HTML이나 웹사이트 들 웹 콘텐츠를 앱 내부에 표시
    + 필요하면 이전페이지보기/ 다음페이지보기 버튼을 활성화한다:
    + 기본적으로 비활성화 되었다. 앱에서 여러 페이지의 웹뷰를 보여줘야 한다면 활성화 하는 것이 좋다.
    + 웹뷰를 웹브라우저로 사용하지 않는다.  

#### Temporary Views: UI Elements
+ Alerts
  + 중요한 상황에만 사용한다:
    + 사용자 작업을 한 번 더 확인하거나 삭제 등의 작업을 수행하거나 문제 사항을 알릴 때 등에만 사용한다.
    + 기본 알림창은 보통 커스터마이징 X
    + 필요한 정보만 노출시키도록 사이즈를 최소화한다.
    + Landscape 모드, Portrait 모드에서 모드 확인해본다.
  + 제목 
    + 한 줄로 작성한다.
    + 한 단어만 사용하진 않는다: 한 단만 사용하면 내용란에 부가적인 설면이 필요할 수 있다.
  + 설명 
    + 설명은 되도록 X
    + 꼭 적어야 한다면, 짧은 문장으로 적는다.
  + 버튼
    + 주로 버튼 2개만 배치
    + 버튼 1개로는 사용자가 상황을 컨트롤하기 힘들다.
    + 3대 이상의 버튼이 필요하면 액션시트로 대체한다.
    + 사용자들이 더 많이 누를 것 같은 버튼은 오른쪽에 배치하며, 취소버튼은 항상 왼쪽에 배치한다.
    + 취소버튼명은 항상 "취소"로만 표시되어야 한다.
    + Delete등의 버튼은 Destructive 스타일(UIAlertActionStyleDestructive)로 만든다. 또 취소 버튼도 같이 제공한다.
    + 홈 버튼 등으로 앱이 종료되는 경우, 알림이 취소되도록 구현한다:
      + 알림창이 노출된 상황에서 홈 회면으로 앱이 종료되면, '취소'버튼을 누른 것과 같은 결과를 내야 한다.
      + 만약 알림창에 취소 버튼이 없으면 앱이 종료되는 시점에 취소 액션을 구현할 수도 있다.

+ Action Sheets
  + 알림 컨트롤러의 일종으로, 2~3개 이상의 선택지 제공
    + 새 작업창을 열거나, 종료 여부 확인시 사용하면 좋다.
    + 작은 화면에서는 액션시트가 화면 아래에 표시되지만, 큰 화면에서는 Popover형태로 나타내야 한다.
    + 아이패드에서는 구현 시에 팝오버로 띄우지 않으면 에러 발생
    + 취소 버튼을 반드시 넣는다: 액션 시트 마지막 항목으로 배치하면 좋다.
    + 위험한 선택지는 눈에 띄게 넣는다: 빨간색을 사용하여 눈에 띄게 표시한다. 액션 시트 첫 항목으로 배치하면 좋다.
    + 스크롤이 생기지 않도록 너무 많은 항목을 넣지 않는다.

+ Popovers
  + 특정 컨트롤이나 영역 탭 시 콘텐츠 위에 잠시 뜨는 뷰
    + 비모달 형태:
    + 스크린의 다른 부분을 탭하거나 popover 위의 버튼을 누르면 닫힘
    + 한 번에 1개만 표시된다.
    + Popover 위에는 알림 외의 다른 뷰를 띄우지 않는다.
    + 너무 크게 만들어 스크린 전체를 사용하지 않도록 주의
    
+ Activity Views
  + 해당 페이지에 관련된 액티비티 관리
    + 액티비티:
    + 현재 페이지 내에서 수행할 수 있는 복사, 즐겨찾기, 검색 등의 작업단위
    + 액티비티 뷰의 관리를 받는데, 액션시트나 popover 형태로 표시
    + 시스템 제공 빌드인 액티비티: Print, Message, AirPlay, 액티비티 뷰에 가장 먼저 표시되며, 순서를 변경 X -> 단, 제외는 가능
    + 작업명은 아이콘 바로 아래 간단히 표시: 작업명이 길면 ios는 텍스트를 먼저 줄인 후 너무 길면 자른다. 또한 회사나 제품 이름을 포함시키지 않는다.
    + 시스템이 제공하는 Action 버튼을 사용한다.

#### Controls: UI Elements
+ 시스템 제공 버튼

<img width="511" alt="스크린샷 2022-02-17 오후 10 57 20" src="https://user-images.githubusercontent.com/80015108/154507096-3b0b5c45-0886-42de-99c0-c32d28e58845.png">

+ Labels
  + 텍스트는 읽기 쉽게 쓴다.
    + 여러 글꼴, 색 등을 입혀 창의적인 방법을 사용할 수 있지만, 콘텐츠 가독성을 유지하는 것이 중요하다.
    + Dynamic Type을 사용하면 사람들이 거기에서 텍스트 크기를 변경하는 경우에도 여전히 좋게 보이게 할 수 있다.

+ Text Fields
  + 1줄짜리 라인 필드로, 소량의 정보를 요청할 때 사용
    + 높이는 고정이다.
    + 사용자가 탭하면 키보드가 자동으로 노출한다.
    + 되도록 라벨을 따로 두지 말고 힌트를 사용한다.
    + 오른쪽 끝에 Clear 버튼을 삽입한다.
    + 암호와 같은 중요한 데이터를 요청할 떄, 항상 보안 필드를 활용한다.
    + 이미지와 버튼을 사용하여 텍스트 필드에 목적과 추가기능을 표시한다: 일반적으로 텍스트 필드의 왼쪽 끝은 필드의 목적을 나타내고, 오른쪽 끝은 북마크와 같은 추가 기능이 있음을 나타낸다.
    + 여러 줄의 텍스트를 입력받기 위해서 Text View를 사용한다.
    + 적절한 키보트 유형을 표시한다.(UIKeuboardType)

+ Edit Menus
  + 현재 페이지에 적합한 메뉴들만 표시:
    + 기본적으로 잘라내기,복사하기,붙여넣기,선택,전체 선택, 삭제 기능을 제공하지만, 선택적으로 비활성화 시킬 수 있다.
  + 필요한 경우 위치를 변경한다:
    + 시본적으로 선택한 부분의 위 또는 아래에 배치되지만, 중요한 콘텐츠를 가리고 있는 경우 위치를 변경할 수 있다.
  + 수정 불가한 텍스트는 선택/복사가 가능하고록 만들면 좋다.
  + 수정 메뉴는 한 번 실행되면 취소할 수 없기 때문에, Undo/Redo 명령을 제공한다.

+ Progress Indicators

<img width="516" alt="스크린샷 2022-02-18 오전 12 06 46" src="https://user-images.githubusercontent.com/80015108/154509895-cc0767e6-b293-4792-8329-bd52f1cd431a.png">

+ Refresh Content Controls
  + 주로 테이블뷰에서 수동으로 새로고침 시 사용된다.
  + 기본적으로 숨겨져 있으며, 화면을 아래로 드래그하면 나타난다.
  + 자동 업데이트도 정기적으로 수행하도록 구현한다:
    + 사용자들을 자동 업데이트가 실행되기를 기대한다.
  + 값이 추가되는 경우에만 짧은 제목을 제공:
    + 제목을 포함시킬 수 있는데, 대부분의 경우 불필요하다
    + 제목을 포함할 경우엔 콘텐츠에 대한 가치있는 정보를 제공한다.
    

+ Page Controls
  + 여러 페이지 중 현재 페이지를 나타냄
    + 일련의 작은 점으로 표시 -> 색칠된 점 == 현재 페이지
    + 점들은 항상 같은 거리 유지 -> 너무 많으면 잘림
    + 페이지 컨트롤의 앞/뒤를 탭하면 이동하지만 특정 페이지론 이동 불가
    + 계층구조의 페이지에는 사용X: 페이지 컨트롤은 페이지들이 관련된 방식을 보여주지 않고, 각 점에 해당되는 페이지를 나타내지 않는다 -> 페이지 컨트롤은 동등한 관계에 있는 페이지를 위해 설계
    + 항상 콘텐츠와 스크린 사이에 위치해야 한다.
    
+ Segmented Controls
  + 각 세그먼트는 상호배타적이며, 다른 뷰를 표시하는 데 사용되기도 함
    + 모든 세그먼트와 폭은 동일, 텍스트나 이미지를 삽입X -> 단, 텍스트와 이미지를 혼합하지 않는다.
  + 세그먼트 수를 제한 -> 아이폰에서는 5개 이하
  + 콘텐츠 크기로 일정해야 한다.
    + 모든 세그먼트가 동일한 폭을 가지기 때문에 콘텐츠가 일부 세그먼트만 채우고 다른 세그먼트는 채우지 않으면 좋아보이지 않는다.
    
+ Switches

<img width="447" alt="스크린샷 2022-02-18 오전 12 18 09" src="https://user-images.githubusercontent.com/80015108/154512107-39ea4169-91f9-40d1-bb32-ccfced486215.png">

+ Sliders
  + 가로트랙 위에서 최소값과 최댓값 사이를 이동시켜 특정 값 변경
    + 양쪽으로 최소값, 최댓값을 의미하는 아이콘을 표시
    + 오디오 볼륨에는 슬라이더를 사용X
      + 앱에서 볼륨 컨트롤을 제공하는 경우 -> Volume View를 사용

+ Steppers
  + 2개의 세그먼트로 이뤄진 컨트롤, 값을 증가/감소시키는 데 사용
    + 스테퍼가 영향 주는 값을 명확히 표시한다:
      + 스테퍼 자체는 값을 표시하지 않기 때문에 변경하는 값이 뭔지 알여줘야 한다.
    + 큰 값을 변경할 때는 스테퍼 사용 X:
      + 스테퍼는 보통 몇 번의 탭으로 변경할 수 있는 정도에만 사용

+ Pickers
  + 보통 화면 아래쪽에 표시되거나 팝오버 형태로 표시 -> 테이븡 특정 행의 인라인으로 표시되기도 함
  + 피커의 높이는 5개 행 정도이다.
  + 논리적으로 정렬된 값을 사용
    + 많은 값이 숨겨져 있기 때문에 어떤 값이 나올지 예측 가능하도록 만드는 것이 중요
  + 피커를 보여주기 위해 화면전환을 하지 않는다:
    + 현재 체이지 내에서 편집한는 필드 아레나 근처에 위치
  + 아주 긴 리스트를 보여줘야 할 때는 피커 대신 테이블을 사용
    + 너무 긴 피커는 탐색할 때 지루할수 있다. 반면, 테이블은 높이를 조절 할 수 있고 색인이 있디 때문에 빠르게 탐색 가능 
+ EX) Date Picker

<img width="497" alt="스크린샷 2022-02-18 오전 12 27 30" src="https://user-images.githubusercontent.com/80015108/154514014-f4b118ac-9612-4a72-b1bf-38dd5a6fb0d2.png">
















