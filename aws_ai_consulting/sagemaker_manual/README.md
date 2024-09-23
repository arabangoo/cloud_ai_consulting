[주피터 노트북 소개]

컴퓨터와 소통하기 위해서는 개발 환경과 언어가 필요하다. 
다양한 언어와 툴이 있지만 그중에서도 가장 많이 사용되는 언어는 '파이썬', 가장 인기 있는 개발 환경은 '주피터 노트북'이다. 
주피터 노트북은 '파이썬'을 비롯해 다양한 개발 언어로 코드를 작성해 프로그래밍 할 수 있는 개발 환경이다. 
주피터 노트북은 파이썬을 코딩할 때 주로 사용하며 단계적으로 코드를 실행할 수 있어서 문서화/시각화/분석에 용이하다.


프로그래밍 언어들 자체의 개발 환경이 있고, 또 다양한 개발 환경 플랫폼이 있지만, 
주피터 노트북을 많이 사용하는 이유는 웹 기반의 통합 개발 환경(IDE: Integrated Development Environment)이기 때문이다.
통합 개발 환경(IDE)은 프로그래밍에 필요한 툴들이 하나의 인터페이스에 통합되어 있는 개발 환경을 말한다.
주피터 노트북은 인터넷이 연결된 어느 컴퓨터에서나 웹 브라우저만 열면 접속 가능한 웹 기반 환경이다. 
그래서 어디서든 쉽게 사용 가능하다는 장점이 있고 게다가 오픈 소스라 무료이다.


주피터 노트북은 '노트북'이라는 명칭에 걸맞게 대화형 모드를 지원하기에, 
코드를 한 줄 입력하면 실행되는 결과를 즉시 확인할 수 있다. 
에러가 발생해도 문제의 코드를 바로 수정하고, 실시간 피드백을 반영하면서 다음 코드를 이어 나갈 수 있다.
주피터 노트북은 데이터 시각화에도 매우 용이하다. 
'마크다운' 기능으로 작성한 코드에 대해 설명을 추가할 수 있다. 
또, 데이터 분석이나 시각화에 활용되는 라이브러리를 사용해 불러온 데이터를 표, 그래프 등의 형태로 바로 시각화할 수 있다.
이런 편의성 때문에 주피터 노트북은 데이터나 공식에 대해 시각화가 필요한 데이터 사이언스는 물론, 머신러닝과 딥러닝 등 AI에도 많이 활용된다.
<img width="800" alt="image1" src="https://github.com/user-attachments/assets/58c59714-00a2-475d-9b8e-a4e2d864f191">


(1) 파이썬 설치 확인

윈도우 cmd 창에서 "py" 명령어를 입력했을 때 아래 이미지와 같이 나오면 파이썬이 설치된 것이다.
파이썬이 설치되어 있으면 주피터 노트북을 설치하기 위한 준비가 된 것이고 만약 파이썬이 설치가 안 되어 있다면 구글 검색 등을 통해 파이썬을 먼저 설치하자.
<img width="1600" alt="image2" src="https://github.com/user-attachments/assets/3855f7f9-e3c3-4ef4-b96d-0d2b5dcf6fcb">


(2) 주피터 노트북 설치

주피터 노트북을 설치하는 방법은 두 가지가 있다. 
하나는 cmd 창에서 설치하는 방법이고 하나는 아나콘다를 통해 설치하는 방법이다.
아나콘다를 통해 설치하는 방법은 아나콘다도 깔아야 하고 시간이 더 걸리기 때문에
여기서는 cmd 창에서 설치하는 방법을 설명하도록 하겠다.

윈도우 cmd 창에서 아래 명령어를 입력해 주피터 노트북을 설치하도록 한다.

명령어 : pip install jupyter
<img width="1600" alt="image3" src="https://github.com/user-attachments/assets/c4718cf4-d7b9-4e06-bbcd-4a76bda2acab">


(3) 주피터 노트북 경로 설정

설치가 완료되었다면 주피터 노트북 파일이 저장될 경로를 가정 먼저 설정해주어야 한다.
주피터 노트북을 실행할 때 경로를 입력하지 않으면 현재 경로를 기준으로 실행된다.
경로를 설정할 때는 아래의 명령어를 사용한다.
명령어 : jupyter notebook
특정 경로를 저장 위치로 설정하고 싶으면 아래와 같이 설정한다.
경로는 본인이 원하는대로 바꿔줄 수 있다.
명령어 : jupyter notebook --notebook-dir='C:\jupyter\notebook'
<img width="1600" alt="image4" src="https://github.com/user-attachments/assets/4da599f6-4da3-4511-9e92-61ff557b8647">

경로 설정을 하고 나면 얼마 지나지 않아 웹브라우저에서 주피터 노트북이 실행된다.
<img width="1800" alt="image5" src="https://github.com/user-attachments/assets/f4078b59-2eee-4633-9338-b59da1c9f256">


(4) 주피터 노트북 테스트

이제 주피터 노트북을 테스트 해보도록 하겠다.
"New -> Python 3 (jpykernel)"을 클릭해서 새로운 노트북을 생성한다.
<img width="1000" alt="image6" src="https://github.com/user-attachments/assets/a2d17ce6-5701-4fe4-9703-84d50842f4ca">

ChatGPT 등의 생성형 AI를 통해 주피터 노트북에서 실행할 게임 코드를 알려달라고 하고 주피터 노트북에 코드를 복사하자.
<img width="800" alt="image7" src="https://github.com/user-attachments/assets/8a4998f9-8b7a-47b6-9b0e-5fbedb44f88e">
<img width="600" alt="image8" src="https://github.com/user-attachments/assets/3528127f-fbe5-4a60-870e-6b45d5f7893d">

코드를 작성하고 실행할 때는 상단의 Run 버튼을 눌러도 되고, Shift+Enter(=Run)를 누르면 코드가 실행된다.
<img width="1000" alt="image9" src="https://github.com/user-attachments/assets/6f2a11cb-611f-4c87-805d-553f8c365459">
<img width="1000" alt="image10" src="https://github.com/user-attachments/assets/4e11ee8b-23c4-4616-a6bc-a8146a1fb6f0">
