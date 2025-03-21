---
title: (제작중) SSAFYcial) 0️⃣부터 시작하는 개발 Blog 생활 1화, Jekyll로 개발 블로그를 만들어 같이 성장하자!
keywords: [SSAFY, SSAFYcial]
tags:  [SSAFY, SSAFYcial]
summary: "SSAFYcial 기사 3호. SSAFY 그냥 배우게? Jekyll와 github Page를 이용하여 개발 블로그를 만들어서 같이 성장하자!"
sidebar: SSAFY_sidebar
permalink: SSAFYcial_03.html
folder: SSAFYcial
---
<div style="text-align: center;">
  <img src="https://1drv.ms/i/c/0475b30c6541160c/IQSF5SO9oAv2Q52Kl45iMPucAc5qKrEfw9o1d1rro_vYZgo?width=1024" width="100%" height="auto"/>
</div>

해당 포스트에 사용된 삽화는 ChatGPT DALL·E 를 사용한 AI 그림임을 알려드립니다.  
또한 저를 형상화한 이모지는 삼성 AR 이모지를 이용하여 제작된 AI 이미지임도 알려드립니다.

<div style="text-align: center;">
  <img src="https://1drv.ms/i/c/0475b30c6541160c/IQQMFkFlDLN1IIAECgIAAAAAAZEcR1EUcRc0Ppn-iL8d9to?width=256" width="256" height="auto"/>
</div>

안녕하세요!   SSAFYcial 13기 기자단 정승재 입니다.  
저는 SSAFY를 하면서 동시에 개발 블로그를 운영하고 있습니다. 
특히 github의 github-page의 기능을 이용하여 호스팅을 하고, 정적 프레임 워크로 jekyll을 사용하고 있습니다.  

쉽게 말하자면 저는 jekyll라는 도구를 사용해서 블로그를 만들어서, github-page라는 땅을 임대해서 운영하고 있다고 말하면 쉽게 이해할 수 있으리라 생각됩니다.  

그래서 개발 블로그(IT 블로그)에 대해 소개하면서, 왜 개발 블로그를 만드는 것이 장점을 가지게 되는지 한번 소개해보려고 합니다.  

## 개발 블로그(IT Blog)

[Top Page](#)

<details style="text-align: center;">
  <summary><img src="https://1drv.ms/i/c/0475b30c6541160c/IQRzWWAk9hVFTI3dreGhiGqJAWbOuaUyZxGSh_XRHO3cNWU?width=1024" width="1024" height="auto" /></summary>
  <img src="https://1drv.ms/i/c/0475b30c6541160c/IQQxcGrtIKD-SrYUMWvG1lMwAZEMW4t48MuyjHeU3ejSM5k?width=1024" width="1024" height="auto" />
  <br>
  <a herf="https://www.canva.com/">[요약_사진_제공_Canva]</a>
</details>

<div style="text-align: center;">
  <img src="https://1drv.ms/u/c/0475b30c6541160c/IQTMexQZJduVQI6ctHVELpnPAWdoIWxA0OAPZ5UqVMc6LeM?width=400" width="400" height="auto" />
</div>  
> **블로그(Blog)**  
> 자신의 관심사에 따라 자유롭게 칼럼, 일기, 취재 기사 따위를 올리는 웹 사이트.  
> -표준국어대사전  

Blog라는 개념에 대해서는 많이들 알고 계시리라 생각됩니다.  
자신만의 간단한 홈페이지를 만들어 그 곳에 자기가 원하는 정보들을 올려 공유하거나,  
일상을 일기처럼 올려서 SNS처럼 이용하는 경우도 있습니다.  
최근에는 인플루언서가 되어 블로그를 이용해서 하나의 사업을 하시는 분들도 계십니다.  

<div style="text-align: center;">
  <img src="https://1drv.ms/i/c/0475b30c6541160c/IQQMFkFlDLN1IIAEDgIAAAAAASFyFuMJYg6NQVWp0_v-Baw?width=256" width="256" height="auto" />
</div>

그럼 그 Blog와 개발자와 무슨 상관 관계가 있는가?  
어떤 장점이 있는가?  왜 해야 하는가?  
의문점이 드실 수 있습니다.  

특히나 SSAFY에서 수업을 듣고계신 분들은 하루하루 수업 내용 따라가기도 바쁜데 왜 해야하는가?  
예비 SSAFY 지망생들도 지금 SSAFY에 들어갈 공부를 하기도 바쁜데, 또 다른 IT 지식으로 코딩 연습하기도 바쁜데,  
굳이 Blog까지 운영해서 시간을 할애해야하는가에 대한 의문을 가지실 수 있으리라 생각됩니다.  

이에 개발 블로그를 했을때의 이점에 대해서 설명해보고자 합니다.  

### 1. 공부 내용을 리마인드 할 수 있다.
<div style="text-align: center;">
  <img src="https://1drv.ms/u/c/0475b30c6541160c/IQQm05_pHk7wSoqAfQTik-Y8Aaosy2JzBw9Z06GWqIiD_NE?width=400" width="400" height="auto" />
</div>  
자기가 공부한 내용을 올리고 추후에 리마인드 할 수 있는 기회를 제공합니다.  
저같은 경우 제가 오늘 푼 알고리즘 문제를 기록하는 방식으로 활용하고 있습니다.  
물론 Notion 같은 메모, 문서 관리 등에 특화된 프로그램/사이트를 이용하는 것도 방법이며, 편하기도 합니다.  
그럼에도 개발 Blog만의 이점이 있는 이유는 다음 장점으로 연결됩니다.  

### 2. 포트폴리오 연계가 가능하다.  
<div style="text-align: center;">
  <img src="https://1drv.ms/u/c/0475b30c6541160c/IQTAisD0vJa6Qb_y6l8F3nWLAZgnLhfcO297sS2r4HH3z5U?width=400" width="400" height="auto" />
</div>  
요즘 IT회사들의 표준 규격 이력서에 blog가 있다면 적어달라는 곳들이 간간히 보이고 있습니다.  
이는 개발 블로그도 포트폴리오로 활용될 수 있는 좋은 수단 중 하나로 보일 수 있다는 증거로도 볼 수 있다고 봅니다.  
단순히 github 링크를 띄우는 것 보다 시각적으로, 또 요약하고 싶은 부분을 보여줄 수 있고, 자기가 강조하고 싶은 포인트롤  
강조해서 보여줄 수 있기 때문에 이 점에서는 유리하다고 생각됩니다.

### 3. 글 쓰는 능력을 기를 수 있다.
<div style="text-align: center;">
  <img src="https://1drv.ms/u/c/0475b30c6541160c/IQRsJ4zS_dD5TZwGCX7NlrNGAXK3cYpJfEy_djLX4nRT4Bg?width=400" width="400" height="auto" />
</div> 
블로그를 하려면 글을 계속 쓰게되고, '어떻게 쓰면 더 사람들에게 잘 받아들여질까?'를 고민하면서 쓰다보면,  
글을 계속 쓰게 되므로 어느정도 글쓰기에 대한 두려움을 줄일 수 있는 선택지가 될 수 있다고 생각됩니다.  
특히, 후에 프로젝트를 프레젠테이션 할 일이 있을 때, 어느정도 어떻게하면 확실하고 전달력있게 PT를 할 수 있을까 라는  
좋은 연습 교재가 될 수 있다고 생각됩니다.  

<div style="text-align: center;">
  <img src="https://1drv.ms/i/c/0475b30c6541160c/IQQMFkFlDLN1IIAEDAIAAAAAAZIhI_Z2cJAVt6NTwHRhnMU?width=256" width="256" height="auto" />
</div>  
위와 같은 이유들로 개발 블로그는 자기 개발과 취업적인 측면으로 봤을때,  
결정적인 수단이 되진 않더라도 선택지 중 하나가 될 수 있다고 충분히 생각할 수 있다고 보여집니다.  

## 개발 블로그 플랫폼 소개

[Top Page](#)

<div style="text-align: center;">
  <img src="https://1drv.ms/i/c/0475b30c6541160c/IQQMFkFlDLN1IIAEDgIAAAAAASFyFuMJYg6NQVWp0_v-Baw?width=256" width="256" height="auto" />
</div>  
그럼 개발 블로그를 하기 정했다면 플랫폼을 정해야하는데,  
정말 많은 플랫폼들이 존재하여 고르는 것도 고민이 될 듯 합니다.  
본문의 주제와 앞으로 시리즈로 나올 기사는 github-page를 이용한 jekyll에 초점을 둘 예정입니다만,  
이 글을 읽고계신 분들의 선택권을 위하여 전부는 아니더라도 유명한 몇가지를 소개를 해보고자 합니다.  

### 네이버 블로그(Naver Blog)

[Top Page](#)

<details style="text-align: center;">
  <summary><img src="https://1drv.ms/i/c/0475b30c6541160c/IQRzWWAk9hVFTI3dreGhiGqJAWbOuaUyZxGSh_XRHO3cNWU?width=1024" width="1024" height="auto" /></summary>
  <img src="https://1drv.ms/i/c/0475b30c6541160c/IQS4jHbcUPsLSr707B6VqihDAXBecWnAxm-Ev-VqDvVdslg?width=1024" width="1024" height="auto" />
  <br>
  <a herf="https://www.canva.com/">[요약_사진_제공_Canva]</a>
</details>
<br>
<div style="text-align: center;">
<img src="https://1drv.ms/i/c/0475b30c6541160c/IQSRW6sxoqjRRqp8TWelgdyxAZBqHd2rTTx-Awi_OIi0ruk?width=1024" width="1024" height="auto" />
</div>  
<br>
<div style="text-align: center;">
  <img src="https://1drv.ms/i/c/0475b30c6541160c/IQQdNNBXLsZjT4g03pvQO4gkAV6BixtypuwABmn9o-mt0RQ?width=256" width="256" height="auto" />
</div>  

블로그 화면 출처 : [SSAFYcial_13기_기자단_동료_블로그](https://blog.naver.com/iong_00)

우리 한국 사람들에게 가장 친숙하고 가장 익숙하고 가장 많이 노출되는 블로그입니다.  
초초초 메이저 블로그 플랫폼인 만큼 단순히 많은 사람들에게 노출시켜서 인플루엔서형 블로그를 지향하겠다고 마음먹었다면,  
가장 적은 노력을 들여서 높은 효과를 보일 수 있다는 특징을 가지고 있습니다.  

예전에는 개발자 블로그를 하기 위한 매우 유용한 코드 스니펫 기능(코드를 입력하여 IDE 탬플릿과 유사하게 입력창을 보여주며 복사도 간편한 기능)도 없었고 다른 기능들도 범용적인 블로그 운영에 초점이 맞춰지다보니 크게 선택받지 못하는 경향을 지녔습니다만,  
최근에 코드 스니펫도 추가되었고, 그래도 메이저하고 접근성 좋은 플랫폼이라 선택 메리트는 예전보다는 있다고 생각됩니다.

#### 장점
1. 타 플랫폼 대비 별 노력을 안 들여도 노출되기 쉽다.  
   네이버는 구글과 더불어서 대한민국 사람들이 가장 자주 사용하는 포털 사이트인 만큼 대중성 있으며, 큰 설정을 안 하더라도 네이버 자체 알고리즘이 게시글을 노출시켜줍니다.  따라서 robot.txt를 작성하느니, 서치 콘솔에 각각 일일이 등록시키느니 하는 별도의 SEO 작업 없이도 많은 사람들이 블로그를 방문할 수 있어 노출 효과가 큰 편입니다.
   
3. 낮은 입문 난이도.  
   학창 시절이나 다른 직업을 하면서, 혹은 취미로 지금에도 네이버 블로그를 하는 사람은 아직도 매우 많고, 어린아이도 조금만 공부한다면 금방 블로그 운영을 할 수 있을정도로, 관리 툴을 쉽고 직관적으로 제공하고있습니다.  또한 서버는 네이버에서 담당하기 때문에 별도로 서버비같은 돈이 나갈 필요없이 네이버 계정만 만들면 된다는 점은 큰 메리트입니다.  만약 블로그를 하고싶은데, 따로 공부하기 싫다 싶으면 좋은 선택지가 될 수 있다고 생각됩니다. 또한 포스팅 난이도도 쉬운게 깔끔한 포스팅 에디터 툴을 제공하고 있기 때문에 직관적이고 빠르고 생산적으로 글을 쓸 수 있다는 장점이 있다고 생각됩니다.  

#### 단점
1. 낮은 자유도.  
   이것저것 다양한 기능을 제공하는만큼 블로그를 이리저리 꾸밀 수 있는 자유도는 타 블로그 플랫폼들에 비해 떨어진다고 생각됩니다.  물론 그만큼 꾸미기 쉽고, 나름 DIY할만한 거리는 있지만, 그래도 꽤 제한적이라고 생각됩니다.  

2. 구글 애드센스 사용 불가. 
   > 네이버의 동의 없이 자동화된 수단에 의해 네이버 서비스 상에 광고가 게재되는 영역 또는 그 밖의 영역에 부호, 문자, 음성, 음향, 그림, 사진, 동영상, 링크 등으로 구성된 각종 콘텐츠 자체 또는 파일을 삽입해서는 안 됩니다. 또한, 네이버 서비스 또는 이에 포함된 소프트웨어를 복사, 수정할 수 없으며, 이를 판매, 양도, 대여 또는 담보로 제공하거나 타인에게 그 이용을 허락해서는 안 됩니다. 네이버 서비스에 포함된 소프트웨어를 역 설계, 소스코드 추출 시도, 복제, 분해, 모방, 기타 변형하는 등의 행위도 금지됩니다(다만, 오픈소스에 해당되는 경우 그 자체 조건에 따릅니다). 그 밖에 바이러스나 기타 악성 코드를 업로드하거나 네이버 서비스의 원활한 운영을 방해할 목적으로 서비스 기능을 비정상적으로 이용하는 행위 역시 금지됩니다.  
   > [출처](https://policy.naver.com/policy/service.html)
   
   수익화를 신경 안 쓴다면 상관 없다는 분도 계시지만(물론, 저 포함), 네이버 블로그는 자체 에드 서비스가 있어서 타 플랫폼 에드센스 사용이 불가능합니다.  에드센스를 붙이기 위한 기능을 제공하고 있지도 않고 억지로 하려해도 약관 위반이라 제재를 받을 가능성이 높습니다.  

3. 타겟층의 괴리감 문제.  
   네이버의 장점은 별 노력없이 검색창에 잘 노출된다는 점인데, 네이버 블로그 안에서 개발 블로그는 그렇게 주목도가 높은 편은 아니라고 생각됩니다.  단순히 개발 블로그가 마이너한 것만이 문제가 아니라 대부분 개발자 분들은 네이버 보다 구글을 압도적으로 많이 애용합니다.
   그런데 네이버 블로그의 글들은 구글 검색에 알고리즘 노출하기 꽤나 불편한 축에 속합니다.  안 뜨는건 아니지만 어느정도 자신의 의지로 뜨게 만드는게 꽤 힘든 편에 속합니다.  그래서 이러한 점을 고려한다면 네이버 블로그는 별로 좋은 선택이 아닌 편입니다.

### 티스토리 블로그(Tistroy)

[Top Page](#)

<details style="text-align: center;">
  <summary><img src="https://1drv.ms/i/c/0475b30c6541160c/IQRzWWAk9hVFTI3dreGhiGqJAWbOuaUyZxGSh_XRHO3cNWU?width=1024" width="1024" height="auto" /></summary>
  <img src="https://1drv.ms/i/c/0475b30c6541160c/IQQul699sUbfR6tQTQ5qh52tAeryxKRHyMsfqlyeiPrt8FA?width=1024" width="1024" height="auto" />
  <br>
  <a herf="https://www.canva.com/">[요약_사진_제공_Canva]</a>
</details>
<br>
<div style="text-align: center;">
<img src="https://1drv.ms/i/c/0475b30c6541160c/IQSPfnoTU4gaTYLEiAbg2gmdAWY-ERJ8__3DvrN8nTAmOeM?width=1024" width="1024" height="auto" />
</div>  
<br>
<div style="text-align: center;">
<img src="https://1drv.ms/u/c/0475b30c6541160c/IQQHNxUTFDQiSLaUzXskT4rVAVXPj1tBuG3ggPlxgz6p59I?width=256" width="256" height="auto" />
</div>  

블로그 화면 출처 : [SSAFYcial_13기_기자단_동료_블로그](https://0njung.tistory.com/)

과거에 네이버 블로그에 대한 대안 블로그로도 유명했고, 특히 높은 자유도로 매우 유명한 블로그입니다.  
과거에 많은 개발자 분들이 특히 애용했던 블로그이며, 최근에는 다른 블로그 플랫폼들이 많이 생겨 그쪽으로 옮겨가시는 분들이 많고, 아예 그쪽에서 시작하시는 분들도 많지만,  
많은 대안이 생긴 지금도 여전히 개발자 블로그 플랫폼 중에서는 상당히 메이저한 편에 속하고 있습니다.  

#### 장점
1. 높은 자유도와 쉬운 관리의 적절한 중간점.  
   티스토리는 네이버 블로그와 마찬가지로 기본적인 블로그 관리 툴을 제공하고 있어, 관리 난이도의 저점은 꽤나 높은 축에 속하며, 세세하게 파고들면 다양한 기능을 제공해줍니다.  긴 서비스 기간동안 쌓인 다양한 플러그인과 기능들이 축척되어있으며, HTML, CSS, Javascript등 프로그래머들이 자기 입맛대로 꾸밀만한 요소가 많습니다.  
   
2. 개발자들에게 특히 최적화가 잘 된 플랫폼.  
   티스토리는 SEO(검색 엔진 최적화)에 유리한 구조를 가지고 있어, 구글 검색 결과에서 잘 노출될 수 있습니다. 이를 통해 더 많은 사람들에게 블로그 내용을 공유할 수 있습니다. 따로 서치 콘솔들에게 올릴때도 가이드라인과 관리툴을 제공해주고있어, 쉽게 등록할 수 있습니다.  물론 무료로 서버를 제공해주고 있다는 장점뿐만아니라, 개인이 소유한 도메인을 등록시켜 블로그를 운영할 수 있다는 장점도 가지고 있습니다. 

#### 단점
1. 좀 공부해야하는 꾸미기 난이도.  
   물론 티스토리도 기본적으로 샘플 탬플릿을 제공해줍니다만, 갯수가 네이버 블로그에 비하면 많이 적어서, 사실상 본인이 직접 꾸며야 어느정도 특별함을 지닐 가능성이 큰데, 이를 꾸미려면 어느정도의 HTML, CSS, Javascript에 대한 지식을 요구합니다.  

2. 조금 어려운 블로그 관리.  
   티스토리는 기본적으로 사용자층이 얇은 편이라 SEO를 직접 발품팔아가며 설정해줘야 포스트가 잘 노출됩니다.  물론 SEO 난이도는 더 어려운 플랫폼들이 있어서, 그래도 티스토리 정도면 SEO에 대한 개념정도만 알면 적용시키기 쉬운 편입니다.  추가로 티스토리는 과도한 트래픽이 발생하면 서버에 가끔 무리가 가는 경우도 있습니다.  
