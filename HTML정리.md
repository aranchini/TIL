# HTML
**HTML**
- 웹페이지를 구성하고 있는 요소 하나하나를 태그 라는 표기법으로 작성한다.
- 태그를 통해서 어떤 요소인지(제목,이미지,비디오 등) 명시한다.
- 태그의 이름은 HTML5 웹 표준에 맞게 작성한다.
> 여는 태그 & 닫는 태그는 사용자에게 보이지 않고 개발자가 명시하기 위한 용도이다.

**HTML의 기본 구조**

```
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Document</title>
</head>
<body>
    
</body>
</html>
```
**`<!DOCTYPE html>`**<br>
- 문서 형식 선언
- DOCTYPE는 해당 문서가 어떤 마크업 언어 형식으로 작성되었는지를 명시하는 역할을 함
-  DOCTYPE의 뒤에 HTML이라고 쓰여있는것은 "이 문서는 HTML5로 작성되었습니다." 라는걸 뜻함

**`<html>`**<br>
- 웹페이지 전체를 감싸는 가장 바깥 태그
- 브라우저에게 이 안에 있는 모든게 HTML 코드라는걸 알려줌


**`<meta>`**
- 웹 페이지의 추가 정보를 설정하느 태그
- 문자 인코딩,화면 크기 등을 설정함<br>
  `charset="UTF-8" ->` 한글 깨짐 방지<br>
  `viewport` -> 모바일 화면 맞춤


**`<hrml lang="en">`**
- lang 속성은 페이지의 언어를 설정함<br>
  > (예: en=영어, ko=한국어)
  
  
**`<head>`**
- 웹페이지의 정보를 담는 영역
- 브라우저에 문서의 정보를 전달함

**`<title>`**
- 웹페이지의 제목을 정하는 태그
- 반드시 <head> 안에 들어가야함
- 사용자가 보는 탭 이름
  
  

**`<body>`**
- 사용자가 보는 영역
- 웹 브라우저 화면에 표시될 콘텐츠를 입력하는 태그



  
