---
title: SSAFYcial) 0️⃣부터 시작하는 개발 Blog 생활 3화, 좀 더 세부적인 포스트 방법과 유용한 플러그인 소개!
keywords: [SSAFY, SSAFYcial]
tags:  [SSAFY, SSAFYcial]
summary: "SSAFYcial 기사 7호. 좀 더 다채롭게 포스트를 하고 싶은 당신에게"
sidebar: SSAFY_sidebar
permalink: SSAFYcial_07.html
folder: SSAFYcial
---
<a href="https://hits.sh/jsj0per.github.io/SSAFYcial_07.html/"><img alt="Hits" src="https://hits.sh/jsj0per.github.io/SSAFYcial_07.html.svg?style=for-the-badge&label=PostView&color=347DBE&logo=Perso"/></a>

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/ssafycial_series_header.png"/>
</div>

해당 포스트에 사용된 일부 삽화는 ChatGPT DALL·E 를 사용한 AI 그림임을 알려드립니다.  
또한 저를 형상화한 이모지는 삼성 AR 이모지를 이용하여 제작된 AI 이미지임도 알려드립니다.    

> 해당 포스트는 전 포스트에 이은 SSAFYcial 기획 시리즈 입니다.  
>> [0️⃣부터 시작하는 개발 Blog 생활 1화](https://jsj0per.github.io/SSAFYcial_03.html)
>> [0️⃣부터 시작하는 개발 Blog 생활 2화](https://jsj0per.github.io/SSAFYcial_05.html) 
>
> 또한 해당 포스트는 HTML과 Markdown를 기본적으로 이해하고있다는 전제하에 작성된 글입니다.  
> HTML은 단기간 숙달이 어려운 편이니 관련 강의를 찾아보시거나, [나무위키 HTML/태그](https://namu.wiki/w/HTML/%ED%83%9C%EA%B7%B8)문서를 참조해보시는 것을 추천드립니다.  
>
> 마크다운(Markdown, MD)는 아래 다른 기자분의 SSAFYcial 포스트를 참조하여 주신다면 해당 포스트를 이해하기 쉽습니다.  
>> [[Markdown] 마크다운, 그것이 알고싶다](https://memezz.tistory.com/20)

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_Hello.png"/>
</div>

안녕하세요!   SSAFYcial 13기 기자단 정승재 입니다.  
저번 포스트에 이어서 이번에도 Jekyll Blog를 운영하는 방법을 같이 공부해보도록 하겠습니다.  
저번 포스트에서 디렉토리 분석과 포스트 하는 방법에 대해서 같이 공부했습니다.

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_HMM.png"/>
</div>

다만, 분량상 디렉토리 소개와 포스트 소개를 같이 하려고 하다보니 그 포스트를 쓰는데 필요한 세부적인 기술들은 언급하지 못 한것이 아쉬워서,  
다음 시리즈 마지막인 검색 등록을 알려드리기전에 포스팅을 하는데 도움을 주는 세부적인 기능을 알려드리도록 하겠습니다.  
마지막까지 힘내서 같이 공부해볼 수 있는 시간을 가져보았으면 좋겠습니다!!  

## 포스팅에 사진 첨부하는 방법

깃허브 블로그는 사진을 올리는 방법이 크게 2가지가 있습니다.  
같은 깃허브 블로그 레포지토리에 보관하여 내부에서 가져와서 쓰는 것과, 외부 클라우드에 저장해서 가져와서 쓰는 방법이 있습니다.  
두 가지 방법에는 각각의 장단점이 있습니다.  

### 내부 레포지토리를 이용한 사진 첨부

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_01.png"/>
</div>

먼저 내부 레포지토리를 이용한 사진 첨부 방식을 소개해드리도록 하겠습니다.  
해당 방식은 레포지토리에 그냥 사진을 넣어두고, 경로에 맞게 링크를 걸어 사용하는 방식입니다.  

사진 경로는 가장 상위 레포지토리에 있다면 "/나 사진.png" 이런 식으로 올리면 되고,  
하위 폴더에 있다면 "/하위폴더 1/그 폴더의 하위 폴더 2/그 폴더의 그 폴더의 하위 폴더 3/나 사진.png" 이런식으로 링크가 걸린다고 생각해주시면 됩니다.  

해당 방식의 장점은 사진 로딩이 매우 빠릅니다.  
당연하게도 내부 레포지토리에서 직접 불러들이는 것이니 외부에서 불러들이는 것보다 훨신 빠르다는 장점이 있습니다.  

단점은, 깃허브 블로그 레포지토리는 1GB 이하로 레포지토리 용량을 유지하는 것을 권장하는만큼 너무 용량이 큰 사진을 집어넣다보면, 금세 레포지토리 저장소가 1GB를 초과해버린다는 단점이 있습니다.  

따라서 휴대폰이나 DSLR사진 같은 큰 용량의 사진을 저장하기에는 다소 무리가 있습니다.  
가벼운 용량의 사진이나 웹 캡쳐정도의 사진을 빨리 로딩하는 것이 중요하다면 깃 레포지토리를 이용하여 저장하여 그냥 쓰시면 된다고 생각됩니다.  

이 사진을 불러들이는 방법도 2가지가 있는데, 마크다운 문법으로 사진을 불러오는 방법이 있고, HTML 문법으로 사진을 불러오는 방법이 있습니다.  

위의 사진을 예시로 한다면,  

```markdown
![응애 나 사진](/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_01.png)
```

위 방식으로 올리는 방법이 마크다운 방식의 사진 첨부입니다.  

느낌표를 붙이고, []안에는 페이지에 출력될 사진의 이름(이름은 순전히 원래 사진명이 아니어도 됩니다.), ()안에는 사진 경로를 작성해주시면 됩니다.  
당연하지만 HTML 형식의 파일로 구성된 일부 Page 방식의 포스트에서는 작동하지 않고, .md 혹은 .markdown 형식의 파일만 사용할 수 있습니다.  
여기에 []와 ()를 더 붙힌다면...

```markdown
[![응애 나 사진 누르면 네이버로 넘어가](/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_08/SSAFYcial_May_01.png)](naver.com)
```
이런식으로 사진에 링크까지 걸 수 있습니다.  

매우 간단한 방식이지만, CSS 스타일을 적용할 수 없는 단점이 있습니다.  

```html
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_01.png"/>
```

이를 극복하기 위해서 있는 방식이 html 방식으로 첨부하는 것입니다.  
HTML문서는 물론이고, 마크다운에서도 활용이 가능한 문법으로, 해당 포스트도 대부분은 사진 중앙 정렬을 위하여 HTML 방식으로 사진을 첨부하고 있습니다. 
이 위에 div태그를 덧붙혀서 여러 CSS를 적용해서 다채롭게 사진을 조정하실 수 있습니다.  
저는 별다른 사진 조정이 필요없다면, 해당 방식으로 사진을 첨부하는 것을 권장드립니다.  
만약 사진에 링크를 걸고 싶다면,

```html
<a href="naver.com">
    <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_01.png"/>
</a>
```
이런식으로 링크를 걸면 앞서 했던 마크다운 사진 링크걸기처럼 링크를 걸 수 있습니다.  
이러한 부분은 HTML파트를 그대로 적용시키면 되니, 해당 부분은 따로 공부를 해두심이 좋을듯합니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_OK"/>
</div>  
물론 SSAFY에서도 HTML 파트를 가르쳐주니, 오셔서 배우시는 것도 하나의 방법이라고 생각됩니다.  

### 외부 클라우드 저장소를 활용한 사진 첨부

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_02.png"/>
</div>

구글 드라이드, 원 드라이브같은 클라우드 저장소에 사진을 저장하고 불러와서 사용하는 방법도 물론 가능합니다.  

앞서 언급하였듯, MB단위의 대용량 사진을 사용할 것이라면, 해당 방식이 가장 좋은 방법이라고 생각됩니다.  
외부 저장소를 사용하는 것이기에 용량 제한이 없기 때문입니다.  

다만 단점은, 내부 저장소를 쓰는 것 보다는 당연히 사진 로딩이 느린 편이며(특히, 용량이 더 클 수록 느립니다.), 서버 상태에 따라서는 엑박이 뜨는 경우도 간간히 보인다는 점이 단점입니다.  
만약, 이 점이 싫다 싶으시면, 용량이 큰 파일의 해상도를 변경하거나 품질을 살짝 열화시켜서 파일 크기를 줄여서 내부 레포지토리에 저장하는 것도 방법이라고 생각됩니다.

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_03.png"/>
</div>
저는 외부 레포지토리는 MicroSoft의 OneDrive의 사용을 권장하는 편입니다.  
OneDrive의 경우 블로그에 사용하기 좋도록 크기마저 조정해주어 자동으로 html코드를 만들어주는 임베딩 기능을 기본적으로 제공해주고 있어서, 딸깍딸깍만 하면 사진을 바로 첨부할 수 있는 코드를 만들어주는데, 
HTML코드로 만들기를 설정한후 그대로 붙여넣어주면 되기 때문입니다.  

물론 다른 클라우드 저장소를 사용하셔도 무방합니다.  

---

## 포스팅에 동영상 첨부하기

동영상은 가장 간단한 방법은 유튜브를 통해서 올리는 방법입니다.  
유튜브에 영상을 올리신 다음 아래 순서대로 따라주시면 됩니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_04.png"/>
</div>

유튜브 영상을 올리신 뒤, 영상에 직접 들어가보시면 아래 공유 버튼이 있습니다. 이를 누른 뒤...  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_05.png"/>
</div>

퍼가기 버튼을 누르시면 됩니다.  
그러면 iframe 형식으로 유튜브가 해당 영상에 대한 코드를 줍니다.

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_06.png"/>
</div>

그런 다음 해당 코드를 복사하거나, 밑에 복사버튼을 누른 뒤, 코드를 그대로 작성하실 포스트에 갖다 붙이시면 되는데, 만약 동영상의 출력해상도를 조정하시고 싶으시다면, 앞쪽의 width, height를 수정해주시면 됩니다.  

추천하는 해상도는 "560x315", "640×360(nHD)" "854x480(SD)", "960x540(qHD)", "1280x720(HD)" 까지만 권장드립니다. 너무 해상도가 커버리면 블로그에 최적화 되지 않을 가능성이 높기 때문입니다.

만약 플랫폼이 Youtube-Shorts(숏츠)라면 이러한 iframe 기능을 현재는 지원하지 않는 것을 알 수 있는데,  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_07.png"/>
</div>

```plaintext
https://www.youtube.com/watch?
```

해당 ?뒤에 빨간 박스안에 든 영상 코드를 붙여넣어서 일반 동영상으로 실행하여 위 과정을 똑같이 밟으면 iframe 코드를 가져올 수 있습니다.  

---

## 코드 스니펫 기능 추가하기.

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_OK.png"/>
</div>

깃허브 블로그는 Markdown 문법을 사용하는만큼 코드 스니펫 기능 또한 사용이 가능합니다.  
이 글을 보시는 분들은 개발을 목표로 블로그를 만드는만큼, 코드 스니펫 기능은 빼놓을 수 없는 꼭 필요한 기능이라는 점은 아실거라 생각됩니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_19.png"/>
</div>

엑센트 그레이브(` 억음부호)키를 3번 입력한 뒤, 뒤에 입력할 프로그래밍 언어를 입력한 뒤,  
다음 엑센트 그레이브 3개 전 사이에 원하는 코드를 집어넣으면 코드 스니펫이 완성됩니다.  
만약 markdown 코드를 입력하고싶다면 markdown, html을 입력하고 싶다면 html, python을 입력하고 싶다면 python을, 그냥 평범한 텍스트를 입력하고 싶다면 planetext를 입력하시면 됩니다.  

---

## 이외의 유용하고 간단한 플러그인 소개

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_HMM.png"/>
</div>

한 발자국 더 나아가서 포스팅에 유용한 기능을 소개해보도록 하겠습니다.  
깃허브 블로그는 다양한 플러그인들이 존재하여 이를 활용하여 여러가지를 해볼 수 있습니다.  
플러그인 종류는 많지만 이중 몇가지를 소개해보고자 합니다.  

---

### 슬라이더/캐로셀(Slider/Carousel)

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_08.png"/>
</div>

[참고: 캐로셀 플러그인 Docs](https://jekyllcodex.org/without-plugin/slider/)

저희가 설치한 NOCC에는 기본적으로 Carousel 플러그인이 설치되어있습니다.  
이 기능은 하나의 공간에 사진을 여러개 집어넣고 슬라이드 형식으로 볼 수 있게 만든 플러그인입니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_09.png"/>
</div>

만약 NOCC 테마가 아니라 해당 캐로셀 기능이 없으시다면 공식 문서에 들어가셔서, 
Installation의 Step 1.에 위치한 carousel.html을 눌러, 그대로 전체 내용을 복사하신 뒤,  
'_includes’ 폴더에 같은 이름으로 넣어주시면 적용 완료입니다.  

NOCC같은 이미 캐로셀이 설치되신 분들이라면 위에 부분은 건너뛰가 아래 사진부터 시작하시면 됩니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_20.png"/>
</div>
위의 YAML 머릿말(front-matter, 가장 앞쪽에 title, layout 등등이 있는 부분) 부분에 해당 부분을 입력하고,  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_21.png"/>
</div>

캐로셀을 넣고싶은 부분에 해당 코드를 집어넣으시면 됩니다.  
위 처럼 한다면 2개의 캐로셀이 적용될 것입니다.  
여러 개를 집어넣고 싶다면 위의 images: 밑 부분을 복사하여 똑같이 YAML 머릿말에 집어넣고,  
아래 include의 number를 1개씩 높혀가면 하나의 포스트에 여러개의 캐로셀을 집어넣을 수 있습니다.  

---

### 게시글의 조회수 기능 추가 ( HITS.sh )

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_10.png"/>
</div>

[HITS.sh 조회수 만들기](https://hits.sh/)

HITS를 이용하여 게시글에 조회수 기능도 만들 수 있습니다.  
왼쪽부분을 작성한 뒤, 오른쪽에 Markdown이나 HTML 코드를 복사해서 붙여넣으시면,  
게시글마다 조회수를 추가할 수 있는 기능을 제공해줍니다.  
만약 Navbar 등에 넣어두면 블로그 방문자 수 카운터로도 활약할 수 있기도 합니다.  

---

### 댓글 기능 추가 ( utterances )

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_11.png"/>
</div>

[utterances 댓글 플러그인](https://utteranc.es/)

깃허브 페이지도 댓글 기능을 추가할 수 있습니다.  
여러 댓글 플러그인들이 존재하지만 개인적으로 utterances를 추천하는 편입니다.  
가볍고, 간단하고, Github Id로 등록하여 사용하는 구조로 되어있으며, 광고가 없기 때문입니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_12.png"/>
</div>

먼저, [github app](https://github.com/apps/utterances)을 통하여 설치를 해야합니다.  
Install 버튼을 클릭합니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_13.png"/>
</div>

그 후, Only Select repositories를 선택한 후, 블로그 레포지토리로 설정하시면 됩니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_14.png"/>
</div>

repo에는 앞쪽에는 github 이름을 적고 / 뒤쪽에는 블로그 레포지토리 명을 집어넣습니다.  
제 예시대로라면 "SSAFYJUNGSJ/ssafyjungsj.github.io"가 될 것 같습니다.  

그 후 Blog Post <-> Issue Mapping은 어지간하면 "Issue title contains page pathname"으로 설정해주셔야 각자의 포스팅마다 댓글창이 독립적으로 달리게 됩니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_15.png"/>
</div>

이후 테마는 자신의 블로그 테마에 어울릴만한 적당한 테마로 설정하신 뒤, 아래 Copy를 눌러주시면 코드가 복사가 됩니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_16.png"/>
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_17.png"/>
</div>

이후 '_layout'폴더에 들어가셔서 'post' 파일에 적용시키면 됩니다.  
NOCC 기준으로 div class="divider"위가 가장 적당한 위치라고 생각됩니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_07/SSAFYcial_May_18.png"/>
</div>

이 상태로 저장하면 이렇게 포스트마다 댓글창이 생기는 것을 확인할 수 있습니다.  

---

## 마치며.

[Top Page](#)

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_THANKS.png"/>
</div>  
이번 기사에서는 Jekyll Blog의 포스트에 도움이 되는 포스팅 방법들과 플러그인 들을 같이 공부하는 시간을 가졌습니다.  
다음 포스트는 앞서 언급하였듯, 1학기 기획 포스팅 시리즈의 마지막으로 드디어 블로그 검색 등록을 해보는 시간을 가져보도록 하겠습니다.

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
