[Amazon 생성형 AI 서비스 베드락(Bedrock)]    
     
베드락(Bedrock)은 아마존이 ChatGPT의 대항마로 내놓은 생성형 AI 서비스다.   
ChatGPT 등의 생성형 AI를 이용해본 사람은 베드락에서도 비슷한 기능을 이용할 수 있다.  
다만 일반 사용자 입장에서는 편의성이나 기능이 ChatGPT가 압도적으로 좋다.   
본 문서는 베드락에 대해 참고 사항 수준으로 작성한다.  
  
  
1. 베드락은 사용 가능 리전이 제한되어 있다.   
사용하기 전에 먼저 사용 가능한 리전을 확인해본다.  
<img width="400" alt="image" src="https://github.com/user-attachments/assets/54f8127a-3a1d-4910-93fc-9bfe91c36897">
  
  
2. AWS에서 베드락 서비스로 들어간다.  
<img width="1400" alt="image" src="https://github.com/user-attachments/assets/8069c7c6-4fd0-4e2d-a353-521b0b3b656a">
     
    
3. 보통은 AI 모델에 대한 액세스 권한이 없다.  
AI 모델을 사용하기 위해서는 하단의 "모델 액세스"에서 액세스 권한을 요청해야 한다.  
![image](https://github.com/user-attachments/assets/ba486729-6fb4-4f1d-b15e-2e418a306c49)
  
  
4. "모델 액세스"에서 사용을 원하는 AI 모델을 선택하고 액세스 권한을 요청한다.  
엔트로픽 모델은 사용 사례 세부 정보를 제출해야 한다. (보통은 테스트용으로 기입하면 됨)  
다른 모델은 액세스 권한을 요청하면 바로 사용 가능하다.  
<img width="1400" alt="image" src="https://github.com/user-attachments/assets/64d715ec-9817-4ba1-86be-ab0bb718122c">
<img width="1800" alt="image" src="https://github.com/user-attachments/assets/3208cefb-a39b-48e7-bdc0-9e147aaf9313">
  
           
5. 이제 "플레이그라운드 -> 텍스트"에 들어가서 AI 모델을 선택하고 ChatGPT 등의 생성형 AI를 사용하듯이 AI와 소통해보자.  
<img width="1400" alt="image" src="https://github.com/user-attachments/assets/966491da-99bc-4c55-82f3-9139b0c3fcc9">
<img width="1400" alt="image" src="https://github.com/user-attachments/assets/1a250a03-c3a2-4edd-b0d5-a5dae67a1b99">
  
  
6. 이번에는 이미지 AI 모델을 이용해서 이미지를 생성해보자.  
텍스트 AI 모델과 비슷한 방식으로 이미지 AI 모델 액세스 권한을 요청하면 된다.  
여기서는 Amazon Titan 모델을 이용해보도록 하겠다.  
<img width="1800" alt="image" src="https://github.com/user-attachments/assets/32d455b2-442f-4418-bcd0-a855c2e8500d">
  
  
7. 이제 "플레이그라운드 -> 이미지"에 들어가서 AI 모델을 선택하고 ChatGPT, Bing 이미지 크리에이터 등의 이미지 생성형 AI를 사용하듯이 AI와 소통해보자.  
<img width="1800" alt="image" src="https://github.com/user-attachments/assets/84f3f5b0-9f00-46b3-a354-c14f5f1ae45f">
  
  
8. 한글로 명령어를 내리면 엉뚱한 이미지를 생성할 수도 있다.  
아직 한글 명령어가 제대로 실행되지 않는다는 뜻이니 영어로 바꿔서 명령어를 실행하자.  
<img width="1200" alt="image" src="https://github.com/user-attachments/assets/70945767-5a73-4383-b6e8-0212ab593291">
  
  
9. 영어로 명령어를 내리면 제대로 이미지를 생성하는 것을 확인할 수 있다.  
ChatGPT나 Bing 이미지 크리에이터에서 한글 명령어가 제대로 실행되는 점과 비교해보면 아직 베드락이 부족한 건 사실이다.    
<img width="1400" alt="image" src="https://github.com/user-attachments/assets/6c98ddd5-fdab-4119-a42e-9f793d294237">
  
  
10. 베드락은 AI 모델을 사용하는 경우에만 요금이 부과된다.  
요금은 많이 나온다고 볼 수는 없으나 여전히 편의성이나 기능만을 보면 일반 사용자 입장에서는 ChatGPT, Claude 등이 훨씬 낫다.    
![image](https://github.com/user-attachments/assets/0bb0810a-4eb5-43f3-a66c-ccb66f61c9ec)
<img width="1200" alt="image" src="https://github.com/user-attachments/assets/d6d773cd-734b-455c-9058-e9296d43069d">
  
  
---
  
  
AWS 콘솔이 아닌 파이썬 코드를 통해 로컬 PC나 윈도우 서버에서 베드락을 실행시키는 방법은 아래와 같다.  
해당 방법을 응용하면 베드락을 연동하여 별도의 웹 서비스를 구성할 수 있다.  
  
  
1. AWS 콘솔 Bedrock "모델 액세스"에서 사용을 원하는 AI 모델을 선택하고 액세스 권한을 요청하는 것은 동일하다.   
AI 액세스 권한이 없으면 로컬 PC에서 코드를 실행해도 동작하지 않는다.  
여기서는 텍스트 생성 작업을 테스트 할 예정이라 현재 가장 성능이 좋은 엔트로픽 클로드 모델을 선택하도록 하겠다.  
<img width="1400" alt="image" src="https://github.com/user-attachments/assets/caf007c9-3815-4c98-b4d9-edd8104741dc">  
  
  
2. 로컬 PC나 윈도우 서버 상에 아래의 파이썬 스크립트 파일(aws_ai_consulting/bedrock_test.py)을 작성해 놓는다.  
영어권 대학생들에게 블랙홀에 대해 설명하라는 내용이다.  
  
  
```python
import boto3
import json
brt = boto3.client(service_name='bedrock-runtime')

body = json.dumps({
    "prompt": "\n\nHuman: explain black holes to university student\n\nAssistant:",
    "max_tokens_to_sample": 500,
    "temperature": 0.1,
    "top_p": 0.9,
})

modelId = 'anthropic.claude-v2'
accept = 'application/json'
contentType = 'application/json'

response = brt.invoke_model(body=body, modelId=modelId, accept=accept, contentType=contentType)

response_body = json.loads(response.get('body').read())

# text
print(response_body.get('completion'))
```
  
  
AI 모델 ID의 경우 Bedrock 제공업체 항목에서 하단의 API 요청 부분을 보면 나와있다.  
코드를 작성할 때 AI 모델 ID를 기입해야 하는 경우 해당 부분을 참고해서 코드를 작성하면 된다.  
<img width="1800" alt="image" src="https://github.com/user-attachments/assets/fd25b974-5515-42cc-a46e-87eff14cd5dd">  
  
  
3. 윈도우 cmd 창에서 aws configure 명령어를 통해 적절한 권한이 있는 액세스키, 베드락 사용 리전, json 포맷을 등록한다.   
보통 액세스키에 AmazonBedrockFullAccess 권한을 주면 되나 해당 권한으로 안 되는 것이 있으면 다른 AWS 권한들을 추가해준다.  
  
  
4. 파이썬 스크립트 파일 내용을 살펴보고 필요한 모듈이 있다면 미리 설치해주자.  
boto3 등의 모듈이 없으면 pip install boto3 명령어로 모듈을 설치해주면 된다.  
  
  
5. 파이썬 스크립트 파일을 실행하기 위한 모든 모듈 설치가 완료되면 윈도우 cmd 창에서 python bedrock_test.py 명령어를 통해 베드락 AI를 호출해보도록 하자.    
<img width="1600" alt="image" src="https://github.com/user-attachments/assets/0d3adf09-c1ad-411f-aa92-33b9b3373ef7">  
