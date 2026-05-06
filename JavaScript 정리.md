# JavaScript 기본 문법

## 1. 변수
>값을 저장하고 참조하기 위한 공간
- **`let`**:값을 재할당할 수 있는 변수 선언시 사용
- **`const`**:값을 재할당할 숭 없는 상수 선언시 사용(값의 변경을 막아 안정성을 높이므로 기본적으로 권장됨)
```
let score = 90; // 재할당 가능
const PI = 3.14; // 재할당 불가능
```
## 2. 조건문
>조건에 따라 다른 코드를 실행하도록 흐름을 제어함
- **`if`,`else if`,`else`**:주어진 조건이 참(`True`)일 때 해당하는 코드블록을 실행
- **`switch`**:하나의 변수나 표현식을 여러 값과 비교할 때 사용
```
if (score >= 80) {
  console.log("합격입니다.");
} else {
  console.log("불합격입니다.");
}
```
```
const day = '수';

switch (day) {
  case '월':
    console.log('한 주의 시작입니다.');
    break;
  case '수':
    console.log('일주일의 절반이네요! 힘내세요.');
    break;
  case '금':
    console.log('불금입니다!');
    break;
  default:
    console.log('평범한 날입니다.');
}
```
## 3. 반복문
>특정 조건이 만족될때 까지 코드 블록을 반복해서 실행함
- **`for`**:횟수 반복
- **`while`**:특정 조건이 참인 동안 계속 반복
```
for (let i = 0; i < 3; i++) {
  console.log(i); // 0, 1, 2 출력
}
```
## 4.함수
>특정 작업을 수행하는 코드들의 집합.재사용성을 높여줌
- **함수 선언문**:`function`키워드를 사용하여 정의
- **화살표 함수**:화살표 함수는 ES6에서 도입된 문법으로, `function` 키워드 대신 `=>`를 사용하여 함수를 더 간결하고 직관적으로 작성할 수 있게 해줌
```
// 함수 선언문
function greet(name) {
  return "Hello, " + name;
}

// 화살표 함수
const add = (a, b) => a + b;
```
## 5. 자료구조
>여러 개의 데이터를 효율적으로 저장하고 관리하는 구조
- **배열**:순서가 있는 데이터의 목록.인덱스(0부터 시작)을 통해 접근함
- **객체**:키(Key)와 값(Value)의 쌍으로 이루어진 데이터 집합
```
// 배열 예시
const fruits = ['사과', '바나나', '포도'];
console.log(fruits[0]); // '사과'

// 객체 예시
const user = { name: 'Kim', age: 25 };
console.log(user.name); // 'Kim'
```