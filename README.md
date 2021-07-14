# rnn(recurrent neural network)

# 자연어 처리 소개 introduction to natural lagnuage process(nlp)
## 자연어 처리란?
자연어(natural language) : 사람들의 사회생활에서 자연스럽게 발생하여 쓰이는 언어  
    컴퓨터에게 명령을 하기 위해 정제한 단어들과 반대되는 의미로 쓰임

자연어 처리(nlp) : 자연어를 그대로 컴퓨터로 처리하는 학문 분야  
    언어학적 측면 : 언어의 규칙성이나 변화 양상 등을 파악  
    전산학적 측면 : 자연어를 입출력으로 사용하는 컴퓨터 프로그램에 사용되는 처리과정

## 자연어 처리의 응용 분야
언어학적인 활용 : 전산 언어학에서 언어를 분석하는 데 사용  
전산학적인 활용 : 기계번역, 음성인식, 개인비서 서비스, 날씨정보 요약, 인공지능 스피커 등

## 자연어 처리의 연구 분야
### nlp(natural language process) : language -> computer -> language
chatbot  
summarization  
question answering  
machine translation

### nlu(natural language understanding) : language -> computer
text classification  
pos tagging  
sentiment analysis  
machine reading comprehension  
named entity recognition  
semantic parsing

### nlg(natural language generation) : computer -> language
language modeling  
article generation

## 자연어 처리는 어렵다?
많이 알려진 것에 비해 정확도는 크게 높지 않다  
번역기가 많이 사용되어도 전적으로 번역기에만 의지하지는 않음  
개인 비서 서비스도 원하지 않는 응답을 많이 하여 사용률이 높지 않음

자연어는 숫자와 다르다  
숫자는 누가 보아도 항상 같은 상태를 가리킴  
언어의 특징 때문에 자연어 처리는 복잡하고 불확실

자연어 처리를 어렵게 하는 다섯 가지 요인 (nlp 5 problems)  
언어의 중의성 (ambiguity)  
규칙의 예외 (exception)  
언어의 유연성과 확장성 (flexibility, extendability)  
바꾸어 말하기 (paraphrase)  
단어 간 유사도 측정 (similarity)

### 언어의 중의성(ambiguity)
'배'에 담긴 의미들  
과일의 한 종류 : 배가 맛있다.  
운송 수단 : 배를 타고 간다.  
크기 비교의 단위 : 세 배는 더 재미있다.

영어의 'read', 한자 '行' 역시 두 개 이상의 의미를 찾을 수 있음  
read 는 뜻에 따라 읽는 방법도 다름

비꼬는 의미의 '참 잘 했다.' 역시 상황에 따라 여러 의미를 내포

완벽히 같은 글자의 조합이 여러 의미를 가지고 있음 : 처리의 복잡도가 상승

### 규칙의 예외(exception)
형태론 : 언어의 규칙을 연구하는 분야  
형태론이라는 학문 분야로 자리잡을 정도로 규칙이 어렵고 복잡

언어 규칙의 예  
-ed 로 끝나는 영어 동사는 과거형  
'보슬비'의 '보슬' : '바람없이 조용히 내리는'

숙어로 쓰인 동사나 명사는 원본 단어의 규칙을 그대로 적용할 수 없음  
"Hit the sack" : 잠들다  
"Hit the brown sack" : 갈색 자루를 때리다

규칙을 모든 단어에 그대로 적용할 수 없음 : 처리의 복잡도가 상승

### 언어의 확장성과 유연성(extendability, flexibility)
언어는 무한하다  
단어와 소리의 개수는 유한하지만, 이를 조합하여 만들 수 있는 문장의 수/길이가 무한함

구조 문법을 사용한 확장성의 이해  
문장의 여러 단어가 이루는 구조를 통해 문장이 구성된다는 문법 모델  
중의성을 완전히 해결할 수는 없지만, 언어의 확장성을 설명할 수 있음  
단어가 들어갈 자리에 구를 넣어서 문장의 길이를 계속 늘릴 수 있음  
man -> old man  
party -> party that she would also attend

언어의 유연성  
언어는 항상 변하며, 시대가 지나 더 이상 쓰이지 않는 단어도 있고, 새롭게 탄생한 용어도 있음  
새롭게 언어가 태어나는 방법도 다양  
이 모든 방법들을 규칙화 할 수 없음

### 바꾸어 말하기(paraphrase)
사진묘사  
남자가 기타를 치고 있다.  
남자가 기타를 친다.  
남자가 기타 연주를 하고 있다.  
남자가 앉아서 기타를 연주한다.  
어떤 남자가 기타를 이용하여 음악을 연주한다.

문장의 표현 형식은 다양하고, 비슷한 의미의 단어들이 존재하기 때문에 paraphrase 문제가 존재함

### 단어 간 유사도 측정(similarity)
이산적인 값을 갖는 자연어는 사람 입장에서 인지가 쉬울 수 있지만 기계 입장에서 매우 어려운 값

one-hot 인코딩으로 표현된 값은 유사도나 모호성을 표현하지 못한다.  
서로 다른 one-hot 벡터끼리 유사도 및 거리는 모두 동일  
예) '파란색'과 '하늘색' 중 '녹색'에 가까운 단어는 무엇인가?  
사람의 언어 체계는 계층적 구조를 가짐

높은 차원으로 표현되어 sparse vector 가 됨

딥러닝에서는 단어 임베딩(word embedding)을 통해 해결

## 한국어 자연어 처리가 어려운 이유
### 교착어
어근과 접사에 의해 단어의 기능이 결정되는 언어의 형태

형태론적 관점의 언어 분류  
교착어 : 한국어, 일본어, 몽골어 : 어간에 접사가 붙어 단어를 이루고 의미와 문법적 기능이 정해짐  
굴절어 : 라틴어, 독일어, 러시아어 : 단어의 형태가 변함으로써 문법적 기능이 정해짐  
고립어 : 영어, 중국어 : 어순에 따라 단어의 문법적 기능이 정해짐

접사 추가에 따른 의미 파생  
잡다, 잡히다, 잡히시다, 잡히셨다, 잡았다, 잡겠다, 잡겠더라, 잡혔다, 잡혔겠다, 잡히셨겠더라, ...

유연한 단어 순서 규칙  
"나는 밥을 먹으러 간다." 순서에 의한 다양한 변형  
나는 밥을 먹으러 간다. (o)  
간다 나는 밥을 먹으러. (o)  
먹으러 간다 나는 밥을. (o)  
밥을 먹으러 간다 나는. (o)  
나는 먹으러 간다 밥을. (o)  
나는 간다 밥을 먹으러. (o)  
간다 밥을 먹으러 나는. (o)  
간다 먹으러 나는 밥을. (o)  
먹으러 나는 밥을 간다. (x)  
먹으러 밥을 간다 나는. (x)  
밥을 간다 나는 먹으러. (x)

### 모호한 띄어쓰기
근대 이전까지 동양권 언어에서는 띄어쓰기가 존재하지 않음  
중세시대 서양에서는 띄어쓰기 확립됨

우리말은 아직 띄어쓰기 정착 단계  
전 국립언어원장의 고백 "띄어쓰기, 나도 자신 없다"

띄어쓰기는 어느 정도 틀려도 의사소통에 문제가 없기 때문

### 평서문과 의문문의 차이 부재 & 주어 부재
언어 : 평서문 : 의문문  
영어 : I ate my lunch. : Did you have lunch?  
한국어 : 점심 먹었어. : 점심먹었어?

### 한자 기반의 언어 & 단어 중의성
한자 기반의 언어  
한자(표의 문자) -> 한글(표음 문자)로 감싸 안음(wrapping)  
표의 문자 : 의미 또는 사물의 형상을 글씨로 표현  
표음 문자 : 사람이 말하는 음성, 소리를 글씨로 표현  
감싸는 과정에서 정보의 손실 발생  
茶 vs 車

단어의 중의성에 의한 문제  
'차'

### 어려운 한국어 자연어 처리
다른 문자에 비해 한글 체계는 늦게 만들어짐  
기존 다른 문자들의 장점을 흡수  
과학적인 원리

효율성을 극대화했기 때문에 한국어 자연어 처리는 더욱 어려움

## 자연어 처리 연구의 패러다임
### 규칙 기반 (rule-based)
언어의 문법적 규칙을 사전에 정의하고 이에 기반하여 자연어를 처리

초창기의 자연어 처리 연구에 많이 사용됨  
1954년 : 영어-러시아어 번역기 (IBM, 조지타운대학)  
1960년 : 대화형 시스템(SHRDLU ELIZA)

규칙 기반 자연어 처리 예시  
기계 번역 : 형태소 등의 단위로 문장을 분해하고, 그 사이에서 찾아낸 규칙을 사용하여 번역  
명령 인식 : 목적어와 동사 등이 문장에서 위치하는 규칙을 이용하여 대상과 행동 등을 이해

뚜렷한 한계가 존재하여 더 이상 사용되지 않음  
어순이 정형화되어 있지 않은 언어라면(한국어), 분석에 한계가 있음  
규칙을 미리 지정하는 것이 큰 부담  
규칙을 적용할 단위로 분해하는 작업의 정확도가 낮음

### 통계 기반 (statistical(word-based, phrase-based))
규칙 사전 정의를 통계적으로 처리  
어떤 규칙이 언어에 있다면 어구나 단어 사이에 통계적으로 유의미한 값이 도출된다고 가정

컴퓨터 성능이 발전하여 대량 데이터를 빨리 처리할 수 있게 되면서 발전함  
통계적 분석을 위해서는 사전에 수집된 대량의 문장들을(코퍼스) 처리해야 함

조건부 확률이라는 수학 개념이 가장 핵심  
어떤 사건이 이미 일어난 것을 가정하고, 그 상황에서 다른 사건이 일어날 확률  
어떤 단어가 나타날 확률을 앞뒤의 단어(들)을 기반으로 계산하는 것

통계 기반 분석의 한계  
복잡한 규칙을 처리하기 어려움  
여전히 사람 손이 많이 가는 통계 분석 자료를 활용함

### 딥러닝 기반(neural)
알고리즘(algorithm)  
(일반적인)알고리즘 : 어떤 상황에서 어떻게 어떤 값을 계산해야 하는 지를 사전에 지정한 연산의 흐름  
어떤 데이터가 들어올 지 예측이 가능해야 하고, 개발자 역시 그 처리법을 명확히 알고 있어야 함 (explicit)

기계 학습(machine learning)  
입력으로 들어올 데이터를 대입하여 알고리즘이 스스로 연산의 가중치를 학습하게 함  
프로그램 작성 후 바로 사용하지 않고 학습하는 과정이 필요 (train & inference)  
학습 완료된 가중치는 저장 후 나중에 다시 활용 가능

신경망(neural network)  
기계 학습 종류의 일종으로 신경계 구성 형태를 모티브로 만든 구조  
여러 입력에 가중치를 곱하여 합하고, 활성 함수에 통과한 후 전달  
입력, 출력을 제외한 층을 은닉층이라 함

딥러닝  
신경망 구조의 은닉층 수를 매우 많이 추가한 것  
은닉층 개수에 대한 정해진 기준은 없지만, 연산의 가중치나 흐름이 무엇을 의미하는 지 개발자 조차 알 수 없음  
하지만 여러 복잡한 특징을 처리하게 되어 각광받는 중

딥러닝 기반 자연어 처리  
모델을 구성하는 것이 중요함  
문장 전체를 고려하는 모델을 만들고 싶다면, 모든 단어에 적용되는 연결을 하나 만듦  
통계적 분석에 비해 고차원적인 분석이 가능해 자연어 처리의 성능이 비약적으로 상승함

## 딥러닝을 사용하는 자연어 처리의
### 딥러닝을 사용하는 자연어 처리의 연구 순서
어떤 목적으로 자연어 처리를 도입하는 것인지 결정 (task)  
목적과 관련한 코퍼스(자료) 구축 (data collection, preprocessing)  
코퍼스로 학습할 모델 구조 작성 (design)  
준비된 코퍼스를 이용해 모델 학습 (train)  
완성된 모델을 검증하고 실전에 투입 (inference)

주로 2, 3 단계에서 성능 개선 진행됨

### 단어 임베딩(word embedding)
자연어로 이루어진 문장을 컴퓨터가 입력 받을 수 있도록 하는 문장의 전처리 과정 (모델의 일부)  
다양한 방법이 존재하나, 단어간 연관성 등을 유지하는 벡터화 방법이 많이 쓰임  
문법적으로만 사용되는 단어는(조사, be 동사 등) 일반적으로 삭제  
사전에 임베딩된 단어 사전을 사용하여 연구를 진행하는 경우 많음

### 코퍼스, 모델
### 코퍼스(corpus)
매우 많은 문장을 정제하여 모은 것  
corpora(복수형)  
통계 기반 & 딥러닝 기반 자연어 처리에 가장 핵심인 자료

연구 필요성에 따라 문장 성분을 문장에 기입하거나 대응되는 번역문과 쌍을 구성하는 등, 연구에 사용할(모델이 학습해야 할) 정보를 함께 기입

포함된 언어 숫자에 따라  
monolingual corpus  
bi-lingual corpus  
multilingual corpus

parallel corpus : 대응되는 문장 쌍이 labeling 되어 있는 형태

### 모델(model)
딥러닝 기반 연구의 핵심  
연구의 목적에 맞게 모델이 어떤 부분을 읽고, 어떤 형식으로 출력하는 지 결정  
감정분석인 경우 분류(classification) 모델, 번역인 경우 생성(generation) 모델 등  
성능이 매우 좋은 모델은 출력 부분에 변화를 주어 다른 작업에 사용되기도 함 (transfer learning)

## 딥러닝을 사용하는 다른 연구 분야와 자연어 처리 비교
### AI 를 활용한 주요 분야
computer vision  
image recognition  
object detection  
image generation  
super resolution

natural language processing(nlp)  
text classification  
machine translation  
summarization  
question & answering

speech processing  
speech recognition (stt)  
speech synthesis (tts)  
speaker identification

reinforcement learning

data science

### 자연어 처리 vs 이외 분야
자연어 처리  
이산적인 값을 다룸 : 단어, 문장  
분류 문제로 접근 가능  
샘플의 확률 값을 구할 수 있음 : P(x=단어)  
문장 생성(자연어 생성) : auto-regressive 속성 지님, gan 적용 불가

다른 분야(예 : 컴퓨터 비전)  
연속적인 값을 다룸 : 영상, 음성  
문제에 다라 접근 방식이 다름  
샘플의 확률 값을 구할 수 없음 : P(x=영상)  
영상 생성 : auto-regressive 속성 없음, gan 적용 가능

### 자연어 처리의 필수 요건
언어적 지식 필요 (domain knowledge)  
예) 한국어의 언어적 특성은 무엇인가?

어려운 전처리 과정  
문제에 따른 정제 과정 필요







## requirements
google colab  
pytorch  
torchvision
pandas
numpy
selenium
beautifulsoup
openpyxl

## ex.py36.ipynb
pytorch tutorial, mnist data load

## py36.형태소분석+품사태깅.ipynb
konlpy package library  
Okt, Kkma, Hannanum, Komoran, Twitter, Mecab

## py36.RNN.mnist.ipynb

### datasets
mnist(28x28 images), 10 calsses

model
lstm
linear

loss
CEL cross entropy loss

optimizer
adam



0. Data 전처리.sms.p36.ipynb

data load
column
word length
duplicate
shuffle
train test split
save


1. RNN.sms.p36.ipynb

### datasets
sms data

model
lstm
linear
logsoftmax

loss
NLLLoss

optimizer
adam

## billboard_crawling.ipynb
selenium, chromedriver, beautifulsoup, openpyxl  
billboard chart crawling  
song_list, artist_list  
remove '\n'  
save 'billdata.tsv'
