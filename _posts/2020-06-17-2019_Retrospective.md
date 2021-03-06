---
title: "아주 늦은 2019년 회고"
layout: single
classes: wide
date: 2020-06-17 10:00

category: 
    - Retrospective

tag:
    - retrospective
    - quantified self
    - clova
    - larva
    - aicall

toc: true
toc_label: "Table of Contents"
toc_icon: "list-alt"
toc_sticky: false
---



개인적으로 간단하게 작년 연말에 회고를 하였지만, 블로그를 제대로 시작할 겸..! 
2019 회고글을 작성해보고자 한다. 생각보다 시간이 지났기 때문에 당시 회고하면서 바라보는 관점과 지금의 관점은 약간의 차이가 있을 수는 있을 것 같다.

## 회사


그 어느 때보다도 회사의 일에 집중을 했던 한해라고 생각을 한다.
매일 매일 되도록이면 일기를 쓰려고 하는데, 지금 돌아가서 그때의 일기들을 들여다보면 회사에서 느꼈던 감정들이 대부분인 정도이다. 그래서 2019년 회고는 회사 관련한 글이 많지 않을까 싶다.

### LaRva 프로젝트와 PM

 18년도 10월에 [BERT](https://arxiv.org/abs/1810.04805)라는 논문이 공개되고, NLP 분야에서는 바야흐로 BERT의 시대가 되었었다. 논문의 abstract에도 다음의 문구가 포함되어 있을 정도이다. 

`It obtains new state-of-the-art results on eleven natural language processing tasks`  

 "물 들어올 때, 노 저어라" 라는 말처럼, 이 BERT 모델의 급 물살을 탈 수 있었던 프로젝트가 LaRva 프로젝트이다. (이 자리를 빌려, 프로젝트를 셋팅하고 PM을 맡겨주신 [서민준](https://seominjoon.github.io/)님께 감사의 말씀을 드린다.) 

최근에는 PM으로서, 제품에 대한 공부를 많이 하고 있다보니 지금의 시각으로 프로젝트를 돌아보려고 한다.
LaRva는 연구위주의 프로젝트이지만, 좋은 언어모델을 만드는 목적을 가진 하나의 제품으로서도 바라볼 수 있다고 생각이 든다.
다음은 [≪인스파이어드≫](https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=176659275) 에서 제품 발견의 목적으로서, 아래 4가지 항목의 위험에 대비해야 함을 말하고 있다.

- 고객이 과연 이 제품을 구매하거나 사용할 것인가? (가치 위험 Value Risk)  
⇒ 다양한 NLP 서비스에 쉽게 적용할 수 있고, 성능을 올림으로서 서비스 품질에 기여할 수 있다는 것
- 사용자가 이 제품의 사용 방법을 이해할 수 있는가? (사용성 위험 Usability Risk)  
⇒ Github에 코드들이 계속 공개 되고 있었고 특히, huggingface에서 지금의 [transformers](https://github.com/huggingface/transformers) 저장소를 만들어낸 것과 같이, 누구나 쉽게 쓸 수 있도록 정말 빠른 속도로 작업을 하고 있었다.
- 우리가 만들 수 있는 것인가? (실현 가능성 위험 Feasibility Risk)  
⇒ 가장 큰 제약은 GPU 일 것이다. 네이버이기 때문에 이런 제약은 해결이 될 수 있었다.
- 우리 사업에 효과가 있는 솔루션인가? (사업 유효성 위험 Business Viability Risk)  
⇒ 시간이 지나면서 이 BERT라는 모델의 중요성은 부각이 될 것이고, 이에 따라서 자연스럽게 풀릴 수 있는 문제라고 생각했다.

지금 와서 생각해보면.. 이렇게 잘 정의될 수 있는 프로젝트는 드물 것이라 생각을 한다. 

위와 같이 위험한 부분이 없는 프로젝트로서 좋은 결과물들을 만들어 나아갈 수 있었고, KorQuAD v1 리더보드와 연말에는 Deview 2019 발표 그리고 사내 연구 아이템 2위로 선정이 되는 등 여러가지로 정말 얻은 것들이 많다고 생각한다.

![2019%204d025a4489ba4870828420f0b38f75b6/Untitled.png]({{ site.url }}{{ site.baseurl }}/assets/images/2019%204d025a4489ba4870828420f0b38f75b6/Untitled.png)

 <figcaption class="caption">[KorQuAD v1 Leaderboard](https://korquad.github.io/category/1.0_KOR.html), Anonymous 때문에 힘들었던.. </figcaption>


![2019%204d025a4489ba4870828420f0b38f75b6/Untitled%201.png]({{ site.url }}{{ site.baseurl }}/assets/images/2019%204d025a4489ba4870828420f0b38f75b6/Untitled%201.png)

 <figcaption class="caption"> 출처 : https://www.pinterest.co.kr/pin/515662226060509153/ </figcaption>

![2019%204d025a4489ba4870828420f0b38f75b6/Untitled%202.png]({{ site.url }}{{ site.baseurl }}/assets/images/2019%204d025a4489ba4870828420f0b38f75b6/Untitled%202.png)

 <figcaption class="caption"> 출처 : https://m.mk.co.kr/news/english/view/2017/11/777734/ </figcaption>

여담이지만, 프로젝트의 이름을 LaRva로 짓게 된 이유도 이야기해보려고 한다.
NLP에 계시는 분들은 ELMo, BERT, ERNIE 이런 식으로 네이밍을 하는 이유가 Sesame Street의 캐릭터들의 이름에서 가지고 왔다는 것을 알고 있을 것이다. 어쩌다보니 우리팀 역시 이러한 네이밍 트랜드를 따라서 국산 애니메이션 LaRva로 이름을 짓게 되었다. 지금도 참 입에 잘 붙고, 좋은 네이밍이였다고 생각을 한다. 
(LaRva의 풀네임은 **La**nguage **R**epresentations by Clo**va** 이다.)
그리고 실제로 이러한 네이밍이 가지는 영향에 대해서도 어느정도 실감할 수 있었다. KorQuAD와 Deview 등 모두 LaRva 라는 이름으로 리더보드에 등록하고, 발표를 진행하면서 하나의 팀으로서, LaRva는 어떠한 팀인지 브랜드를 구축했다고 본다.

그리고 또 한가지 나에게 이 프로젝트가 중요한 의미를 가지는 것은 PM 으로서의 커리어이다.
기존에는 팀에서 ML Engineer 로서 역할을 하고 있었지만, 새롭게 프로젝트가 정리되고 기존 팀이 나눠지면서 PM 제안을 받게 되었다.
 시작은 나를 포함해서 총 4명으로 일을 진행했고, 매니징보다는 실무를 많이 보았었다. 소수이지만 모두 정말 잘하시는 분들이었기 때문에 위처럼 좋은 결과를 냈다고 생각한다. 그리고 당연하게도 좋은 결과를 내면서 PM이라는 Role에도 약간의 재미를 느꼈던 것 같다.
또한 이때는 이러한 PM이라는 역할이 더 나아가게 될지는 알지 못 했다...!


### CLaF 오픈소스화

![2019%204d025a4489ba4870828420f0b38f75b6/Untitled%203.png]({{ site.url }}{{ site.baseurl }}/assets/images/2019%204d025a4489ba4870828420f0b38f75b6/Untitled%203.png)

[CLaF](https://github.com/naver/claf)(**C**lova **La**nguage **F**ramework)는 Clova AI에 합류했을 때, 기존의 팀에서 진행했던 프로젝트이다. NLP 프레임워크로서 다양한 Task들을 셋팅하고 돌릴 수 있으며 각각의 `Experiment` 들을 Pipeline 화하여, 하나의 모듈 혹은 컴포넌트를 쉽게 만들 수 있도록 틀을 제공해주는 프레임워크로 설계하였다.

개인적으로 아쉬웠던 점은 Github을 살펴보면.. 다수의 ML/DL 관련한 프레임워크들이 오픈소스화 되어있었는데, 대부분이 미국회사였다. 특히 Google과 Facebook..! 이러한 여러 좋은 프로젝트들에 뒤지지 않는 좋은 퀄리티의 프레임워크를 만들어보고 싶었고, 특히 오픈소스를 만들어서 많은 NLP 종사자분들과 이야기하며 퀄리티도 올리고, 이력서의 하나의 아이템으로도 쓸 수 있도록 만들고 싶었다. 솔직하게, 기대보다는 관심을 받지 못 하였다. Github의 Star가 높다고 맹목적으로 좋다라고 말을 할 수는 없지만.. 관심과 영향도의 측면은 충분히 보여주는 지표라고 생각한다. 현재 기준으로.. Star 182개 이고 나 역시 유지보수에 시간을 사용하지 못하고 있으므로 확실히 정체가 되어있는 상황이라 볼 수 있다.

'차별화'는 무엇이든 만들 때 적용되는 원리이다. 프레임워크를 만들때 역시 차별화를 확실하게 해야한다는 점을 뼈저리게 느꼈다. 혹은 선구자가 되거나. 사내의 팀용으로 처음 개발을 시작했기 때문에, 다양한 요구사항을 충족시키기 위해 점점 하나의 특징보다는 다양한 케이스를 커버할 수 있는 프레임워크가 되어갔고 이때, 가장 많이 참고했던 [allennlp](https://github.com/allenai/allennlp) 와의 차별점을 가지지 못 했던 것 같다. 

이렇게 비슷한 방향으로 프레임워크가 발전해 나아갔지만, AllenNLP의 경우 그때 당시에도 이미 유명한 프로젝트 였으며 이렇게 될 수 있었던 것은 2가지 요인이 있다고 본다. 첫 번째는 Zero to One 으로 당시에는 이 정도로 잘 만들어져있는 범용 NLP 프레임워크가 없었던 것. 다음으로는 [allenai](https://allenai.org/) 에서 나오는 논문들이 이 프레임워크에서 릴리즈가 되기도 하면서 특히 수혜를 많이 보았다고 생각한다. [ELMo](https://allennlp.org/elmo)가 대표적일 것이다. claf의 경우에는 후발 주자 이기도 하였고, 논문이 구현되는 등의 이런 수혜를 받을 수 없었기 때문에 어쩌면 당연한 결과일지도 모르겠다.

나에게는 다소 아쉬울 결과였다고 해도, 시작부터 끝까지 만들어나가면서 결국 오픈소스화까지 할 수 있었고 여기서 배운 것들은 매우 많다. 특히 설계부분에 대해서 신경을 썼고, 내부적으로 여러 PR들에 대해 이야기할 때도 설계자의 관점으로서 이야기를 할 수 있다는 것은 특별한 경험이기도 하였다. 앞으로 시간이 좀 날 수 있다면, 유지보수와 더불어서 확실한 색깔을 갖춰보고 싶다.


### DUET PM 그리고 AiCall

![2019%204d025a4489ba4870828420f0b38f75b6/Untitled%204.png]({{ site.url }}{{ site.baseurl }}/assets/images/2019%204d025a4489ba4870828420f0b38f75b6/Untitled%204.png)

 <figcaption class="caption"> 출처: [아웃백 미금점 AiCall 이벤트](https://clova.ai/m/ko/events/aicall/) </figcaption>

커리어측면으로 확실한 방향 전환이 일어난 사건이다. 사내에서 개발 중인 '전화를 대신 받아주는 AI 서비스' 프로젝트인 DUET의 Project Manager를 9월 혹은 10월 쯤에 맡게 된 것이다. 기존 연구 중심의 LaRva 프로젝트와는 다르게 철저히 Product 중심의 프로젝트였기 때문에 내가 해야하는 역할 또한 기존과는 확실히 달랐다. 이때부터 실무를 볼 수 있는 시간이 급격하게 줄어드는 것이 느껴졌다...

해당 프로젝트는 이미 잘 셋팅이 되어있었기 때문에, 내가 주로 맡았던 일은 '제품 실행 관리자 (Delivery Manager)' 에 가깝다. 어느 회사나 비슷할 것 같지만.. PM 이라는 역할은 필요한 일이면 무엇이든 하고 있는 사람이기에..  [≪인스파이어드≫](https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=176659275)에서 '제품 실행 관리자' 의 역할을 다음과 같이 소개하고 있다.

> 제품 실행 관리자는 특별한 유형의 프로젝트 관리자로서 모든 장애물과 방해 요소를 없애는 임무를 가지고 있다. 때로는 다른 제품팀이 장애물이 되기도 하고, 어떤 경우는 제품 외부의 기능 조직이 되기도 한다. 하루 동안 그들은 여러 종류의 일을 해낸다. 마케팅 부서의 누군가를 찾아서 의사결정이나 승인을 요구하고, 다른 팀의 제품 실행 관리자와 협업하여 의존성이 있는 일에 대한 우선순위를 논의한다. ... 제품 실행 관리자는 보통 팀의 스크럼 마스터 역할도 수행한다. ... 채찍을 휘두르는 것이 아니라 일을 가로막는 방해 요소를 제거함으로써 이를 가능하게 한다.  
━ 19. 제품 실행 관리자의 역할 중에서  

모든 장애물과 방해 요소를 없애는 임무라.. 이미 들어가 있는 단어가 굉장히 위험하다고 생각이 든다. '모든' 이라니... 그래도 이 한 문장은 PM의 특히나 중요한 임무이면서, 어려운 일을 이야기하고 있다. **위험 요소를 미리 파악하고 대처하며 제거한다는 것**. 여기에는 굉장히 많은 일들이 포함될 수 있다. 성능이 안 나오는 컴포넌트의 성능을 올리는 일, 다른 부서와의 커뮤니케이션, 팀원 분들과의 면담과 계속해서 일하고 싶은 팀을 만드는 일 등 사실상 모든 일들이 포함될 수 있다.

그리고 조금 더 많은 인원의 PM으로 일을 하면서 느꼈던 점은 감정노동이 굉장히 많다는 것이다. PM의 기본적인 롤에서 한 가지는 사람을 적재적소에 배치해야 한다는 것이다. 이를 피터드러커의 [≪매니지먼트≫](https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=976448)에서는 아래와 같이 이야기를 하고 있다.

> 가장 중요한 것은 실제로 행하는 일이다.  
  - 일과 직장에 대해 성과와 책임을 부여한다.  
  - 함께 일하는 사람들을 활용해야 할 대상으로 파악한다.  
  - 강점이 성과에 결부되도록 사람을 배치한다.   
이에 따라 사람을 활용해야 할 대상으로 보고 적재적소에 배치할 수는 있을 것이다. 또한 조직의 목표가 온전히 업적으로 향하도록 만들 수도 있다. ... 분명한 것은 신뢰와 성과가 눈에 보일 것이라는 점이다. 확신컨대 매니지먼트는 진정한 리더십으로 나아갈 수 있을 것이다.  
━ 13. 사람이 최대의 자산이다 중에서

사람을 활용해야 할 대상으로 본다는 것은 얼핏보면 거부반응이 일어날 수도 있다. 하지만 이는 정확한 표현이라는 것들을 시간이 지나면서 실감하였다. 이렇게 일을 할 수 있다면, 자연스럽게 아래의 매니저가 해야하는 일 또한 달성이 가능하기 때문이다.

> 첫 번째 역할은 투입한 자원의 합계보다 큰 것을 만들어 내는 생산체를 조직하는 것이다.  
두 번째 역할은 모든 결정과 행동에 있어 필요한 것과 미래에 필요하게 될 것을 조화시켜가는 것이다.  
━ 20. 매니저의 일 중에서

그리고 많은 사람들이 함께 일을 하면 할 수록, 수 많은 문제가 생기기도 하고 그러한 문제를 팀원들을 모두 고려하면서 푸는 것이 기본이 된다. 이때에는 감정노동이 꼭 수반된다. 한창 힘들때, 감정노동 관련해서 공감과 위로를 받았던 부분이 [≪실리콘벨리의 팀장들≫](https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=193890896) 에 있어 적어보고자 한다.

> "제 일이 훌륭한 기업을 만드는 걸까요, 아니면 감정적인 보모 노릇을 하는 걸까요?"  
"보모 노릇이 아닙니다. 그걸 관리라고 부릅니다. 바로 당신이 해야하는 일이죠!" 

특히 위의 ≪실리콘 벨리의 팀장들≫ 이라는 책에서는 '완전한 솔직함'을 기준으로 신뢰관계를 구축하는 것의 중요성을 말하고 있는데, 이러한 신뢰관계가 구축할 수 있다면 팀내의 '심리적 안정감' 역시 구축할 수 있을 것이라 생각을 한다.

여기서 '심리적 안정감'은 [≪두려움 없는 조직≫](https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=210117981), [≪함께 자라기≫](https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=175977462) 등의 책에서 많이 다뤄지는 개념이다. 김창준님이 저술하신 [≪함께 자라기≫](https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=175977462) 에 있는 구절을 적어보자면 다음과 같다.

> 구글은 데이터 중심 회사답게 데이터 기반으로 뛰어난 관리자의 특징을 찾는 옥시전 프로젝트 이후에도 뛰어난 팀의 특징을 찾기 위해 2년간 노력했습니다. 이름하여 아리스토텔레스 프로젝트 입니다.   
1. 팀에 누가 있는지 (전문가, 내향/외향, 지능 등) 보다 팀원들이 서로 어떻게 상호작용하고 자신의 일을 어떻게 바라보는지가 훨씬 중요했다.  
2. 5가지 성공적 팀의 특징을 찾았는데, 그중 압도적으로 높은 예측력을 보인 변수는 팀의 심리적 안전감이었다.  
3. 팀 토론 등 특별히 고안된 활동을 통해 심리적 안전감을 개선할 수 있었다.  
━ 구글이 밝힌 탁월한 팀의 비밀 중에서

이런 '심리적 안정감' 개선하기 위한 특별한 활동들을 해보지는 못하였는데, 다음에는 기회가 되면 이러한 여러가지 활동을 해보는 것도 많은 것을 배울 수 있을 것이라 생각한다.

마지막으로 [≪매니지먼트≫](https://www.aladin.co.kr/shop/wproduct.aspx?ItemId=976448) 에서 피터드러커가 말하는 매니저의 근본적인 자질에 대한 글로 PM 파트를 마무리하고자 한다.

> 먼저 사람을 관리하는 능력을 배워야만 한다. ... 근본적인 자질이 필요하다. 바로 성실함이다.   
조직원들에게 업무 처리를 일류로 해 낼 것을 요구하며 똑같이 엄격한 기준을 스스로에게도 적용한다. 기준을 높이 설정하고 그것을 지킬 것이라 기대한다. '무엇'이 옳은지만 생각할 뿐 '누가' 옳은지는 생각하지 않는다. 성실함보다 지적 능력을 평가하는 일도 없다. ... 매니저의 일은 체계적인 분석의 대상이다. 매니저가 할 수 있어야 하는 일은 그 대부분이 가르쳐 주지 않아도 배울 수 있는 것이다. 그러나 배울 수 없는 자질, 후천적으로 획득할 수 없는 자질, 처음부터 갖추고 있지 않으면 안 되는 자질이 한 가지 있다. 다시 말하지만 재능이 아니라 성실함이다.  
━ 20. 메니저의 일 중에서


## 대외활동

### Deview 2019 발표

![2019%204d025a4489ba4870828420f0b38f75b6/Untitled%205.png]({{ site.url }}{{ site.baseurl }}/assets/images/2019%204d025a4489ba4870828420f0b38f75b6/Untitled%205.png)

Deview 발표는 네이버로 이직을 했을 때부터 막연하게라도 생각해오던 목표 중 하나이다. 그 동안 Deview 에서 다양한 세션들을 들어오면서 한번 쯤은 발표자가 되는 것을 생각해보기도 하였고, 무엇보다 회사 내부에서 한 일을 외부에도 공유하고 알리고 싶었다. 개인은 물론이고, 팀의 기술력 또한 홍보할 수 있는 아주 좋은 기회이기에..!

[엄~청 큰 언어 모델 공장 가동기! (LaRva: Language Representation by Clova)](https://deview.kr/2019/schedule/291) 

위에서 다루었던 LaRva 프로젝트에 대한 발표였고, 굉장히 많은 분들께서 자리를 채워주셔서 BERT 라는 모델의 영향력이 어느정도 인지 실감할 수 있었다. 발표자료를 준비하면서.. 조금이라도 더 의미있는 시간으로 만들고 싶어서 욕심을 부리다보니.. 발표자료가 총 109장이 되었었다. 막상 발표 떄는 장수에 비해서 조금 빨리 마무리하기는 하였지만 그래도 잘 마무리 했다고 생각을 한다.

아쉬웠던 점은 결국, BERT 모델을 학습할 수 있는 것은 개인으로는 어려움이 있고 기업 특히, GPU 리소스가 풍족한 곳에서 가능한 일이기에 많은 분들에게는 실효성이 조금 적었을 수 있다. 이 분야에 종사하고 있는 분들에게는 도움이 될 수 있겠지만, NLP에 관심이 있는 정도라면.. 조금은 멀게 느껴졌을 수도 있다고 생각이 된다.

그래도 발표를 준비하면서 청중이 누구인지, 그리고 발표의 흐름이 매끄럽게 잘 이어지는지, 각 페이지의 설명이 충분한지, 시간 배분 등.. 이러한 다양한 포인트에 대해서 피드백도 받고 준비를 하면서 많이 배웠다고 생각한다. 20년에도 이렇게 인사이트를 공유할 수 있었으면..!


## Quantified Self

### 주간 작업 리포트의 변화

약 3~4년 전에 사이드 프로젝트로 [kino-bot](https://github.com/DongjunLee/kino-bot) 이라는 나 자신의 데이터를 수집하고, 반복되는 일들을 자동화 시켜주는 개인용 봇을 만들면서 계속해서 데이터를 수집해오고 있었다. 그 중 하나가 생산성을 측정하기 위해, 진행하는 일들에 대해서 시간을 기록하는 것이다.

Task의 카테고리들은 아래와 같다.

- Seminar: 스터디, 강연 등
- Review: 명상, 일기, TIL 정리, 회고, Deview 발표연습 등
- Research: 논문을 포함한 연구관련 작업들
- Develop: 개발관련 작업들
- Planning: 계획
- Meeting: 미팅..
- Management: 프로젝트 관리에 해당하는 일들 (e.g. 칸반보드, 스크럼 운영, 문서 정리, 커뮤니케이션 등)
- Exercise: 운동 (산책, 자전거 출퇴근, 요가, 근력 등)
- Book: 종류에 상관없이 책을 읽는 경우
- Article : 새로운 정보들을 확인하는 경우 (RSS 피드, 뉴스레터, 블로그, Reddit 등등)

![2019%204d025a4489ba4870828420f0b38f75b6/Untitled%206.png]({{ site.url }}{{ site.baseurl }}/assets/images/2019%204d025a4489ba4870828420f0b38f75b6/Untitled%206.png)

위 차트들은 주 단위의 Task 로서, 월요일부터 일요일까지의 Task들의 시간을 Stacked Bar Chart로 보여준다. 위 카테고리에 해당하는 시간들을 생산적인 일에 사용했다고 가정하고 시간을 기록해오고 있다.

이 차트를 보면, Role의 변화를 체감할 수 있다. 19년 초반에는 주로 `Develop` 에 대한 일들이 많았다면, 점점 시간이 지나면서.. 8월부터는 `Management` 라는 카테고리가 추가되기 시작했으며.. 시간이 갈수록 `Meeting` 과 매니징의 시간이 늘어나고 개발에는 시간을 사용하지 못하는 모습을 보이고 있다. 

실제 `Management` 와 `Meeting` 만 따로 뽑아보면, 아래와 같은 양상을 보인다. 뒤로 갈수록 개발에는 시간을 쓰기 어려워지면서 시간에 대한 고민과 커리어에 대한 고민이 계속 되었던 것이 기억이 난다.

![2019%204d025a4489ba4870828420f0b38f75b6/Untitled%207.png]({{ site.url }}{{ site.baseurl }}/assets/images/2019%204d025a4489ba4870828420f0b38f75b6/Untitled%207.png)

### 생활 습관을 만든다는 것

Quantified Self로 사이드 프로젝트를 진행했던 이유 중의 하나는 습관이 한 사람에 대해서 가장 많은 것을 설명할 수 있는 단면이라고 생각하기 때문이다. 이러한 습관이 가지는 꾸준함을 개인적으로는 굉장히 중요하게 생각하는데, 꾸준함이 끝내는 변화를 만들어낸다고 생각하기 때문이다. 이 글 ([습관은 자신의 참 모습을 보여주는 창이다](https://newspeppermint.com/2019/04/02/m-habitus/))은 내가 바라보는 습관에서 잘 말해주고 있어서 덧붙인다.

여기서 특별히 신경을 쓰고 있는 생활 습관은 아래 3가지 이다.

1. Exercise : 운동
2. Diary : 일기
3. BAT : Today I Learnd 오늘 배운 것을 정리

**19년 3월**

![2019%204d025a4489ba4870828420f0b38f75b6/Untitled%208.png]({{ site.url }}{{ site.baseurl }}/assets/images/2019%204d025a4489ba4870828420f0b38f75b6/Untitled%208.png)

**20년 3월**

![2019%204d025a4489ba4870828420f0b38f75b6/Untitled%209.png]({{ site.url }}{{ site.baseurl }}/assets/images/2019%204d025a4489ba4870828420f0b38f75b6/Untitled%209.png)

19년도에는 BAT(Today I Learned)를 해야지해야지 했지만.. 제대로 된 작업을 진행하지 못했던 때이다. 그래도 일기와 운동은 19년도나 20년도나 꾸준히 진행 중에 있다. 이 글을 작성하는 지금은 20년 5월인데, 지금은 어느정도 습관으로서 자리가 잡혀있는 상태이다.

위의 Heatmap은 했다/안 했다 의 유무만 보여주고 있지만, 실제로는 시간도 꾸준히 트랙킹을 하면서 적정 시간을 유지할 수 있도록 노력하고 있다.

![2019%204d025a4489ba4870828420f0b38f75b6/Untitled%2010.png]({{ site.url }}{{ site.baseurl }}/assets/images/2019%204d025a4489ba4870828420f0b38f75b6/Untitled%2010.png)

위의 3가지 요소 말고도 한가지 더 신경을 쓰는 카테고리는 'Book' 이다. 책 읽는 시간은 현재 4~6시간은 주에 사용할 수 있도록 노력 중이다! 

(11월 쯤에 있는 `Review` 가 아주 높은 주는.. Deview 준비의 흔적으로 보인다!)

### 마무리

개인적으로 19년은 굉장히 다사다난하기도 했고, 커리어적으로도 큰 변화가 있었던 해이다. 

새로운 경험 또한 할 수 있었으며.. 무엇보다 좋은 사람들을 만나고, 프로젝트에 대한 결과까지 만들어 낼 수 있었기에 만족하는 해이기도 하다. 물론 수 많은 고생들이 있었지만, 되돌아 보았을 때는 추억으로 되는 것처럼 좋은 기억들이 남아있다.