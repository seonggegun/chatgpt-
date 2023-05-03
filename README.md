# Tweet을 활용한 ChatGPT 긍부정분석

## 1. 개요
- [배경](#배경)
- [목적](#목적)
- [방법](#방법)
- [결과](#결과)

<hr>

## Tweet이란?
트위터(Twitter)는 2006년에 시작된 미국의 소셜 미디어 플랫폼으로 사용자들이 280자 이내의 짧은 메시지를 공유할 수 있는 서비스입니다. 이를 "트윗(tweet)"이라고 합니다. 트위터는 누구나 회원가입을 통해 계정을 만들고 팔로우와 팔로워를 통해 다른 사용자들과 연결되어 소셜 네트워크를 형성할 수 있습니다.

트위터는 뉴스, 정보, 엔터테인먼트 등 다양한 주제에 대한 실시간 업데이트와 의견 공유가 가능하며 특히 글로벌한 대중과 쉽게 소통할 수 있는 장점을 가지고 있습니다. 최근에는 브랜드, 기업, 정치인 등 다양한 분야에서 마케팅, 홍보, 소통 등의 목적으로 활용되고 있습니다. <br>
<img src =https://user-images.githubusercontent.com/79897862/235725974-8031eb61-13dd-403f-9073-15529ad905af.jpg width="300" height="300">

## 트위터 여론조사 의미
트위터 여론조사는 트위터를 활용하여 일정 기간 동안의 특정 주제에 대한 사용자들의 의견을 수집하고 분석하는 것입니다. 이를 통해 특정 주제에 대한 대중의 인식과 태도를 파악할 수 있으며, 정치, 사회, 경제 등 다양한 분야에서 활용될 수 있습니다.

트위터 여론조사는 일반적인 여론조사와는 차이가 있을 수 있습니다. 트위터는 특정 성향이나 연령층 등의 그룹이 많이 사용하는 플랫폼이기 때문에, 해당 그룹의 의견이 과대표집될 수 있다는 한계가 있습니다. 또한, 트위터는 익명성을 보장하므로 일부 사용자들이 의견을 조작하거나 공격적인 의견을 제시하는 등의 문제가 발생할 수 있습니다.

하지만, 트위터 여론조사는 빠르고 실시간적으로 대중의 반응을 파악할 수 있다는 장점이 있습니다. 특히, 정치인이나 기업 등의 관심 주제에 대해서는 트위터를 통해 대중의 의견을 파악하여 이를 활용하는 경우도 많습니다.

<hr>

## 배경 
### 1.1 ChatGPT란?
ChatGPT는 대화형 인공지능 모델로서 OpenAI에서 개발됐습니다. ChatGpt는 자연어 처리 분야에서 매우 뛰어난 성능을 보이며 대화를 통해 사용자의 요구사항을 이해하고 적절한 응답을 생성합니다. 따라서 이 모델은 대화형 인터페이스, 챗봇, 자동 응답 시스템 등 다양한 분야에서 활용될 수 있습니다.

긍정적인 측면에서는 ChatGPT는 사용자와의 대화에서 매우 자연스러운 언어 처리 능력을 보이며 다양한 상황에서 적절한 대답을 제공하여 사용자 만족도를 높일 수 있습니다. 또한 이 모델은 대화를 통해 사용자의 선호도와 취향을 파악하여 맞춤형 서비스를 제공할 수 있다는 장점이 있습니다.

부정적인 측면에서는 ChatGPT가 생성하는 응답이 완벽하지 않을 수 있으며 때로는 사용자의 요구사항을 완전히 이해하지 못할 수도 있습니다. 또한 이 모델은 인간과의 대화에서 발생하는 감성적인 요소를 완벽하게 처리하지 못할 수도 있습니다. 이러한 한계를 극복하기 위해서는 모델의 향상이 필요합니다.

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
<img src= "https://user-images.githubusercontent.com/79897862/235815407-137068a4-29cc-4b9e-85f2-c94435081ba7.png"><br>

<img src="https://user-images.githubusercontent.com/79897862/234441500-29bdcfc8-9a64-4e9a-98db-bffcee53c021.png">

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

<img src =https://user-images.githubusercontent.com/79897862/235750530-4665d5cc-4993-4aa5-805e-5f4bc721917e.png width="300" height="300"> [출처2]

<br>

<img src =https://user-images.githubusercontent.com/79897862/235750669-9777233b-ab98-425b-b90e-a9b6f1e9a5c7.png width="300" height="300">

## 결과

<hr>

[출처1] <a href="https://twitter.com/EconomyApp/status/1622029832099082241">출처: App Economy Insights 트위터</a> <br>
[출처2] <a href="https://www.kaggle.com/datasets/charunisa/chatgpt-sentiment-analysis">출처 Kaggle </a> <br>
