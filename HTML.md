# What makes a Website?
## HTML(Hypertext Markup Language)
- content(내용)-> title, link, imag등 content의 구조를 설명해준다.
- 브라우저는 우리 언어를 잘 이해못해서 content를 알려줘야 함. 그래서 HTML 사용함.
- 웹사이트의 뼈대역할을 한다.

## CSS(Cascading Style Sheets)
- 브라우저에게 웹사이트가 어떻게 보여줘야 하는지 알려줌  ex)제목의 색깔
- CSS는 혼자 사용할 수 없음.
- 웹사이트의 근육역할을 한다.

## JS(javaScript)
- 웹사이트의 뇌역할을 하여 동작을 담당한다.
- interactivity

# Learning HTML
## HTML 파일
- 파일,폴더명은 소문자여야한다.
- Vs code를 사용해 변경사항이 생길때마다 바로바로 저장해야한다. 저장방법은 window: ctrl+s

## HTML TAG
- tag의 기본구조:
- tag는 한번 열면 반드시 닫아야한다. 
- 브라우저는 tag로 이해한다.
- h1~h6: title을 표시. 점점 글자크기가 작아진다.
- ul: unordered list (순서 없는 리스트)
- ol: ordered list(순서 있는 리스트)
- li: list item(항목들)
- src: 이미지 tag
- a(anchor): 링크 tag 

## tag attributes(태그에 추가하는 속성)
### a tag의 attributes : href , target
- href="링크주소"
- target : _self 는 현재 탭에서 url 이동, _blank는 다른 탭을 열어서 화면을 띄움
- ex) <a href="http://google.com" target="_blank">Go to google.com</a>

### img(이미지)는 self-closing tag라서 닫는 태그('/')가 없음. 
- src : 주소나 파일 경로를 넣으면 해당 이미지가 나타남. / 이미지 tag

## More Tags and Head
1. 내가 가지고있는 이미지도 올릴수 있다.  ex) img src="ddd.jpg"
2. 이미지가 폴더안에 들어있다면 ex) img src="img/ddd.jpg"
3. html로 감싸고 그 안에 head와 body 존재
4. head는 웹페이지 환경설정(보이지 않는 기본 설정)  
5. body는 웹페이지에 보여질 내용설정  

## Its All About the Head 
### head의 태그및 속성들
1. link / rel: shortcut icon , href="링크(아이콘그림)  
2. meta / charset : utf-8(사이트에서 텍스트가 어떻게 그려지는지 알려주고 한글이나 특수문자 등을 깨지지 않게 해줌.)
3. meta / description:(google이 검색할 때 찾는 태그), content 

## More Tags  
### 다양한 태그 이용(다 못외운다..)
- p : 단락 구분
- abbr : 툴팁같이 나타남  ex) <!--<p>My name is <abbr title="KIM HYUN WOO">KHW</abbr></p> -->
- audio: 오디오 파일 실행해주는 태그  / 속성: controls, autoplay, src="소리 링크"  

## Form Tags
### form 태그 공부  
#### input 태그  
- 속성) type: 유형 설정 ex) file,color,email, date, file,password,submit.. 
- accept: type이 file인 경우 업로드할 수 있는 확장자 제한 / required : 필수 입력/ placeholder : 힌트 표시 / minlength: 최소길이 
#### label 태그  
- 속성: for="~"
- lable의 for 속성과 input의 id를 같게 하면 label을 누르면 id로 연결된 input에 반응한다.
- id는 유니크 해야하고, 한 태그당 하나의 id
