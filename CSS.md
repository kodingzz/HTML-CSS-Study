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
