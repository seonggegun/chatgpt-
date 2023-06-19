# ChatGPT Tweet여론 긍부정분석 <img src =https://www.emoji.co.uk/files/emoji-one/animals-nature-emoji-one/1474-bird.png width="50" height="50">


## 목적
ChatGPT 긍부정 프로젝트의 목적은 tweet 데이터에서 긍부정을 분류하는 것입니다. 이 프로젝트를 통해 주어진 텍스트 데이터에서 긍부정을 분류할 수 있습니다. 이를 통해 자연어 처리 분야에서 긍부정 문장 분석을 보다 정확하게 수행할 수 있으며 이는 소셜 미디어에서 사용자들의 반응을 분석하거나 고객 리뷰를 분석하여 제품의 만족도를 파악하는 등 다양한 분야에서 활용될 수 있습니다.<br>

감성분석 프로젝트는 자연어 처리 분야에서 매우 중요한 주제 중 하나입니다. 이 프로젝트를 통해 tweet 텍스트 데이터에서 긍부정문을 분류하여 여론분석등을 할수있습니다.

<hr>

## Tweet이란?

<img src =https://user-images.githubusercontent.com/79897862/235725974-8031eb61-13dd-403f-9073-15529ad905af.jpg width="300" height="300">

트위터는 280자 이내의 짧은 메시지를 공유하는 미국 소셜 미디어 플랫폼으로, 다양한 주제에 대한 실시간 업데이트와 의견 공유가 가능하며 글로벌 대중과의 소통을 촉진하는데 활용되고 있다.


## 트위터 여론조사 의미
트위터 여론조사는 일정 기간 동안의 특정 주제에 대한 사용자들의 의견을 수집하고 분석하여 대중의 인식과 태도를 파악하는 것으로, 빠르고 실시간적인 반응 파악이 가능하나, 일부 그룹의 과대표집이나 익명성으로 인한 문제점이 있을 수 있다.
<hr>

## 배경 
ChatGPT는 자연어 처리 분야에서 우수한 성능을 보이는 대화형 인공지능 모델로, 사용자와의 대화에서 자연스러운 언어 처리 능력을 가지고 만족도를 높일 수 있습니다. 그러나 완벽하지 않은 응답 생성과 사용자 요구사항의 완전한 이해 부족이 있을 수 있습니다. ChatGPT는 정보 제공, 문제 해결, 개인화된 서비스 제공, 새로운 경험 제공 등 다양한 영향력을 가지고 있으며, 인공지능 기술의 발전과 함께 그 영향력은 계속해서 증가할 것으로 예상됩니다.<br>
<img src = https://github.com/seonggegun/chatgpt-/assets/79897862/6c590748-9596-4662-aa5d-32052e1a1d67 width="300" height="300">
<img src = https://user-images.githubusercontent.com/79897862/232948648-5797ee6e-9fde-4b28-bf5a-b000826cab6d.jpg width="300" height="300">[출처1]

<hr>

## 방법 
1 : kaggle에서 ChatGPT tweet여론 데이터 수집<br>
2 : 데이터 전처리<br>
3 : 수정데이터 학습<br>
4 : 입력을 통해 긍부정 예측<br>
<hr>

# 데이터

## 원시데이터
https://www.kaggle.com/datasets/charunisa/chatgpt-sentiment-analysis <br>
<img src= "https://github.com/seonggegun/chatgpt-/assets/79897862/5e65bc7f-c10e-4e17-bcc2-2f5484abbf72">[출처2](#출처2)<br>

<img src="https://github.com/seonggegun/chatgpt-/assets/79897862/a200f602-4ce2-42ad-a16a-5bd9629a4391"><br>
2084개의 데이터 차이가 보이는데 그 이유는 저 원본데이터에서 긍부정 중립 라벨을 잘못해서입니다.<br> 그 잘못된 2084개의 데이터를 제거했습니다.

<hr>

## 데이터 전처리과정
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

전처리 과정 그림판으로 그려넣을것 ex)성찬

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
이모지, 링크글, 잘못된 라벨링 제거 전처리<br>
<img src =https://github.com/seonggegun/chatgpt-/assets/79897862/f0f58557-cf29-40ee-9bbe-065e1edbd5cf><br>

<table style="width:100%">
  
  <tr>
    <th>데이터</th>
    <th>전처리 전</th> 
    <th>전처리 후</th>
  </tr>
  <tr>
    <td>good</td>
    <td>55027 </td>
    <td>52791</td>
  </tr>
  <tr>
    <td>bad</td>
    <td>106051</td>
    <td>93755</td>
</table><br>

## 결과

<hr>

[출처1] 이 사진은 현재 ChatGPT이용자수를 보여주는 사진입니다.<a href="https://twitter.com/EconomyApp/status/1622029832099082241">출처: App Economy Insights 트위터</a> <br>
[출처2] <a href="https://www.kaggle.com/datasets/charunisa/chatgpt-sentiment-analysis">출처: Kaggle </a> <br>
