# Tweet을 활용한 ChatGPT 긍부정분석 <img src =https://user-images.githubusercontent.com/79897862/235725974-8031eb61-13dd-403f-9073-15529ad905af.jpg width="50" height="50">


## 1. 개요
- [배경](#배경)
- [목적](#목적)
- [방법](#방법)
- [결과](#결과)

<hr>

## Tweet이란?
트위터는 280자 이내의 짧은 메시지를 공유하는 미국 소셜 미디어 플랫폼으로, 다양한 주제에 대한 실시간 업데이트와 의견 공유가 가능하며 글로벌 대중과의 소통을 촉진하는데 활용되고 있습니다. <br>
<img src =https://user-images.githubusercontent.com/79897862/235725974-8031eb61-13dd-403f-9073-15529ad905af.jpg width="300" height="300">

## 트위터 여론조사 의미
트위터 여론조사는 일정 기간 동안의 특정 주제에 대한 사용자들의 의견을 수집하고 분석하여 대중의 인식과 태도를 파악하는 것으로, 빠르고 실시간적인 반응 파악이 가능하나, 일부 그룹의 과대표집이나 익명성으로 인한 문제점이 있을 수 있습니다.
<hr>

## 배경 
### 1.1 ChatGPT란?
ChatGPT는 대화형 인공지능 모델로서 OpenAI에서 개발됐습니다. ChatGpt는 자연어 처리 분야에서 매우 뛰어난 성능을 보이며 대화를 통해 사용자의 요구사항을 이해하고 적절한 응답을 생성합니다. 따라서 이 모델은 대화형 인터페이스, 챗봇, 자동 응답 시스템 등 다양한 분야에서 활용될 수 있습니다.

긍정적인 측면에서는 ChatGPT는 사용자와의 대화에서 매우 자연스러운 언어 처리 능력을 보이며 다양한 상황에서 적절한 대답을 제공하여 사용자 만족도를 높일 수 있습니다.

부정적인 측면에서는 ChatGPT가 생성하는 응답이 완벽하지 않을 수 있으며 때로는 사용자의 요구사항을 완전히 이해하지 못할 수도 있습니다.

### 1.2 ChatGPT 영향력
현대 사회에서 인공지능 기술은 빠르게 발전하고 있으며 인공지능 챗봇인 ChatGPT도 그중 하나입니다.
ChatGPT는 다양한 분야에서 사용자들에게 정보를 제공하고 문제 해결에 도움을 주는 등의 기능을 수행합니다.
이를 통해 다음과 같은 영향력을 가지고 있습니다.
정보 제공 역할
문제 해결에 대한 도움
개인화된 서비스 제공
새로운 경험 제공
위와 같은 ChatGPT의 영향력은 계속해서 증가할 것으로 예상됩니다. 
<img src = https://user-images.githubusercontent.com/79897862/232948648-5797ee6e-9fde-4b28-bf5a-b000826cab6d.jpg width="300" height="300"> [출처1](#출처1)<br>
이 사진은 현재 ChatGPT이용자수를 보여주는 사진입니다.
<hr>

## 목적
ChatGPT 긍부정 프로젝트의 목적은 텍스트 데이터에서 감성을 분류하는 것입니다. 이 프로젝트를 통해 주어진 텍스트 데이터에서 감성을 자동으로 분류할 수 있습니다. 이를 통해 자연어 처리 분야에서 감성분석을 보다 정확하게 수행할 수 있으며 이는 소셜 미디어에서 사용자들의 반응을 분석하거나 고객 리뷰를 분석하여 제품의 만족도를 파악하는 등 다양한 분야에서 활용될 수 있습니다.<br>

감성분석 프로젝트는 자연어 처리 분야에서 매우 중요한 주제 중 하나입니다. 이 프로젝트를 통해 ChatGPT 모델을 사용하여 주어진 텍스트 데이터에서 감성을 자동으로 분류할 수 있습니다.

<hr>

## 방법 
1 : kaggle에서 ChatGPT tweet여론 데이터 수집<br>
2 : 데이터 전처리<br>
3 : 수정데이터 학습<br>
4 : 입력을 통해 긍부정 예측<br>
# 원시데이터소개
https://www.kaggle.com/datasets/charunisa/chatgpt-sentiment-analysis <br>
<img src= "https://user-images.githubusercontent.com/79897862/235815407-137068a4-29cc-4b9e-85f2-c94435081ba7.png">[출처2](#출처2)<br>

<img src="https://user-images.githubusercontent.com/79897862/234441500-29bdcfc8-9a64-4e9a-98db-bffcee53c021.png"><br>
2084개의 데이터 차이가 보이는데 그 이유는 저 원본데이터에서 긍부정 중립 라벨을 잘못해서입니다.<br> 그 잘못된 2084개의 데이터도 제거했습니다.

<hr>

# 데이터소개
<table style="width:100%">
  <tr>
    <th>일</th>
    <th>기술 설명</th> 
    <th>사용한도구</th>
  </tr>
  <tr>
    <td>데이터 수집</td>
    <td>kaggle에서 수집 </td>
    <td>kaggle</td>
  </tr>
  <tr>
    <td>데이터 전처리</td>
    <td>중립감성 제거, 이모지, http/https등 링크제거</td>
    <td>엑셀,코렙</td>
</table><br>

import pandas as pd
df = pd.read_csv('/content/sample_data/file3.csv',engine='python')
df (넣을것 오류뜸)

<table style="width:100%">
  <tr>
    <th>데이터</th>
    <th>구분</th> 
  </tr>
  <tr>
    <td>tweet</td>
    <td>글 내용 </td>
  </tr>
  <tr>
    <td>labels</td>
    <td>0(good),1(bad)으로 나눔</td>
</table><br>

<img src =https://user-images.githubusercontent.com/79897862/235750530-4665d5cc-4993-4aa5-805e-5f4bc721917e.png width="300" height="300">

<br>

<img src =https://user-images.githubusercontent.com/79897862/235750669-9777233b-ab98-425b-b90e-a9b6f1e9a5c7.png width="300" height="300">

## 결과

<hr>

[출처1] <a href="https://twitter.com/EconomyApp/status/1622029832099082241">출처: App Economy Insights 트위터</a> <br>
[출처2] <a href="https://www.kaggle.com/datasets/charunisa/chatgpt-sentiment-analysis">출처: Kaggle </a> <br>
