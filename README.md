# rnn(recurrent neural network)

## 자연어 처리란?
자연어(natural language) : 사람들의 사회생활에서 자연스럽게 발생하여 쓰이는 언어  
  - 컴퓨터에게 명령을 하기 위해 정제한 단어들과 반대되는 의미로 쓰임

자연어 처리(nlp) : 자연어를 그대로 컴퓨터로 처리하는 학문 분야  
  - 언어학적 측면 : 언어의 규칙성이나 변화 양상 등을 파악  
  - 전산학적 측면 : 자연어를 입출력으로 사용하는 컴퓨터 프로그램에 사용되는 처리과정

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

nlp 5 problems
ambiguity
exception
flexibility, extendability
paraphrase
similarity

자연어 처리가 어려운 5 가지 요인
언어의 중의성(ambiguity)
규칙의 예외(exception)
언어의 유연성과 확장성(flexibility, extendability)
바꾸어 말하기(paraphrase)
단어 간 유사도 측정(similarity)




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
