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
| count| `tweets` | `labels` |
| --- | --- | --- |
| 0 | ChatGPT: Optimizing Language Models for Dialogue https://t.co/K9rKRygYyn @OpenAI | neutral |
| 1 | Try talking with ChatGPT, our new AI system which is optimized for dialogue. Your feedback will help us improve it. https://t.co/sHDm57g3Kr	  | good |
| 2 | ChatGPT: Optimizing Language Models for Dialogue https://t.co/GLEbMoKN6w #AI #MachineLearning #DataScience #ArtificialIntelligence\n\nTrending AI/ML Article Identified &amp; Digested via Granola; a Machine-Driven RSS Bot by Ramsey Elbasheer https://t.co/RprmAXUp34 | neutral |
| 3 | THRILLED to share that ChatGPT, our new model optimized for dialog, is now public, free, and accessible to everyone. https://t.co/dyvtHecYbd https://t.co/DdhzhqhCBX https://t.co/l8qTLure71 | good |
| 4 | As of 2 minutes ago, @OpenAI released their new ChatGPT. \n\nAnd you can use it right now ?몙 https://t.co/VyPGPNw988 https://t.co/cSn5h6h1M1 |bad|
|... | ... | ... |
| 219289| Other Software Projects Are Now Trying to Replicate ChatGPT https://t.co/6TDsIUokBI | bad	 |
| 219290 | I asked #ChatGPT to write a #NYE Joke for SEOs and it delivered: \n\nWhy did the SEO make a resolution to eat healthier in the New Year? \n\nBecause they wanted to rank higher on Google's search results for 'healthy habits'! #SEO #NewYear | good |
| 219291 | chatgpt is being disassembled until it can only dissemble | bad	 |
| 219292 | 2023 predictions by #chatGPT. Nothing really specific, just some trends from the past years. \nShould be around this topic, we will see in 364 days ?럦 https://t.co/4ZD3kpH0DC | bad |
| 219293 | From ChatGPT, neat stuff https://t.co/qjjUF2Z2m0 | neutral	 |<br>

<img src=https://github.com/seonggegun/chatgpt-/assets/79897862/1eef6de5-a245-4f1d-9076-554219990a0a><br>
1. 2084개의 데이터 차이가 보이는데 그 이유는 저 원본데이터에서 긍부정 중립 라벨을 잘못해서입니다.<br> 그 잘못된 2084개의 데이터를 제거했고 neutral 데이터(54460개)를 제거할것입니다.<br>
2. oldlength는 원본데이터 텍스트 리뷰 길이에 대한 도수분포표입니다. <br> #, http:~, @ 와같은 태그와 링크글을 삭제할것입니다.
<hr>

## 데이터 전처리과정

<table style="width:100%">
  <tr>
    <th>전처리과정</th>
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
    <td>neutral, 이모지, 태그글, 링크글 제거</td>
    <td>엑셀,코렙</td>
</table><br>
1. 엑셀로 neutral 데이터및 잘못된라벨링 삭제. <br>
2. 코렙을 이용하여 이모지, 태그글, 링크글 제거.<br>

| count| `cleaned_tweets` | `labels` |
| --- | --- | --- |
| 0 | try talking chatgpt new ai system optimized dialogue feedback help u improve | good |
| 1 | thrilled share chatgpt new model optimized dialog public free accessible everyone	  | good |
| 2 | launched chatgpt new ai system optimized dialogue | good |
| 3 | chatgpt coming strong refusing help stalk someone agreeing providing someone waldo | good |
| 4 | deployed thing helping build last couple month chatbot based gpt really excited share vl |good|
|... | ... | ... |
| 146543 | implementation rlhf reinforcement learning human feedback top palm architecture basically chatgpt palm via | bad	 |
| 146544 | chatgpt banned stack overflow notice | bad |
| 146545 | indie medium today chatgpt ai bias hunter biden twitter censorship result jeffrey sachs nato biggest threat peace ukraine glenn greenwald call medium buffalo snowstorm update | bad	 |
| 146546 | software project trying replicate chatgpt | bad |
| 146547 | chatgpt disassembled dissemble | bad	 |<br>

<img src = https://github.com/seonggegun/chatgpt-/assets/79897862/d9fa101f-f76b-49ec-aa2f-49c8d102ae36>


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

## 결과 
<img src = https://github.com/seonggegun/chatgpt-/assets/79897862/3fe73401-0086-48c6-83f5-3c7b0f6cd95c>

<hr>

[출처1] 이 사진은 현재 ChatGPT이용자수를 보여주는 사진입니다.<a href="https://twitter.com/EconomyApp/status/1622029832099082241">출처: App Economy Insights 트위터</a> <br>
[출처2] <a href="https://www.kaggle.com/datasets/charunisa/chatgpt-sentiment-analysis">출처: Kaggle </a> <br>
