---
title: SSAFYcial) 0️⃣부터 시작하는 개발 Blog 생활 2화, 디렉토리 분석과 포스팅 해보기!
keywords: [SSAFY, SSAFYcial]
tags:  [SSAFY, SSAFYcial]
summary: "SSAFYcial 기사 5호. 만들었는데, 이제 모함? 본격적으로 뜯어보며 하나하나 꾸며보자. 블로그를 만들었으니 이제 운영을 해볼 차례"
sidebar: SSAFY_sidebar
permalink: SSAFYcial_05.html
folder: SSAFYcial
---
<a href="https://hits.sh/jsj0per.github.io/SSAFYcial_05.html/"><img alt="Hits" src="https://hits.sh/jsj0per.github.io/SSAFYcial_05.html.svg?style=for-the-badge&label=PostView&color=347DBE&logo=Perso"/></a>

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/ssafycial_series_header.png"/>
</div>

해당 포스트에 사용된 일부 삽화는 ChatGPT DALL·E 를 사용한 AI 그림임을 알려드립니다.  
또한 저를 형상화한 이모지는 삼성 AR 이모지를 이용하여 제작된 AI 이미지임도 알려드립니다.    

> 해당 포스트는 전 포스트에 이은 SSAFYcial 기획 시리즈 입니다.  
>> [0️⃣부터 시작하는 개발 Blog 생활 1화](https://jsj0per.github.io/SSAFYcial_03.html)  
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
저번 포스트에서 각자 github에 Github-Page 레포지토리를 만들었고, 원하는 테마를 가져와서 설치하는 것 까지는 아마 Git에 대해 지식이 있다면 무난하게 했을리라고 생각됩니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_Rain.png"/>
</div>

그런데 말입니다...  
설치는 했는데, 아직은 내 블로그처럼 다룰 수 없는게 사실인 건 맞습니다. 
만들어진 오픈 소스 템플릿을 가져와서 편하게 시작할 수 있는 교보재가 생긴 건 좋은데,  
우리가 프로그래밍을 공부할 때 가장 어려운 것 중 하나가 남의 코드를 읽는거니까요.  

그래서 이번 포스트에서는 간단하게 jekyll blog의 구조를 알아보고 post를 작성하는 방법을 같이 공부해보고자 합니다.  

---

## jekyll 디렉토리와 파일을 차근차근 연구해보자.

[Top Page](#)

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_01.png"/>
</div>

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_apr_02.webp"/>
</div>

워워워...  
진정하세요. 무슨 말을 하고싶은진 알고있습니다.  
저 폴더는 또 뭔 역할을 하고, 저 파일은 또 어떤 역할을 하고...  
도데체 이걸 어떻게 수정한단 말이지?  

수 많은 생각이 스쳐 지나간건 충분히 이해합니다. 저도 그랬고, 이번에 교보재로 쓰는 NOCC 스킨은 저도 처음 써보는 거니까, 여러분들과 크게 다른 기분은 아닐껍니다.  ~~헤헤~~

물론 이번 포스트에서 모~든 기능을 다 공부하진 않을 겁니다.  
모든 디렉토리에 대해 공부하려면 너무 많은 정보가 필요하니 차근차근 필요한 부분만 먼저 공부해보도록 합시다.  

### 일단 기본적인 디렉토리 구조...

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_03.png"/>
</div>
[출처: Jekyll 공식 문서](https://jekyllrb-ko.github.io/docs/structure/)

일단 jekyll의 기본적인 디렉토리 구성은 위 사진과 같이 되어있습니다.  
물론, 템플릿마다 추가적인 기능 차이는 있을겁니다.  
하지만 기본적으로 위 구조를 기반으로 변형만 되어있기 때문에 일단 이 기능들 부터 차근차근 알아가봅시다.

지금 당장 이번 포스트에서 우리가 알아두면 되는 기능은 '_config.yml'과 '_posts', 'index.html(index.md)' 정도만 일단 기억해두시면 됩니다.  

지금 다른 기능에 대해 알고싶으시다면 일단은 공식 문서를 통해서 스스로 공부해보시는 것을 추천드립니다.  거기까지 설명했다간 아마 처음 jekyll을 다루는 입장에서 엄청 어려워지니까요.  

### '_config.yml' ( 블로그 환경 설정 정보 )

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_04.png"/>
</div>

레포지토리에 있는 위 파일을 한번 클릭해보도록 하겠습니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_05.png"/>
</div>

이 파일이 바로 우리 블로그의 기초 환경설정을 할 수 있는 설정 파일이라고 생각하시면 됩니다.  
어우... 너무 줄글이 많아서 현기증이 올거 같은거 압니다.  

차근차근 알아가봅시다.  
다행스럽게도 어느정도 [템플릿 소개 페이지](https://jekyll-themes.com/carlesloriente/bootstrap-theme-jekyll)에서 config.yml에 대한 설명을 어느정도 해두었으므로 그것에 기반을 두고 설명하도록 하겠습니다.

제일 윗 단락 부분은 블로그의 제목(title), 소유자 명(author), 주소 정보(url), 소개(decription), 그리고 지역 정보 설정들인 locale과 lang, timezone이 눈에 보입니다.  
가장 기본적인 설정을 담당하는 부분입니다. gh_repository는 일단은 이번 포스트에서는 건들지 않겠습니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_06.png"/>
</div>

이 정보들을 먼저 바꿔보는 걸로 해보도록 하겠습니다.  
title에는 자기가 정하고 싶은 블로그 명은, description과 full_description은 블로그에 대한 소개글을, gh_repository에는 이 블로그의 원래 레포지토리, 즉 깃허브의 블로그 레포지토리의 주소를 적어넣고, url은 지금 이 블로그 주소를 적어 넣어보도록 하겠습니다. timezone 역시 한국의 IBM 기준 시차코드인 Asia/Seoul을 집어 넣어보도록 하겠습니다.

landing 부분은 추후에 설명해보도록하고 일단 권장사항인 false로 바꾸도록 하겠습니다.  

locale과 lang은 바꿔도 지금 이 영어 페이지를 한국어로 자동으로 바꿔주는 기능은 아니니까, 안 바꿔주셔도 무방합니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_07.png"/>
</div>

그랬더니, 짜잔!  이 부분이 바뀐 것을 확인할 수 있었습니다.  
중간에 Your content here.으로 바뀐 부분은 나중에 설명하겠습니다. landing을 false로 설정해서 그렇습니다.  

블로그 홈버튼을 담당하는 부분이 title로 입력한대로 바뀌었고 아래 footer 부분에도 author 부분이 들어간다는 사실을 알게되었습니다.  
또한 description 부분이 대문 이미지 쪽 글씨에 들어간다는 사실도 알게되었습니다.  
NOCC 부분이 바뀌진 않았지만 이 부분은 조금 있다가 말하겠습니다.  

'# Features' 부분과 '# Theme Notice (please don't remove it ;))' 부분은 건너 뛰도록 하겠습니다.

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_08.png"/>
</div>

안 건들기로한 부분 다음 부분을 보면 # Social Profiles 문단이 나오는데... 

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_09.png"/>
</div>

분석해보니 홈페이지에 이 부분을 담당하는 기능으로 보여집니다.  
SNS를 연동시키는 용도로 설정부분을 남겨두신 것 같습니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_10.png"/>
</div>

일단 본인이 홈페이지에 연동시키고싶은 SNS만 저렇게 적어두시면 될 것 같습니다.  
아이디 명만 적어두면 이동 가능하도록 코드가 짜여진 것 같습니다.  
저는 SNS를 주력으로 하는 계정이 없으니, email과 github_username 만 적어두도록 하고, 
나머지는 주석처리 하도록 하겠습니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_11.png"/>
</div>

그랬더니 딱 적어둔 부분만이 등록된 것을 확인할 수 있었습니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_12.png"/>
</div>

바로 다음 부분은 Google Search console에서 사이트 검색 관리를 할 때 사용하는 코드입니다.  
일단은 저희는 당장에 사이트를 포털에 등록시킬 생각은 없으니 주석처리 해두도록 하겠습니다.  

나머지 config 부분은 일단은 이번 포스트에서 건들지 않도록 하겠습니다.  

config 파일은 이 처럼 우리 블로그의 기초적인 환경설정을 담당하는 부분입니다.  

다만 이 config 파일은 템플릿마다 개발자 스타일마다 좀 천차만별로 달라지는 부분중 하나이니,  
템플릿 페이지 설명에 적어둔 설명들을 참고하거나 스스로 분석하는 방법밖에는 없습니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_OK.png"/>
</div>

하나씩 차근차근 수정해보고 오류가 발생하면 커밋을 리셋 시켜보는 방식으로 하나하나 차근차근 알아보는 방법이 느리긴 하나 가장 효과적이니 겁먹지말고 한번 도전해볼 수 있도록 합시다.

### 'index.html' (메인 페이지 문서)

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_13.png"/>
</div>  
레포지토리에 index.html(템플릿에 따라선 index.md 문서일 수 있음)는 블로그의 메인 페이지를 담당하게되는 부분입니다.  
블로그를 방문할 사람들이 가장 먼저 보게되는 부분을 담당하는 부분입니다.  

이 또한 템플릿마다 조금씩 차이가 있겠지만 가장 눈에 띄는 부분은 위의 하이픈 3개씩으로 구분되어지는 공간인데, 이 부분이 jekyll의 큰 특징중 하나인 YAML 머릿말(front-matter)입니다. 

이 부분에 보통 이 페이지에 관한 정보가 들어가는 일종의 간이 환경설정 칸이라고 아시면 이해하기 쉽습니다.  

그러고보니 title 부분에 NOCC 부분이 눈에 띄입니다.  
방금 우리는 NOCC 부분이 config에서 바꿀 수 없었는데, 드디어 그 입력부분을 찾은셈이 되겠습니다.  
이 부분이 페이지의 제목을 담당하는 부분입니다.  

background와 carousel은 배경설정 부분으로 이 템플릿에는 carousel(사진을 한칸에서 여러개 볼 수 있도록 앨범형식으로 출력하게 하는 기능)이 기본 기능으로 들어가있습니다.  

본문 부분을 확인하겠습니다.  
일단 아까 config에서 landing을 false로 설정했는데, 그래서 else부분이 출력되어지고 있는 것으로 보여집니다.  
이제 우린 이 else부분 밑에 입력하면 그 내용이 홈페이지 메인에 출력될 것이라는 걸 새롭게 또 알게되었습니다.  
이제 마음껏 꾸며보도록 하겠습니다.
해당 탬플릿의 index는 제가 몇번 시도해본 결과 나온 결론으로 Description 부분은 건들이지 마시길 바랍니다.

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_14.png"/>
</div>  

이렇게 바꾸어보았습니다.  
이 글을 보시고 계신 분들도 각자 자기가 원하는대로 이 블로그를 찾아올 게스트들에게 보여주고 싶은 첫 대문 화면이라 생각하고 꾸며보도록 합시다.  
다만 HTML에 사용하는 만큼 HTML에 대해 조금 지식이 필요한 편입니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_15.png"/>
</div>  

꾸몄다면 이렇게 수정한 부분이 반영된 것을 확인활 수 있습니다.  

### '＿posts' (블로그 포스트 저장 폴더)

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_16.png"/>
</div>  

jekyll 블로그에서 가장 중요한 기능 중 하나로 우리들이 쓸 글들이 들어갈 구역입니다.  
사진에서 POST탭에 들어갈 글들이 저장될 폴더가 바로 '_post' 입니다.  


<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_17.png"/>
</div>  

해당 폴더에서 '년-월-일-제목.md' 혹은 '년-월-일-제목.markdown' 형식으로 하나의 포스트가 저장됩니다.  
여기서 md, markdown은 '마크다운' 문법을 사용하는 문서라는 뜻입니다.  
저번 포스트에서 벨로그가 대표적인 마크다운 문법을 사용하는 블로그라고 소개한 적이 있었습니다.  
그 마크다운을 말하는 겁니다.  

자세한 문법에 대해서는 아래 다른 기자분의 SSAFYcial 포스트를 참조하여 주신다면 해당 포스트를 이해하기 쉽습니다.  
[[Markdown] 마크다운, 그것이 알고싶다](https://memezz.tistory.com/20)  

마크다운 자체는 그렇게 많이 어려운 문법은 아니기 때문에 수 분 안에 금방 배우실 수 있습니다.

일단 마크다운에 대한 설명은 해당 블로그로 갈음하고, 포스트를 한번 작성해보도록 합시다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_18.png"/>
</div>  

저는 VS Code를 통해 작성할 예정이지만, github 레포지토리에서 create new file을 이용해서 작성해도 되고, MD 파일 작성 프로그램을 써도 무방합니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_19.png"/>
</div>  

아까 index 작성할 때 보신것 처럼 post 역시 YAML 머릿말(front-matter)을 사용합니다.  
템플릿 마다 요구되는 머릿말이 조금씩 차이가 날 수 있으니, 기본으로 제공되는 예시 포스트에서 머릿말만 살짝 복사해와서 자기가 작성할 포스트로 옮겨서 작성합니다.  

title은 제목, layout은 post로 해주시고(후에 '_layout' 폴더에 템플릿을 만들어서 다른 레이아웃을 적용시킬 수 있으니 이번 포스트에서는 다루지 않겠습니다.)  
comments는 일단 false로 하도록 하겠습니다.  
date는 수동으로 알아서 작성해주시고, tags에 원하는 태그를 작성해주시면 됩니다.
해당 템플릿에서는 background가 있어서 사진을 경로 지정해서 등록해주시면 헤더 배경화면에 첨부됩니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_20.png"/>
</div>  

이렇게 첫번째 포스트를 작성해보았습니다. 이대로 등록시킨다면?  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_21.png"/>
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_22.png"/>
</div>  

이렇게 포스트가 작성되는 것을 확인할 수 있습니다.  

### '_include' 폴더

include 폴더는 쉽게 말하자면 포스트 템플릿을 저장하는 폴더(html 재사용을 위한 폴더)라고 생각하시면 됩니다.

#### post.html

아까 포스트를 작성했을 때, 원래 제작자가 남겨둔 후원 링크가 다소 거슬렸을 겁니다.  
이는 post 기본 탬플릿을 건드려야 수정할 수 있는 부분입니다.  
이를 수정하려면 '_include' 폴더에 접근하여야 합니다.

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_23.png"/>
</div>  

아까 포스트를 작성하셨을 때, 그냥 마크다운으로 입력했는데, html로 바로 변환하여 출력되는 것이 include에 있는 템플릿에 content 부분에 아까 그 마크다운 내용을 집어넣고 바로 출력하는 원리로 되어있습니다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_24.png"/>
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_25.png"/>
</div>  

post.html에 들어가셔서 해당 부분을 지워주시면 포스트에서 후원 부분이 깔끔하게 지워지는 것을 확인하실 수 있습니다.  

#### navbar.html
<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_27.png"/>
</div> 
화면 상단에 위치한 네비게이션 바를 담당하는 부분입니다. 
혹시나 다른 page 부분을 추가하여 상단바에 추가하고 싶다면 해당 부분을 수정하시면 됩니다.  

### page
<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_26.png"/>
</div>  

그러고보니, posts와 home을 제외한 다른 기능은 수정한 적이 없으니 한번 살펴보도록 합시다.  
jekyll은 posts가 가장 메인인 페이지 제작이긴 합니다만, 그렇다고 다른 방식이 없는 것은 아닙니다.  
<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_28.png"/>
</div>  

레포지토리를 찾아보시면 마침 제작자가 친절하게도 이름까지 통일시켜두어 해당 파일을 수정하면 된다는 식으로 설정을 해두셨는것을 보실 수 있습니다. 이중 저희는 about 부분을 예시로 수정해봅시다.  

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/SSAFYcial_05/SSAFYcial_Apr_29.png"/>
</div>  

전반적으로 index.html 파일과 대충 비슷한 양식으로 되어있는데,  
수정 역시 비슷한 방식으로 수정하시면 됩니다.  
YAML 머릿말 부분에 원하는 방식으로 수정하고, 
내용도 html 형식에 맞게 수정하시면 됩니다.  

주의할 점은 만약 title과 permalink(url 링크에 path를 담당하는 부분)를 수정하실꺼면 이에 맞게 navbar.html에 가서 해당 navbar 버튼의 href를 변경된 permalink에 맞게 수정해주셔야 합니다.  

---

## 마치며.

[Top Page](#)

<div style="text-align: center;">
  <img src="/pages/SSAFYcial/SSAFYcial_img/JSJ_THANKS.png"/>
</div>  
이번 기사에서는 저번 포스트에 이어서 이번에도 Jekyll Blog의 몇몇 디렉토리와 포스트 작성 방법을 같이 공부해보았습니다.  
이것 이외에도 다른 디렉토리나 기능도 있지만, 차근차근 천천히 접근해보도록 하는 편이 저와 이 글을 보시는 여러분들도 공부하는데 더 쉬우리라 생각됩니다.  

앞으로도 저도 jekyll 블로그에 대해 공부를 계속하여 남들과 다른 포트폴리오를 만들 수 있는 공간을 같이 만들 수 있도록 같이 노력해봅시다.  

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
