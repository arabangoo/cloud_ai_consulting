![image1](https://github.com/user-attachments/assets/1068e438-ffca-4444-aad5-cb4df8c7d301)

Hugging Face(허깅페이스)란 자연어 처리, 이미지 생성모델, 컴퓨터 비전모델 등 다양한 도구와 라이브러리를 제공하는 곳이다.   
쉽게 말해서 다양한 인공지능 모델들을 오픈 소스로 제공하는 곳이라고 생각하면 된다.   
또한 간단한 파이썬 지식이 있다면 학습 모델들을 쉽게 사용해볼 수 있는 곳이라고도 할 수 있다.   
허깅페이스는 트랜스포머 기반의 다양한 모델들과 학습 스크립트를 구현해놓았다.   
기존의 트랜스포머를 학습시킨다고 하면 딥러닝 프레임워크를 선택하고 그에 맞게 구현을 해야했다.    
하지만 허깅페이스는 그런 함수들이 이미 정의 되어있기 때문에 간단하게 모델을 불러서 쓸 수 있다.    
즉, 따로 구현을 하지 않고 arguments를 줌으로써 편하게 사용이 가능하다.     
<br/><br/>     

1. 허깅페이스 가입하기
<br/>     
(1) 우선 허깅페이스 사이트에 들어가서 계정을 만들도록 하자.
<br/>

https://huggingface.co/
![image2](https://github.com/user-attachments/assets/f3de8983-4f31-41e0-8a14-4f9326d6d1d4)
<br/>
        
(2) 허깅페이스 계정을 만든 후 사이트 상단에 보이는 이메일 인증을 해준다.
"Resend confirmation email" 버튼을 클릭할 필요는 없고 가입시 등록한 이메일의 메일함을 보면 된다.
또한 Welcome 페이지에 나오는 리포지토리 생성 작업 역시 아직 할 필요없다. 
![image3](https://github.com/user-attachments/assets/4927a3f3-b792-4b5b-8a41-172fff8eaaff)
<br/>
        
(3) 이메일 인증까지 완료하면 아래와 같은 첫 메인 페이지를 볼 수 있다.
![image4](https://github.com/user-attachments/assets/bccf7ae0-5ed1-4c2b-9293-47253c36b2b6)
<br/>

(4) 상단의 "Models" 항목을 클릭하면 허깅페이스를 통해 사용 가능한 AI 모델을 볼 수가 있다.
가능한 경우 Hosted inference API를 활용해서 모델을 사용해 볼 수 있다.
![image5](https://github.com/user-attachments/assets/48c93d45-d700-4ec5-b61a-6f5ed8120a65)
<br/>

(5) 상단의 "Datasets" 항목을 클릭하면 허깅페이스를 통해 사용 가능한 데이터셋을 볼 수가 있다.
머신러닝에 활용할 수 있는 데이터셋을 확인할 수 있다. 위키, 뉴스, 웹 데이터 등 다양한 데이터들을 사람들이 올린다.
![image6](https://github.com/user-attachments/assets/2de5c12f-2104-489d-abd3-a17edc7fef6d)
<br/>

(6) 상단의 "Spaces" 항목을 클릭하면 커뮤니티에 의해 개발된 다양한 머신러닝 앱을 사용해 볼 수 있다.
![image7](https://github.com/user-attachments/assets/c27a86ea-7a29-4bb0-a706-bcb0030338d8)
<br/>

(7) Post는 유저들이 글을 작성하고 게시할 수 있는 공간이다.
![image8](https://github.com/user-attachments/assets/44d2fba1-e449-4e9f-9589-c2470e0f6b3e)
<br/>

(8) Docs는 항목별로 API 레퍼런스, 가이드 등이 카테고리별로 정리되어 있다. 
![image9](https://github.com/user-attachments/assets/34c2d1e3-03c8-46db-a746-d9c3cd058dc5)
<br/>

(9) 마지막으로 "HuggingChat"에 대해 알아보도록 하겠다.
맨 우측 상단의 세 줄 아이콘을 클릭하고 "HuggingChat"을 선택한다.
![image10](https://github.com/user-attachments/assets/09e6891a-5a88-49a0-a897-3637aa65de69)
<br/>

(10) 그러면 ChatGPT나 Claude 등에서 볼 수 있는 채팅창이 열리고 AI와 대화할 수 있다.
![image11](https://github.com/user-attachments/assets/d22d6385-f4bf-46e4-aeb1-8242b75567e1)
![image12](https://github.com/user-attachments/assets/e69be82d-9be1-4e5e-b674-7de11c5c4e32)
<br/>

(11) 좌측 항목에서 "Models"을 클릭하면 허깅페이스에서 자유롭게 쓸 수 있는 인공지능 모델을 선택할 수 있다.
![image13](https://github.com/user-attachments/assets/3b6fcaea-76d4-4b04-8467-c1577fa7643e)
<br/><br/>

2. 허깅페이스 기능 및 도구
<br/>      
(1) Transformers 라이브러리   
Hugging Face의 Transformers 라이브러리는 BERT, GPT-2, GPT-3, RoBERTa, T5 등 다양한 NLP 모델들을 제공하는 오픈소스 라이브러리다.       
이 라이브러리는 복잡한 AI 모델을 쉽게 사용할 수 있도록 설계되었으며 특히 자연어 이해(NLU), 자연어 생성(NLG) 작업에서 큰 성과를 내고 있다.       
Transformers 라이브러리는 수백 개의 미리 훈련된 모델을 지원하며 이를 특정 작업에 맞게 미세 조정(Fine-Tuning)할 수 있는 기능도 제공한다.       
예를 들어 사용자는 Transformers를 사용하여 텍스트 분류, 감정 분석, 번역, 텍스트 요약, 질문 답변 등의 작업을 손쉽게 수행할 수 있다.      
<br/><br/>

(2) Datasets 라이브러리   
AI 모델을 훈련시키기 위해서는 대규모 데이터셋이 필요하다.       
Hugging Face의 Datasets 라이브러리는 데이터셋에 쉽게 접근할 수 있는 도구를 제공하며 연구자들이 모델을 훈련시킬 수 있도록 지원한다.       
이 라이브러리는 텍스트, 이미지, 오디오 등 다양한 형식의 데이터를 빠르게 로드하고 전체 작업을 단순화한다.      
Datasets 라이브러리는 대규모 데이터셋을 효율적으로 처리할 수 있도록 설계되었으며, 데이터의 크기가 아무리 커도 원활하게 작동한다.       
또한, 데이터 증강(Data Augmentation), 샘플링, 전처리 등의 작업을 위한 다양한 유틸리티를 제공한다.      
<br/>

(3) Hugging Face Hub   
Hugging Face Hub는 AI 모델과 데이터셋을 공유하고 재사용할 수 있는 플랫폼이다.    
전 세계의 연구자와 개발자가 자신이 만든 모델을 업로드하고, 다른 사람들이 이를 활용할 수 있도록 허브 형태로 운영되고 있다.    
이를 통해 커뮤니티 내 협업이 활발히 이루어지며, 시기성을 빠르게 맞출 수 있도록 지원한다.   
Hub에 업로드된 모델은 다양한 작업에 맞도록 미리 훈련된 상태로 제공되며 모델 및 데이터 버전 관리, 권한 설정, 협업 도구 등을 지원한다.    
이를 통해 대규모 팀이 효율적으로 프로젝트를 관리할 수 있도록 돕는다.   
<br/>

(4) Inference API   
허깅페이스는 Inference API를 통해 실시간 AI 모델 제공 서비스를 운영하고 있다.    
이 API를 사용하면 복잡한 인프라 없이도 AI 모델을 즉시 배포하고 사용할 수 있다.   
예를 들어 웹 애플리케이션에서 실시간으로 텍스트를 번역하거나 감정 분석을 수행하는 등의 작업이 가능하다.   
Inference API는 다양한 프로그래밍 언어와 프레임워크에서 쉽게 통합될 수 있다.   
그리고 REST API를 통해 간편하게 호출할 수 있다.   
이는 특히 AI 모델을 웹 서비스나 모바일 애플리케이션에 통합하고자 하는 개발자들에게 유용하다.   
<br/><br/>

3. 허깅페이스 커뮤니티와 협력 활동     
(1) 허깅페이스의 성공 비결 중 하나는 강력한 오픈소스 커뮤니티이다.    
수많은 개발자와 연구자들이 이 플랫폼에 기여하고 있으며 서로의 지식을 공유하고 협력한다.   
허깅페이스는 GitHub와 같은 플랫폼을 통해 코드와 모델을 공유하며 이를 통해 커뮤니티가 공동으로 발전해 나간다.   
예를 들어 사용자는 새로운 모델을 훈련시키고 이를 Hugging Face Hub에 업로드하여 다른 사람들이 사용하도록 공유한다.   
<br/>

(2) 허깅페이스는 다양한 연구 기관 및 기업과 협력하여 AI 기술의 발전을 이끌고 있다.   
예를 들어 Google, Microsoft, Amazon과 같은 주요 기술 기업들은 허깅페이스의 라이브러리를 자사의 클라우드 플랫폼과 통합하여 고객들이 AI 모델을 더 쉽게 사용하도록 지원하고 있다.   
또한, 대학과 연구소와의 협력을 통해 새로운 모델 아키텍처나 훈련 기업을 개발하는데 기여하고 있다.
![image14](https://github.com/user-attachments/assets/ab4d01c4-dc4a-4475-94c0-8cef93a2632c)
<br/><br/>

4. Hugging Face의 활용 사례
<br/>
(1) 금융 업계 - 고객 서비스 자동화      
NLP 모델을 활용한 고객 지원 챗봇과 문서 분석 시스템을 개발하는데 사용된다.

이를 통해 고객 응대 속도를 높이고 문서 처리를 자동화할 수 있다.       
<br/>

BNP Paribas : 유럽의 대형 은행인 BNP Paribas는 Hugging Face의 NLP 모델을 사용해 고객 서비스 자동화를 구현했다.       
이를 통해 고객의 질문을 자동으로 처리하고, 맞춤형 금융 솔루션을 제공할 수 있었다.       
고객 만족도와 응답 속도가 크게 개선되었으며 고객 지원 팀의 효율성도 향상되었다.      
<br/>

(2) 의료 업계 - 의료 기록 분석   
환자의 의료 기록을 분석하여 진단을 지원하거나 환자와의 대화를 통해 건강 상태를 모니터링하는 시스템을 구축하는 데 활용된다.       
NLP 모델은 의료 데이터의 자연어 처리를 통해 의료 전문가의 의사 결정을 돕는다.      
<br/>

Roche : 글로벌 제약 회사인 Roche는 허깅페이스 NLP 기술을 활용해 의료 기록을 분석하고    
환자의 건강 상태를 모니터링하는 시스템을 개발했다.       
이를 통해 의료진은 환자의 상태를 실시간으로 모니터링할 수 있고 필요한 경우 신속하게 대응할 수 있었다.       
또한, 연구 개발 과정에서 중요한 데이터 인사이트를 도출할 수 있었다.   
<br/>

(3) 전자상거래 업계 - 제품 추천   
제품 리뷰 분석, 고객 피드백 분석, 상품 추천 등 다양한 작업에 Hugging Face의 모델이 사용된다.       
이를 통해 사용자의 경험을 개선하고 개인화된 서비스를 제공할 수 있다.      
<br/>

Shopify : Shopify는 허깅페이스의 모델을 사용하여 개인화된 제품 추천 시스템을 개발했다.      
이를 통해 사용자들이 검색하거나 관심을 가진 제품과 관련된 추천을 제공함으로써 구매 전환율을 높였다.      
AI를 통한 맞춤형 추천은 고객 경험을 향상시키고, 판매를 촉진하는데 중요한 역할을 했다.      
<br/>

(4) 전자상거래 업계 - 제품 추천   
교육용 챗봇, 학습 자료 분석, 온라인 학습 도구 등 다양한 교육용 애플리케이션에서 Hugging Face의 모델이 활용된다.      
AI를 통한 교육의 개인화와 자동화가 가능하다.      
<br/>

Duolingo : 언어 학습 플랫폼 Duolingo는 허깅페이스의 NLP 기술을 활용해 사용자 맞춤형 학습 경험을 제공한다.      
이를 통해 학습자의 수준에 맞는 문제를 제시하고 자연어로 피드백을 제공하여 학습 효과를 극대화하고 있다.
<br/><br/> 

5. 허깅페이스 비즈니스 모델과 가격 정책
<br/>      
(1) Hugging Face의 비즈니스 모델   
허깅페이스 비즈니스 모델은 프리미엄 서비스와 API 사용료가 있다.   
<br/>

프리미엄 서비스 : 허깅페이스는 기본적인 도구와 모델을 오픈소스로 제공하지만 기업 고객을 위한 프리미엄 서비스도 운영한다.   
이러한 서비스에는 맞춤형 모델 개발, 기술 지원, 클라우드 배포 옵션 등이 포함되며 기업의 요구에 맞춘 솔루션을 제공한다.   
<br/>

API 사용료 : 허깅페이스는 Inference API를 통해 AI 모델을 쉽게 배포할 수 있는 서비스를 제공한다.   
Inference API는 사용량에 따라 과금하는 방식으로 수익을 창출한다.   
이 API는 특히 웹 애플리케이션이나 모바일 애플리케이션에 AI 기능을 통합하려는 기업에게 유용한 도구이다.   
<br/>

(2) Hugging Face의 가격 정책   
Hugging Face는 다양한 사용자층을 고려한 유연한 가격 정책을 제공하고 있다.    
주로 오픈소스 라이브러리와 서비스는 무료로 제공되지만 기업 고객과 대규모 프로젝트를 위한 프리미엄 옵션도 마련되어 있다.    
<br/>

- 무료 플랜 :    
Hugging Face의 많은 기본 기능은 무료로 제공된다.    
특히, 오픈소스 라이브러리인 Transformers와 Datasets 라이브러리는 누구나 자유롭게 사용할 수 있다.    
이 플랜에서는 모델을 사용하거나 학습할 수 있으며 제한된 리소스로 서비스를 운영할 수 있다.
<br/>

- Pro 플랜 :    
프로 플랜은 월 $9 정도의 요금으로 제공되며 추가적인 API 호출량, 더 높은 성능의 모델 실행, 그리고 더 많은 데이터 처리 능력을 제공한다.    
이 플랜은 중소기업이나 팀 프로젝트에 적합하다.
<br/>

- 기업용 플랜 (Enterprise) :    
기업 고객을 위한 맞춤형 플랜으로 비용은 사용자의 요구 사항에 따라 변동된다.    
이 플랜은 전용 지원, 맞춤형 솔루션, 더 높은 수준의 보안, 그리고 무제한 API 호출을 포함한 다양한 혜택을 제공한다.    
가격은 고객과의 협의에 따라 결정된다.
<br/>

- Inference API :    
Inference API를 통해 실시간으로 AI 모델을 배포할 수 있으며 사용량에 따라 비용이 부과된다.    
이 API는 특히 웹 애플리케이션, 챗봇, 자동화된 시스템에서 실시간 AI 기능을 구현하는데 사용된다.    
가격은 사용량에 따라 다르며 일반적으로 API 호출당 몇 센트에서 수십 센트 사이이다.
<br/>

Hugging Face의 가격 정책에 관해서는 아래 공식 사이트에서 더 상세히 확인 가능하다.      
https://huggingface.co/pricing
![image15](https://github.com/user-attachments/assets/bd8b1c0b-20bf-4efc-9cfe-0a3c86680b6d)
<br/>
   
      
6. 허깅페이스 GitHub 리포지토리    
허깅페이스에서 제공하는 GitHub 리포지토리는 아래 링크에서 확인 가능하다.   
https://github.com/huggingface
<img width="1800" alt="image16" src="https://github.com/user-attachments/assets/3e0ea123-c4f1-4f5f-9b7d-3b84f36d6c30">
<br/><br/>

---
<br/>

## 구글 코랩에서 허깅페이스 사용
<br/>

이제 구글 코랩에서 허깅페이스를 사용해보도록 하자. 
<br/>
    
1. 허깅페이스에서 Access Token 발급받기      
(1) 우선 아래 링크에 접속해서 허깅페이스 토큰을 발급받도록 하자.      
https://huggingface.co/settings/tokens   
<img width="1000" alt="image1" src="https://github.com/user-attachments/assets/2edc5e10-7876-4f7c-b02c-cc722c8bc00f">
<br/><br/>

(2) 토큰 이름은 자유롭게 정하면 되고 권한은 "Read"를 선택한다.   
<img width="1000" alt="image2" src="https://github.com/user-attachments/assets/6a819b36-46fd-4a8b-b57b-d71fb3ad95f0">
<br/><br/>
         
2. 구글 코랩 환경 구성    
(1) 딥러닝 Open API를 사용하려면 코딩이 필요한데, 코딩을 하려면 파이썬이 치된 환경이 필요하다.      
구글이 만들어 놓은 코랩을 사용하면 파이썬으로 코딩을 할 수 있다.      
https://colab.research.google.com/?hl=ko      
<img width="1800" alt="image3" src="https://github.com/user-attachments/assets/cf343e66-a9db-4483-bd18-a7fb98c25f88">
<br/><br/>

(2) 우선 구글 계정으로 로그인 하면 계정 정보 옆에 네모 표시가 나타난다.   
하위 메뉴에서 "드라이브"를 선택해준다.   
![image4](https://github.com/user-attachments/assets/e321da5c-c18f-4bef-8a5f-04decc61e371)
<br/><br/>
    
(3) 드라이브 왼쪽 상단에 "+ New" 버튼을 누르면, 드라이브에서 사용할 수 있는 기능이 나오는데   
"더보기" 버튼을 눌러 "Google Colaboratory"를 클릭한다.    
만약 "Google Colaboratory" 메뉴가 보이지 않으면 이 앱을 추가해줘야 한다.   
"연결할 앱 더보기" 버튼을 클릭한다.   
"Colaboratory"를 검색한 후 설치를 진행한다.   
<img width="1000" alt="image5" src="https://github.com/user-attachments/assets/9940d2d9-388d-4932-9993-8539a9c243fa">
<br/><br/>
    
(4) 이제 다시 코랩 웹페이지로 돌아가서 새 노트를 만들어보자.   
https://colab.research.google.com/?hl=ko   
이제 파이썬 코드를 작성해서 실행할 수 있는 환경이 마련되었다.   
로컬 PC에 파이썬이 설치된 것은 아니고 가공간에 파이썬을 설치하고 사용권한을 받은 것이다.   
<img width="1800" alt="image6" src="https://github.com/user-attachments/assets/b206185d-e5c6-4701-ad25-0096cb24699c">
<br/><br/>
           
(5) hello world! 출력하기   
코 노트에 아래 문구를 입력하고 실행해보자.   
코드 : print("hello world")   
<img width="500" alt="image7" src="https://github.com/user-attachments/assets/a5cbdab9-2e96-41e6-8c38-34842d45f36c">
<br/><br/>

(6) 코랩 파이썬 버전 확인하기   
아래 명령어로 코랩의 파이썬 버전을 확인해보자.    
python 앞에 !(느낌표)를 붙이면, 명령 프롬프트에서 시스템 명령어를 실행하는 것과 동일하다.   
코드 : !python --version   
<img width="400" alt="image8" src="https://github.com/user-attachments/assets/8fdb3285-3156-40e1-b74a-bcb19040a3b8">
<br/><br/>

3. 구글 코랩에서 허깅페이스 사용하기      
(1) 우선 구글 코랩의 런타임 유형을 "T4 GPU"로 바꾸도록 한다.   
<img width="500" alt="image9" src="https://github.com/user-attachments/assets/752e75fe-1e9a-4445-bf80-707aa8efac0a">
<br/><br/>
    
(2) 구글 코랩에서 아래 코드를 입력하고 실행해보자.   
만약 코드에 기입된 모델이 더 이상 지원이 안 되면 다른 모델로 바꾸도록 하자.   
모델에 따라서는 허깅페이스 모델 페이지에서 사용 요청을 해야할 수도 있다.   
<img width="800" alt="image10" src="https://github.com/user-attachments/assets/80e0c9d9-567e-4ebc-8a06-8a5932472bca">

사용이 허락된 모델은 아래 링크에서 확인 가능하다.      
https://huggingface.co/settings/gated-repos   
<img width="800" alt="image11" src="https://github.com/user-attachments/assets/9f3691b7-210d-457d-a610-6ed8a4a5796e">
<br/><br/>

```python       
import os
import torch
import transformers
from transformers import AutoTokenizer, AutoModelForCausalLM, pipeline

# ==== Step 1: Securely Provide Your Hugging Face API Token ====
# 추천 방법: 입력을 통해 토큰을 안전하게 제공
hf_token = input("Enter your Hugging Face API token: ")

# ==== Step 2: Define the Model ID ====
model_id = "meta-llama/Meta-Llama-3.1-8B"

# ==== Step 3: Initialize the Tokenizer and Model with Authentication ====
try:
    # 토크나이저 초기화 (토큰을 'token' 파라미터로 전달)
    tokenizer = AutoTokenizer.from_pretrained(
        model_id,
        token=hf_token
    )
    
    # 모델 초기화 (토큰을 'token' 파라미터로 전달)
    model = AutoModelForCausalLM.from_pretrained(
        model_id,
        torch_dtype=torch.bfloat16,  # 하드웨어가 지원하지 않으면 변경
        device_map="auto",
        token=hf_token
    )
    
    print("모델과 토크나이저가 성공적으로 로드되었습니다.")
except Exception as e:
    print(f"모델/토크나이저 로딩 중 에러 발생: {e}")
    raise e

# ==== Step 4: Create the Text Generation Pipeline ====
try:
    text_gen_pipeline = pipeline(
        "text-generation",
        model=model,
        tokenizer=tokenizer,
        device_map="auto",
        torch_dtype=torch.bfloat16,
    )
    print("텍스트 생성 파이프라인이 성공적으로 생성되었습니다.")
except Exception as e:
    print(f"파이프라인 생성 중 에러 발생: {e}")
    raise e

# ==== Step 5: Define Your Prompt and Instructions ====
PROMPT = '''당신은 유용한 AI 어시스턴트입니다. 사용자의 질의에 대해 친절하고 정확하게 답변해야 합니다.
You are a helpful AI assistant, you'll need to answer users' queries in a friendly and accurate manner.'''

instruction = "대한민국의 관광지 5곳만 추천해달라."

messages = [
    {"role": "system", "content": f"{PROMPT}"},
    {"role": "user", "content": f"{instruction}"}
]

# ==== Step 6: Construct the Chat Prompt ====
def construct_chat_prompt(messages):
    chat_prompt = ""
    for message in messages:
        if message["role"] == "system":
            chat_prompt += f"System: {message['content']}\n"
        elif message["role"] == "user":
            chat_prompt += f"User: {message['content']}\n"
        elif message["role"] == "assistant":
            chat_prompt += f"Assistant: {message['content']}\n"
    # 어시스턴트의 응답을 유도
    chat_prompt += "Assistant: "
    return chat_prompt

chat_prompt = construct_chat_prompt(messages)
print("구성된 챗 프롬프트:")
print(chat_prompt)

# ==== Step 7: Define Terminators ====
# 생성 종료 토큰 정의
terminators = [
    tokenizer.eos_token_id,
    tokenizer.convert_tokens_to_ids("<|eot_id|>")  # 모델 따라 조정
]

# ==== Step 8: Generate the Response ====
try:
    outputs = text_gen_pipeline(
        chat_prompt,
        max_new_tokens=256,                 # 필요에 따라 조정
        eos_token_id=terminators,            # 생성 종료 토큰
        do_sample=True,                      # 샘플링 활성화
        temperature=1.0,                     # 무작위성 조절
        top_p=0.9,                           # 누적 확률 조절
    )
    
    # 생성된 텍스트 추출 및 출력
    generated_text = outputs[0]["generated_text"]
    response = generated_text[len(chat_prompt):].strip()
    print("\n생성 응답:")
    print(response)
except Exception as e:
    print(f"텍스트 생성 중 에러 발생: {e}")
    raise e
```
<br/>

(3) 모델과 instruction에 따라서 시간이 다소 걸릴 수도 있으니 30분 정도는 기다려보자.   
아래와 같이 답변이 출력되면 정상적으로 코드가 실행된 것이다.    
<img width="800" alt="image12" src="https://github.com/user-attachments/assets/be2727b4-cca4-43ab-a7d1-3fcaad75a630">
<br/><br/>

---
<br/>

