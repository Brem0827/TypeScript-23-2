[![Since](https://img.shields.io/badge/since-2023.08.31-333333.svg?style=flat-square)](https://github.com/Brem0827/TypeScript-23-2)
[![author](https://img.shields.io/badge/author-Brem0827-0066FF.svg?style=flat-square)](https://github.com/Brem0827/TypeScript-23-2)
[![All Contributors](https://img.shields.io/badge/all_contributors-2-orange.svg?style=flat-square)](#TypeScript-23-2)

[![Watch on GitHub](https://img.shields.io/github/watchers/Brem0827/Tech-Stack.svg?style=social)](https://github.com/Brem0827/TypeScript-23-2/watchers)
[![Star on GitHub](https://img.shields.io/github/stars/Brem0827/Tech-Stack.svg?style=social)](https://github.com/Brem0827/TypeScript-23-2/stargazers)
[![Fork on GitHub](https://img.shields.io/github/forks/Brem0827/Tech-Stack.svg?style=social)](https://github.com/Brem0827/TypeScript-23-2/network/members)

# 💎TypeScript
📔 201930324 이현종

<table align="center">
    <tr>
        <td align="center">
	    <a href="https://github.com/Brem0827">
	    	<img src="https://avatars.githubusercontent.com/u/62270266?v=4?s=100" width="100px;" alt=""/>
				<br/>
					<sub>
					<b>이현종</b>
				<br/>
	    	<img src="https://us-central1-progress-markdown.cloudfunctions.net/progress/100"/>
	        </sub>
	    </a>
	</td>
    </tr>
</table>

💎 주차
---
1. 💭[1주차](#1주차)➡️
2. 💭[2주차](#2주차)➡️
3. 💭[3주차](#3주차)➡️
4. 💭[4주차](#4주차)➡️
5. 💭[5주차](#5주차)➡️
6. 💭[6주차](#6주차)➡️
7. 🔖[중간고사](#중간고사)➡️
8. 💭[7주차](#7주차)➡️

---
# 7주차

🔋 2023.10.25

[📖7주차 수업 자료](https://gainful-appendix-a7a.notion.site/null-undefined-generic-7ba912c878ed4576931bb1aec6944caa)

# null and undefined

- `타입스크립트에서`도 위의 두 값을 의미하는 타입이 존재하며 이 타입들이 동작하는 방식은 `strictNullChecks` 옵션의 사용 여부에 따라 달라집니다.

## strictNullChecks off

- `strictNullChecks`를 끄면 `null`이거나 `undefined`값에 정상적으로 액세스할 수 있으며, `null` 및 `undefined`은 모든 유형의 프로퍼티에 할당할 수 있습니다.

```tsx

function greet(name?: string) {
    // 'name'은 string 또는 undefined 일 수 있습니다.
    return "Hello, " + name.toUpperCase();
}

```

## strictNullChecks on

- `strictNullChecks`를 켜면 값이 `null`이거나 `undefined`인 경우 해당 값에 메서드나 속성에 접근하기 전에 값을 테스트해야 합니다.

```tsx

function greet(name?: string) {
    // 'name'은 string 또는 undefined 일 수 있습니다.
    return "Hello, " + name.toUpperCase();
}

```

## Non-null Assertion Operator (Postfix !)

- `타입스크립트`에는 직접적인 체크 없이 타입에서 `null` 과 `undefined`을 제거하는 특별한 구문도 있습니다. 

- 표현식 뒤에 `!` 을 사용하면 사실상 값이 `null` 과 `undefined` 이 아니라는 것을 의미합니다.

```tsx

function liveDangerously(x?: number | null) {
  // No error
  console.log(x!.toFixed());
}

```

# Generic Type 

- `C# 및 Java`와 같은 언어에서 `재사용 가능`한 컴포넌트를 만들기 위한 기능 중 하나는 `generics`입니다.

- 이는 `단일 타입`이 아닌 `다양한 타입`에서 작동할 수 있는 `컴포넌트`를 만들 수 있는 기능입니다. 

```tsx

function identity(arg: string|number): string|number {
  return arg;
}

let id = identity("dealim"); //let id: string | number

```
```tsx

function identity<Type>(arg: Type): Type {
  return arg;
}

let id = identity<string>("dealim"); //let id: string
let id2 = identity<number>(52); //let id: number
let id3 = identity<boolean>(true); //let id: boolean

let nid = identity("dealim"); //let id: string
let nid2 = identity(52); //let id: number
let nid3 = identity(true); //let id: boolean

```

- 해당 함수를 호출할때는 두가지 방법으로 호출이 가능합니다.

1. 인수 호출 전 <> 안에 캡쳐할 타입을 명시적으로 선언하기
2. 평소대로 호출하고 인수값을 바탕으로 typescript가 타입을 추론하도록 하기

---
# 중간고사

[📖1주차 수업 자료](https://gainful-appendix-a7a.notion.site/acee91b0b4bc4f3c904c33bb50024ab0?pvs=4)

[📖2주차 수업 자료](https://gainful-appendix-a7a.notion.site/Type-550436e1eba6414bbc1d2e5fb5b19e6a)

[📖3주차 수업 자료](https://gainful-appendix-a7a.notion.site/Object-Union-d9a258182b464231bf3db529290dc480?pvs=4)

[📖4~6주차 수업 자료](https://gainful-appendix-a7a.notion.site/Type-Alias-Interface-37dba0ea83bb4b40aa24833bcd7bb495)

[📖중간고사](중간고사.md)

[📖중간고사(코드)](중간고사(코드).md)


## 🏃시험 관련내용

- 수요일 오전 10시 ~ 10시50분

- 객관식 + 주관식 문제

- 주관식 : 예제코드 빈칸 채우기, 코드 해석 1문제(동작 로직) -> 어떤걸 인수로 받는지 등등.. 

- 리펙토링 : 코딩 컨벤션, 백틱, 템플릿 스트링, 디스트럭처링

- 문항: 20문제

## ❗실습 문제들

- 🔥 7주차

1. 문제 1번

- 실습1에서 CRUD 함수를 추가해보세요.

- addStudent(student) -> student를 data에 추가

- updateStudent(student) -> student 객체 안의 id를 기반으로 data 업데이트

- seletctStudent(id) -> 해당 id를 가진 student 리턴

- deleteStudent(id) -> 해당 id를 가진 student 삭제

- 🔥 6주차

1. 문제 1번

[문제 1](https://www.typescriptlang.org/play?#code/MYewdgzgLgBAJgQygmBeGBtAUDGBvHXGAIgEs5iAuGARgBpDdiwEBbAUypMAE6wAcnAJteIMiJBAHNO1AEz1GouHABO7CBC4ERTYKSgBPLsUA4g4A6xoXKZxS0RaWBQDgVBrAFQ2AbWuJyAvsKLE47AA4IilAcYPbUxIAvc4AXK4AMizCArzWAmquAPzVmIsRiigh+BlJJgCKN6T4IdqQAbjqkKlzYmvjmPnr+kiTAADYArgBGxfXMbK3EgCCrgDodgB+1gBntgLA9MICbzYAio4A1ne71Xo0a9STNQ6BhKvbe-SwcBgDKAOowgDIzgA2dvKuaHnIAuoTruJtM5FxSRyQnIaAF3HABqrgAFxvqiCS-P5yYg5JQqNTUL4+bR6AyAAN7AA0DkIsVigNjsBkALquAFrHAADNbk8-18ASCIXYYQMgBRWwAJ44APcZgqUhmWyuQiAGZCrzSlAKlUatQ6ppURkdgYOj08T5AazOTBACVDsRZjxEzxEb1wHwaGR+1EFtLVEUAqD2AAEnAIBjouh0ktcIRylU6kaxHR+giHMAOTMq3wEonhEhOObU-W0vyBYKhCPEQC9NQ6ebSsjkhgAWEW0sUS8VSzAbRpMBURPZQA4qpjWkhpmALIEswAtozAKYAYtb1RBNIjlTV0LUVXV6-wyDdTDpggAfRlzzZa942vd7eVFkCjUHNWwYGQCoE4Af7sMztaUgADAWFJ7kabNL6dP6SCYQ5ZrLZk84Y324-TE0zkxieJkjSTN+SGGh83dMpKmLW8ZQHcttmHXYxzrAE9wiMYplmRYVkaA0iCNGATQ3c0YAAVl3U4IkAHVnAAwhwARydPX4d3da8kW9fo-SxXEJxIN9CQ-UlKW-Y1fwTRlmQidkuQzOEswFEg8yKAsYMleCyy2ZCRyrND+PrTCSFkrUdWXEjV3EwgyK3GAADZqKGbhABA1+iWOkWQMg9TiUR9HiA2DfjQ3fYkIijMSSIkhkkwMNN5IyRShnyVToPFWDqk0+pBwrFDFXAGtoHQgYaMbGcW3bTsewIyzIusuFyIAdkcgwbV4J0CxdGApFhLyOK9XzuMfAwXyCwTw0cVxe37AS-ykwC4kSeKfESgxhRSrz1Lg2otK2YhKzafSkOKoZsJmRd8LWGrSPq2yAA5moiIFeAWdyurdXrEX6u8Mn8kgcVfMNhIickqSmqL-2k4yNSWpgVoiZLRU2jLtqyo79t9Q7tOO9UuW1XVqsNNc6rNWyAE4HpIQBS8cMZzXpkK9PtvQcHwxAKAZC5NwrBuF42igDYvTUCFPAgxIPWkokZLBCiGynTdny2sDIwkrp2bVsO27czCNwYjrpJrgaEvOEpyBQAa8cEDqzyNj6by4+9fqMUxRsB0KSC-bmMl5iH5uAmGSDhkgxcRtKNJR2U0dyvTlSV7GsImM68K1q6sDeIA)

- 위 링크의 데이터 구조를 파악하고 type을 정의해보세요.

- type, interface 사용

- 리터럴 타입 사용

- eslint 체크

2. 문제 2번

[문제 2](https://www.typescriptlang.org/play?#code/MYewdgzgLgBAJgQygmBeGBtAUDGBvHXGAIgEsoBTAWwEk5iAuGARgBpDdiAHAJxDgCuwKADkEVCoxKALPsAgNTEAXnYBolhcXZESvUsElMAzAAYjB9UWLAkFAOYgeATynFAGuOANTrUcSEAQCMAwpZt7KQINTig7Ll0SQEGBp3dQkipLHlIEABtHQBcu4g8AX1MwhCsIKWwEkISScMjHUDTbeMriADd0gSjiaUBUGpyE-I9cCoTiao7oOzTJAtCWto7ABLnAH4nAHtHe0NyPAF1CfsGPMkpaeiYAJmnuPkFhMQlHQBQ+wAuOmEBamcAUHsABycbOLR0pABZjCZ9hZKIEHExnG5zl4-AFbOD8AMqhEOoANVbi004SUoKXSjkADs2ADaa1rhdmZkMVSkihjNRrUQPUeF8Zq00u1HIAYZcAie0kohkjQ0jQjFGOcaTZlC1nsiH4wA+44Aazt5pK2O1MNIO1DoUj0514-CEonEHUAJUOAG+XAARzMEALWOATebACprzIu2iizEBQKFIOs8McgAOhwA4PY6Yf5Qd6mILkTUIbaHZjEslUhkIYADmsALN28-lVIolJhlULhsIiiF1BqxzhSjqAB3XAJMDSpgGb2lQjHQAZgIwMJSOAJWZy45bYBKsdrGw021Jav25E1xxgf11lwNN0rVcUKkdPyiJwAHMZzp6wY5XIGfMGvUEw0jhZGYhiL9iKLjEyRsnlzhTs5hqUiC1fzAyS1+SF7CFqyHWN8ybUVwnFUtALmRxABuhwAYVaHFUx0IdVJyOKQAFY531a4jUcQAAmsAVAmYEAGqHAEz2401xSX4mD+bCd2BOEzxIQ9oWPViEXDS80RvYY7wfRxABfl+VAAXR41AAZF9NXyzKlygAvj6UZbsyzgiFSNAz9G2UiExSmJSgJIEjAFLxlCR1VdCJ0OLUmAANjwq5DVuCFAAga5dAB0OwAfZdo50pGYE5AV3bjfQDTjYRDNjeLpCFABtawAFFu7YghITRxAAAawBfidk-Y3wUvMlNikhiyZGDZjZDoPO0xTdKK4gDLU2CKscMzByRYciFHOtxyFTC7JgAB2JyF0IiFABJGwAXccAET6V1UOd-NOABOZiPVCiEOP2IM1sRYY6tiZLUrxCFnw0DMRnknMdKaOqSsa8rpRIblqoK2rC08KDDN04ziCQizOqshszD66dN2GgjXJIIkXg+Pz6JgPRtyMEKooRSEj0i08eIvOr0QO+Mjsh4kX1yi6Pxq663t-VSyu+p72rAwrKYammNMhhU-twLqyQw2zp0WsGXI6QAIDsAHZaYGNQAJpsAE7nAAjJ2Gok3JikZYlGwvRk993PXbKejPGcTS5M02JoU8su8ntZ-W6WeaiFumegVGZ-ZmjNZ4hjUADqXAH7OjmYC5nqgd5gL3TMPVnMXRxAA-awAGzpgQAHpcAFUHzXlqQgpWsw91DdioU2rjVa12lKf22MUvxx9iBOvk5MpM2Xopy2-1Kl2bZIQAIWcAXQ77aIcC9PeiZPqab6llWdrULrLBtiwIA)

- 위 링크의 데이터를 바탕으로 타입을 정의해보세요.

- type, interface 사용

- 리터럴 타입 사용

- eslint 확인

- 🔥 5주차

1. 문제 1번

![문제 1]('./image/thumbnail2.png')

- Type Aliases 를 사용하여 위의 코드를 리펙토링해 보세요.
- Interfaces를 사용하여 위의 코드를 리펙토링해 보세요.

2. 문제 2번

- 실습1에서 만든 코드에서 추가로 printAdminUserInfo 함수 구현
- 해당 함수에서는 기존의 User정보에 role이라는 컬럼을 추가해서 출력
- 기존의 Interface, type을 확장

3. [문제3](https://www.typescriptlang.org/play?#code/MYewdgzgLgBAJgQygmBeGBtAUDGBvHXGAIigE8AHAU2IC4S4QBzYgGkN2LAQFsb7igU87AJUNsOJBE34wArOyIkA7lQCWTABZQ6MAEwAGeUWIAjAE5UqcbcUA1nYA6lm4BCe4oQC+hggtKVpxRi0NObj5rQAuO0LEvSWkdQKVVDS16AEYDcRNzS2tADxXAE5aXXHdCTyNyamtgJEijYN9AD+666s5o7QBmOOJlNU1tABYO0AAbEFNrQACawFQJgpgi3BLOMt9KrQ7a60AVefWmiSltZI6uxLaBkGHRgUAHdcBJgenXLABdLCA)

- 위 링크에서 포함된 데이터 세트에 대한 타입과 인터페이스를 지정하세요.
- 그리고 강아지 또는 고양이만 console로 출력하는 함수를 만들어 보세요.

- printData("dog")
- printData("cat")

4. [문제4](https://www.typescriptlang.org/play?#code/MYewdgzgLgBAJgQygmBeGBtA3gKBvmAIgEs5CAuIgBwEZCAaPAwsBAWwFMKjAagcB+ahk3yEqAJ2LAulGgFYADHMYEi0EMADW3GoqFFgSDgHMQogJ7dCgXaHAESuDlhOMQigArmCgXtAUkJMAvkowuPakFlQATHbMrJwWgB6NgB1LgIG9UcJiElIwsgo5gcKqGtwyeXoGxmYWgCATgAnjgDgTtiWEEFQcwBbEAOz0WQBsAOIAQjAASgCCALK++AFMwcyhlCIAzKlEMZmEgA9LgCqDgARzqyLiktzhOTr2BZqUp436UEYm5ouAGuOAGp0HEMQAXhuT-oFzYQLagAFgO6wslkArn0HdLHa7yc7MS7cJZI4R3B4VRY2A6OZwgNweSiI-6zXQkMiLKgycHsDaAFnXAADNgAfl2FHTLaM7olRQNRXLI8wiY8pPIg1ep4pyudwWGQ+HB+AC6OBwADM3MAoMRwPBpYT3AA1BAAGxcHAAFPiZVBKNBxGBDAAfMAuNgAIw4om6cI45FdHq9AEo5iaOLBRBwIC4TVAAMpQB2GGB2xPER3oADkmYA3Kr8MQ1RaoKYWiA1XqCUS0KgswHPaJMyHdPhI9HYwmkzAANToAAG9EABquAD3HAAA1lAAJFgLb6YABaSs2oMAOj5ABk1KaOJ304YLUG-IAFsb7eeUfhgHBNEA4MELxdLHHLi4NsFrWftu6bgIIbZj8bTjo9v23QjqOKYwFOM4cjAABUMAWjQ84wFQCCiNeACS7hWvqRJBgA9FyQYruum5hjujr7keJ66H4TCRlALiiGAMC-h2AGGIqqqIMgy5qiYACiCDAAAFhaUEgHALhauBWCkOQH6Ot06zyexPocv6boNt0lwaYG3owCKjwqUm3TWi+AD8xm7i6mletp3wcJZCmGNpLTAE57F+EGaAAHxBEwoCQLAWC3nASn0mpGSmTh7jaXyGjdIZZj2T8rmtDA57oGIElSVAp4wGGEZRn+5HJv26EACLkFOpABDAgAu44AIZ3VVg6x1aOgCVNS1vqriAG76GR7GUceeZMHeZm4SxxVsV2vbPkSxpmpaE2xb6Qb5XR03-rNwEwIANeOAAc1LWXHVgAuc4AMosHYANZ0tUlph+H2+a3kWnw-N5rHbbuQEwAOMA8PVgARk8dDkPWNL1ue9W2ld9v08IAiaPHW5oMBeAEAgGGy4miAe4faVQaKkGQA)

- 지금까지 배운 내용을 바탕으로 지난시간에 진행했던 실습을 리펙토링 해 보세요.

- type 또는 interface 사용

- literal types 적용

- 🔥 4주차

```js

const data = [{
    "id": "p1",
    "name": "사과",
    "price": 1500,
    "stock": 10,
    "category": "식품",
    "discount": "10%"
  },
  {
    "id": "p2",
    "name": "노트북",
    "price": 1500000,
    "stock": 5,
    "category": "전자제품",
    "spec": "i7, 16GB RAM"
  },
  {
    "id": "p3",
    "name": "티셔츠",
    "price": 20000,
    "stock": 20,
    "category": "의류",
    "size": "M"
  },
  {
    "id": "p4",
    "name": "식빵",
    "price": 2500,
    "stock": 30,
    "category": "식품",
    "discount": 500
  },
  {
    "id": "p5",
    "name": "휴대폰",
    "price": 1000000,
    "stock": 10,
    "category": "전자제품",
    "discount": "5%"
}]

```

![문제 1]('./image/thumbnail.png')

- 🔥 3주차

1. 위 함수의 문제점을 찾아보세요. 위 함수가 문제가 발생하는 케이스를 작성하고 해결하기 위해서 어떻게 해야할지 코드를 수정해보세요.

```js

function calculateAverage(scores: number[]) {
  let total = 0;
  let count = 0;
  for (const score of scores) {
    if (score) {
      total += score;
      count++;
    }
  }
  return total / count;
}

```

2. 위 코드에서 

```js

function printBoard(result: any) {
  console.log(result)
}

```

- 이 부분만 수정해서 아래와 같이 출력되도록 수정해보세요.
그리고 result: any 부분을 아래의 출력에 필요한 데이터만 받도록 처리하고 type 선언을 해주세요.

```js

function printBoard(result: any) {
  console.log(result)
}

fetch('https://static-contents-serve.s3.ap-northeast-2.amazonaws.com/response.json').then((result)=>{
  return result.json()
}).then(list => {
  list.forEach((data: any)=>{
    printBoard(data)
  })
}).catch(err => {
  console.log(err)
});

```

---
# 6주차

🔋 2023.10.04

[📖6주차 수업 자료](https://gainful-appendix-a7a.notion.site/Type-Alias-Interface-37dba0ea83bb4b40aa24833bcd7bb495)

# 📂Literal Types

- typescript에서는 `string`이나 `number`와 같은 타입 뿐만 아니라 값 자체를 의미하는 `리터럴 타입`도 정의할 수 있습니다. 이러한 `리터럴 타입`을 `정의`하는 방법과 함께 `타입스크립트`가 `javascript`에서 변수를 선언하는 방식에 따른 동작을 이해할 필요가 있습니다.

```js

let changingString = "Hello World";
changingString = "안녕하세요.";
// 위에서 changingString은 가능한 모든 스트링을 나타낼 수 있기 때문에
// 타입스크립트에서는 아래와 같이 인식합니다.
changingString; // let changingString: string

const constString = "Hello World";
// constString은 오로지 "Hello World"라는 문자열만을 의미합니다.
// 타입스크립트에서는 아래와 같이 인식합니다.
constString;   //  const constString: "Hello World"

```

```js

let x: "hello" = "hello";
x = "hello"; // 정상동작
x = "howdy"; // 에러
Type '"howdy"' is not assignable to type '"hello"'.Type '"howdy"' is not assignable to type '"hello"'.

```

```js

function printText(s: string, alignment: "left" | "right" | "center") {
  // ...
}
printText("안녕하세요.", "left");

printText("반갑습니다.", "centre");
Argument of type '"centre"' is not assignable to parameter of type '"left" | "right" | "center"'.Argument of type '"centre"' is not assignable to parameter of type '"left" | "right" | "center"'.

```

```js

function compare(a: string, b: string): -1 | 0 | 1 {
  return a === b ? 0 : a > b ? 1 : -1;
}

```

```js

interface Options {
  width: number;
}
function configure(x: Options | "auto") {
  // ...
}
configure({ width: 100 });

configure("auto");

configure("automatic");
Argument of type '"automatic"' is not assignable to parameter of type 'Options | "auto"'.Argument of type '"automatic"' is not assignable to parameter of type 'Options | "auto"'.

```

# 📂Literal Inference

```js

const obj = { counter: 0 };
obj.counter = 1;

```

- `TypeScript`는 이전에 0이었던 필드에 1을 할당하는 것을 오류라고 가정하지 않습니다. (const임에도 불구하고) 다르게 말하면, obj.counter에는 0이 아닌 타입인 number로 추론합니다. 

```js

declare function handleRequest(url: string, method: "GET" | "POST"): void;

const req = { url: "https://example.com", method: "GET" };
handleRequest(req.url, req.method);

Argument of type 'string' is not assignable to parameter of type '"GET" | "POST"'.Argument of type 'string' is not assignable to parameter of type '"GET" | "POST"'.Try

```

- 위의 예제에서 req.method는 "GET"이 아닌 string으로 추론됩니다. req를 생성하고 handleRequest를 호출하는 사이에 “안녕하세요"와 같은 다른 문자열을 req.method에 할당할 수 있기 때문에 TypeScript는 이 코드에 오류가 있는 것으로 간주합니다.

- 이 문제를 해결하기 위해 두가지 방법을 사용 할 수 있습니다.

1. 둘중 하나의 위치에 as를 통해 명시적으로 타입을 지정하는 방법이 있습니다.

```js

// Change 1:
const req = { url: "https://example.com", method: "GET" as "GET" };
// Change 2
handleRequest(req.url, req.method as "GET");

```

- `Change 1`은 "req.method가 항상 `리터럴 타입` "GET"을 갖도록 하여 이후 해당 필드에 "안녕하세요"와 같은 다른 문자열을 할당할 수 없도록 하겠습니다."를 의미합니다. 

- `Change 2`는 "req.method가 "GET" 값을 갖습니다."를 의미합니다.

2. `as const` 를 이용하여 `req 객체` 자체를 `type literals`로 고정합니다.

```js

const req = { url: "https://example.com", method: "GET" } as const;
handleRequest(req.url, req.method);

```

[📖6주차 과제 1](https://www.typescriptlang.org/play?#code/JYOwLgpgTgZghgYwgAgGIHt0BMAKVsCuCYyA3gFDLLBYBcyAzmFKAOYDclyIcAthPSYsQHLgAcWSeiAK8ARtE5Um6BAGtpshVCXIEcSK3RQAnvQBEgXaHAESvndWYAwToC4QczbIAPty2LyAL7k5KCQsIgoAKIANhDE+CDACHiExGRcNO7ColQ8-FlsuhJJAr7y-spgqhpl2rr6hsZmyOaAIBOACeOAOBO2ugxicQUi9o7OrmAA-IOiQSHg0PBIyADC0ehgABZsKVhEJBRUmYweQ1x5pUKF4pKlMuU6XCrqmnf1BhBGphaAGuOAGp12D8AAF7nY7TYJgEz9ZDbXbIAC8aEwuHwOzSPhicWY6ESyRRsJ8KzWmxEMOInHIAHoKchACdNgA9O5CASh7LIAeccAOh3IQAOzYAXccADIuAH07kIAIWcADHWAFTXyM4QExkFgDHB6KSwABtAC68OQavJUplMGAUCYABF5fQMNglRr9tQ6C0xABGcwAGlOfFK5kANQOAH5qnVcSvQ7QBWAAMQedlWq-tDXAa7yaFhsPqoDicLjcLTtQYApOZAtrsTKGHFsVhjWAFcgMfFsUkLQirYdzGIAEyJ7iuiyAD0bAB1LgEDe1vFKTIQMhkdho4R5ABscxj7NNpdWxjvoDFrAADsjqHADYAOIAIWQACUAIIAWRzATz0pIG31JZNy1Wt5JeLSdYyNsbAGZW2cLIAHpcAFUHAAI5-trnoJsRyjcMnmQSDpzeWdvj+JcgTdc9c2CHUSBgFwoA2UtyzNZFUhId8Dk-MQABZf3bFpLEAVz6wL9ODg2g8dYK-diZzjejFy4ZNRjTNjMMlfMcOAGACIfSssRxWt0goiwxADWj8haQAWdcAAGbAAfl5jBwzKD2MeGoMwQxpPhaDpulbQTUzACwA2zJd+gQCxABKhwAJzq7PTRKpLk+WQQAkGsAEXHkEABh7ABfRwAF0eQQAU2cAABrAB1VmkADpyDlMtUrEAgGHWAAKPUDTAQjN0LKV7zLTdbygSq4E3XCCHw9ZSuQPUpJa+UAEpyRgVxiGAbFZRGeyADU4GiAgIHyuyximLxbm0TcBwERboC6q1YhIKAIAYAhojAABlUFkCmBEAHJzvJA4YHyiF+nQGBhpTMZ4ThC61qgc6Nq4KgqB2vaDuO7JkAAagRAADR1AANVwAPcYS+gABJSHylbkAAWmeoSwC61KqgAGVUCaIGBth8q6gJAAWxiHdCoAJkAgaJC2oW77ogR6sfst6LouERvqtP7kAB-ajpO8HkCh5A4YS07kGR1HrmQAAqZB8rtDHkDEOADQgABJcAZpGsYuopQyutxgmidiUmRHJqmad+5Agn+iAwCakAhd2kWbdYQJgkyuBUtwqBIkQAqFdI2XSEyXnWE3P9Y+W8DPrKqonhTvRELjRPObGSZY4WvwoDKtD89BMrXLL7IAi6+EAD5FL0cSyGtePXSTkpN1m8BU+qTceNMEvgQruInY1CRSN0LbPcB0WQch3XDVoZGaACTduUAEM7l9IM41+QBLAEqa7eVrx9BCf0a3QTt6nrpZw2XvAWvhaBsWEW7sBxsm6b38dFaeq4Lgz856eHFpLQANeOAAOa7eJk96ABc5wAMosQMADWd28B4mACBDYIN18oMDQk-L2L8QagM3O6bkgAIyegWhDBGRbrLgQPg2ePswaQxIYARNHoGuWodGfM6BYipVWKwfKQCfZdUCF1IAA)

[📖6주차 과제 2](https://www.typescriptlang.org/play?#code/JYOwLgpgTgZghgYwgAgIIBN1QgZx8gbwChlkFgwBPALmRzClAHMBuE5dYexhMW75mwC+RIqEixEKVL2AA3CpULsqABwj8Gg9iDgBbDXS0hWREWPDR4SZAGUwAV3QRwy0sHS0QDvQCNobKS6BpqMJoHIcEyG3n4B7HCY2Hi0GFi4OBHOqnBQYAbgodqkTFCJhgLhCbIKYMC4qTWKANoAusKiaigAInBgcMgAvHaOzuBtbEQIAPYg9Bx9cLS9-UPIzezEpKQARB47tACMADTsu8EQB8g7gAJ1gAOTgBNrO6fb11GXtABMJ2dvSRlXLava7kKhXHaAHEHAB1jz1+u04Al44MAqDWACobADa1O1+Qhe2x22Vy+RcYHBgBe5wAXK4AGReQgFeawCaq4Afmthrx2pXK4M+dMAIo3MvGIOq1eo4K4bYFuMXXLrghAAGwcvl5Yp2F3BgBBVwA6HYAP2sAGe2AWB7kIBN5sAIqOAGs6sWKcXDxUqpbQdjNLPRFcDlfoPtdbAB1ZCAGRnAA2dd3NwJEr1a7EtpCBu32X1x5zd4MALuOADVXAALjzp27yun0+cb+6TwgKt9sU4MAAb2ABoHnfCuFokXbAC6rgBaxwAAzZjsXn8RAcnkCiS7YAUVsACeOAD3HkIyM2znOCAMzcjP8+QUIUiq1Rl22kFyhV5lkqwej5CAEqHKQOg68Q9sw6QI9brjHkDPO-vroBUHsAAJOAQDGF9Fs0-fpm-yFrQ667KClDgiOgA5M9W1wInW-bXKiBrthenYEr2xLgoAvTWfhOnZTu6OwACzzp2i6Crgq5iqBeKbvasyQE6u54i+Oy4cgRqJgOgAto8gLaADFr57bLery0bs9GyvKsHxgYOGfsggAPo+ihqmsJN6-NeyC3uuezoFcxHPgmdqAKgTgA-3RCP7up8AAM5FAcKIHFuB4LQrB+K1jwiE7GiqEieh3aEn2ZJUrS+EAYR4KHGRAEUcuVG0KKwLiZKlDqNK24ydcbEajq+rGmaVqXqQWk6QBD4AKxGXJdqADqzgAYQ4AI5NWdmhmxQ5RZKi5dqVu58FeeCzZtsJolwYFmHgOCw5juFLKRXapE8uRTR1Al6xrlaElpURUk7pt2XGdc03Hqe6naZp4a4rpD4AGzVURNyACBr9UtV8PwsokBaOXeYGlna0F9Z5wD1khKEjQFPZEpNdq4bNeLzdcnJLbFK0rolG0Sql6V2g6TEkixslERxXG8fxQlFRdN5XeV+m0AA7Pd4Kvnc37kb+Xy5u1X2dS63XXG5LEeYi3m+eDAEYVD3kUtS9JMgRZTTnac7Ix9qNrUlYn7TskmZQTB01dcuV6qphUWpT2nUyyD4AByM3aiZ3Ear3IJ8-4fR1TldX91y9YL-XA95Q1+VT4vjZLU2HnDuwIzsSMLmr30a9sKXa9tGXSXrroGzsx0nmeFOhpdmw01cACcdvXIApeMQo9zvfPZ3Oe7z3s7ADftAyDOzIcHFuh5DwUw3hcsRQrRHRSrfIJ9RyVa5JjG4PjWtscT3F8YJZ3FcgpWW3iD6HHZAFsYmgA1408bPWQf7uNz9IItwLxb+53osdn3QVYXa0thcPc2j1FMWqwKeKicMYSlTtjLcGcl6HR2EbfKakC5XnDEQMMRAYAOBALIWYyBVBhDAPYJwxIACSIAYDTAABT0AIYUEYVCwAAEpxQOhwNMGUEAAB0MpphMDIb8AABoQ7otAAAkBBKFjDAGwjwOJkCJkACGdwjRGjGJGwi40jAAZDYmBRYjlHvGkYAH4nAAxg1opR4A2GfWSDgNh4EhDIBEdo0x5iMhsMfmAaRjJjG0OcWHPsbiuQePEWwwiQheHsDoZMUgAB6CJTCWHsM4dwnYgAdNYNMgQAlV2AF0O6gOwwnsHsRIuKq1LGkKgAAUUQAACzIWQgplAGGDAAHx3mADAapK1KBsK6EMQYwwGKOhJHQ2iMTWEcK4WQ3hgBQicABqdtBBLHBkfI2xBAakqLdMEnJF5fgQBlDgFAgzZjMOGfEsZUzaAFTmXIhRyzVG8PWSJcMOTzDoEWGw4pZSECVIoSY+hQxGlAhweIfB4jiGkM+bQh5YSgA)

[📖6주차 과제 3](https://www.typescriptlang.org/play?#code/JYOwLgpgTgZghgYwgAgMoFcBGBhOkDmA9lAJ7IDeAUMsmCQA4QBcyAzmFKPgNzXIC2eaMDgAbFu04gelAL6VKoSLEQoAKnHysKfOowkcuvGgDcx6Zm0PTe8xeGjwkybKMJgAFhG1UawSPwAkgAmLCDo-JjQxsj0UITB6AhgAHJw-JaSRnxxwEhhEVFQMQhCRKQGUjI0rFi4BMQkLBg4ZY0xYJqsLBpaANoAurYKeigAInhwyAC8Lm6e3oO8CgiEIOzIwZMsE50zyH18vjTIAET+EEHBpywAjAA0fDSncQlJqekQN2eAFn2AIDXIQAXnYAaJcBp0eJzOuSQ3wAzAAGRHwiEnU6lBqkb6nQAa44ANTvBTzOtVaGJI32OkNOoyxgEGB7EEyHPQTKESiLGAFy7ToTZCjnp0tN9DoydMK+Qwviw0YQ3FAGaLTmZRBYsT9AKg1XOFPMJNApjKp4qx7BIoi+vL1iuVksACXOAH4nAD2jGsZ8khAz4Wp1hPOARC3wATGaXvFEsk0hksYAUPsAFx3IQC1M4AUHsAA5Ny57QiXIAAsSORnvREHKZMleOTRLqbUxLF1YsYWMAGqv0s1MoScMRYwAOzYANpsdNHdqP5rEF2pF8upktWMuLlItadOgBhlwCJ7V2Tj3IZXewbJUaTRPUVO24AfccANZ2L7uE13dlG6r2XH0sWEB17Bj5hyWAEqHADfLgAI55CAFrHAJvNgBU14tAzyNNbizbNKVzfMsUAA6HABweoDiXqPNGnJQd9WrSU-0AhszmZYQW0lQADmsAFm7F2XM4+wHYVVyracx2Ibdnl3SVAAd1wBJgePZAKI9UVKPXM4YHQEBkmANYmLOFizj-QBKsa450TjPbiL09C4rm+dN7yDd5Q2nDigVBIDUz9AAOJEAyg1DC3xAMkLLAsh0pEczjpbdTnw5s2UlTluQDKiWCFRlaP4zCzgY2VcOY8w9M4wceMcvVnNOTdTUHKKlWnQAbocAGFX5NPN0VMpNSb2QABWLS3hDT4sUAAJrAFQJ5BABqhwBM9pfIzOBhFh01K8yc3srEi1s0tSTQ4UMOnOs3I81ksUAF+WD0ABdGX0ABkXyL8rpqKCtKQvo6VGMiyTotqur5Nw4LxsNOgtwOhUjslOrAFLxvKXQKo5VO9a4WAANgqx9dKxQAIGvY5BAB0OwAfZfakDvluX0sws-rJXgxDhpQ8sErorFABtawAFFqmpsZslQAAGsAX4m1s9fyDkHc6kvCiTboywHYs1M7toujcrtSvj6ctM5HrkuL8vPN6io+74AHZfp06rJUAEkbABdxwARPoMsEtKhlhfQATl6yCEbOQbPTskaK3QpLXNw9z8cIs4fMhCiqQ2gKqdZmm9oi1mpNnBc4pZrmkpSumPZy57FNe3jUWKz7kBMyWqufM4O1jRNIc65BYTMxF4aNvWbINlHoONsaksm83pqt04OzJpyHcpmjnYEqVxxuj351Op3ffr-2m7u+PD2DmglJ7S8I++DWY6fadAAgOwAdluQF9AAmmwATucACMnk7TEyeozvqs9OJGhpJVGHNXNnpIAvGWTL0jK97avApXOvQob-b3e7041Vb2v24fzvn4Z19AA6lwA-Z192QAPQq4dRZ3AgqiB8Us46nEAB+1gAGzuQIAB6XAAqgx+Vefo4ZbwPgNHOlJDZ4ILoleuZt0Kly8tbK+fIb5t2HPXWmXdf5nEABCzgBdDvfltT+05v5cw9raB0AsXonldJQVY6wwCxCkGAQI3oQAwEIPsAAFAgeYXhuhzHcBogAlDMAAfEOCRrBpQQAAHRuHwMogABnIy4yBAhjBYAAEnIGo7R3gzER1kMgOWgAQzpcW49RniYGxwgD4wmgBKmsCe4hYrAzGph8YAFznAAyi0RA8MTgnxMsqQHxgABhcAKHjmSPHxKIfmMxowfGABjBwANePFLiWYspjQzGUJ8YAHYX4H1I0RUroLS4D0GUfyAxyBrFqHFIE-kFTxQ8mQAANWihMzQZipyyGsTo1ZOjbDLC2J0MxiioAAFFEAeGUbkcAdiggKMIJsygQA)

---
# 5주차

🔋 2023.09.27

[📖5주차 수업 자료](https://gainful-appendix-a7a.notion.site/Type-Alias-Interface-37dba0ea83bb4b40aa24833bcd7bb495)

# 📂Type Alias

- `type alias`는 타입에 대한 이름을 지정하여 재 사용 가능하도록 하는 구문입니다.

```js

type Point = {
  x: number;
  y: number;
};

function printCoord(pt: Point) {
  console.log("The coordinate's x value is " + pt.x);
  console.log("The coordinate's y value is " + pt.y);
}

printCoord({ x: 100, y: 100 });

```

- `객체 타입`은 위와 같이 type을 선언하여 사용 할 수 있습니다. 

- `printCoord`의 파라미터 값에 타입 어노테이션을 이용해 pt에 대한 타입을 지정했던 방식과는 달리 상단에 type alias를 선언해서 pt에 지정해주는 방식을 사용함으로 써 Point라는 타입을 재사용 할 수 있도록 처리했습니다.

- 유니온 타입의 경우도 아래와 같이 사용 가능합니다.

```js

type ID = number | string;

```

# 📂Interfaces

- 인터페이스는 type의 이름을 지정하는 또 다른 방법입니다.

```js

interface Point {
  x: number;
  y: number;
}

function printCoord(pt: Point) {
  console.log("The coordinate's x value is " + pt.x);
  console.log("The coordinate's y value is " + pt.y);
}

printCoord({ x: 100, y: 100 });

```

# 📂Type Aliases 와 Interfaces의 차이점

```js

// 1. 병합
interface User {
  name: string;
}
interface User {
  age: number;
}
const userInfo: User = { name: "철수", age: 22 }; // No error


type UserType = { // Error: Duplicate identifier 'UserType'.
   name: string;
};
type UserType = { // Error: Duplicate identifier 'UserType'.
   age: number;
};


// 2. 확장
interface Animal {
  sound: string;
}
interface Dog extends Animal {
  breed: string;
}
class MyDog implements Dog {
  sound = "멍멍";
  breed = "진돗개";
}
const dog: Dog = {
  sound: "왈왈",
  breed: "치와와"
}


type AnimalType = {
  sound: string;
};
type DogType = AnimalType & {
  breed: string;
};

// 3. Union, Intersection (확장)

// interface Button = PrimaryButton | SecondaryButton;  // Error

type PrimaryButton = { label: string, primary: true };
type SecondaryButton = { label: string, primary: false };

type ButtonType = PrimaryButton | SecondaryButton;

// 4. 처리 가능한 속성
// interface ComputedProps {  // Error
//   [key: `prop_${string}`]: string;
// }

type ComputedPropsType = {
  [key: `sound_${count}`]: string;
};

```

```js

interface User {
  id: string;
  name: string;
}

type ID = string | number;
type AnimalOrID = Animal | ID;

```

[📖5주차 과제 1](https://www.typescriptlang.org/ko/play?&classId=2f34722d-e01a-41f3-aa35-6232eed0ed81&assignmentId=030c664f-4393-4107-be90-e96652a1073b&submissionId=5b7fdcd8-c88a-162d-993f-385aa5ff4dd7#code/C4TwDgpgBAqgzhATgSQHYDMD2UC8UDeAsAFBRlSoCGAthAFxzCICWqA5gDRSVv0UCu1AEZIuEapWYAbOlEYt2XSgBNliCHDiz5rNiQC+JEq2BJ0lAMbR4SNFgBMBEuQo16O9gG5n5Hn1SCIojepOTikjJyTLohLipqGlpRCmwhhsQk6PyoFsDMmKhQFuqUpjaIABRUtNrRity8sgHColDh0rUpSqrqmp26AJREoWTqwPyIqMMuLtUQHD4zDfOLM+1SCyMz8b1wq-ppJAD0RwAq4NAAglLMlHvEWTl5BVBgCsDldpgVMMiynxhMAMnFsLAU4JgpBAAHRSTBsCoAA0ALuOAEM7ZAASfC-aFzfRcQAZDcjMdjkNC-PioMjACpdgB9xkk49aUwA-E4AYwYZZJ2iX0iIGhwyxDeJgBWAq+FcNSgACJALJrgA46wCbzVKlI0oPYAKxiCQdaUACwKbAAAhAAB40MBQ6Fg6jK7g9RKyKWAHEHAB1jUqg+j5RmIJxMZksEEy2Vy+UKQtQHwQKEB9h+yHs-yjX3swOm5DBqAhlrhCJR6KgWN+9lxbkpRI5xYpXBp9ILpOLTK4bIr5Ptmh5XuI6RI4cjthjYolfFlittflkGq1EUd+vYxrN1AtMOtY7bSWdbo9nZIQA)

[📖5주차 과제 2](https://www.typescriptlang.org/ko/play?#code/C4TwDgpgBAqgzhATgSQHYDMD2UC8UDeAsAFBRlSoCGAthAFxzCICWqA5gDRSVv0UCu1AEZIuEapWYAbOlEYt2XSgBNliCHDiz5rNiQC+JEq2BJ0lAMbR4SNFgBMBEuQo16O9gG5n5Hn1SCIojepOTikjJyTLohLipqGlpRCmwhhsTGqKaI5lawCCgYmADMUBAAHqaoynD5tkWORKFkiJhSfB6pBkbE6PyoFsDMmKhQFuqUpjaIABRUtNrRity8sgHComUS0ospSqrqmru6AJRNLurA-Iio5y7k8xAcPvcrTy-34dLPzffxh3APvo0iQAPSggAq4GgAEEpMxKIDev1BsNRmAFMBpnZMDN+MxZNiiicnL8LCM4G0IAA6KSYNgzAAGgBdxwAhnbIACT4fHUx76LiADIbmZzucxqX5+VBmYAVLsAPuMinlfKSSwA-E4AYwYVYv+iX0jJOIIyxAxJiJWBm+FcCygACJALJrgA46wCbzdalKsoPYAKxibaRa0ACxGbAAAhUaGB2tTydQXdwDolZNbADiDgA6x61QfT6nrgkxmSwQEh9AZDEZQY1ZU2Yex45j2QkFHH2El3Mjk1CUiN0hks9lQLn4+y8tySoWagcSrgy+W90UDpWqjXT-viuOaXWZ4jpEhlrH1hrmy18O1OmN+WSe70RBMB9gh8phiNRk8rpJJ1Pp9dg0E5nJ5qCAVTXAFLxgsUWLdFMQrYpq2KOt6iwYomw+Vt2xpTsmTZTVikHWhh2FRdmEw8cpTlDDqTnLh1RI7VVy4QBb0cAA1WSNado1wNLdwN3OD90eBMHWdV0+HPLZLxta9g1DahwxpR99gSI4bRTGMmMPQBNVcAXYG0wzEISCAA)

[📖5주차 과제 3](https://www.typescriptlang.org/ko/play?#code/C4TwDgpgBAqgzhATgSQHYDMD2UC8UDeAsAFBRlSoCGAthAFxzCICWqA5gDRSVv0UCu1AEZIuEapWYAbOlEYt2XSgBNliCHDiz5rNiQC+JEqEiwEiAIKrcZpGixQAZARLkoiTFL472Bo8VZgJHRKAGNoeDsMTAAmF1JyKloGJl0AbldyHj5UQRFEDISycUkZOVT2QrcVNQ0tcoU2QsNiEkDgsIjze0wAZigIAA8g1GU4WxRouKIi909vCqa-VuJ0flRQ4GZMVChQ9UogyMQACiSFxqVeWVzhUQGJaW1FpVV1TWfGgEoZt3VgfiIVC-NyJGgQDiZUHcXiQ2ZuErSOHQsg1d5wKFQfTNEgAelxABVwNALFJmJQMat1pttrswApgMceid+MxZEzolAAD4THoxL7xNyhHZweYAOikmDYJwABoAXccAIZ2yAAk+FZYvO+i4gAyGuUqtXMMXZLVQOWAFS7AD7j+vViKkJsAPxOAGMHrYa0XV9DKvjiVsLUIwoPxzDZ8OdZAAiQCya4AOOsAm81hq58GIAVjEjzKYYAFjs2AABIY0MBeMXC6jx7hvOrhwA4g4AOsbD2P89MCHKwLPMXv8+PaiBC4SggFU1wCl4yQ1hstjsoE3UIzutFeizmL12bOsL0BSCyL7RUXJdL5UqoKrWb0NeCTbqXSfjVxzVbDwaT7aHc778ejRXNCbALejgANVy9ijwvA9DtiBaEgpxnKJVxOfAKHBcNozjBNZGTVNSnDLN2DzQYCyLEsyzdD4oDDWsy0Avgw0ATVXAF2BsMsRAkggA)

[📖5주차 과제 4](https://www.typescriptlang.org/play?#code/JYOwLgpgTgZghgYwgAgAoTMg3gKGcsATwAcIAuZAZzClAHMAaPZEOAW3Kpvqfzjs4gArmwBG0XsgDuEYHQAWYCsLEScAXwDcOHKEixEKACIB7OsggAPSCAAmlNBmzNRUCBFsVqtEIw069aHgkZABhOEwrG3tHTFx8BBMAGxMoL25fJnUdIlJYgBUSFABeZFM6AB9wsG0cRJBqZFIwSgoACnQwQtIASgBtAF1kUr7mePxkACJciEmKSdszScl8SdYOOanAU87AEqHl5lX+WYoAVhWpmTlFTYAmAAZzydd3W03JwBrOwA6l98AQnsnmdSScarGZvRZ0fYTKbrY5TQAXHXDIRNJkdbo9LgowJsAIwPA5TZ4eN6ADxXACct-3wgLG+OmRTeCAiSNWMLegA-u1lMqaoigAZnRskxmwALI9EikoG9AAE1gFQJinIKn4YFTUHzBlYx4s+aAFXmtZyUQIcfyrljeaLkqk3oAHdcAkwNy7IDHQwIQgBBgYAmEBNHxgTqUNqheQQBAAa26KHSPjoPXGAHoAFTMZqUAB0MFSAFFEPI2m1msh2uVkBUwhEej1hgA+ZxQ4AwXMYZMzYbFUoBoOhorR-EJD2UZIQZMpOj1sA9fHZSlj-BxmM6HsNTBuShCJKYUpJ1PAVfQHPNCidMPl4pVpVuMBCKCekeNorN1uBkOHgFT5D1PtJAdDtpLlej7TZHBiG9X02gWJYem0IC9BAyY1UmCCgA)

---
# 4주차

🔋 2023.09.20

[📖4주차 수업 자료](https://gainful-appendix-a7a.notion.site/Type-Alias-Interface-37dba0ea83bb4b40aa24833bcd7bb495)

# 📂Type Alias

- `type alias`는 타입에 대한 이름을 지정하여 재 사용 가능하도록 하는 구문입니다.

```js

type Point = {
  x: number;
  y: number;
};

function printCoord(pt: Point) {
  console.log("The coordinate's x value is " + pt.x);
  console.log("The coordinate's y value is " + pt.y);
}

printCoord({ x: 100, y: 100 });

```

- `객체 타입`은 위와 같이 type을 선언하여 사용 할 수 있습니다. 

- `printCoord`의 파라미터 값에 타입 어노테이션을 이용해 pt에 대한 타입을 지정했던 방식과는 달리 상단에 type alias를 선언해서 pt에 지정해주는 방식을 사용함으로 써 Point라는 타입을 재사용 할 수 있도록 처리했습니다.

- 유니온 타입의 경우도 아래와 같이 사용 가능합니다.

```js

type ID = number | string;

```

# 📂Interfaces

- 인터페이스는 type의 이름을 지정하는 또 다른 방법입니다.

# 4주차 과제 1

[📖4주차 과제 1](https://www.typescriptlang.org/ko/play?&classId=2f34722d-e01a-41f3-aa35-6232eed0ed81&assignmentId=64e5512f-9a65-4f5e-8d3f-3f264fec083e&submissionId=1af5914e-54a3-8b14-c0db-3924dffab99d#code/MYewdgzgLgBAJgQygmBeGBtA3gKBvmAIgEs5CAuIgBwEZCAaPAwsBAWwFMKjAagcB+ahk3yEqAJ2LAulGgFYADHMYEi0EMADW3GoqFFgSDgHMQogJ7dCgXaHAESuDlhOMQigArmCgXtAUkJMAvkowuPakFlQATHbMrJwWgB6NgB1LgIG9UcJiElIwsgo5gcKqGtwyeXoGxmYWgCATgAnjgDgTtiWEEFQcwBbEAOz0WQBsAOIAQjAASgCCALK++AFMwcyhlCIAzKlEMZmEgA9LgCqDgARzqyLiktzhOTr2BZqUp436UEYm5ouAGuOAGp0HEMQAXhuT-oFzYQLagAFgO6wslkArn0HdLHa7yc7MS7cJZI4R3B4VRY2A6OZwgNweSiI-6zXQkMiLKgycHsDaAFnXAADNgAfl2FHTLaM7olRQNRXLI8wiY8pPIg1ep4pyudwWGQ+fwAXRwOAAZm5gFBiOAYOl3AAFUQgOAuTUASTAqpAAAoxMbTVBKHNSJRoOIwIYANxMdauqDur1MOEcShgFxsABGHFE3vwl1D4ajMaYIsefoDsfg0sJ7gA-OniB6YAAfGBhyPRzPNVr5mBuwuBuPfDi1+se71+ACUQRT4GgQRgpG6626we6l26qbM3XxMqg45awHHzZgfjQuqNJs13qYABsOLBZzn7nBDRkd-hiKqYNaoKYWiBr0eiWhUOgAORtwzv7uAmCgSBD2zIl9WjSR3AQQwOHXKgEFECAOAtKBrWfdxum0TtM3wVCTzPSQYI5GAAFob2DGAACoswJECwI4CCoJgAB6QU5Ew-wYA4XcEMHa9b3vDhHyoudXw-cskx-HtlBwjhT0I9AyJInDMzXTjuL-aTZIyAjz38FV8AA-sABUQGQXc8Og+SOQAOj5AAZNQEH3ABlf0G2tNj9L7WBjNMgARYD3Bk8z1w08ybJAez9Gc1yPXci8YH3WBRA4CAXF3WB0AAAzNXzKAAEiwUgAhgQAXccAEM78qwdZisAABrAEqayqfMc8y-EABbHukAA1XAA9xmrGpMxz-OowLNMkNrukAGvHAAOayrLmKwAXOcAGUXJsAGs7KqnUw-Ey+KrxvatgBgABCN8YDcOAOFVQsZN-XRktS9KYAAaiy7pABKhwBM5ZmxdNuUvSeN2lcjvQU7zsuuBruUW60tgJ6YEy7oeBKwAIyZm5tvt0phkqgFxRDAGBIfSjsVStUQbwM2A7S3WBBMQZBwf-LyN3tc1LRAbSDU3B0LStW0Oc1Dz6cgEB9ys3cQEMHmmagLmQDYvwgA)

```js

const data = [{
    "id": "p1",
    "name": "사과",
    "price": 1500,
    "stock": 10,
    "category": "식품",
    "discount": "10%"
  },
  {
    "id": "p2",
    "name": "노트북",
    "price": 1500000,
    "stock": 5,
    "category": "전자제품",
    "spec": "i7, 16GB RAM"
  },
  {
    "id": "p3",
    "name": "티셔츠",
    "price": 20000,
    "stock": 20,
    "category": "의류",
    "size": "M"
  },
  {
    "id": "p4",
    "name": "식빵",
    "price": 2500,
    "stock": 30,
    "category": "식품",
    "discount": 500
  },
  {
    "id": "p5",
    "name": "휴대폰",
    "price": 1000000,
    "stock": 10,
    "category": "전자제품",
    "discount": "5%"
  }]

function printProductInfo(product: {
  id: string;
  name: string;
  price: number;
  stock: number;
  category: string;
  discount?: string | number;
  spec?: string;
  size?: string;
}) {
  const { id, name, price, stock, category, discount, spec, size } = product;

  let discountedPrice;

  if (typeof discount === 'string') {
    const discountPercentage = parseInt(discount, 10);
    discountedPrice = price - (price * discountPercentage / 100);
  } else if (typeof discount === 'number') {
    discountedPrice = price - discount;
  } else {
    discountedPrice = price;
  }

  const TotalPrice = price.toLocaleString();
  const TotalDiscountedPrice = discountedPrice.toLocaleString();

  let result = `ID: ${id}, 이름: ${name}, 가격: ${TotalPrice}원, 할인가: ${TotalDiscountedPrice}원, 재고: ${stock}, 카테고리: ${category}`;

  if (spec !== undefined) {
    result += `, 스펙: ${spec}`;
  }

  if (size !== undefined) {
    result += `, 사이즈: ${size}`;
  }

  return result;
}

for (const product of data) {
  const productInfo = printProductInfo(product);
  console.log(productInfo);
}

```

---
# 3주차

🔋 2023.09.13

[📖3주차 수업 자료](https://gainful-appendix-a7a.notion.site/Object-Union-d9a258182b464231bf3db529290dc480?pvs=4)

# 📂일반적인 유형 (Object, Union)

## Object Types

- 객체 타입을 타입스크립트에서 정의하는 법

```tsx

function printUserName(name: string){ 
	console.log(name)
}

function printCoordinate(pt: {x: number, y: number}){
	console.log(`x 좌표 ${pt.x}`);
	console.log(`y 좌표 ${pt.y}`);
}

printCoordinate({ x: 3, y: 7 });

```
- 함수 파라미터에 두개의 속성이 있는 타입을 `number`로 정의했습니다.

- 명시적으로 타입을 지정하지 않을 경우 `any` 타입으로 지정됩니다.

- 이때, `noImplicitAny` 설정이 되어있다면 에러가 발생하고, `any` 타입으로 가정하여 에러가 발생하지않습니다.

## Optional Properties

- 객체 타입을 지정할 때 경우에 따라 일부 속성값은 들어갈 수도 있고, 들어가지 않을 수도 있는 선택사항일수도 있습니다.

- 그럴 경우에는 해당 속성 값의 바로 뒤에 `?`를 넣어서 표현

```tsx

function printUser(obj: { name: string, age?: number }, ) {
	if(!obj) console.log(`아무런 정보가 없습니다.`);
	else{
		console.log(`Name: ${obj.name}`);
		if (obj.age) console.log(`Age: ${obj.age}`);
	}
}
printUser();
printUser({name: "홍길동"});
printUser({name: "김길동", age: 21});

```

## 자바스크립트에서 ?를 사용한 문법

### Optional Chaining : ?.

- Optional Chaining은 객체의 속성이나 배열의 요소, 함수의 리턴값이 `null` 또는 `undefined`일 경우에 안전하게 접근할 수 있게 해주는 JavaScript 문법입니다.

### Optional Chaining을 사용하지 않은 경우

```tsx

function printCity(obj: { name: string; address?: { city: string }}) {
	console.log(`Name: ${obj.name}`);

	if( obj.address & obj.address.city) {
		console.log(`City: ${obj.address.city}`);
	}
}

printCity({ name: "홍길동" });
printCity({ name: "김길동", address: { city: "서울" } });

```

### Optional Chaining을 사용한 경우

```tsx

function printCityO(obj: { name: string; address?: { city: string }}) {
	console.log(`Name: ${obj.name}`);
	// address에 city값이 있을 경우 진행하고 없을 경우 "알수없음" 출력
	console.log(`City: ${obj.address?.city || "알수없음"}`);
}

printCity({ name: "홍길동" });
printCity({ name: "김길동", address: { city: "서울" } });

```

### Temary Operator : ? :

- Temary Operator는 `조건 ? 참일때 리턴 : 거짓일때 리턴` 형식으로 if문을 대신하여 사용할 수 있는 연산자입니다.

```tsx

function printUser(obj: { name: string; age?: number }){
	console.log(`Name: ${obj.age}`);
	if(obj.age) {
		console.log(`Age: ${obj.age}`);
	}else{
		console.log("Age: UnKnown");
	}
	// const result = obj.age ? obj.age : 'Unknown';
	// console.log(result)
}

printCity({ name: "홍길동" });
printCity({ name: "김길동", age: 21 });

```

### Temary Operator 사용 코드

```tsx

function printUser(obj: { name: string; age?: number }) {
  console.log(`Name: ${obj.name}`);
  console.log(`Age: ${obj.age ? obj.age : 'Unknown'}`);
}

printUser({ name: "홍길동" });  // Output: "Name: 홍길동", "Age: Unknown"
printUser({ name: "김길동", age: 21 });  // Output: "Name: 김길동", "Age: 21"

```

# Union Types

## Defining a Union Type

- 타입을 결합하는 방법중 하나는 union type입니다. union type은 두개 이상의 다른 타입으로 구성된 타입으로 해당 타입중 하나가 될 수 있는 것을 의미합니다. 이러한 타입들을 유니온의 각 member라고 합니다.

- string 또는 number가 될 수 있는 타입을 선언할 수 있습니다.

```tsx

function printId(id: number | string) {
  console.log(`당신의 ID: ${id}`);
}

printId(101);
printId("202");
printId({ myID: 22342 });

```

## Working with Union Types

```tsx

function printId(id: number | string) {
  console.log(`당신의 ID: ${id.toUpperCase()}`);
}

printId("202");

```

- 타입스크립트에서 `string | number` 로 유니온 타입을 사용 할 경우 해당 함수 내부에서는 두 타입 모두가 허용하는 속성과 메서드만 사용 할 수 있습니다.

- 이런 상황에서의 해결책은 javascript 코드를 기반으로 타입스크립트가 해당 타입을 ‘추론’ 할 수 있도록 명시적으로 처리하는 것입니다.

```tsx

function printId(id: number | string) {
  if (typeof id === "string") {
    console.log(`당신의 ID: ${id.toUpperCase()}`);
  } else {
    console.log(id)
  }
}

printId("202");

```

# javascript의 비교 연산자

## && 연산자 (AND 연산자), || 연산자 (OR 연산자)

- `&&` 연산자는 두 피연산자가 모두 true일 경우 true를 반환합니다. 첫 번째 피연산자가 false이면 두 번째 피연산자는 체크하지 않습니다. (short-circuit evaluation - 단축평가계산)

- 좀 더 정확하게 표현하면 첫번째 피연산자가 `Falsy`이면 첫번째 피연산자 값을 리턴하고 모두 `Truthy` 면 마지막 피연산자 값을 리턴합니다.

- `||` 연산자는 두 피연산자 중 하나라도 true일 경우 true를 반환합니다. 첫 번째 피연산자가 true이면 마찬가지로 두 번째 피연산자는 평가되지 않습니다.

- 여기도 좀 더 정확하게 표현하면 첫번째 피연산자가 Truthy면 첫번째 피연산자를 리턴하고 둘 다 Falsy면 마지막 피연산자를 리턴합니다.

```tsx

let isAccountActive = true;
let isEmailVerified = true;

if (isAccountActive && isEmailVerified) {
  console.log("로그인 성공!");
} else {
  console.log("로그인 실패!");
}

if (!isAccountActive || !isEmailVerified) {
  console.log("로그인 실패!");
} else {
  console.log("로그인 성공!");
}

```

```tsx

let isConnected = false;
function fetchData() {
  console.log('데이터를 가져옵니다.');
	return true
}

if (isConnected && fetchData()) {
  console.log('데이터 조회 성공');
}

```

```tsx

let age = 25;
let isAdult = (age >= 18) && "해당 사용자는 성인입니다.";

console.log(isAdult);

age = 15;
let message = (age >= 18) || "해당 사용자는 성인이 아닙니다.";

console.log(message);

```

## Truthy, Falsy

- `JavaScript`에서 `"truthy"`와 `"falsy"`는 논리 연산자의 피연산자가 true 또는 false로 간주되는 경우를 설명하는 용어입니다. 이 차이를 이해하지 않고 각종 조건문을 사용하면 코드가 의도한대로 동작하지 않는 상황을 마주할 수 있습니다.

- `Javascript`에서 아래의 조건절들은 모두 `truthy`로 취급됩니다.

```tsx

if (true)
if ({})
if ([])
if (42)
if ("0")
if ("false")
if (new Date())
if (-42)
if (12n)
if (3.14)
if (-3.14)
if (Infinity)
if (-Infinity)

```

- 정리하면 아래와 같은 값들이 `truthy` 입니다.

1. ` **`true`**
2. 모든 숫자 (0을 뺀)
3. 모든 문자열 (**`''`, `“”`**을 제외)
4. 모든 객체와 배열 (빈 객체와 빈 배열 포함)

- `Javascript`의 이러한 특징 때문에 아래와 같은 코드는 문제를 발생 시킬 수 있습니다.

```tsx

const score = 0;

if (score) {
  console.log(`현재 스코어: ${score}`);
} else {
  console.log('서버로부터 스코어 값을 받아오지 못했습니다');
}

```

- 위 코드의 경우 다양하게 해석 될 수 있지만 의도는 아래와 같다고 가정하겠습니다.

1. `score` 값을 서버로부터 받아옴
2. `score` 값 자체가 비어있을 수 있기에 `if (score)`를 통해 예외처리
3. 현재 서버로부터 `score`의 값을 받아왔고 해당 값은 `0`

- 따라서 위 코드의 결과는 `현재 스코어: 0` 이 출력되어야 합니다.

```tsx

function welcomePeople(x: string[] | string) {
  if (Array.isArray(x) && x.length > 0) {
    console.log(`${x[0]}님 외 ${x.length}명의 방문을 환영합니다.`);
  } else {
    console.log(`${x}님 환영합니다.`);
  }
}

```

- `Array.isArray` 메서드를 이용해 array타입인지 체크하고 각각의 케이스에 맞는 동작 코드를 수행하도록 처리되어 있습니다. 해당 코드에 따라 타입스크립트는 welcaomePeople에서 사용되는 유니온 타입들중 현재 x값이 array인지 string인지 체크 할 수 있습니다. 따라서 오류가 발생하지 않습니다.

- 유니온 타입의 모든 맴버가 공통적으로 가지고 있는 메서드를 호출할 때 역시 별도의 오류 메세지를 발생시키지 않습니다. 대표적으로 slice 메서드는 string과 array 모두 가지고 있는 메서드입니다. 따라서 아래의 코드는 오류를 발생시키지 않습니다.

```tsx

function getFirstThree(x: number[] | string) {
  return x.slice(0, 3);
}

console.log(getFirstThree("안녕하세요"));
console.log(getFirstThree([1,2,3,4,5,6,7,8]));

```

## 🏠3주차 과제

1. 위 함수의 문제점을 찾아보세요. 위 함수가 문제가 발생하는 케이스를 작성하고 해결하기 위해서 어떻게 해야할지 코드를 수정해보세요.
타입스크립트 플레이그라운드(https://www.typescriptlang.org/play) 에서 코드를 작성하고 주석을 이용해 수정한 내용과 설명을 작성해주세요.
코드 링크 (Export -> Copy as Markdown Link)와 코드 화면을 캡쳐해서 첨부 후 제출하세요.

```tsx

function calculateAverage(scores: number[]) {
  let total = 0;
  let count = 0;
  for (const score of scores) {
    if (score) {
      total += score;
      count++;
    }
  }
  return total / count;
}

```

[📖3주차 과제 1](https://www.typescriptlang.org/play?#code/GYVwdgxgLglg9mABBAhgGwiNKoFMCCAbrgE4oDmuAFAM4Rwm40BciYIAtgEakDaAugEpEAbwBQiRGlxREUOFHSIAvIgAMAbglSZyOOFmrN24A0RV6YGrLoNciOMES3GNYeMmSA9F8QByNT9EQE41wAFxxAA5FAjATBrwv2B0GgBPP0AkGsAXccRAG+XAC1XADBbAFtHACPHAEXHEQF6awAaxwAXRwBSmxEAObsAcCcAAGsRAHB7AXYHAA1XADCHAEebEYsBWocAJpsATpoA6bW9fQBA1wBrxxEAVecAdlprAHEGGmCdaekZBQB9OxEAagcBKscANVcAb0fVygCJEtBT7wB0OxEAQGsAficvAA5rEQAs3YAdob+w3G01miB8iF25gAhDAaFEIvs7IJ3IhABkzgB-2xB9QCoE+UbpFooAPccAA5OIQAio4AZpspgFU10mXBrrd6AAZ6KohAC6rgB9RxCAS1XJjNPDC9gikdFUYcMZDJPJFGhEABqVQuXAaRCQgC+kPoBiVSo12h1IsYUBAJCQ8qUvj1YCgWh1YksNDg0imaDg5As6Ew2DwRFIFGovAAjGoADSIABMkcQAGY43GAKxxgBsaiEgg0QA)

- 답안

```tsx

function calculateAverage(scores: number[]) {
  let total = 0;
  const count = scores.length;
  for (const score of scores) {
    total += score; 
    count++; 
  }
    return count === 0 ? '입력값X' : total / count;
}

console.log(calculateAverage([10, 20, 30, 0, 50, 60]));

```

2. 

[📖3주차 과제 2](https://www.typescriptlang.org/ko/play?#code/MYGwhgzhAEBCD2YBOATASgUwgVxAF2gG8AoaaYeAOwjyW2D3iQApSzoAHbAIxAEtg0NADkAqgFkA+gBEAogGUAwgC5oNJH0oBzADRsyXXgOiKAggBVZAcQDyaAJqTh41es279nHv0EB1NACSljIWsq607nrsXkaCABJB8qqU2AC23BhIUeyGPtAAYgEAMrKSisLmyWkZSGwAlEQAvsTNxABm2JQMfFScGpR4CMgozEhYuHiqQ6iYOPgNJGQU1PAgGAB0IPBazAAGACSEY3N46yISMgqKjdAAtNCHxxPrZpa2Dk7iN-eP4-jr-iCpWkoW+0EADhOAGLWHkc-qcEuZ5GDABUzgADewAwy4AfccAGEMwp7-QolMoVRq7OotYjtDB4YAAC2YAHJaXg8BwIMoAPQcmhgPACW7LPAYAYQW4QTIANw2EAAzOswBxbpQmHhaRhIHhbgAmeWpMAALyoYAA7hB1hRUhzjhwqOL1gArCBUBl1daq4XMUZwuoAXgAfItoGM8NgkJQg3CHU7KMxyY1Xe6Y-waNB-UQ2MnTm0mLIwHTPSheWBVGBKABPX0BzwcfqDRCoZiFvBgclkeMtV3AXn5zJIVN+9NLW2rDZbHa9uN1ADcQA)


- 답안

```tsx

function printBoard(result: {
  RNUM_DESC: string;
  CATEGORY_NM: string;
  WRITE_DATE: string;
  HITS: number;
  FILE_CNT: number;
}) {

  const { RNUM_DESC, CATEGORY_NM, WRITE_DATE, HITS, FILE_CNT } = result;

  console.log(`${RNUM_DESC} - ${CATEGORY_NM} - ${WRITE_DATE} - 조회 ${HITS} - 첨부파일수 ${FILE_CNT}`)
}

fetch('https://static-contents-serve.s3.ap-northeast-2.amazonaws.com/response.json').then((result)=>{
  return result.json()
}).then(list => {
  list.forEach((data: any)=>{
    printBoard(data)
  })
}).catch(err => {
  console.log(err)
});

```

---
# 2주차

🔋 2023.09.06

[📖2주차 수업 자료](https://gainful-appendix-a7a.notion.site/Type-550436e1eba6414bbc1d2e5fb5b19e6a)

## 📂원시 타입

* 자바스크립트에서 주로 사용되는 원시 타입인 `string`, `number`, `boolean`은 타입스크립트에서 대응하는 타입이 있습니다.
* `string`은 "Hello World"와 같은 문자열 값을 나타냅니다.
* `number`는 42와 같은 숫자를 나타냅니다. 자바스크립트에는 정수에 대한 특별한 런타임 값이 없으므로 int나 float에 해당하는 값을 없으며 모든 것이 숫자입니다.
* `boolean`은 `true`, `false`두 값에 사용됩니다.
* 원시 타입의 이름을 지정할때 String, Number와 같이 대문자로 시작하면 안됩니다.

## 📂원시 타입
- 불변성
- 메모리 효율성
- 비교 시 값 자체를 비교 (Call by value)

## 📂래퍼 객체
- 가변성
- 객체로서 추가 메서드 및 프로퍼티를 가질 수 없음
- 비교 시 참조를 비교 (Call by reference)

## 📂배열
* 배열에 타입을 지정할 때는 그 배열을 구성하는 타입과 [] 표기를 사용합니다.

## 📂any
* TypeScript의 any타입은 변수가 어떤 타입이든 될 수 있음을 나타냅니다. 일종의 프리패스권 또는 타입체크를 회피 하는 용도로 사용되다 보니 타입스크립트에 익숙하지 않은 개발자가 개발하는 과정에서 무분별하게 많이 쓰이게 되는 타입중 하나입니다.
* 이름 그대로 모든 것을 허용하는 타입입니다.
* 자바스크립트 프로젝트를 타입스크립트로 마이그레이션하는 과정이 아닌 한, 기본적으로 사용하지 않는 것을 권장

## 📂any는 아래와 같은 상황에서 사용될 수 있습니다.
* 해당 라인이 문제가 없을것이라는 것을 확신 할수 있을 때
* 타입정보가 없거나 미흡한 외부 라이브러리 등을 사용할 때
* 실행시점에 타입이 결정되어서 타입을 미리 정할 수 없을 때

## 📂noImplicitAny
* 기본적으로 타입스크립트에서 타입이 지정되어 있지 않은 변수들에 대해 `문맥상 타입을 추정할` 수 없다면 컴파일러에서는 `any`타입으로 가정합니다.

## 📂Type Annotations on Variables

* 타입스크립트는 일반적인 언어에서 사용하는 int x = 0; 와 같은 “왼쪽에 타입을 정의하는” 스타일을 사용하지 않습니다. 타입 어노테이션은 항상 작성한 내용 다음에 오게 됩니다.

## 📂Functions

- Parameter Type Annotations

* 함수를 선언할 때 각 매개변수 뒤에 타입 어노테이션을 추가하여 함수가 허용하는 매개변수 타입을 선언할 수 있습니다. 

* 매개변수에 타입 어노테이션이 지정되면 해당 함수를 호출 할 때 인자값을 체크하게 됩니다.

## 📂Template strings - 백틱(``) 사용 문자열

* 템플릿 스트링은 ES6에서 도입된 자바스크립트의 문자열 처리 방식중 하나입니다. 이 방식은 기존의 문자열을 다루기 위한 작은따옴표(‘’ ), 큰따옴표(“”) 대신 백틱(``) 이라는 문자를 사용하여 표현됩니다.

* 이를 사용하면 두가지 장점을 가져갈 수 있습니다.

1. 멀티라인 문자열: 백틱을 사용하면 문자열을 여러 줄에 걸쳐 쓸 수 있습니다.

2. 문자열 삽입: ${}를 사용하여 문자열 안에 변수나 식을 삽입할 수 있습니다.

## 📂Return Type Annotations

## 📂Functions Which Return Promises

* Promises를 리턴하는 함수에 타입 어노테이션을 달고 싶다면 Promise 타입을 사용해야 합니다.

## 📂Promise?

* Promise는 비동기 작업의 최종 완료 또는 실패를 나타내는 객체입니다. 주로 서버와의 비동기 통신, 파일 읽기 등에 사용됩니다.

* 비동기 작업 - 일반적으로 Javascript는 코드를 실행할때 위에서부터 아래의 순서대로 실행되게 됩니다.

## 📂Anonymous Functions

* 익명 함수(또는 arrow function)의 경우도 비슷한 방식으로 타입 어노테이션을 달 수 있습니다.  

## 📂익명함수?

* 익명 함수(Anonymous Function)는 이름이 없는 함수를 의미합니다. 이러한 함수는 주로 함수의 인자로 전달되거나, 변수에 할당되어 사용됩니다. 

* 기본 문법 - JavaScript 및 TypeScript에서 익명 함수를 만드는 가장 기본적인 방법은 다음과 같습니다

* 콜백 함수로 사용 - 익명 함수는 콜백 함수로도 많이 사용됩니다. 예를 들어, 배열의 map 메소드에 익명 함수를 전달할 수 있습니다

* 화살표 함수 - ES6(ES2015) 이후, 화살표 함수(arrow function)라는 더 간단한 문법으로 익명 함수를 만들 수 있습니다

* 즉시 실행 함수(IIFE) - 익명 함수는 즉시 실행되도록 할 수도 있습니다. 이를 즉시 실행 함수 표현식(IIFE, Immediately Invoked Function Expression)이라고 합니다.

* 익명 함수는 함수의 이름을 명시하지 않기 때문에 디버깅이 어렵거나, 재귀 호출 같이 함수가 자기 자신을 호출해야 하는 상황에서는 사용이 제한될 수 있습니다. 그러나 간단한 로직을 변수에 할당하거나, 콜백으로 전달해야 하는 경우에는 코드를 간결하게 만들어 주는 장점이 있습니다.

---
# 1주차

[📖1주차 수업 자료](https://gainful-appendix-a7a.notion.site/acee91b0b4bc4f3c904c33bb50024ab0?pvs=4)

🔋 2023.08.30

- 💻오리엔테이션

- 📃타입스크립트 개요
* TypeScript는 Microsoft에서 개발한 자바스크립트의 확장 버전으로, 정적 타입 검사와 클래스 기반 객체 지향 프로그래밍을 추가한 언어입니다.
* TypeScript는 큰 규모의 애플리케이션 개발에 적합하며, 오류를 줄이고 가독성과 유지보수성을 향상시키는데 도움을 줍니다.

- 📜JavaScript와 TypeScript의 차이점
* JavaScript는 동적 타입 언어입니다. 즉, 변수의 타입이 실행 시점에 결정되며, 변수의 타입을 변경할 수 있습니다.
* TypeScript는 정적 타입 언어입니다. 변수의 타입은 선선 시점에 결정되며, 이후 변경할 수 없습니다. 이러한 특성은 개발자가 코드에서 오류를 더 쉽게 발견할 수 있도록 도와줍니다.
* TypeScript는 클래스, 인터페이스, 제네릭 등과 같은 고급 객체 지향 프로그래밍 기능을 제공합니다.

- 📃TypeScript를 사용해야 하는 이유
1. 📋더 나은 에러 검출
* 정적 타입 검사를 통해, 개발자는 컴파일 시점에 코드의 오류를 더 쉽게 발견할 수 있습니다.

2. 📋개발 도구(IDE)의 지원 향상
* 정적 타입 검사는 개발 도구에게 유용한 정보를 제공합니다. 이를 통해, 개발 도구는 더 나은 자동완성, 리팩토링 도구, 타입 검사 등을 제공할 수 있습니다.

3. 📋향상된 문서화 및 코드 가독성
* TypeScript의 타입 시스템은 코드를 작성하는 개발자 뿐만 아니라 다른 개발자에게도 변수나 함수가 어떤 값을 가지거나 변환해야 하는지 명확히 알려줍니다. 이러한 코드는 팀 작업이나 큰 프로젝트에서 특히 중요합니다.

- TypeScript 설치 및 개발 환경 설정
1. 📋Node.js 설치 : TypeScript는 Node.js 환경에서 실행되므로, 먼저 Node.js를 설치해야 합니다.
2. 📋TypeScript 설치 : Node.js를 설치한 후에는, npm을 사용하여 TypeScript를 설치할 수 있습니다. 터미널에서 다음 명령어를 실행합니다.
`npm install -g typescript`
3. 📋텍스트 에디터 설치 : Vscode, subtime Text, Atom 등의 텍스트 에디터를 설치합니다. 이중 Vscode는 TypeScript에 대한 강력한 지원을 제공하므로, TypeScript 개발에 매우 적합합니다.

- 컴파일 언어 & 인터프리터 언어 & 트랜스파일 언어

*컴파일언어, 인터프리터언어*
* 컴파일러는 고수준 언어로 작성된 소스 코드를 한 번에 기계어나 다른 저수준 언어로 변환하는 프로그램입니다. 이 변환된 코드는 별도의 파일로 저장되며, 이 파일을 실행하며 프로그램을 동작시킵니다.

* 📜컴파일 언어의 특징
1. 실행 속도가 빠름
2. 저수준 언어로 변환된 코드를 배포하기에 코드에 대한 보안성이 용이
3. 컴파일 과정에서 전체 코드에 대한 문법 오류를 확인 할 수 있습니다.
4. 코드의 규모가 크다면 컴파일이 오래 걸릴 수 있습니다.
5. 실행하기 전 반드시 컴파일 과정을 거쳐야 하기에 디버깅이 불편합니다.
6. 코드의 변경이 생기면 반드시 컴파일을 다시 해야 합니다.

* 📜인터프리터는 고수준 언어로 작성된 소스 코드를 한 줄씩 읽어가면서 즉시 실행하는 프로그램입니다. 이는 별도의 변환과정이 없이 소스 코드를 직접 실행한다는 것을 의미합니다.

* 📜인터프리터 언어의 특징
1. 코드의 변경과 실행을 매우 빠르게 할 수 있다보니 디버깅 등이 쉽다.
2. 실행 속도가 느릴 수 있습니다.
3. 문법이 잘못된 코드가 있더라도 실행해서 해단 코드를 호출하기 전까지는 에러가 발생하지 않습니다.
4. 소스코드 그대로 실행하다 보니 코드에 대한 보안이 부족합니다.

- 패키지 매니저
* 패키지 매니저는 코드 라이브러리를 관리해주는 도구를 의미합니다.

* NPM : Node.js에서 사용되는 패키지 매니저
* PIP : Python에서 사용되는 패키지 매니저
* Maven, Gradle : Java에서 사용되는 빌드 도구 겸 패키지 매니저
* NuGet : .NET에서 사용되는 패키지 매니저
* apt, yum : Linux에서 사용되는 패키지 매니저
* Homebrew : macOS에서 사용되는 패키지 매니저

* 📜패키지 매니저를 사용해야 하는 이유
1. 손쉬운 외부 패키지 설치
* TypeScript 파일 다운로드, 설치, 각종 설정 -> npm install typescript

2. 프로젝트에 사용된 패키지 버전의 관리
* 설치된 패키지의 버전을 수동으로 추적해야 하고 이 정보를 별도 문서나 주석으로 남겨둬야 함 -> package.json과 같은 파일을 통해 자동으로 관리

3. 패키지의 의존성 관리
* 각 패키지의 의존성을 직접 파악하고 필요한 패키지를 버전에 맞게 하나씩 설치 -> 자동으로 해줌