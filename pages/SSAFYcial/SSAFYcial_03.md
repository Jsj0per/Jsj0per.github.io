---
title: SSAFYcial) 0️⃣부터 시작하는 개발 Blog 생활 1화, Jekyll로 개발 블로그를 만들어 같이 성장하자!
keywords: [SSAFY, SSAFYcial]
tags:  [SSAFY, SSAFYcial]
summary: "SSAFYcial 기사 3호. SSAFY 그냥 배우게? Jekyll와 github Page를 이용하여 개발 블로그를 만들어서 같이 성장하자!"
sidebar: SSAFY_sidebar
permalink: SSAFYcial_03.html
folder: SSAFYcial
---
<a href="https://hits.sh/jsj0per.github.io/SSAFYcial_03.html/"><img alt="Hits" src="https://hits.sh/jsj0per.github.io/SSAFYcial_03.html.svg?style=for-the-badge&label=PostView&color=347DBE&logo=Perso"/></a>

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/ssafycial_series_header.png"/>
</div>

해당 포스트에 사용된 삽화는 ChatGPT DALL·E 를 사용한 AI 그림임을 알려드립니다.  
또한 저를 형상화한 이모지는 삼성 AR 이모지를 이용하여 제작된 AI 이미지임도 알려드립니다.  
또한 글 작성에 ChatGPT의 도움을 일부 받은 게시글 입니다.  

해당 포스트는 GIT의 사용법을 알고있다는 전제하에 작성된 포스트로, Windows 환경을 기준으로 작성되었습니다.  
해당 내용을 잘 모르겠다면 아래 다른 SSAFYcial 게시글을 추천드리겠습니다.  
[SSAFYcial) #2. 개발자의 첫걸음, Git과 알고리즘으로 시작하기](https://blog.naver.com/imdg3530/223810097602)  
[SSAFYcial) 항해하기 위한 첫걸음 - 깃허브(GitHub) 알아보기](https://blog.naver.com/masterwayfinder/223627600291)  
[SSAFYcial) 자주 쓰는 "GIT COMMAND" 정리✍🏻 (기본편)](https://velog.io/@king_kang/SSAFYcial-%EC%9E%90%EC%A3%BC-%EC%93%B0%EB%8A%94-GIT-COMMAND-%EC%A0%95%EB%A6%AC)  
[SSAFYcial) 자주 쓰는 "GIT COMMAND" 정리👨‍👩‍👧‍👦 (협업편)](https://velog.io/@king_kang/SSAFYcial-%EC%9E%90%EC%A3%BC-%EC%93%B0%EB%8A%94-GIT-%EB%AA%85%EB%A0%B9%EC%96%B4-%EC%A0%95%EB%A6%AC)  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_Hello.png"/>
</div>

안녕하세요!   SSAFYcial 13기 기자단 정승재 입니다.  
저는 SSAFY를 하면서 동시에 개발 블로그를 운영하고 있습니다. 
특히 github의 github-page의 기능을 이용하여 호스팅을 하고, 정적 프레임 워크로 jekyll을 사용하고 있습니다.  

쉽게 말하자면 저는 jekyll라는 도구를 사용해서 블로그를 만들어서, github-page라는 땅을 임대해서 운영하고 있다고 말하면 쉽게 이해할 수 있으리라 생각됩니다.  

그래서 개발 블로그(IT 블로그)에 대해 소개하면서, 왜 개발 블로그를 만드는 것이 장점을 가지게 되는지 한번 소개해보려고 합니다.  

---

## 개발 블로그(IT Blog)

[Top Page](#)

<details style="text-align: center;">
  <summary><img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_06.png"/></summary>
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_05.png"/>
  <br>
  <a herf="https://www.canva.com/">[요약_사진_제공_Canva]</a>
</details>

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_01.png"/>
</div>  
> **블로그(Blog)**  
> 자신의 관심사에 따라 자유롭게 칼럼, 일기, 취재 기사 따위를 올리는 웹 사이트.  
> -표준국어대사전

Blog라는 개념에 대해서는 많이들 알고 계시리라 생각됩니다.  
자신만의 간단한 홈페이지를 만들어 그 곳에 자기가 원하는 정보들을 올려 공유하거나,  
일상을 일기처럼 올려서 SNS처럼 이용하는 경우도 있습니다.  
최근에는 인플루언서가 되어 블로그를 이용해서 하나의 사업을 하시는 분들도 계십니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_HMM.png"/>
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
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_02.png"/>
</div>  
자기가 공부한 내용을 올리고 추후에 리마인드 할 수 있는 기회를 제공합니다.  
저같은 경우 제가 오늘 푼 알고리즘 문제를 기록하는 방식으로 활용하고 있습니다.  
물론 Notion 같은 메모, 문서 관리 등에 특화된 프로그램/사이트를 이용하는 것도 방법이며, 편하기도 합니다.  
그럼에도 개발 Blog만의 이점이 있는 이유는 다음 장점으로 연결됩니다.

### 2. 포트폴리오 연계가 가능하다.

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_03.png"/>
</div>  
요즘 IT회사들의 표준 규격 이력서에 blog가 있다면 적어달라는 곳들이 간간히 보이고 있습니다.  
이는 개발 블로그도 포트폴리오로 활용될 수 있는 좋은 수단 중 하나로 보일 수 있다는 증거로도 볼 수 있다고 봅니다.  
단순히 github 링크를 띄우는 것 보다 시각적으로, 또 요약하고 싶은 부분을 보여줄 수 있고, 자기가 강조하고 싶은 포인트롤  
강조해서 보여줄 수 있기 때문에 이 점에서는 유리하다고 생각됩니다.

### 3. 글 쓰는 능력을 기를 수 있다.

<div style="text-align: center;">
   <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_04.png"/>
</div> 
블로그를 하려면 글을 계속 쓰게되고, '어떻게 쓰면 더 사람들에게 잘 받아들여질까?'를 고민하면서 쓰다보면,  
글을 계속 쓰게 되므로 어느정도 글쓰기에 대한 두려움을 줄일 수 있는 선택지가 될 수 있다고 생각됩니다.  
특히, 후에 프로젝트를 프레젠테이션 할 일이 있을 때, 어느정도 어떻게하면 확실하고 전달력있게 PT를 할 수 있을까 라는  
좋은 연습 교재가 될 수 있다고 생각됩니다.

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_OK.png"/>
</div>  
위와 같은 이유들로 개발 블로그는 자기 개발과 취업적인 측면으로 봤을때,  
결정적인 수단이 되진 않더라도 선택지 중 하나가 될 수 있다고 충분히 생각할 수 있다고 보여집니다.

---

## 개발 블로그 플랫폼 소개

[Top Page](#)

<div style="text-align: center;">
    <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_HMM.png"/>
</div>  
그럼 개발 블로그를 하기 정했다면 플랫폼을 정해야하는데,  
정말 많은 플랫폼들이 존재하여 고르는 것도 고민이 될 듯 합니다.  
본문의 주제와 앞으로 시리즈로 나올 기사는 github-page를 이용한 jekyll에 초점을 둘 예정입니다만,  
이 글을 읽고계신 분들의 선택권을 위하여 전부는 아니더라도  
일단은 운영시 비용이 들어가지 않는 유명한 플랫폼 몇가지를 소개를 해보고자 합니다.

### 네이버 블로그(Naver Blog)

[Top Page](#)

<details style="text-align: center;">
  <summary><img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_06.png"/></summary>
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_08.png"/>
  <br>
  <a herf="https://www.canva.com/">[요약_사진_제공_Canva]</a>
</details>
<br>
<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/naverblog_pic_01.png"/>
</div>  
<br>
<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/naverBlog_logo.png"/>
</div>

블로그 화면 출처 : [SSAFYcial_13기_기자단_동료_블로그](https://blog.naver.com/iong_00)

우리 한국 사람들에게 가장 친숙하고 가장 익숙하고 가장 많이 노출되는 블로그입니다.  
초초초 메이저 블로그 플랫폼인 만큼 단순히 많은 사람들에게 노출시켜서 인플루엔서형 블로그를 지향하겠다고 마음먹었다면,  
가장 적은 노력을 들여서 높은 효과를 보일 수 있다는 특징을 가지고 있습니다.  

예전에는 개발자 블로그를 하기 위한 매우 유용한 코드 스니펫 기능(코드를 입력하여 IDE 탬플릿과 유사하게 입력창을 보여주며 복사도 간편한 기능)도 없었고 다른 기능들도 범용적인 블로그 운영에 초점이 맞춰지다보니 크게 선택받지 못하는 경향을 지녔습니다만,  
최근에 코드 스니펫도 추가되었고, 그래도 메이저하고 접근성 좋은 플랫폼이라 선택 메리트는 예전보다는 있다고 생각됩니다.

#### 장점

1. 타 플랫폼 대비 별 노력을 안 들여도 노출되기 쉽다.  
   네이버는 구글과 더불어서 대한민국 사람들이 가장 자주 사용하는 포털 사이트인 만큼 대중성 있으며, 큰 설정을 안 하더라도 네이버 자체 알고리즘이 게시글을 노출시켜줍니다.  따라서 robot.txt를 작성하느니, 서치 콘솔에 각각 일일이 등록시키느니 하는 별도의 검색 등록 작업 없이도 많은 사람들이 블로그를 방문할 수 있어 노출 효과가 큰 편입니다.

2. 낮은 입문 난이도.  
   학창 시절이나 다른 직업을 하면서, 혹은 취미로 지금에도 네이버 블로그를 하는 사람은 아직도 매우 많고, 어린아이도 조금만 공부한다면 금방 블로그 운영을 할 수 있을정도로, 관리 툴을 쉽고 직관적으로 제공하고있습니다.  또한 서버는 네이버에서 담당하기 때문에 별도로 서버비같은 돈이 나갈 필요없이 네이버 계정만 만들면 된다는 점은 큰 메리트입니다.  만약 블로그를 하고싶은데, 따로 공부하기 싫다 싶으면 좋은 선택지가 될 수 있다고 생각됩니다. 또한 포스팅 난이도도 쉬운게 깔끔한 포스팅 에디터 툴을 제공하고 있기 때문에 직관적이고 빠르고 생산적으로 글을 쓸 수 있다는 장점이 있다고 생각됩니다.  

#### 단점

1. 낮은 자유도.  
   이것저것 다양한 기능을 제공하는만큼 블로그를 이리저리 꾸밀 수 있는 자유도는 타 블로그 플랫폼들에 비해 떨어진다고 생각됩니다.  물론 그만큼 꾸미기 쉽고, 나름 DIY할만한 거리는 있지만, 그래도 꽤 제한적이라고 생각됩니다.  플러그인 적용도 사실상 안 된다고 보는게 맞습니다.  

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
  <summary><img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_06.png"/></summary>
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_09.png"/>
  <br>
  <a herf="https://www.canva.com/">[요약_사진_제공_Canva]</a>
</details>
<br>
<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/Tistory_pic_01.png"/>
</div>  
<br>
<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/Tistory_logo.png"/>
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

2. 조금 어려운 블로그 노출 관리.  
   티스토리는 기본적으로 사용자층이 얇은 편이라 SEO를 직접 발품팔아가며 설정해줘야 포스트가 잘 노출됩니다.  물론 검색 등록 난이도는 더 어려운 플랫폼들이 있어서, 그래도 티스토리 정도면 SEO에 대한 개념정도만 알면 적용시키기 쉬운 편입니다.  추가로 티스토리는 과도한 트래픽이 발생하면 서버에 가끔 무리가 가는 경우도 있습니다.( 이 글을 읽어주시는 분들 중에서 정보를 찾기위해 어느 티스토리 블로그를 들어갔는데 로딩이 정말 정말 느리거나 아예 안 되는 경우를 경험해보신 분들이 계실거라 생각이 듭니다. )

### 벨로그(Velog)

[Top Page](#)

<details style="text-align: center;">
  <summary><img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_06.png"/></summary>
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_10.png"/>
  <br>
  <a herf="https://www.canva.com/">[요약_사진_제공_Canva]</a>
</details>
<br>
<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/velog_pic_01.png"/>
</div>  
<br>
<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/velog_logo.jpg"/>
</div>

블로그 화면 출처 : [SSAFYcial_13기_기자단_동료_블로그](https://velog.io/@develeep)

혜성같이 등장한 개발자 친화 블로그 플랫폼입니다.  
태생부터 개발자를 타겟으로 하고 나온 플랫폼이라 개발자 친화적인 편이며,  
매우 깔끔한 디자인과 낮은 운용난이도 덕분에 개발자 분들의 주력 블로그로 혜성같이 뜨고있습니다.  

#### 장점

1. 깔끔한 UI/UX와 쉬운 관리 난이도.  
   기본 제공 스킨들이 군더더기 없이 매우 깔끔한 편이며, 포스트 에디터는 개발자에게 매우 친숙한 마크다운 기반으로 작동되기 때문에 관리 난이도가 상당히 쉬운 편에 속합니다.  마크다운 언어만 활용할 줄 안다면 모든 블로그 플랫폼 중에서 관리 난이도는 가장 쉽다고 볼 수 있습니다.  
   
3. 개발자를 "타겟"으로 출시한 플랫폼.    
   태생부터 개발자 블로그 전문으로 등장한 플랫폼인만큼 벨로그는 코드 하이라이팅, Markdown 지원, GitHub 연동 등의 기능을 제공하여 개발자가 블로그에 기술적인 내용을 편리하게 작성할 수 있습니다. 또한, GitHub 계정으로 로그인할 수 있고 연동하기에도 꽤나 간편합니다.  

4. 빠르다.
   서버 리소스 자체를 적게 사용하는 경량화된 플랫폼이라 로딩속도가 매우 빠른 편에 속합니다.  벨로그를 운영중인 개발자님의 블로그를 들어가보면 코드를 리딩하기 위해 수초를 기다려야하는 경험은 하지 않아도 된다는 점이 장점입니다.  

#### 단점

1. 커스텀이 사실상 불가능.  
   벨로그는 기본적으로 제공되는 템플릿을 사용해야 하며, 다른 블로그 플랫폼에 비해 디자인 커스터마이징의 자유도가 낮습니다. HTML, CSS 등을 사용해 세밀한 디자인 수정이 불가능하여, 독특한 스타일을 만들기 어렵습니다.  

2. 조금 어려운 블로그 노출 관리.  
   티스토리랑 맥락을 같이하는 단점입니다.  역시나 검색에 노출이 되려면 별도로 검색 설정을 건들어야하는 부분이 있습니다.  벨로그 역시 이용층이 그렇게 두텁지 않기 때문에 사이트 내 이용자만으로는 조회수를 얻기 어렵습니다.  

3. 플러그인 자유도 없음.  
   벨로그는 수익화 기능이 제한적이어서, 구글 애드센스나 다른 광고 플랫폼을 통해 수익을 창출하기 어려울 수 있습니다.  또한, 기능 면에서 제약이 있을 수 있습니다. 다양한 플러그인이나 추가적인 기능을 활용하기에는 한계가 있어, 개발자 블로그에 필요한 모든 기능을 제공하지는 않습니다.

---

## Github-Page와 Jekyll로 블로그를 만들어보자!

[Top Page](#)

<details style="text-align: center;">
  <summary><img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_06.png"/></summary>
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_13.png"/>
  <br>
  <a herf="https://www.canva.com/">[요약_사진_제공_Canva]</a>
</details>
<br>
<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_11.png"/>
</div>  
<br>
<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/jekyll_logo.png"/>
</div>
본 주제로 돌아와서 저는 이제 jekyll과 github-page 기능을 이용하여 블로그를 만드는 법을 알려주고자 합니다.  
Jekyll은 프로그래밍 언어인 "Ruby"로 만들어진 정적 사이트 프레임 워크입니다.

정적 사이트 생성기는 미리 만들어진 정적 파일(HTML, CSS, JS 등등)을 기반으로 뚝딱 페이지를 만드는 방식이기 때문에, 모든 콘텐츠들이 미리 렌더링 되어 생성된....

라고 말하면 어려우니 쉽게 말하자면, 틀을 만들어 두고 그 틀에 맞게 움직이는 사이트라하면 이해하기 쉽습니다.  

<br>
<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_HMM.png"/>
</div>

이러한 정적 사이트 생성기의 종류로는 Jekyll(Ruby), Hugo(Go), Gatsby(React), Hexo(Node.js) 등이 존재합니다만, 그 중에서 왜 Jekyll를 사용하려는지에 대한 이유를 설명하고자 합니다.  

#### 1. Github에서 Jekyll를 사용하면 즉시 블로그를 호스팅해준다.

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_07_github_jekyll_upload.png"/>
</div>  
<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/github-page_logo.png"/>
</div>  
Github에서는 Jekyll 로 블로그를 작성한 뒤 레포지토리를 만들어 저장해두면, 즉시 블로그를 무료로 호스팅 해주는 파격적인 서비스를 제공해주고 있습니다. 추가로 SSL 인증서도 무료로 자동적으로 제공하고 있다는 점도 장점이라 볼 수 있습니다.  
물론 제약이 있긴 있습니다. 레포지토리는 1GB 내외까지만 제공해주고 있어, 그 이상의 용량을 보관하려하면 경고문구를 띄우고 있고, 단일 파일은 100MB를 넘을 수 없습니다.  
그래도 이 점을 고려하더라도 블로그 단위 혹은 포트폴리오 용 사이트 정도까지는 충분히 감수할만한 단점이라고 생각됩니다.

#### 2. 능력만 된다면 뭐든 가능한 매우 높은 자유도

상상하는 어떤거든 제작할 수 있다는 장점이 있습니다.  
페이지 전체의 헤더, 바디, 푸터의 하나하나까지 전부 html과 css로 다 뜯어고칠 수 있고, bootstrap이나 node.js 같은 외부 프레임 워크, 라이브러리, 개발 환경이랑 엮어서 다양한 기능도 구현할 수 있습니다.  
0부터 만들지 못하더라도 걱정할 필요가 없는게, 수년간에 거쳐서 쌓인 다양한 오픈소스 탬플릿들이 존재하여 해당 탬플릿을 기반으로 개조하는 것도 물론 가능합니다. 실제로 저의 블로그도 jekyll documentation theme를 기반으로 어느정도 개조하면서 사용하고있기 때문입니다.  
이 점이 중요한 것이 실제 프론트엔드 공부에도 꽤 큰 도움이 된다는 점을 꼽을 수 있습니다.  
단순히 프론트엔드를 부트캠프나 수업에서 연습하지 않으면 실력이 늘지 않는데, jekyll 블로그를 관리하다보면 직접 자신이 기능을 구현하기 위해 자신이 아는 지식으로 개조를 하게 되므로 학습에 꽤 큰 도움이 된다고 저는 생각합니다.  
실제로 SSAFY에서 배운 web 파트의 Javascript나 html, css 지식을 이용하여 블로그를 꾸미고 있다보니 최근 프론트 엔드 수업을 정말 재밌게 듣고있기도 합니다.  

#### 3. 개발자로서 메리트가 높은 블로그 운영방식.

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_12.png"/>
</div>  

앞의 1, 2번 장점을 합해서 생기는 장점입니다.  
Github-page를 이용하여 생성되는 블로그다보니 Github의 기능을 끌어와서 사용하기 쉬우며, 개발자로서의 지식을 접목시켜 하나의 포트폴리오로 승화시키기 적절한 탬플릿이라고 생각됩니다.  
물론 난이도는 결코 낮지 않습니다. 기본적으로 어느정도의 프론트엔드 지식이 있어야 꾸밀 수 있다는 점이 가장 큰 벽으로 느껴질 수 있습니다.  
하지만 흥미를 가지고 연구한다면 개발자로서 이만한 재밌는 장난감이 없을 정도로 다양하게 꾸밀 수 있다보니 자기 개발에 큰 도움이 됩니다.  
부가적인 장점으로 Github에 계속 push하면서 글을 쓰거나 작업을 하게되다보니, 매일매일 잔디를 심을 수 있다는 점도 재밌는 점입니다.

#### 4. 웹페이지 로딩이 빠르다.

기본적으로 정적 사이트 생성기이다보니, 블로그 사이트내 로딩이 꽤 빠릅니다.  정적 사이트 생성기란 웹사이트의 콘텐츠를 미리 생성하여 정적인 HTML 파일로 만들어 주는 프레임워크 이다보니 사전에 모든 페이지가 미리 생성되어 있기 때문에 서버에서의 렌더링 시간이 필요 없습니다.  
#### 5. 블로그 플랫폼 서비스 종료로 인한 불가항력에서 자유로움.  
github는 전 세계 개발자들이 제 1 옵션으로 GIT 배포용으로 쓰이는 메이저 사이트입니다.  거기에 뒷배로 마이크로소프트를 비롯한 다양한 대기업들이 서포트하고있고, 비즈니스적으로 대기업에서 1인개발자까지 모두가 쓰고있는 상태입니다.  
Github_page는 그 깃허브에서 서비스로 제공하는 옵션이기 때문에 운영적인 리스크에서 매우 자유로우며, 심지어 그 블로그 파일의 관리 주체는 블로그 운영자 본인이 되기 때문에 외부의 불가항력에 대해서 꽤 자유롭습니다.  템플릿을 가져와서 사용한다고 해도 한번 가져온 시점에서 그 템플릿은 관리 주체가 블로그 운영자로 변하기 때문에 걱정할 필요도 없습니다.  
따라서 종합적으로 사이트 서비스 종료 걱정에서 매우 자유로운 편입니다.  만의 하나의 경우에 그 불가항력이 찾아온다해도 그냥 파일 전체를 다운로드시켜 백업처리하여 다른 호스트 플랫폼을 찾을 수 있기때문에 불가항력에 대한 대비도 훌륭한 편입니다.  
 
<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_OK.png"/>
</div>  
위의 장점들이 있기 때문에 저는 jekyll 블로그 방식으로 개발 블로그를 운영중이며,  
현재까지도 SSAFY 생활을 즐기면서 재밌게 가꿔나가고 있습니다.

---

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_Rain.png"/>
</div>

물론, jekyll 블로그의 단점도 꽤 많습니다.  

#### 1. 일단 어렵다!

일단 프론트엔드 지식이 없으면 굉장히 힘듭니다.  
저도 처음에 탬플릿을 복사한 뒤 옮겨서 운영을 할려고하니 관련 지식이 아무것도 없는 상태에서는 도무지 손을 댈 수 없었습니다.  
기본적으로 HTML과 Markdown, CSS, Javascript에 대한 지식을 요구하며, 추가로 jekyll 사이트 내에서 jekyll 만의 구조와 명령어를 하는 것에 어느정도 시간과 노력을 할애하여야 합니다.  
저도 SSAFY에 들어온 뒤 관련된 지식을 배우고 나서야 jekyll를 어느정도 다룰 수 있게 되었으며, 솔직히 이 기사를 쓰는 시점에서도 이 jekyll의 모든 기능과 탬플릿 내 코드들을 전부 해석하고 파악하고 있지 않아서 계속 공부하고 있습니다.  
거기에 탬플릿에 따라선 bootstrap, Typescript 등 다른 언어나 외부 프레임워크들을 활용했을 경우, 추가로 그 프레임워크에 대한 지식도 요구합니다.  

#### 2. SEO도 신경 써줘야한다!

다른 블로그 플랫폼은 어느정도 검색 노출 기능을 툴로 보조해주거나 아예 사이트에서 자제적으로 SEO 구조를 자동적으로 설정해주는 경우도 있습니다.  
하지만 Github-page 기능을 통해서 블로그를 호스트했다면, 웹사이트 내 SEO구조도 잡아줘야하고 검색 등록도 수동으로 하나하나 다 해줘야합니다.  
사실상 앞서 언급했던 블로그들과 비교하면 검색 등록 난이도는 제일 높다고 봐도 과언이 아닙니다.  
탬플릿에 따라서는 새로운 포스트를 올리면 sitemap도 추가 설정을 해줘야 합니다.  
거기에 SEO 최적화도 자동으로 해주지 않기 때문에 관리를 할때 신경쓰면서 관리해야합니다.

#### 3. 손이 많이 갑니다.

포스트 에디터 같은 편리한 기능은 없습니다.  
모든 포스트는 github를 통해서 일일히 push하면서 업데이트 해야하고, 
앞서 언급한 높은 자유도 또한 이를 테스트하고 적용시키려면 꽤 많은 수정을 거쳐야하는 만큼 많은 시간을 할애해주어야합니다.  
거기에 다양한 이유로 오류가 발생하면 운영자인 블로그 소유자가 일일이 수정을 해줘야 합니다.  
사진이나 동영상 같은 미디어도 외부 저장소(클라우드, 웹드라이브 등)를 통해서 올리는 방식이 권장되며(블로그 레포지토리를 통해서도 올릴 수 있지만, github-page에서 권장하는 레포지토리 용량인 1GB를 넘기기 가장 쉬운 행동이라 몇몇 사진은 내부 레포지토리를 이용해서 사진을 올리더라도 왠만하면 대부분 사진들은 외부 저장소를 통해서 올리는 것이 권장됩니다.) 만약 외부 저장소의 공유 링크등이 그 사이트 약관 변경이나 보안 업데이트 등으로 인하여 링크가 변경되면 그걸 일일이 재수정 해줘야하는 번거로움도 주의하여야 합니다.  

하지만 이러한 위의 단점을 극복할 수 있도록 이번 SSAFYcial 상반기 기획 기사들 통하여 여러가지 알려드릴 수 있도록 노력해보겠습니다!

---

## 본격적으로 jekyll로 블로그를 만들어 보자.

[Top Page](#)

<div class="videoWrapper" style="position: relative; padding-bottom: 56.25%; height: 0;">
  <iframe style="position: absolute; top: 0; left: 0;" width="100%" height="100%" src="https://www.youtube.com/embed/pIpm4NwaH1s?si=sM7wnUFAd-cFf5xw" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
</div>

이번 기사에서는 jekyll 블로그를 위한 PC 개발 환경을 구성해보고, 외부에서 탬플릿을 가져오고,  
github 레포지토리에 push하여 github-page로 블로그를 생성해보는 것까지 알려드리도록 하겠습니다.  
해당 기사는 Windows 환경을 베이스로 설명하도록 하겠습니다.  
해당 내용은 [jekyll의 공식 문서](https://jekyllrb-ko.github.io/docs/installation/) 에서도 확인이 가능합니다.  

---

### Ruby + jekyll 설치하기

[Top Page](#)

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_14.png"/>
</div>  
먼저, jekyll의 기반 프로그래밍 언어인 Ruby를 설치하여야합니다.  
Ruby의 경우 Windows 기준으로 RubyInstaller를 통하여 설치할 수 있습니다.  
MacOS의 경우 [공식 문서](https://jekyllrb-ko.github.io/docs/installation/macos) 를 참조 부탁드리겠습니다.

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_15.png"/>
</div>  
Download에 들어가시면, With DEVKIT에서 가장 굵은 글씨로 강조되어있는 부분이 Stable Version이므로 해당 버전을 사용하시면 됩니다.

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_16.png"/>
</div>  
설치시 가급적이면 C드라이브에 설치하는 것을 권장드리며 2 항목 모두 체크하시고 다운로드 받으시면 됩니다.

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_17.png"/>
</div>  
설치가 완료되었다면 MSYS2 설치 부분도 체크하시고 Finish를 눌러주셔야 합니다.  
MSYS2는 Ruby의 네이티브 젬 컴파일 및 패키지 관리를 담당하기 때문에 설치해주셔야 합니다.

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_18.png"/>
</div>  
이후 명령 프롬포트로 해당 화면이 뜰껀데, 1번과 3번을 각각 설치해주시면 됩니다.  
정상적으로 설치가 완료되었다면 초록글씨로 succeeded라 뜨고 다른 설치를 할꺼냐고 메뉴가 뜹니다.

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_OK.png"/>
</div>  
이제 이러면 Ruby는 설치가 완료된 상태가 됩니다! 와우!

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_19.png"/>
</div>  
이제 cmd를 열어서 'gem install jekyll bundler'를 입력하여 jekyll와 bundler를 깔아줍니다.  
jekyll 블로그를 만들기 위해서 필수적인 플러그인입니다.

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_20.png"/>
</div>  
추가로 VScode에서 Ruby LSP도 설치해주시면 됩니다.  
과거에는 Ruby와 VScode Ruby를 사용하였지만, 지금은 Ruby LSP로 통합 변경되었습니다.

---

### 로컬 영역에 jekyll 블로그 만들어보기

[Top Page](#)

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_21.png"/>
</div>  
이제 본격적으로 블로그를 만들 시간입니다.  
바탕화면이나 블로그 파일을 만들 곳에 새폴더를 생성해줍니다.  
가능하면 영어 이름으로 해두는 편이 오류를 방지하기 좋습니다.

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_22.png"/>
</div>  
이후 만들 파일에 들어와서 'Code(으)로 열기'를 해주시면 됩니다.  
만약 해당 커맨드가 안 보인다면, VSCode를 설치하셨을때 'Code(으)로 열기'를 설정 안 하시고 설치하신거라,  
직접 VSCode를 여셔서 경로를 설정해주시면 됩니다.

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_23.png"/>
</div>  
이후 Control + '~' 버튼을 눌러 콘솔을 켜시고,  
콘솔창에 'jekyll new (프로젝트 명)'을 입력해주시면 됩니다.  
예시에서는 홈페이지에 나온대로 myblog라 입력하겠습니다.  
참고로 해당 경로에 파일을 만들꺼면 'jekyll new ./ -f'를 입력해주시면 됩니다.  
force로 설치하는 이유는 다른 파일이 있어서 Conflict 에러가 발생할 수 있는데, 이를 무시하고 강제 설치하기 위함입니다.  
현재 경로에 설치할 예정이라면 경로에 다른 파일이 없는지 확인하시고 설치하는 것을 권유합니다.

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_24.png"/>
</div>  
명령어가 종료된다면, 가장 기본 형태의 jekyll 블로그 플랫폼이 설치된 것을 확인할 수 있습니다!  
이것으로 여러분만의 블로그가 미약한 형태로나마 생긴 것입니다!

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_25.png"/>
</div>  
이제 그럼 로컬 서버를 열어보면서, 블로그가 어떻게 보이는지 확인할 시간입니다.  
다시 VSCode 콘솔에 'bundle exec jekyll serve' 를 입력하여 로컬 서버를 여시면 됩니다.  
만약 저처럼 ./ 를 하여 현재 경로로 설치하지 않고 프로젝트 명을 입력하시고 설치했다면, 해당 디렉토리로 이동한 뒤(ex: cd myblog) 입력하시길 바랍니다.  
로컬서버는 127.0.0.1의 루프백IP에 포트 4000이 기본으로 설정되어,  
127.0.0.1:4000 으로 주소창에 입력하시면 로컬 서버로 사이트 확인이 가능해집니다.

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_26.png"/>
</div>  
네. 이것으로 기념비적인 첫 블로그가 완성되었습니다!

---

### 테마 템플릿 가져와서 쓰기

[Top Page](#)

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_27.png"/>
</div>  
물론 진짜 0부터 만들어도 되지만, 이제 막 개발자로 한걸음 나선 학생으로서 너무 무리한 부탁이기도 합니다.  
따라서 이미 있는 테마 중 오픈소스에 수정허가가 되어있는 테마를 사용해볼 예정입니다.  

[jekyll 공식 문서](https://jekyllrb-ko.github.io/docs/themes) 에 있는 4가지 테마 보관 주소 중 어느 한가지를 이용해도 되지만,  
이번 예시에서는 [Jekyll Theme](https://jekyll-themes.com) 에 저장되어있는 [NOCC Jekyll Bundle](https://jekyll-themes.com/carlesloriente/bootstrap-theme-jekyll) 을 예시를 사용해보도록 하겠습니다.  
이유는 bootstrap 5 를 지원하며, MIT 라이센스라 상업적 이용 및 수정, 배포, 개인적 이용이 가능하기 때문입니다.  
그리고 굉장히 깔끔하고 적당한 기능까지 있어 예시로 적합할 것으로 판단하였습니다.

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_28.png"/>
</div>  
링크 내부에 들어가셔서 Download 버튼을 누르면 해당 탬플릿의 git 레포지토리로 이동됩니다.  
여기서 <>code를 누르시고 주소를 따셔서 http를 복사하여 git clone을 해서 가져오시는 것이 일반적이나,  
탬플릿에 따라서는 데모 사이트에서 다운로드가 가능한 경우도 있고,  
혹은 아예 git 레포지토리에서 복사할 수 있는 버튼을 만든 경우도 있으니 편한대로 하시면 됩니다.  
저는 demo 페이지에 있는 다운로드로 다운로드 하였습니다.

---

### github에 blog 레포지토리 만들기.

[Top Page](#)

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_OK.png"/>
</div>  
우리는 이제 원하는 jekyll 테마까지 다운로드 하였습니다.  
이제 github에 블로그 파일을 올려 github-page에 넘겨줄 차례가 되었습니다.

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_29.png"/>
</div>   
github에 새로운 레포지토리를 제작합니다.

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_30.png"/>
</div>   
레포지토리 명은 Owner명.github.io 가 권장사항입니다.  
공개 범위는 Public으로 설정하시고 본 예제에서는 Readme File을 체크한 상태로 제작하겠습니다.

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_31.png"/>
</div>   
<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_32.png"/>
</div>   
이후 <>code를 눌러 html 주소를 복사한 뒤, 가져올 빈 폴더에서 git clone. 해주시면 됩니다.

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_33.png"/>
</div>   
아까 받아두었던 탬플릿 파일을 그대로 복사하여 clone 해온 폴더에 붙혀넣고,  
git add . -> git commit -m "커밋명 입력" -> git push origin main
순으로 github에 push해주시면 됩니다.

<div style="text-align: center;">
<img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_03/SSAFYcial_mar_34.png"/>
</div>   
이후에 자기 레포지토리 이름을 주소에 입력하면,  
보시는바와 같이 탬플릿이 블로그에 등록되어 정상적으로 출력되는 모습을 보실 수 있으며,  
드디어 블로그 개설에 성공하게 되었습니다!  
참고로 push 한 뒤 github-page에 반영되기 최소 1분에서 최대 5분 이상 걸리기 때문에 여유를 가지시고 기다리시면 됩니다.

---

## 마치며.

[Top Page](#)

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_THANKS.png"/>
</div>  
이번 기사에서는 개발 블로그에 대한 소개, 플랫폼 소개, github-page와 jekyll를 이용한 블로그 소개, 그리고 그 블로그의 개설까지 한번에 기사로 기록해보았습니다.  
저도 jekyll에 대해 전문가 수준으로 많이 아는 사람이 아닌 같이 공부하는 학생으로서 부족한 점이 많습니다.  
하지만 이 기획 기사를 제작하고 SSAFY에서 공부하면서 이 기사를 읽는 분들과 같이 성장하고 싶은 마음에 해당 기사 주제를 기획하게 되었습니다.

여러분들도 개발 블로그를 운영하면서 같이 배우면서 성장하는 개발자 지망생이 되었으면 하는 마음을 담아,  
끝으로 SSAFY에 대해 소개를 하면서 이 기사를 마치도록 하겠습니다.  

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
