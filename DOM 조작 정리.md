# DOM 조작
>DOM이란? <br>HTML 문서를 자바스크립트가 조작할 수 있게 객체 형태로 바꿔 놓은 것
## 1. 요소 선택
- **`document.querySelector('선택자')`**
    - 역할 및 특징: CSS 선택자에 일치하는 **첫번째 요소 1개**를 반환
    - 추가 정보:
        1. 매칭되는 요소가 없다면 `null`을 반환함
        2. 복합 선택자(예:`'.container .box'`)를 활용하여 구체적으로 요소를 찾을수 있음
```
const header = document.querySelector('#header');
```
- **`document.querySelectorAll('선택자')`**
    - 역할 및 특징:CSS 선택자에 일치하는 **모든 요소**를 `NodeList`형태로 반환
    - 추가 정보:
        1. `NodeList`는 배열과 유사한 객체(유사 배열)임
        2. `forEach`메서드를 지원하여 요소를 순회하며 일괄 처리할 수 있음(단, `map`이나 `filter` 같은 배열 전용 메서드는 바로ㄴ 사용할 수 없음.)
```
const items = document.querySelectorAll('.list-item');
items.forEach(item => {
  item.style.color = 'blue';
});
```
## 2. 요소 생산 및 수정
- **`document.createElement('태그명')`**
    - 역할 및 특징: 메모리 상에 새로운 HTML요소를 생성함
    - 추가 정보:
        1. 생성 직후에는 메모리에만 존재하며 화면(DOM 트리)엔 아직 추가되지 않은 상태
        2. 화면에보이게 하려면 반드시 `appendChild`등의 메서드로 DOM에 연결 해야함
```
const newDiv = document.createElement('div');
```
