[![Since](https://img.shields.io/badge/since-2023.08.31-333333.svg?style=flat-square)](https://github.com/Brem0827/Tech-Stack)
[![author](https://img.shields.io/badge/author-Brem0827-0066FF.svg?style=flat-square)](https://github.com/Brem0827/Tech-Stack)
[![All Contributors](https://img.shields.io/badge/all_contributors-2-orange.svg?style=flat-square)](#Tech-Stack)

[![Watch on GitHub](https://img.shields.io/github/watchers/Brem0827/Tech-Stack.svg?style=social)](https://github.com/Brem0827/Tech-Stack/watchers)
[![Star on GitHub](https://img.shields.io/github/stars/Brem0827/Tech-Stack.svg?style=social)](https://github.com/Brem0827/Tech-Stack/stargazers)
[![Fork on GitHub](https://img.shields.io/github/forks/Brem0827/Tech-Stack.svg?style=social)](https://github.com/Brem0827/Tech-Stack/network/members)

# 🏃TypeScript
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

💕 주차
---
1. 💭[2주차](#2주차)➡️
1. 💭[1주차](#1주차)➡️

---
# 2주차

🔋 2023.09.06

## 원시 타입

* 자바스크립트에서 주로 사용되는 원시 타입인 `string`, `number`, `boolean`은 타입스크립트에서 대응하는 타입이 있습니다.
* `string`은 "Hello World"와 같은 문자열 값을 나타냅니다.
* `number`는 42와 같은 숫자를 나타냅니다. 자바스크립트에는 정수에 대한 특별한 런타임 값이 없으므로 int나 float에 해당하는 값을 없으며 모든 것이 숫자입니다.
* `boolean`은 `true`, `false`두 값에 사용됩니다.
* 원시 타입의 이름을 지정할때 String, Number와 같이 대문자로 시작하면 안됩니다.

## 원시 타입
- 불변성
- 메모리 효율성
- 비교 시 값 자체를 비교 (Call by value)

## 래퍼 객체
- 가변성
- 객체로서 추가 메서드 및 프로퍼티를 가질 수 없음
- 비교 시 참조를 비교 (Call by reference)

## 배열
* 배열에 타입을 지정할 때는 그 배열을 구성하는 타입과 [] 표기를 사용합니다.

## any
* TypeScript의 any타입은 변수가 어떤 타입이든 될 수 있음을 나타냅니다. 일종의 프리패스권 또는 타입체크를 회피 하는 용도로 사용되다 보니 타입스크립트에 익숙하지 않은 개발자가 개발하는 과정에서 무분별하게 많이 쓰이게 되는 타입중 하나입니다.
* 이름 그대로 모든 것을 허용하는 타입입니다.
* 자바스크립트 프로젝트를 타입스크립트로 마이그레이션하는 과정이 아닌 한, 기본적으로 사용하지 않는 것을 권장

## any는 아래와 같은 상황에서 사용될 수 있습니다.
* 해당 라인이 문제가 없을것이라는 것을 확신 할수 있을 때
* 타입정보가 없거나 미흡한 외부 라이브러리 등을 사용할 때
* 실행시점에 타입이 결정되어서 타입을 미리 정할 수 없을 때

## noImplicitAny
* 기본적으로 타입스크립트에서 타입이 지정되어 있지 않은 변수들에 대해 `문맥상 타입을 추정할` 수 없다면 컴파일러에서는 `any`타입으로 가정합니다.

---
# 1주차

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