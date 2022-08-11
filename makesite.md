## Sign Up Screen part One
- 코딩에서 index : 첫번째 // index.html : 첫번째 페이지
- '!'키: html구조를 한번에 생성
- 사용자가 css를 볼때 단순히 class="column"이라고 써있으면 어느부분의 column인지 파악하기 어렵기때문에 class명은 알아볼 수 있게 정함.

## BEM 
BEM(block element modifier)
- 사용자가 소스코드를 더 쉽게 알아볼 수 있다.
- class만을 이용한다.
- ex).btn {} : btn 클래스에 적용// .btn__price{} : btn안에 price가 있다. //.btn--orange {} : btn을 orange색으로 변경한다.

## Icon Site
- 아이콘 관련 사이트 : Heroicons, FontAwesome 참고->html코드(Script) 복붙
- 스크립트는 항상 마지막에 배치되어야 한다.(body안의 맨 밑)  

## Sign Up Screen part Three
- reset CSS 활용 //모든 CSS 요소를 초기화함.
- text-align : center..  // h1, p같은 text를 옮길때 사용
cf) opacity: 투명도

## Log In Form
- :not([type="submit"p]){}  //  type이 submit이 아닐때 ~ 적용 // ex) input:not([type="submit"]) {}
- cursor :pointer // 버튼에 마우스 갖다대면 마우스 모양변경

