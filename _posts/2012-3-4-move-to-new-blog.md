---
layout: post
title: 블로그 이사
comments: true
share: true
tags: [개발, github]
---
<p class="meta">2012년 3월 4일 - 안양</p>

내가 블로그를 신경 안쓰는 것 처럼 보여도 마음 속에선 항상 버려진 [블로그](http://plan9.kr)에 대해 미안한 마음을 가지고 있었다. 많은 생각을 해봤는데 내가 블로그를 안하게 된 이유는 첫째로 트위터탓! 둘째로 작성한 글 관리의 애매함, 셋째로 긴 글에 대한 부담감 때문이었다.

트위터는 내가 블로그에 자주 쓰던 정보 전달 형식의 글을 굉장히 쉽고 간단하게 발행할 수 있게 해줬다. 발행 속도 뿐만 아니라 확산 속도도 블로그에 비할바가 아니었다. 그리고 사실, 정보 수집과 전달은 블로그에 쓰고나면 나중에 부끄럽다. 그런 글은 빨리 써서 발행했기 때문에 내용이 부실하고 문장도 어색하고 정보의 내용도 나중에 다시 볼 이유도 없는 것이기 때문이다. 검색도 잘 안되고 내가 쓴 글을 나중에 다시보기도 힘든 트위터의 휘발성은 그냥 기술이 부족해서 그런 것 같지만 짧은 잡담과 빠른 정보들을 다루기에 마음이 편하다. 

글 관리도 항상 마음에 걸리는 부분인데 포털의 블로그 서비스를 이용하면 블로그가 완전히 내 것이 아닌 기분이 들어서 싫고, 좀 마음에 드는 서비스는 백업하기가 귀찮았다. 결국 웹호스팅 서비스에 워드프레스를 올려서 한참 사용했지만 역시 블로그와 플러그인의 업데이트와 글 백업이 너무 귀찮았다! 

그래서 이런 생각이 떠올랐다. **'아 블로그를 다시 살리려면 한번 죽여야겠구나!'** 그때부터 조금씩 새 블로그에 대한 생각을 하기 시작했다. 새로운 블로그의 조건은 이랬다. 

1. 어느 환경에서도 한번에 글 작성이 가능해야한다. (티스토리 정기점검 OUT!)
2. 수동으로 백업을 하지 않아도 로컬에 자동으로 백업이 된다.
3. 블로그 레이아웃을 완전히 내가 바꿀 수 있어야 한다. (네이버 OUT!)
4. 언제 어떤 내용을 추가하고 바꿨는지 글에 대한 버전 관리가 되어야 한다. 

그래서 처음에 생각한 것이 [google app engine](http://code.google.com/intl/en/appengine/)에 직접 만든 블로그 엔진을 올리고 거기에 글을 작성하는 것이었다. 제작에 착수까지 했으나 표준화 된 도구(텍스트 포맷팅, 블로그 구조 생성)가 없고 내가 마음대로 블로그 테마를 만들 수는 있지만 백업이나 글 작성의 자유로움, 버전관리 등은 보통의 블로그 플랫폼과 다를바가 없었다.

app engine 블로그를 포기하고 어떤 방법이 있을까 찾던 중에 **버전 관리 == git** 이라는 생각이 떠올라 *SCM-based blog engines*으로 검색해보니 과연 여러 방법이 이미 있었다. (git: 프로그램 소스를 버전별로 엉키지 않게 관리해주는 시스템) 역시 git을 이용한 소셜코딩 사이트 [github](https://github.com/)에서도 git으로 블로깅하는 방법을 제공해주고 있었다. github이 제공하는 블로그 기능은 기대한 것 보다 더 마음에 들었다. 

1. 내 컴퓨터에서 sungchi.github.com 이라는 디렉토리를 생성해서 github.com에 올리면 10분 후에 [sungchi.github.com](http://sungchi.github.com) 이라는 페이지를 생성해준다. 
2. 그때부터 [github 저장소](https://github.com/sungchi/sungchi.github.com)에 올리는 html 파일은 그대로 그 페이지에서 보여지게 된다.
3. github에선 웹사이트 생성기 [Jekyll](https://github.com/mojombo/jekyll)을 제공하여 글과 블로그 스킨과 레이아웃을 분리해준다. (한번 세팅하면 글만 작성하면 됨)

**이 방법은 새로운 블로그의 조건을 죄다 만족한다.** 로컬 컴퓨터에서 마크업 언어를 이용해 글을 작성하고 Jekyll 서버를 돌려서 올릴 글을 미리 확인 해 볼 수 있고, 소스 관리 시스템을 기반으로 하고 있기 때문에 글 작성 한번으로 글의 버전 관리와 백업도 함께 된다. 게다가 이렇게 여러가지 조건을 만족하면서도 글만 작성하면 나머지 태그, 글주소, 블로그 스킨, RSS 생성 등은 다 알아서 처리해준다. 

github pages 기능을 사용하면서 github 사람들의 센스에 다시한번 감탄했다. 자신들이 뭘 원하는지 정확히 알고 그걸 현실화 시켜서 사람들의 삶을 좀 더 낫게 만들어주는 [github 팀](https://github.com/about)에게 다시한번 감사를 드린다. 

링크:

* github pages : [http://pages.github.com/](http://pages.github.com/)
* Sungchi' Blog 저장소: [https://github.com/sungchi/sungchi.github.com](https://github.com/sungchi/sungchi.github.com)
* Spoqa 블로그 탄생비화(한글 설치 안내): [http://spoqa.github.com/...](http://spoqa.github.com/2011/12/17/about-spoqa-blog-creation.html)
* github 맥 클라이언트: [http://mac.github.com/](http://mac.github.com/)
* jekyll+github으로 블로그 만들기, 테마설정: [http://jekyllbootstrap.com/](http://jekyllbootstrap.com/)
