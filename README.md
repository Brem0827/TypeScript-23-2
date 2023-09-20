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
3. 💭[4주차](#4주차)➡️

---
# 4주차

🔋 2023.09.20

[📖4주차 수업 자료](https://gainful-appendix-a7a.notion.site/Type-Alias-Interface-37dba0ea83bb4b40aa24833bcd7bb495)

# 📂Type Alias

- 지금까지 우리는 `type annotation`을 통해 타입을 정의해왔습니다. 

- 이 방법은 편리하지만 `동일한 타입`을 `두번 이상` 사용하는 경우 중복되는 코드가 많아지는 단점이 있습니다. 

- 이제 사용해볼 `type alias`는 타입에 대한 이름을 지정하여 재 사용 가능하도록 하는 구문입니다.

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

[📖4주차 과제 1](https://www.typescriptlang.org/ko/play?&classId=2f34722d-e01a-41f3-aa35-6232eed0ed81&assignmentId=64e5512f-9a65-4f5e-8d3f-3f264fec083e&submissionId=1af5914e-54a3-8b14-c0db-3924dffab99d#code/MYewdgzgLgBAJgQygmBeGBtA3gKBvmAIgEs5CAuIgBwEZCAaPAwsBAWwFMKjAagcB+ahk3yEqAJ2LAulGgFYADHMYEi0EMADW3GoqFFgSDgHMQogJ7dCgXaHAESuDlhOMQigArmCgXtAUkJMAvkowuPakFlQATHbMrJwWgB6NgB1LgIG9UcJiElIwsgo5gcKqGtwyeXoGxmYWgCATgAnjgDgTtiWEEFQcwBbEAOz0WQBsAOIAQjAASgCCALK++AFMwcyhlCIAzKlEMZmEgA9LgCqDgARzqyLiktzhOTr2BZqUp436UEYm5ouAGuOAGp0HEMQAXhuT-oFzYQLagAFgO6wslkArn0HdLHa7yc7MS7cJZI4R3B4VRY2A6OZwgNweSiI-6zXQkMiLKgycHsDaAFnXAADNgAfl2FHTLaM7olRQNRXLI8wiY8pPIg1ep4pyudwWGQ+fwAXRwOAAZm5gFBiOAYOl3AAFUQgOAuTUASTAqpAAAoxMbTVBKHNSJRoOIwIYANxMdauqDur1MOEcShgFxsABGHFE3vwl1D4ajMaYIsefoDsfg0sJ7gA-OniB6YAAfGBhyPRzPNVr5mBuwuBuPfDi1+se71+ACUQRV+FAkFgWBgpG6626we6l26qbM3XxMqgk5awEnzZgfjQuqNJs13qYABsOLB5zn7nBDRk9-hiKqYNaoKYWiBbyeiWhUOgAORtwyf7uAmB+2gLMCSJfVo0kdwEEMDhNyoBBRAgDgLSga1X3cbptE7TN8HQs8L0kOCORgABaO9gxgAAqECF3A0RIOQGCYAAekFORsP8GAOH3JDh1ve9Hw4Z8aNPd8v3LJM-x7ZQ8I4c9iPQCiyLwzMN243iANk+SMiIy9-F7QDwGAgAVEBkH3AjYMUjkADo+QAGTUBBDwAZX9BtrQ4vsjNgUzzIAEWzIk5MszctMsuyQEc-RXPcj1PKvGBD1gUQOAgFx91gdAAAMzX8ygABIsFIAIYEAF3HABDOwqsHWUrAAAawBKmuqvznMsvxAAWx7pAANVwAPcbq5qzOcwLQPcEKOQ67pABrxwADmuqy5SsAFznABlF6bABrO6qZ1MPxssSm872rYAYAAQg-GA3DgDhVULOT-10VL0symAAGocu6QASocATOW5uXbbVIMvbrU+H5jtO87LuuuBbuUe6MtgF6YGy7oeDKwAIybm5tfv0vwgA)

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

function discountString(
  price: number,
  discount: string | number
): string{

  return (typeof discount === 'number') ?
    `할인가: ${(price - discount).toLocaleString()}원`
    :
    `할인가: ${(price * (1 - parseInt(discount) / 100)).toLocaleString()}원`
    }

data.forEach((product: {
  id: string,
  name: string,
  price: number,
  stock: number,
  category:string,
  spec?: string,
  size?: string,
  discount: string | number
}) => {

  const { id, name, price, stock, category, discount } = product;

  let result: string = `ID: ${id}, 이름: ${name}, 가격: ${price}원`;

  console.log(result);
});

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