# 자바 삽질의 기록 2009.08

2010-11-28 13:23

MS .NET 이 2001 년도에 소개되서 2002 년도까지 회사에서 .NET 제품들을 만들다가 퇴사하고 만든게 레이소다다.
레이소다 기반을 2003 년도에 잡았으니 .NET 1.0 이었다.
내년 봄이면 .NET 4.0 이 나온다.

꽤 오랜 기간 MS 기술을 사용해와서 큰 모험을 하지 않아야겠다는 생각에
2008 년부터 처음 배우는 기분으로 .NET, C#, ASP.NET, SQL 다시 차곡차곡 읽었다.
LINQ 란 ORM 이 생겨서 데이터베이스 억세스 하는 패턴이 많이 바뀌었다.

2003 년도 당시 사용되던 ASP.NET 컨트롤 모델, 아직도 유용하긴 하지만 MVC 라는 심플 모델이 나와서
프로토타입 사이트 만들어보고 뼈대를 이쪽으로 하기로 했다.
불필요한 컨트롤 라이프 사이클이 사라지고, PostBack 도 생각보다 잘 구현되고, 매우 명쾌하다.

너무 나도 많은 것들이 쏟아져나와 있어서,
무엇이 있는지 파악하는 데만도 겨울이 그냥 지나갔다.

쓰던 MS 계열 기술 계속 쓰는 것에 마음이 편하다가도,
이번 결정이 또 앞으로 10 년간 영향을 미칠 것이란 생각에 주저하다가,
그렇게 시간이 계속 갔다.

고민만 하다가는 망하겠다는 생각에,
먼가 코딩을 시작한 것이 5 월 중순이었다.

6 월 초가 되니 LINQ + MVC 틀로 기본 기능 그럭저럭하는 실험 사이트가 나왔다.
새로 익혀서 이정도 만들었다는데 자신이 좀 붙기 시작했다.

그런데, 6 월초, MS 에서 F# 을 공식지원하겠단 발표를 한다.
C# 은 절차지향적 언어이고, F# 은 함수지향적 언어다.
그 뿌리는 100 년 가까이 전으로 거슬러 올라가는데,
FP 언어들은 변수라는 것을 상정하지 않기 때문에 로직이 폭포수 같이 흐르고,
수식이 정의된 곳이 아니라 사용되는 곳에서 실행된다는 매력적인 개념을 가지고 있다.

FP 관련 기본 개념, F# 문법, 기반 라이브러리 읽는데 3 주가 지났다.
C# 으로 만들었던 실험 작업을 F# 으로 그대로 옮겨서 실행도 끝냈다.

F# 의 단점도 많은데 Partial Class 지원이 안되서 Rad Tool 도움을 못 받는다.
LINQ 대응 문법이 너무 실험적인 상태라 사용할 수가 없다. Model 파트는 C# 코드를 유지해야한다,
Exception, Delegate, Event 모델이 C# 에서 쓰는 그것과 이름만 같고 내부 구현이 완전 다르다.

F# 이 언어적으로 무척 훌륭하긴 하지만
기존 .NET 문화의 지원을 그대로 받을 수 있는 C# 의 장점을 간과할 수가 없어서 한참 또 고민을 했다.

F# 쓰면어 얻은 큰 이득은 복잡한 것을 단순하게 표현하는 펑셔널 프로그래밍의 문법적 능력을 배웠다는 것인데,
F# 을 계기로 관심이 자연스럽게 다른 FP 나 멀티패러다임 언어들로 옮겨갔다.

꼭 .NET 기반이어야 한다는 생각을 버리고, 여기 저기 여행을 하다가 Ruby 를 보게되었다.
일본인이 만든 스크립팅, 다이나믹, 멀티페러다임, 펑셔널 언어인데 귀엽고 매우 인상적이었다.
사실 Ruby 란 단어를 본 것은 수년 전인데, 그것과 인연을 맺기까지 시간이 많이 걸렸다.

Ruby 로 한 젋은 총각이 Rails 라는 웹 개발 프레임웍을 만들었단다.
비디오로 시연을 보는 순간 허걱 소리가 나왔다.
이것 저것 읽기 시작하다가 며칠 그대로 빠져 살았다.
C# / F# 은 까마득해져 갔다.

큰 장애물을 만났다. Ruby 기반 캐릭터 시스템이 1 바이트란다.
UTF16 을 쓰지 않는 21 세기 언어 시스템이라니.

자바로 루비를 구현한 JRuby 라는 것이 있다.
자바는 태어날 때부터 UTF16 을 사용했는데,
황당하게도 자바로 루비를 구현한 JRuby 에서는 UTF16 을 안 쓴단다.

돌다 돌다 C# 으로 돌아왔다.
7 월이 되었다

이때 잊고 있던 Silverlight 새 버전 3.0 이 발표되었다.
2.0 까지 스펙상 여러 가지 한계가 있어서 자세히 들여다 보지 않았는데,
3.0 부터 지원 기능들이 매우 풍부해졌다.

얼핏 사이트 전체를 실버라이트로 만들어도 되겠단 생각이 들었다.
2 주 실버라이트 문서에 또 빠져살았다.

2 주 삽질한 결론으로, XAML 이 과도하게 복잡하다.
기존 데스크탑 어플리케이션 개발하면서 WinForm 디자인하던 것 비하면 XML 출력이 더 좋아진 면이 있지만,
HTML 개발 환경에 있던 사람들 기준에는 너무 난잡하고 이해하기 힘든 시스템이었다.

웹 문화를 그대로 구현하는데 문제점이 있는 것도 걸렸고,
표현 면에서도 예쁘장한 컨트롤만 많을 뿐,
웹 브라우저에 비해 정보를 간단히 흘려 나타내는 랜더링 능력이 한참 못미쳐 보였다.
작업량을 줄여주는 것이 아니라 늘린다는 것도 걸렸다.

RIA 관련 미련을 못 버려서 Adobe Flex 를 보기 시작했다.
플래이어 배포에 일단 문제가 없고, MXML 이 XAML 보다 실용적이긴 했는데,
근본적으로 비슷한 기술이고 실버라이트가 가졌던 한계들이 그대로 남아 이것도 일주일 만에 포기했다.
HTML 이 가진 대중성을 놓고 가기에는 플랙스의 장점이 중요하지 않았다.

Adobe 갔다가 오랜만에 ColdFusion 을 보았다.
이것을 처음 만났을 때는 알레어사 제품이었는데 매크로미디어를 거쳐 현재는 아도브에서 판매하고 있다.
10 년간 뭐가 좋아졌나 다시 들여다 보기 시작했다.

지금도 국내에서는 쓰는 사람이 거의 없는 것 같았고,
가격은 그당시에 비해 3 배나 올라 천만원 가까이 한다.

대신 신기하게도 ColdFusion CFML 과 98% 호환된다는 오픈 소스 제품들이 있다.
이것을 기반으로 쓸까 하는 생각에 혹해 잠시 또 열심히 보다가,
아 세상에, 그간 SQL Injection 해킹 기법이 유행했다는 사실을 다시 떠올리게 되었다.

쿼리를 태그 사이에 자연스럽게 넣어 적는 것이 CFML 의 장점이었는데, SQL Inj 때문에 그게 어렵게 되었다.
알레어 ColdFusion 을 쓸 때는 C 로 제작된 제품이었는데, 요즘은 자바로 만드나 보다.

자바로 처음 프로젝트를 진행한 것은 1995 년 겨울이었다.
자바를 보고는 미래는 이거야라는 생각을 하고 간단한 데모 애플릿들을 제작해서
계획없던 사이트에 슬쩍 붙여 시연을 했는데,
어쩌다 저쩌다 자바 관련 영업이 승인 받는 바람에 6 개월 짜리 자바 프로젝트를 맡았다.

6 개월 프로젝트가 우여곡절 끝에 1 년 반짜리가 되고,
불안정한 플랫폼 때문에 너무 고생을 해서, 그것을 끝으로 자바는 안 보기로 했었다.

거의 15 년만에 보는 자바는 그대로인 면도 있었지만, 무엇인가 산더미처럼 생겼다.
세상에 내가 기억하는 그 안 좋은 자바를 쓰는 사람들이 끝없이 늘어서,
최근 통계를 보니 전 세계 프로그래머중 20% 가 자바를 사용한단다.
인구수로 보면 1 위다.

지난 주부터 열흘 정도 자바 관련 문서들을 있는데로 읽고, 가능한 이것 저것 테스팅하고 있다.
자바 플랫폼 안정성은 매우 좋아진 것 같다.
하루에도 몇 번씩 보던 세그멘테이션 폴트가 사라졌다.

1995 년 당시 NT 에서 도스창 열고 qedit 로 클래스 파일 80 개 짜리 작업하던 기억이 마지막인데,
넷빈즈나 이클립스 같은 IDE 도 생겼다.

Java EE 는 먼가 많이 들어있긴 한데, 너무 복잡하고 산만해 보인다.
Xml 정의 작업이 너무 많아서 이거 집중하고 코딩할 수 있겠나 싶고.

Jetty 웹 서버가 좀 인상적이었는데, 용량 8 메가에, 설정도 간출하고,
앞으로 쓸 기술 목록에 이걸 꼭 넣어야겠다는 생각을 하고 있다.

jQuery 쓰면서 자바스크립트를 재발견하게 되었다.
서버 사이드도 자바스크립트를 쓰면, 브라우저, 서버, 플래쉬까지 언어가 통일되니 좋지 않겠나 싶었는데,
Phobos 라고 관련된 서버 기술이 오픈 소스로 제공이 된다.

이 때쯤이 되니 마이크로소프트 기술들은 마음에서 너무 멀어져 버렸다.
Java 가 효율적이어서라기 보다는 작아서 부담이 없고, 부품이 다양하고,
MS 기술들에 비해 갈아끼우기가 좋아서, 선택의 여지가 많아보인다.

15 년만에 다시 자바를 하게 되는구나 싶다.

단지, 이 때까지는 먼가 이거다 하는 것은 아직 발견하기 전이었는데,
며칠 전에 Groovy on Grails 를 보게 되었다.
어, 어디서 많이 듣던 발음, Ruby on Rails 하고 닮지 않았는가.
아, java 로 이식된 Rails 패턴이다.

오늘은 2009 년 8 월 1 일이고,
작년 8 월부터 읽었던 것을 모두 버리고,
Groovy on Grails 로 작업을 다시 쓰고 있다.