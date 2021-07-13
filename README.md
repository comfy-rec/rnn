# rnn(recurrent neural network)
nlp, nlu, nlg

## nlp(natural language process) : language -> computer -> language
chatbot
summarization
question answering
machine translation

## nlu(natural language understanding) : language -> computer
text classification
pos tagging
sentiment analysis
machine reading comprehension
named entity recognition
semantic parsing

## nlg(natural language generation) : computer -> language
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
