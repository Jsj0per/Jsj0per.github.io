---
title: SSAFYcial) 0️⃣부터 시작하는 개발 Blog 생활 4화, 검색 엔진에 블로그를 노출시키기.
keywords: [SSAFY, SSAFYcial]
tags:  [SSAFY, SSAFYcial]
summary: "SSAFYcial 기사 9호. 마지막으로 이제 검색 엔진에 내 블로그들을 등록시켜보자"
sidebar: SSAFY_sidebar
permalink: SSAFYcial_09.html
folder: SSAFYcial
---
<a href="https://hits.sh/jsj0per.github.io/SSAFYcial_09.html/"><img alt="Hits" src="https://hits.sh/jsj0per.github.io/SSAFYcial_09.html.svg?style=for-the-badge&label=PostView&color=347DBE&logo=Perso"/></a>

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/ssafycial_series_header.png"/>
</div>

해당 포스트에 사용된 일부 삽화는 ChatGPT DALL·E 를 사용한 AI 그림임을 알려드립니다.  
또한 저를 형상화한 이모지는 삼성 AR 이모지를 이용하여 제작된 AI 이미지임도 알려드립니다.    

> 해당 포스트는 전 포스트에 이은 SSAFYcial 기획 시리즈 입니다.  
>> [0️⃣부터 시작하는 개발 Blog 생활 1화](https://jsj0per.github.io/SSAFYcial_03.html)  
>> [0️⃣부터 시작하는 개발 Blog 생활 2화](https://jsj0per.github.io/SSAFYcial_05.html)  
>> [0️⃣부터 시작하는 개발 Blog 생활 3화](https://jsj0per.github.io/SSAFYcial_07.html) 
>
> 마크다운(Markdown, MD)는 아래 다른 기자분의 SSAFYcial 포스트를 참조하여 주신다면 해당 포스트를 이해하기 쉽습니다.  
>> [[Markdown] 마크다운, 그것이 알고싶다](https://memezz.tistory.com/20)

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_Hello.png"/>
</div>

안녕하세요!   SSAFYcial 13기 기자단 정승재 입니다.  
이제 어느 정도 블로그 글을 쓰고, 플러그인을 추가하는 방법을 알았으니,  
마지막으로 블로그를 검색엔진에 노출 시키는 방법을 알려드리겠습니다.

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_Rain.png"/>
</div>

1편에서 말했다시피 아쉽게도 github blog는 자동으로 검색 엔진에 노출되게 해주는 편리한 기능은 없기때문에, 우리가 직접 검색 엔진 봇이 내 사이트를 긁어갈 수 있도록 설정을 따로 해주어야 합니다.  
걱정하지 않으셔도 되는게, 생각보다 어렵진 않습니다.  

---

## Google 검색에 등록시키기 (Google Search Console)

[Top Page](#)

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_01.png"/>
</div>

먼저 서치 엔진 중에서 가장 중요한 구글 검색 엔진에 등록하는 방법입니다.  
구글 검색은 Google Search Console를 통해서 등록시킵니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_02.png"/>
</div>

Google Search Console에 들어가서 사이트를 등록시키는 과정을 거치려고하면,  
위 화면이 맞이해줄 겁니다.  
당황하지 마시고 오른쪽 부분에 **"https를 사용한"** 도메인 주소를 입력시켜 등록을 진행시킵니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_Rain.png"/>
</div>

**https로 등록하여야합니다. 이거 중요합니다.** Jekyll은 https를 통한 보안 페이지로 제공되기 때문에 http가 아닌 https 도메인으로 등록하여야 합니다. 만약 http로 등록을 하면 등록은 될 건데, 이후 세부 사이트 등록이 정상적으로 작동되지 않을 확률이 높습니다.  
이걸 왜 알고있냐 하면... 제가 이 실수를 저질러서 한 몇달을 삽질한 경험이 있기 때문입니다...  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_03.png"/>
</div>

우리 NOCC 테마는 config에 google search console 코드를 입력하면 별도의 페이지 없이도 자동 등록되도록 설정되어있기 때문에, 저희는 HTML 태그 부분을 활용할 예정입니다.  

HTML 태그의 1번에 복사 버튼을 클릭합니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_04.png"/>
</div>

그래서 복사해와서 config 파일에 붙여넣어보면 위 사진과 같이 html 코드가 적힐건데, 이 중에서 content 부분의 큰 따옴표 안의 코드를 복사하고 나머지는 지워버립니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_05.png"/>
</div>

그리고 그 복사한 부분을 google_site_verification 에 붙여넣고 저장하시면 됩니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_06.png"/>
</div>

그리고 잠시 기다리고 레포지토리가 github blog 서버에 deploy가 완료된다면, 별 문제가 없다면 위 사진처럼 소유권이 확인되었다며 이제 관리가 가능해지게 됩니다.  

이중에서 저희가 지금 볼 기능은 sitemaps 업로드 기능과 URL검사 기능입니다.  
사실 저희 포트폴리오용 기술 블로그를 운영할 예정이라면, 굳이 sitemap은 필수가 아니긴 합니다.  
일일이 수동으로 URL검사를 시켜서 등록 시켜도 정상적으로 검색 등록이 되기 때문입니다.  
하지만 sitemaps 를 이용하면 자동으로 검색 봇이 긁어올 수 있게 되기 때문에 편하기 때문에 일단 방법을 알려드리겠습니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_07.png"/>
</div>

sitemaps 부분에 들어오면 해당 페이지처럼 보여집니다.  
jekyll은 최상위 레포지토리에 sitemap.xml 형태로 사이트맵 파일을 제공해줍니다.  
만약 없다면, 수동으로 만들어 주시면 됩니다.  
NOCC 테마의 경우 이미 자동으로 페이지를 긁어올 수 있도록 sitemap.xml 파일이 프로그래밍 되어있습니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_08.png"/>
</div>

실제 "블로그 도메인.io/sitemap.xml" URL로 검색하면 위 형태처럼 sitemap 코드가 짜여져 있음을 알 수 있습니다.  

따라서 저의 예시의 경우 https://ssafyjungsj.github.io/sitemap.xml 이런 형태로 새 사이트맵 추가 부분에 입력시켜주시면 되겠습니다.  

구글 사이트맵 등록의 경우 최소 2-3주에서 최대 몇 달 단위까지 등록이 늦어지는 경우가 있을 수도 있고, 테마에 따라서는 사이트 맵 등록 자체가 안 되는 경우가 있을 수도 있습니다.  
실제로 제 메인 블로그는 현재 사이트 구조 문제로 인하여 사이트맵 등록이 안 되고 있어(이상하게도 구글 검색만 인식을 못 하고 있습니다. naver, daum, bing 은 인식 성공 상태) 이런 경우가 있을 수 있다 정도로 아시고 계시면 될 것 같습니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_09.png"/>
</div>

따라서 만약에 사이트맵 등록이 안 된다면 URL 검사로 일일이 수동으로 등록해주셔도 됩니다.  
웹 페이지 별 주소를 그대로 복사하여 하나하나 색인 요청을 하면 2-3주 정도 소요되어 등록을 시켜줍니다.  
다만 페이지가 SEO 최적화가 안 되었다면 크롤링된 페이지(즉, 정식 인증은 안 된 페이지)로 인식되어 검색 등록이 안 될 수 있습니다.  
만약 등록이 안 된다면 SEO 최적화 부분을 한번 살펴보는 편이 좋습니다.  
저도 구글 검색 부분은 아직 모르는 부분이 많아 계속 해당 문제를 접하는 경우가 꽤 잦아 해결 방법을 찾고있는 중이기도 합니다.  

### robots.txt

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_10.png"/>
</div>

이렇게 등록을 하였다면, 이제 google 검색 봇이 사이트를 찾을 계기를 등록시켰습니다만,  
아직 끝이 아닙니다.  
robots.txt라는 텍스트 파일을 생성하여야 본격적으로 봇이 해당 사이트를 긁기 시작합니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_11.png"/>
</div>

형식은 위 처럼 하면 됩니다.  
이렇게 적으면 구글의 서치봇인 GoogleBot이 내 사이트의 sitemap을 참조하여 가져오게 됩니다.  
만약 안 가져오고 싶은 부분이 있다면 Disallow를 등록시키면 됩니다.  

### 만약 config.xml에 google search console 코드를 적을 수 없는 테마라면?

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_12.png"/>
</div>

제 블로그처럼 config.xml에 코드를 등록시킬 수 없는 테마인 경우도 있을 수 있습니다.  
그런 경우의 google search console 등록 방법을 말씀해드리겠습니다.  
그런 경우라면 HTML 파일을 등록하는 방법으로 진행하시면 됩니다.  
먼저 해당 파일을 다운로드 합니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_13.png"/>
</div>

그 다음 블로그 레포지토리 최상위 디렉토리에 그대로 붙여넣어주시고,  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_06.png"/>
</div>

deploy가 완료된 후에 등록하면 위 화면처럼 등록 성공할 것입니다.  

---

## 네이버 검색 등록(Naver Search Advisor)

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_14.png"/>
</div>

네이버의 경우에는 Naver Search Advisor를 통하여 등록시킵니다.

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_15.png"/>
</div>

먼저, 등록하고자 하는 페이지의 주소를 입력합니다.  
마찬가지로 https페이지로 등록시켜야합니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_16.png"/>
</div>

마찬가지로 사이트 소유자 인지 증명을 하여야합니다.  
이번에는 HTML 파일 업로드 방식을 통해 등록시켜보겠습니다.  
먼저 빨간 네모가 쳐진 부분을 클릭하여 HTML 파일을 받습니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_17.png"/>
</div>

그런 다음 블로그 레포지토리의 최상위 디렉토리에 붙여넣고 deploy 시키면 사이트 등록이 완료됩니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_18.png"/>
</div>

마찬가지로 네이버 역시 sitemap을 등록시켜주시면 됩니다.  
제 개인적인 체감으로는 naver 쪽이 sitemap 인식률이 좀 더 높은 것 같습니다.  
동일하게 도메인 주소/sitemap.xml 방식으로 등록시켜주시면 됩니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_09/SSAFYcial_jun_19.png"/>
</div>

네이버의 경우 검색봇의 이름은 Yeti입니다.  
robots.txt 부분에 User-agent를 저렇게 설정하면 됩니다.  
마찬가지로 Disallow 하고싶은 부분이 있다면 따로 입력시켜주시면 됩니다.  

---

## 마치며.

[Top Page](#)

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_THANKS.png"/>
</div>  
이번 기사에서는 이제 완성된 블로그를 검색 엔진에 등록시키는 방법을 같이 배워봤습니다.  
물론 일반 블로그에 비해면 jekyll 방식의 github blog는 검색 등록이 꽤 까다로운 편에 속하는 것은 부정할 수 없는 사실입니다.  
하지만 그렇다고 아주 도전하기 어려운 정도의 난이도는 아니니, 블로그 완성이 되었다면, 꼭 검색 등록까지 연결시켜보는 시도를 해보는 것이 좋다고 생각됩니다.

현재로서는 기획 기사 "0부터 시작하는 개발blog 생활"은 여기까지가 할 예정이고, 이후 2학기 부터는 다른 기획 기사로 SSAFYcial 활동을 할 예정입니다.  
"그때도 모쪼록 잘 부탁드리겠습니다." 라는 말과 함께 이만 끝내도록 하겠습니다.  
읽어주셔서 감사드립니다.  

---

## SSAFY란?

[Top Page](#)

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_introduce_01.png"/>
</div>   
삼성청년SW·AI아카데미 ( Samsung SW·AI acdemy For youth ) 는 고용노동부의 취업지원 노하우와 삼성의 SW 교육환경을 바탕으로 아이들과 미래재단과 멀티캠퍼스에서 운영하는 청년들을 위한 소프트웨어 교육 부트캠프 입니다.  
각 전문분아별 자문 교수단과 삼성의 SW 전문가가 전공자와 비전공자, 마이스터고 학생들에게 SW 취업을 위해 최고 수준의 교육을 실시하는 프로그램입니다.

서울, 대전, 광주, 구미, 부산에 위치한 캠퍼스에서 파이썬, 자바, 임베디드, 데이터, 로봇, 모바일 트랙으로 나뉘어져 다양한 교육을 받을 수 있고,  
12개월이라는 다소 넉넉한 기간으로 많은 내용을 배울 수 있고, 전반기 코딩-알고리즘, 후반기 프로젝트 제작을 통하여 체계적으로 배울 수 있다는 장점을 가지고 있습니다.  

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_introduce_02.png"/>
</div>   
저 역시 국어국문학과 출신으로서 완전 비전공자로서 SSAFY의 혜택을 받아 교육을 받고 있고, 열심히 수업내용을 따라가고 있습니다.  
SSAFY는 단순한 코딩 교육뿐만 아니라, 기본 코딩을 바탕으로 컴퓨터 알고리즘, 팀원과의 협력, 다양한 포트폴리오 프로젝트 제작, 삼성에서 직접 고용하고있는 SW 전문 취업 컨설턴트님에게 취업 지원까지 받을 수 있는,  
삼성의 이름값만이 아닌 실질적으로 큰 도움을 받을 수 있는 탄탄한 지원을 바탕으로 취업을 정조준할 수 있습니다!

특히 알고리즘 수업을 통하여 코딩의 기초를 쌓을 수 있음과 동시에 기업 코딩 테스트를 천천히 대비할 수 있습니다.  
처음에 배웠던 언어인 파이썬, 자바를 계속 사용하면서 공부하기에 알고리즘 공부를 하면서 프로그래밍 언어에 대해 확실하게 사용할 수 있다는 자신감을 가질 수 있습니다.  

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_introduce_03.png"/>
</div>   
부트 캠프는 어렵다고 들었는데, 나는 따라갈 수 있을지 없을지 고민된다.  
프로그래밍은 배운적이 없는데 따라갈 수 있을지 고민된다.  
비전공자인데 코딩을 할 수 있을까 고민된다.  
저도 그런 고민을 많이 했지만, 실제로 SSAFY에서 수업 커리큘럼을 잘 따라가면서 개발자로서 차근차근 성장하고 있습니다.  
의지와 끈기만 가지고 도전한다면 비전공자든 전공자든 큰 차이 없이 성장할 수 있는 기회가 되실 수 있고,  
혹여나 어려움이 있더라도 프로패셔널한 강사님들과 든든한 동료들이 여러분의 고민을 같이 해주며,  
성장할 수 있는 기회이니 놓치지 마시고 꼭 도전해보시길 바랍니다!

> SSAFY 기자단 인스타그램(더 많은 기사를 볼 수 있는 곳)  
> [![SSAFYcial_Logo](/pages/SSAFYcial/SSAFYcial_img/ssafycial.png)](https://www.instagram.com/hellossafycial)

> SSAFY 공식 홈페이지  
> [![SSAFY_Logo](/pages/SSAFYcial/SSAFYcial_img/new_logo_ssafy.png)](https://www.ssafy.com)

![SSAFYcial_namecard](/pages/SSAFYcial/SSAFYcial_namecard_new.png)
