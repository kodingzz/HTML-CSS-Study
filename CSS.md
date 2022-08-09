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
-id와 다르게 여러 요소들에서 사용할 수 있다.
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


