# ES6(ECMAScript 6) 핵심 정리

## ✅ ES6란?

- **ECMAScript**: JavaScript를 표준화한 언어
- **ES6 (ECMAScript 2015)**: 2015년에 발표된 JavaScript의 6번째 주요 버전
- **React를 사용하려면 필수로 알아야 할 문법들** 포함

---

## 📌 왜 ES6를 배워야 하나?

React 개발에 필수적인 다음과 같은 문법들이 **ES6에서 도입**되었기 때문입니다:

- 클래스 (`class`)
- 화살표 함수 (`=>`)
- 변수 선언 방식 (`let`, `const`)
- 배열 메서드 (`map`, `filter` 등)
- 구조 분해 할당 (`destructuring`)
- 모듈화 (`import/export`)
- 삼항 연산자 (`조건 ? 참 : 거짓`)
- 스프레드 연산자

---

## 1️⃣ `class` 클래스

```jsx
class Person {
  constructor(name) {
    this.name = name;
  }

  greet() {
    console.log(`Hi, I'm ${this.name}`);
  }
}

const user = new Person("Mina");
user.greet();  // Hi, I'm Mina
```

- OOP(객체지향 프로그래밍)를 위한 문법
- 생성자(`constructor`)와 메서드를 가짐

---

## 2️⃣ 화살표 함수 `=>`

```jsx
// 기존 함수
function add(a, b) {
  return a + b;
}

// 화살표 함수
const add = (a, b) => a + b;
```

- 짧고 간결한 함수 표현식
- `this` 바인딩이 기존 함수와 다르게 동작함

---

## 3️⃣ 변수 선언 (`var`, `let`, `const`)

| 키워드 | 특징 |
| --- | --- |
| `var` | 함수 스코프, 중복 선언 가능 (지양) |
| `let` | 블록 스코프, 값 변경 가능 |
| `const` | 블록 스코프, **값 변경 불가** (재할당 금지) |

```jsx
const PI = 3.14;
let count = 0;
count = 1;
```

---

## 4️⃣ 배열 메서드 `.map()`

```jsx
const nums = [1, 2, 3];
const squared = nums.map(n => n * n);  // [1, 4, 9]
```

- 배열의 각 요소에 대해 함수를 실행하고 **새로운 배열 반환**
- React에서 JSX 리스트 출력에 자주 사용

---

## 5️⃣ 구조 분해 할당 (Destructuring)

```jsx
// 배열
const [a, b] = [10, 20];

// 객체
const person = { name: "Mina", age: 25 };
const { name, age } = person;
```

- 배열이나 객체에서 필요한 값을 **간단하게 추출** 가능

---

## 06️⃣ 스프레드 연산자 `...`

```jsx
javascript
복사편집
const arr1 = [1, 2];
const arr2 = [...arr1, 3];  // [1, 2, 3]

const user = { name: "Mina" };
const newUser = { ...user, age: 20 };  // { name: "Mina", age: 20 }
```

- 배열/객체를 **복사하거나 병합**할 때 사용

---

## 7️⃣ 모듈 (Modules)

```jsx
// export.js
export const name = "Mina";

// import.js
import { name } from './export';
```

- 파일 간 **변수, 함수, 클래스** 등을 주고받을 수 있게 함

---

## 8️⃣ 삼항 연산자 `? :`

```jsx
const isLogin = true;
const message = isLogin ? "Welcome!" : "Please log in.";
```

- `if ~ else`를 짧게 표현하는 연산자