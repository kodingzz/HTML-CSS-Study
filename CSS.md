## How to Add CSS to HTML 
### HTML파일에 CSS파일 연결하는방법(2가지)
1. style태그안에 CSS 내용 적기
2. 별도의 css파일을 만들고 HTML파일안에 link태그로 연결한다.(이때 rel="stylesheet", href="~.css")  // rel은 link의 속성

## Writing Our First CSS Lines 
### css 작성법
1. html태그와 이름이 동일해야한다.
2. 속성이름은 띄어쓰기x, 끝은 항상 세미클론으로 끝나야한다. 
ex)
selector {
속성명 : 속성값
}
## What Does Cascading Mean
- CSS (Cascading style sheet)
- 뜻그대로 CSS는 위에서 아래로 실행된다.
- 외부 CSS파일과 html파일안의 CSS가 같은 태그를 가리킬때 가장 밑에있는 코드가 적용된다.

## Blocks and Inlines
- block 은 옆에 다른 것이 올수 없다.
- inline(in the same line)은 옆에 다른것들이 올 수 있다.
- inline tag: span, a, img ...

## Margin Part One
1. margin이란 box의 경계로부터 바깥에 있는 공간이다.
2. inline은 높이와 너비가 없다.
3. block은 높이와 너비가 있다.
4. block->inline으로 바꾸기 // display:inline
5. inline->block으로 바꾸기 // display:block

## Margin Part Two
1.margin:???
- 값이 한개면 상하좌우 모두적용
- 값이 두개면 첫번째는 상하, 두번째는 좌우로 적용
- 값이 네개면 왼쪽부터 상, 우, 하, 좌로 적용
2.collapsing margin
- div 상하 경계와 body 상하 경계가 같을 때 일어나며 그 때 두 box의 margin은 하나가된다.
- 수직으로만 발생한다.
## Paddings and IDs
- padding: box 경계로부터 안쪽에있는 공간
- css에서 id 적용하는 방법: #id명 {}
## Border
- box의 경계를 표시해주는 역할
- 입력은 너비, 스타일, 색깔 순 // ex) border: 2px solid black;
- *: 전체를 뜻함
- border은 inline과 block모두 적용된다. 

## Classes
### inline
- 높이와 너비를 가지지 않기 때문에 위,아래 margin을 가질 수 없다.
- padding은 가능하다.
- 상하를 적용하기 위해서는 inline을 block으로 변경해야한다.
### class
- id와 다르게 여러 요소들에서 사용할 수 있다.
- css에 표기법 -> .class명 {} // ex) .tomato {}
- 한번에 여러클래스가 쓰일 수 있다. ex) class="tomato, apple, grape.."( id는 불가능)

// 여러코드 한번에 수정하는법: 원하는곳 클릭후 ctrl+d(윈도우)
## Inline Block
- display: inline block
- block으로 인식하지만 높이도 가질수 있고 margin도 가지며 옆에 다른요소들이 올 수 있다.
### 단점
- 정해진 형식이 없다.(box사이에 빈공간이 생긴다)-> 잘쓰이지 않는다.
- 반응형 디자인을 지원하지 않음 ==> 창 크기가 달라지면 그 때마다 변경해줘야 한다.

## Flexbox(박스나열에 용이)
### part one
- 부모 요소에만 사용할 것, 자식 요소에는 사용하지 말 것 // div의 부모인 body에 사용
- 부모요소에 display: flex -> flex container가 된다.
- flex container는 두개의 축을 가지고있다.(주축,교차축)
- justify-content(default 수평): space-evenly, space-around, space-beteween등이 있다.
- 기본적으로 주축은 수평, 교차축은 수직이다.
- align items(default 수직)는 교차축에있는 item들을 움직인다.
- 그러나 body에 height을 주지 않으면 align-items는 쓰나마나임.
- height : 100vh; 에서 vh는 viewpoint height 줄임말 // 화면높이의 100%
### part two
#### flex-direction
- default 값은 row이며 , column으로 하면 주축이 수직이된다.
- column-reverse, row-reverse // 축의 진행방향을 바꾸어준다.
#### flex-wrap
- flex-wrap: nowrap; (모든 요소를 같은 줄에 있게 만들어 줌)
- flex-wrap: wrap; (모든 요소들을 최대한 같은 줄에 있게 하고 그게 안되면 다음 줄로 넘김)
- flex- wrap: wrap-reverse도 존재한다.

## Fixed
- 다른 요소들과 있을 때 가장 위에 있음.
- position:fixed // box가 제자리에 고정되어있는것
- 스크롤해도 항상 제자리에 머무른다.
- top,left,right,bottom 변경 시 인접한 요소 위치에 영향받지 않는다.
- 서로 다른 레이어에 존재하기 때문이다.

## Relative Absolute 
### position
1. static
- 박스를 처음위치하는곳에 두는것이다.
2. relative
- top, left, right, bottom을 이용하여 요소가 처음위치한 곳에서 위치 변경한다.
3. absolute
- 가장 가까운 relative를 가진 부모를 기준으로 이동한다. // relative를 설정한 부모가 없다면 body가 부모가 되어 기준이된다.

## Pseudo Selectors part One
1. last-child{} // 마지막 자식 선택
2. first-child{} // 첫번째 자식 선택
3.nth-child(숫자) {} // 원하는 순서의 자식 선택
4.nth-child(even,odd) {} // 짝수or홀수 자식 선택
5.nth-child(2n+1)
- 선택자의 2n+1 요소 선택
- n은 0부터 대입하는 것으로 추측

## Combinators
1. p span {} // p안의 span을 찾는다.
2. div > span {} // div안의 바로 밑 span을 찾는다.
3. p+ span {} // p다음에 오는 span을 찾는다.
cf) '>'는 자식을 찾는 기호이고 , '+'는 형제를 찾는 기호이다.

## Pseudo Selectors part Two
1. p ~ span {} // span이 p의 형제이고 span 바로 뒤에 오지 않을때 적용
2.input:required {} // input 속성이 required인 경우 적용
3.input[placeholder~="name"] {} //input 속성 placecholder가 name을 포함하는 경우 적용
+) a[href$=".org"] {} // href가 org로 끝날때 적용
+)class를 추가할 필요가 없다.

 ## States
1. active // 버튼을 누르고 있으면 적용
2. hover // 버튼에 마우스를 대고있으면 적용
3. focus // 키보드로 선택되었을때 적용
4.visited // 링크에만 적용되며 링크를 클릭하면 방문했다고 표시
5.focus-within// focused인 자식을 가진 부모 엘리먼트에 적용  ex) input이 focused되면 부모인 form이 적용
## Recap
- input::placeholder {} // placeholder를 스타일링한다.
- p:: selection{}  //p안의 내용을 선택할때 스타일링한다.

## Colors and Variables 
### css에서 알아야할 컬러 시스템
1. 16진수 컬러 ex) #FFCCE00
2. rgb ex) rgb(252,206,0) // cf) rgba : 투명도 rgba(252,206,0,0.4)
- :root{--main-color :색깔}
- root은 기본적으로 모든 document의 뿌리.  여기에 변수이름을 쓰고 --main-color라고 변수이름을 주고 이것을 document의 root에 저장하는것이다.
- 변수를 사용할때는 var(--main-color)
3. border색을 root에 저장하는것도 마찬가지
- ex) :root{--default-border: 1px solid var(--main-color);}

## Transitions
- 어떤상태에서 다른상태로 변화하는것을 애니메이션화한것
- state(ex.hover)가 없는 곳에 transition적용해야한다.
- 형태 // transition : background-color 10s ease-in-out;  -> 10초동안 ease-in-out형태로 변경된다.
- transition : all 5s ease-in-out; // 모든 속성을 5초동안 변경

## Transitions part Two 
### ease-in-function
- 브라우저에게 애니메이션이 어떻게 변화하는지를 알려준다.
1) linear: 요소를 직선으로 움직이게 만들어줌. 같은 속도로 움직임.
2) ease-in: 처음에 좀 더 빨라지면서 움직임.
3) ease-out: 끝에서 느려짐.
4) ease-in-out: 처음에 느렸다가 중간에 가속했다가 끝에 느려지면서 끝남.
5)cubic-bazier : 사용자가 직접 애니메이션을 만들어 적용

## Transformations
1. rotate (x ,y,z축 회전), rotate3D
2.scale(X,Y,Z축으로 늘리거나 줄이기)
3. translate 사진 위치 변화
4. transition은 root에 있어야한다. state에 있으면 안된다.
5. color나 border-radius처럼 변화시킬 내용을 state에 적는다.
이외에도 skew, matrix..
cf) transform mdn 검색

## Animations part One
마우스의 움직임이나 transition없이 애니메이션이 일어나는 방법
ex)
@keyframes coinflip {
from {
transform: rotateX(0);
}
to {
transform: rotateX(360deg);
}
}
형태로 하나의 animation을 만든다.
- 하나의 transform에 다양한 기능들을 넣을 수 있다. // roatate,translate,scale...

## Animations part Two
@keyframes coinflip {
0% {
transform: rotateX(0);
}
50% {
transform: rotateX(360deg) translateX(1000px);
}
100% {
transform: rotateX(0);
}
}
-> 0~360도 회전하고 1000px만큼 우측으로 이동하는 애니메이션이 끝나도 툭툭끊기지않고 처음 위치로 자연스럽게 돌아간다.

cf) CSS animations 검색

##  Media Queries
- media query : 반응형 웹사이트 만들 때 사용
- 조건을 추가할수있는 방법(코드의 조건)
- and를 써서 연결한다.
- media query안에 원하는 css를 넣는다. 
- @media print // 스크린을 프린트할때 사용
