# CSS

실제 프로그래밍 언어는 아니고<br><mark>HTML 문서의 색상,폰트,레이아웃 등 화면 표시 방식을 지정하는 스타일 시트 언어</mark>

### 기본 문법
CSS의 기본 문법은 **선택자(selector)** 와
**선언 블록**으로 구성됨

**선택자**<br>
- 선택자는 HTML 요소를 선택하여 스타일을  적용할 대상을 지정함
> 이는 HTML 태그 이름,클래스,ID 등이 될수 있음

**선언 블록**
- 중괄호 { }안에 위치함
- 하나 이상의 선언 포함
- 각 선언은 속성과 값으로 구성됨 
- 콜론( : )으로 구분함
- 여러 개의 선언은 세미콜론( ; )으로 구분함

## 선택자
스타일을 적용할 HTML 요소를 지정하는데 사용됨.<br>
다양한 유형의 선택자가 있고 각각은 서로 다른 방식으로 요소를 대상으로 함.

1. **요소(태그) 선택자**
    - 이는 HTML태그 이름에 해당하는 요소를 대상으로 함
        > ex) p 선택자는 모든 `<p>` 요소에 스타일을 적용한다.
    ```
    p {
        color:blue;
    }
2. 클래스 선택자
    - 특정 클래스 속성이 부여된 요소를 대상으로 함
    - 점(<code>.</code>) 기호와 클래스 이름을 사용하여 지정함
    ```
    .myclass {
        color: red;
    }
    ```
3. ID 선택자
    - 특정 ID 속성이 부여도니 단일 요소를 대상으로 함
    - 해시(<code>#</code>)기호와 ID 이름을 사용하여 지정
    ```
    #myid {
        color: green;
    }
    ```
4. 속성 선택자
    - 특정 속성을 가진 모든 요소들을 대상으로 함
    ```
    input[type="text"]{
        background-color: yellow;
    }
    ```
5. 가상 클래스 선택자 및 가상 요소 선택자
    - 특별한 상태의 HTML요소나 페이지의 일부분에 스타일을 적용하려 할때 사용함
- 가상 클래스 <br>
    1. 마우스 커서를 올렸을 때
    ```
    a:hover{color:orange;}
    ```
    2. 포커스를 올렸을 때
    ```
    input:focus { border: 2px solid blue; }
    ```
    등이 있음
- 가상 요소<br>
    1. 내용 앞에 추가
    ```
    p::before{content:"주의!";}
    ```
    2. 내용 뒤에 추가
    ```
    p::after{content:"끝";}
    ```

6. 조합(복합)선택자
    - 여러개의 선택자를 조합하거나 그룹화하여 복잡한 조건에 맞추거나 코드 중복을 줄일수있음
- 그룹 선택자
    - 여러 요소에 같은 스타일을 동시에 적용할 때 쉼표( , )로 구분 함
    ```
    h1,h2,p{text-align:center;}
    ```
- 교차(일치 선택자)
    - 선택자들을 붙여 써서 모든 조건을 동시에 만족하는 요소 선택.<br><br>
    <i>클래스가 error인 p 태그만 적용</i>
    ```
    p.error{color:red;}
    ```
    
7. 계층적인 선택자
    - 자식,후손,형제,인접 등과 같은 계층적 관계에 따라 HTML요소들을 대응할 수 있음
- 자식 선택자 (>)
    - 부모 바로 아래에 있는 직계 자식만 선택함<br>
    ```
    ul > li{list-style: none;}
    ```
- 후손 선택자(공백)
    - 부모 안에 포함된 모든 하위 요소를 선택함.<br><br>
    <i>div 안의 모든 p태그</i>
    ```
    div p{color:gray;} 
    ```

- 인접 형제 선택자(+)
    - 특정 요소 바로 뒤에 오는 형제 요소 하나만 선택.<br><br>
    <i>h1 바로 다음에 오는 p 요소 딱 하나만 선택</i>
    ```
    h1+p{margin-top:0;}
    ```
    

- 일반 형제 선택자(~)
    - 특정 요소 뒤에 오는 모든 형제 요소들을 선택함<br><br>

    <i>h1 뒤에 나오는 p 요소들을 한꺼번에 선택</i>
    ```
    h1~p{color:blue;}
    ```
## 기초 스타일링

1. **글꼴 속성**

    ```
    body{
        
    font-family:"나눔 고딕","궁서체"; 글꼴 설정 (없을 경우 대비해 대체글꼴 지정)
    font-size: 16px;                글자 크기 (px, em, rem 등 사용)
    font-weight: bold;              글자 두께 (normal, bold, 100~900)
    font-style: italic;             글자 기울임 
    line-height: 1.5;               줄 간격 (보통 1.4 ~ 1.6이 가독성이 좋음)
    text-align: center;             텍스트 정렬 (left, center, right, justify)
    text-decoration: none;          밑줄 등 장식 제거 (a 태그 밑줄 없앨 때 필수) 
    }
    ```

2. **색상 속성**

    ```
    h1 {
    color: red;            글자 색상 (색상 이름)
    color: #ff0000;        16진수 코드 (Hex) 
    color: rgb(255, 0, 0); RGB 값
    opacity: 0.5;          요소 전체의 투명도 (0: 투명 ~ 1: 불투명)
    }
    ```

3. **배경 속성**

    ```
    .container {
    background-color: #f4f4f4;        배경 색상
     background-image: url('bg.jpg'); 배경 이미지 경로
     background-repeat: no-repeat;    배경 반복 여부 (repeat, no-repeat) 
    background-size: cover;           이미지 크기 (cover: 꽉 채우기, contain: 다 보이게) 
    background-position: center;      배경 이미지 위치 (center, top, bottom 등) 
    background-attachment: fixed;     스크롤 시 배경 고정 여부 
    }
    ```

## Box Model

 **margin**<br>
테두리(border) 바깥의 외부 여백
- 역할: 요소와 요소 사이의 간격 조절
- 특징: 배경색이 적용되지 않고 인접한 요소들과 거리를 띄울 때 사용
```
div {
  margin: 30px; /* 다른 요소들과 30px 거리를 둠 */
  margin-bottom: 50px; /* 아래쪽 요소와만 50px 간격 */
    }
```
    
 **padding**<br>
내용과 테두리 사이의 안쪽 여백
- 역할: 박스 내부의 콘텐츠가 테두리에 너무 딱 붙지 않게 여유 공간을 줌
- 특징: 배경색이나 배경 이미지를 적용하면 패딩 영역까지 채워짐
```
div {
  padding: 20px; /* 사방에 20px 여백 */
  padding-top: 10px; /* 위쪽만 10px */
}
```
 **border**<br>
패딩과 마진 사이의 경계선
- 역할: 요소의 범위를 시각적으로 나타냄
- 특징: 두께(width),스타일(style),색상(color) 세가지 속성을 주로 세트로 지정
```
div {
  border: 2px solid black; /* 두께 2px, 실선, 검정색 */
  border-radius: 10px;    /* 모서리를 둥글게 */
}
```

