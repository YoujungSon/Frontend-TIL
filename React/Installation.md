React는 처음부터 점진적 채택을 위해 설계되었습니다. React는 필요한 만큼 적게 또는 많이 사용할 수 있습니다. React를 맛보고 싶든, HTML 페이지에 상호작용을 추가하든, 복잡한 앱을 만드는데 사용하든 이 섹션은 시작하는데 도움이 될 것입니다.

**React 공식문서는 코드 샌드박스와 같은 예제를 포함합니다.**

- HTML 페이지에서 React를 추가해서 사용할 수 있음.
- 이미 존재하는 페이지에 React 부분만 추가하여 사용할 수 있음
- full react app을 만들 수 있음 (stand alone project)
- React Framework를 사용해서 많은 설정을 쉽게 할 수도 있음

```jsx
function Greeting({ name }) {
  return <h1>Hello, {name}</h1>;
}

export default function App() {
  return <Greeting name='world' />;
}
```

## Start a New React Project

React 프로젝트를 시작하는 다양한 방법 소개
새 프로젝트를 시작하는 경우 편리한 개발환경을 위해서 툴체인이나 프레임워크를 사용하세요.
(이러한 도구는 node.js 설치가 필요합니다.)

> **You will learn**
>
> - 툴체인이 프레임워크와 어떻게 다른지
> - 최소 도구 체인으로 프로젝트를 시작하는 방법
> - 완전한 기능을 갖춘 프레임워크로 프로젝트를 시작하는 방법
> - 널리 사용되는 도구 체인 및 프레임워크의 내부 내용

## Choose your own adventure

React는 UI 코드를 component라는 조각으로 나누어 정리할 수 있게 해주는 라이브러리입니다.
**React는 라우팅(routing)이나 데이터 관리(data management)를 처리하지 않습니다.**

- HTML에 CDN으로 React 불러오기(production에서 추천하지 않음, Node.js setup도 필요 없음)
- 기존 프로젝트에 부분적인 적용
- 프레임워크 사용

```bash
npx create-react-app my-app

cd my-app

npm start
```

## Getting started with a minimal toolchain

만약 React를 배우고 있다면 우리는 create-react-app을 사용하길 추천합니다. 이 방법은 React에서 SPA를 만들기 위한 가장 유명한 방법입니다. 이는 React를 위해 만들어졌지만 라우팅이나 데이터 fetching에는 독단적이지 않습니다.

- node.js 설치
- yarn create react-app my-app
- cd my-app
- yarn start

> **CreateReactApp은 백엔드 논리 또는 데이터베이스를 처리하지 않습니다.**
> 모든 백엔드와 함께 사용할 수 있습니다. 프로젝트를 빌드할 때 정적 HTML, CSS 및 JS가 포함된 폴더를 얻을 수 있습니다. Create React App은 서버를 활용할 수 없기 때문에 최상의 성능을 제공하지 못합니다. 더 빠른 로딩 시간과 라우팅 및 서버 측 논리와 같은 기본 제공 기능이 필요한 경우, 대신 프레임워크를 사용하는 것이 좋습니다.

# **Popular alternatives**

- [Vite](https://vitejs.dev/guide/)
- [Parcel](https://parceljs.org/getting-started/webapp/)

## Building with a full-featured framework

프로덕션에 사용하는 프로젝트 같은 경우 Next.js를 사용하세요.

Next는 React로 구축된 정적 및 서버 렌더링 애플리케이션을 위한 널리 사용되는 경량 프레임워크입니다.

라우팅, 스타일 지정 및 서버 사이트 렌더링과 같은 기능이 사전 패키지되어 있어 프로젝트를 빠르게 시작하고 실행할 수 있습니다.

### Popular alternatives

- [Gatsby](https://www.gatsbyjs.org/)
- [Remix](https://remix.run/)
- [Razzle](https://razzlejs.org/)

## Custom toolchains

- **package manager**
  패키지 관리자를 사용하여 타사 패키지를 설치, 업데이트 및 관리할 수 있습니다. - npm yarn, pnpm
- **compiler**
  컴파일러를 사용하면 JSX와 같은 최신 언어 기능과 추가 구문을 컴파일하거나 브라우저용 주석을 입력할 수 있습니다. - [Babel](https://babeljs.io/), [TypeScript](https://www.typescriptlang.org/), [swc.](https://swc.rs/)
- **bundler**
  번들러를 사용하면 모듈식 코드를 작성하고 작은 패키지로 함께 번들하여 로드 시간을 최적화할 수 있습니다. - [webpack](https://webpack.js.org/),[Parcel](https://parceljs.org/),[esbuild](https://esbuild.github.io/),[swc](https://swc.rs/)
- **minifiers**
  minifiers는 코드를 더 압축하여 더 빨리 로드되도록 합니다 - [Terser](https://terser.org/), [swc.](https://swc.rs/)
- **server**
  서버는 components를 HTML로 렌더링할 수 있도록 서버 요청을 처리합니다. - [Express.](https://expressjs.com/)
- **linters**
  linters는 코드에 일반적인 실수가 있는지 확인합니다. - [ESLint](https://eslint.org/)
- **test runners**
  테스트 실행기를 사용하면 코드에 대해 테스트를 실행할 수 있습니다. - [Jest.](https://jestjs.io/)

> 만약 당신이 처음부터 당신만의 자바스크립트 툴체인을 설정하기를 원한다면, **Create React App** 기능을 다시 만드는 [이 가이드](https://medium.com/@JedaiSaboteur/creating-a-react-app-from-scratch-f3c693b84658)를 확인하세요.
> 프레임워크는 일반적으로 **라우팅 및 데이터 가져오기 솔루션**을 제공한다.
> 대규모 프로젝트에서는 **Nx 또는 Turborepo**와 같은 도구를 사용하여 single repository에서 여러 패키지를 관리할 수도 있습니다.

## \***\*Add React to a Website\*\***

React로 웹사이트 전체를 구축할 필요는 없습니다.
HTML에 React를 추가하면 설치가 필요하지 않고 몇 분이 소요되며 대화형 components 작성을 바로 시작할 수 있습니다.

> \***\*You will learn\*\***
>
> - HTML 페이지에 React를 1분 안에 추가하는 방법
> - JSX 구문은 무엇이며 빠르게 시도하는 방법
> - 프로덕션을 위한 JSX 프리프로세서 설정 방법

## \***\*Add React in one minute\*\***

리액트는 처음부터 점진적인 채택을 위해 설계되었습니다. 대부분의 웹 사이트는 React로 완전히 구축되지 않았으며, 그럴 필요도 없습니다. 이 안내서는 기존 HTML 페이지에 "상호작용의 스프린스"를 추가하는 방법을 보여줍니다.

당신의 웹사이트나 빈 HTML 파일로 이것을 시도해 보세요. 필요한 것은 인터넷 연결과 메모장 또는 VSode와 같은 텍스트 편집기입니다. (다음은 구문 강조 표시를 위해 편집기를 구성하는 방법입니다!)

### \***\*Step 1: Add a root HTML tag\*\***

먼저 편집할 HTML 페이지를 엽니다. 빈 <div> 태그를 추가하여 React로 표시할 지점을 표시합니다. 이 <div>에 고유한 ID 특성 값을 지정합니다. 예:

```html
<!-- ... existing HTML ... -->

<div id="like-button-root"></div>

<!-- ... existing HTML ... -->
```

리액트 트리가 시작되는 곳이기 때문에 "**루트**"라고 불립니다. 이와 같은 **루트 HTML 태그**는 <body> 태그 내부 어디에나 배치할 수 있습니다. React는 해당 내용을 React component로 대체하므로 **비워 두십시오.**

**한 페이지에 필요한 만큼의 루트 HTML 태그를 가질 수 있습니다.**

### \***\*Step 2: Add the script tags\*\***

HTML 페이지에서 닫기 </body> 태그 바로 앞에 다음 파일에 대한 세 개의 <script> 태그를 추가합니다:

- [react.development.js](https://unpkg.com/react@18.2.0/umd/react.development.js)를 사용하여 React component를 정의할 수 있습니다.
- [react-dom.development.js](https://unpkg.com/react-dom@18.2.0/umd/react-dom.development.js)를 사용하여 HTML 요소를 DOM으로 렌더링할 수 있습니다.
- like-button.js는 당신이 다음 단계에서 당신의 components를 작성하는 곳입니다!

HTML은 이제 다음과 같이 끝나야 합니다:

```html
<!-- end of the page -->
    <script src="https://unpkg.com/react@18/umd/react.development.js" crossorigin></script>
    <script src="https://unpkg.com/react-dom@18/umd/react-dom.development.js" crossorigin></script>
    <script src="like-button.js"></script>
  </body>
</html>
```

> **함정**
> 라이브 웹 사이트에 배포하기 전에 development.js를 production.min.js로 교체해야 합니다! React의 개발 빌드는 더 유용한 오류 메시지를 제공하지만 웹 사이트 속도를 많이 늦춥니다.

### \***\*Step 3: Create a React component\*\***

HTML 페이지 옆에 like-button.js라는 파일을 만들고 이 코드 조각을 추가한 다음 파일을 저장합니다. 이 코드는 LikeButton이라는 React component를 정의합니다.

```jsx
'use strict';

function LikeButton() {
  const [liked, setLiked] = React.useState(false);

  if (liked) {
    return 'You liked this!';
  }

  return React.createElement(
    'button',
    {
      onClick: () => setLiked(true),
    },
    'Like',
  );
}
```

### **Step 4: Add your React component to the page**

마지막으로 like-button.js의 하단에 세 줄을 추가합니다. 다음 코드 행은 첫 번째 단계에서 HTML에 추가한 <div>를 찾아 React 루트를 만든 다음 그 안에 "좋아요" button React component를 표시합니다:

```jsx
const rootNode = document.getElementById('like-button-root');
const root = ReactDOM.createRoot(rootNode);
root.render(React.createElement(LikeButton));
```

축하합니다! 방금 웹 사이트에 첫 번째 React component를 렌더링했습니다!

- [전체 소스 코드 예제 보기](https://gist.github.com/gaearon/0b535239e7f39c524f9c7dc77c44f09e)
- [전체 예제 다운로드(2KB 압축)](https://gist.github.com/gaearon/0b535239e7f39c524f9c7dc77c44f09e/archive/651935b26a48ac68b2de032d874526f2d0896848.zip)

### **You can reuse components!**

동일한 HTML 페이지의 여러 위치에 React component를 표시할 수 있습니다. 이 기능은 페이지의 React-powered 부분이 서로 다른 경우에 유용합니다. HTML에 여러 루트 태그를 넣은 다음 ReactDOM.createRoot()을 사용하여 각각의 내부에 React component를 렌더링하여 이 작업을 수행할 수 있습니다. 예:

1. index.html에서 컨테이너 요소 <divid="another-root"></div>를 추가합니다.
2. like-button.js에서 끝에 세 줄을 더 추가합니다:

```jsx
const anotherRootNode = document.getElementById('another-root');
const anotherRoot = ReactDOM.createRoot(anotherRootNode);
anotherRoot.render(React.createElement(LikeButton));
```

여러 곳에서 동일한 component를 렌더링해야 하는 경우 각 루트에 ID 대신 CSS 클래스를 할당한 다음 모두 찾을 수 있습니다. 다음은 세 개의 "좋아요" button을 표시하고 각 button에 데이터를 전달하는 예입니다.

### \***\*Step 5: Minify JavaScript for production\*\***

최소화되지 않은 JavaScript는 사용자의 페이지 로드 시간을 크게 늦출 수 있습니다. 웹 사이트를 프로덕션에 배포하기 전에 스크립트를 최소화하는 것이 좋습니다.

- 스크립트에 대한 최소화 단계가 없는 경우 [다음과 같은 방법](https://gist.github.com/gaearon/ee0201910608f15df3f8cd66aa83f98e)으로 스크립트를 설정할 수 있습니다.
- 애플리케이션 스크립트를 이미 최소화한 경우 배포된 HTML이 다음과 같이 product.min.js로 끝나는 React 버전을 로드하면 사이트가 운영 준비 상태가 됩니다:

```jsx
<script src="https://unpkg.com/react@18/umd/react.production.min.js" crossorigin></script>
<script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js" crossorigin></script>
```

## \***\*Try React with JSX\*\***

위의 예는 브라우저에서 기본적으로 지원되는 기능에 의존합니다. 이것이 like-button.js가 자바스크립트 함수 호출을 사용하여 React에 표시할 내용을 알려주는 이유이다:

```jsx
return React.createElement('button', { onClick: () => setLiked(true) }, 'Like');
```

그러나 리액트는 HTML과 같은 자바스크립트 구문인 JSX를 대신 사용할 수 있는 옵션도 제공한다:

```jsx
return <button onClick={() => setLiked(true)}>Like</button>;
```

이 두 코드 스니펫은 동일합니다. JSX는 자바스크립트에서 마크업을 설명하는 데 널리 쓰이는 문법이다. 많은 사람들이 UI 코드 작성에 익숙하고 도움이 된다고 생각한다.

당신은 이 [온라인 변환기](https://babeljs.io/en/repl#?babili=false&browsers=&build=&builtIns=false&spec=false&loose=false&code_lz=DwIwrgLhD2B2AEcDCAbAlgYwNYF4DeAFAJTw4B88EAFmgM4B0tAphAMoQCGETBe86WJgBMAXJQBOYJvAC-RGWQBQ8FfAAyaQYuAB6cFDhkgA&debug=false&forceAllTransforms=false&shippedProposals=false&circleciRepo=&evaluate=false&fileSize=false&timeTravel=false&sourceType=module&lineWrap=true&presets=es2015%2Creact%2Cstage-2&prettier=false&targets=&version=7.17)를 사용하여 HTML 마크업을 JSX로 변환하는 것을 즐길 수 있다.

### \***\*Try JSX\*\***

JSX를 시도하는 가장 빠른 방법은 페이지에 Babel 컴파일러를 <스크립트> 태그로 추가하는 것이다. like-button.js 앞에 놓고 like-button.js의 <script> 태그에 type="text/babel" 속성을 추가합니다:

```jsx
<script src="https://unpkg.com/react@18/umd/react.production.min.js" crossorigin></script>
  <script src="https://unpkg.com/react-dom@18/umd/react-dom.production.min.js" crossorigin></script>
  <script src="https://unpkg.com/@babel/standalone/babel.min.js"></script>
  <script src="like-button.js" type="text/babel"></script>
</body>
```

이제 like-button.js를 열고 바꿀 수 있습니다

```jsx
return React.createElement(
  'button',
  {
    onClick: () => setLiked(true),
  },
  'Like',
);
```

다음과 같은 JSX 코드를 사용합니다:

```jsx
return <button onClick={() => setLiked(true)}>Like</button>;
```

처음에는 JS를 마크업과 혼합하는 것이 약간 특이하게 느껴질 수 있지만, 그것은 당신에게 점점 더 도움이 될 것입니다! 소개는 JSX의 [Writing Markup](https://beta.reactjs.org/learn/writing-markup-with-jsx)을 확인하십시오. 다음은 다운로드하여 사용할 수 있는 [JSX가 포함된 HTML 파일의 예](https://raw.githubusercontent.com/reactjs/reactjs.org/main/static/html/single-file-example.html)입니다.

> \***\*Pitfall\*\***
> Babel <스크립트> 컴파일러는 간단한 데모를 배우고 만드는 데 좋다. 그러나 웹 사이트 속도가 느려져 프로덕션에 적합하지 않습니다. 앞으로 이동할 준비가 되었으면 Babel <script> 태그를 제거하고 이 단계에서 추가한 type="text/babel" 특성을 제거합니다. 대신 다음 섹션에서는 JSX 프리프로세서를 설정하여 모든 <스크립트> 태그를 JSX에서 JS로 변환합니다.

## \***\*Add JSX to a project\*\***

프로젝트에 JSX를 추가하는 데 번들러나 개발 서버와 같은 복잡한 도구가 필요하지 않습니다. JSX 프리프로세서를 추가하는 것은 CSS 프리프로세서를 추가하는 것과 비슷하다.

터미널의 프로젝트 폴더로 이동하여 다음 두 명령을 붙여넣습니다(Node.js가 설치되어 있는지 확인하십시오!):

1. `npm init -y`(실패할 경우 다음과 같은 수정 사항)
2. `npm install @babel/cli@7 babel-party-app@10`

JSX 프리프로세서를 설치하려면 npm만 필요합니다. 당신은 그것이 다른 어떤 것에도 필요하지 않을 것이다. React와 응용 프로그램 코드는 모두 변경 없이 <script> 태그로 유지될 수 있습니다.

축하합니다! 방금 프로젝트에 프로덕션 가능한 JSX 설정을 추가했습니다.

## \***\*Run the JSX Preprocessor\*\***

JSX가 포함된 파일을 저장할 때마다 변환이 다시 실행되도록 JSX 파일을 브라우저가 이해할 수 있는 새로운 일반 JavaScript 파일로 변환할 수 있습니다. 설정 방법은 다음과 같습니다:

1. src라는 폴더를 만듭니다.
2. 터미널에서 다음 명령을 실행합니다. `npx babel --watch src --out-dir. --presets babel-preset-react-app/prod` (끝날 때까지 기다리지 마십시오! 이 명령은 src 내부의 JSX에 대한 편집을 위해 자동 감시를 시작합니다.)
3. JSX-ified like-button.js([이렇게 보여야 합니다!](https://gist.githubusercontent.com/gaearon/be5ae0fbf563d6c5fe5c1563907b13d2/raw/4c0d0b8c7f4fcb341720424c28c72059f8174c62/like-button.js))를 새 src 폴더로 이동합니다.

watcher는 브라우저에 적합한 일반 자바스크립트 코드로 사전 처리된 like-button.js를 만들 것이다.

> \***\*Pitfall\*\***
> "바벨 패키지를 잘못 설치했습니다."라는 오류 메시지가 표시되면 이전 단계를 놓쳤을 수 있습니다. 동일한 폴더에서 수행한 다음 다시 시도하십시오.

방금 사용한 도구의 이름은 Babel이며 설명서에서 자세히 알아볼 수 있습니다. JSX 외에도 오래된 브라우저를 손상시킬 염려 없이 최신 JavaScript 구문 기능을 사용할 수 있습니다.

빌드 도구에 익숙해지고 더 많은 작업을 수행하기를 원하는 경우, 여[기에서 가장 인기 있고 접근하기 쉬운 도구 체인](https://beta.reactjs.org/learn/start-a-new-react-project)에 대해 설명합니다.

### \***\*React without JSX\*\***

원래 JSX는 리액트를 사용한 writing components가 HTML을 작성하는 것처럼 친숙하게 느껴지도록 하기 위해 도입되었다. 그러나 JSX를 사용하고 싶지 않거나 사용할 수 없는 경우가 있을 수 있습니다. 두 가지 옵션이 있습니다:

- 컴파일러 대신 자바스크립트 템플릿 문자열을 사용하는 htm과 같은 JSX 대안을 사용한다.
- 아래에 설명된 특수 구조를 가진 React.createElement()를 사용합니다.

JSX를 사용하면 다음과 같은 component를 작성할 수 있습니다:

```jsx
function Hello(props) {
  return <div>Hello {props.toWhat}</div>;
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(<Hello toWhat='World' />);
```

React.createElement()를 사용하면 다음과 같이 쓸 수 있습니다:

```jsx
function Hello(props) {
  return React.createElement('div', null, 'Hello ', props.toWhat);
}

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(React.createElement(Hello, { toWhat: 'World' }, null));
```

다음과 같은 몇 가지 인수를 사용할 수 있습니다: React.createElement(component, props, ...children).

작동 방식은 다음과 같습니다:

1. HTML 요소 또는 함수 component를 나타내는 문자열이 될 수 있는 component
2. [전달할 props](https://beta.reactjs.org/learn/passing-props-to-a-component)의 객체
3. 나머지는 텍스트 문자열 또는 기타 요소와 같은 component의 하위 항목입니다

React.createElement()를 입력하는 것이 지겹다면, 한 가지 일반적인 패턴은 단축키를 할당하는 것입니다:

```jsx
const e = React.createElement;

const root = ReactDOM.createRoot(document.getElementById('root'));
root.render(e('div', null, 'Hello World'));
```

그렇다면 이 스타일을 선호한다면 JSX만큼 편리할 수 있다.

# \***\*Editor Setup\*\***

적절하게 구성된 편집기는 코드를 읽기 더 명확하고 쓰기 더 빠르게 만들 수 있습니다. 그것은 심지어 여러분이 bugs를 잡는 것을 도와줄 수 있습니다! 편집기를 처음 설정하거나 현재 편집기를 조정하려는 경우 몇 가지 권장 사항이 있습니다.

> **You will learn**
>
> - 가장 인기 있는 editors는 무엇입니까
> - 코드를 자동으로 포맷하는 방법

## \***\*Your editor\*\***

VS Code는 오늘날 사용되는 가장 인기 있는 편집기 중 하나입니다. 그것은 확장의 큰 시장을 가지고 있고 깃허브와 같은 인기 있는 서비스와 잘 통합된다. 아래 나열된 대부분의 기능은 VS Code에 확장 기능으로 추가할 수 있으므로 구성 가능성이 높습니다!

리액트 커뮤니티에서 사용되는 다른 인기 있는 텍스트 편집기는 다음과 같다:

- 웹스톰은 자바스크립트를 위해 특별히 설계된 통합 개발 환경이다.
- Sublime Text는 JSX와 TypeScript, 구문 강조 및 자동 완성 기능을 지원합니다.
- Vim은 모든 종류의 텍스트를 만들고 변경하는 것을 매우 효율적으로 만들기 위해 만들어진 매우 구성 가능한 텍스트 편집기입니다. 대부분의 유닉스 시스템과 애플 OS X에서 vi로 포함되어 있다.

## \***\*Recommended text editor features\*\***

일부 편집기에는 이러한 기능이 기본 제공되지만 다른 편집기에는 확장 기능을 추가해야 할 수도 있습니다. 선택한 편집자가 어떤 지원을 제공하는지 확인하십시오!

## \***\*Linting\*\***

Code linters는 사용자가 작성할 때 코드의 문제를 찾아 조기에 해결하는 데 도움이 됩니다. [ESLint](https://eslint.org/)는 자바스크립트를 위한 인기 있는 오픈 소스 린터이다.

- [React에 대한 권장 구성으로 ESLint를 설치합니다](https://www.npmjs.com/package/eslint-config-react-app)([Node](https://nodejs.org/en/download/current/)가 설치되어 있는지 확인하십시오!)
- [VSCode의 ESLint를 공식 extension과 통합](https://marketplace.visualstudio.com/items?itemName=dbaeumer.vscode-eslint)

프로젝트에 대해 모든 [eslint-plugin-react-hook](https://www.npmjs.com/package/eslint-plugin-react-hooks) 규칙을 사용하도록 설정했는지 확인하십시오. 그들은 필수적이고 가장 심각한 벌레를 일찍 잡습니다. 권장되는 [eslint-config-react-app](https://www.npmjs.com/package/eslint-config-react-app) 사전 설정에는 이미 이러한 기능이 포함되어 있습니다.

## \***\*Formatting\*\***

다른 contributor와 코드를 공유할 때 가장 하고 싶지 않은 것은 [tabs vs spaces](https://www.google.com/search?q=tabs+vs+spaces)에 대한 토론입니다! 다행히 프리티어는 미리 설정된 구성 가능한 규칙에 따라 코드를 다시 포맷하여 코드를 정리합니다. [Prettier](https://prettier.io/) 를 실행하면 모든 탭이 공백으로 변환되고 들여쓰기, 따옴표 등도 모두 구성에 맞게 변경됩니다. 이상적인 설정에서는 파일을 저장할 때 프리티어가 실행되어 빠르게 편집할 수 있습니다.

다음 단계에 따라 VSCode에 Pretty 확장을 설치할 수 있습니다:

1. Launch VS Code
2. 빠른 열기 사용(Ctrl/Cmd+P 누름)
3. `ext installesbenp.prettier-vscode` 붙여넣기
4. Enter 키를 누릅니다

## \***\*Formatting on save\*\***

저장할 때마다 코드를 포맷하는 것이 이상적입니다. VS 코드에 이에 대한 설정이 있습니다!

1. VS 코드에서 `Ctrl/CMD + SHIFT + P`를 누릅니다.
2. “settings”을 입력합니다.
3. Enter를 친다.
4. 검색란에 “format on save”을 입력합니다.
5. 저장 시 “format on save” 이 선택되어 있는지 확인하십시오!

ESLint 사전 설정에 형식 지정 규칙이 있는 경우 Pretty와 충돌할 수 있습니다. ESLint가 논리적 오류를 탐지하는 데만 사용되도록 eslint-config-prettier를 사용하여 ESLint 사전 설정의 모든 형식 지정 규칙을 비활성화하는 것이 좋습니다. 풀 요청이 병합되기 전에 파일 형식을 강제로 지정하려면 freelery --check를 사용하여 연속 통합을 확인하십시오.

# \***\*React Developer Tools\*\***

React Developer Tools를 사용하여 React component를 검사하고, 특성 및 상태를 편집하고, 성능 문제를 식별할 수 있습니다.

> **You will learn**
>
> - React Developer Tools 설치 방법

## \***\*Browser extension\*\***

React로 빌드된 웹 사이트를 디버깅하는 가장 쉬운 방법은 React Developer Tools 브라우저 확장을 설치하는 것입니다. 다음과 같은 유명한 브라우저에서 사용할 수 있다:

- [Chrome용 설치](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en)
- [Firefox용 설치](https://addons.mozilla.org/en-US/firefox/addon/react-devtools/)
- [Edge용 설치](https://microsoftedge.microsoft.com/addons/detail/react-developer-tools/gpphkfbcpidddadnkolkpfckpihlkkil)

이제 React로 작성된 웹 사이트를 방문하면 Components(구성요소) 및 Profiler(프로파일러) 패널이 표시됩니다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/d8a9c505-63f6-48b9-9a73-23cccb0f58db/Untitled.png)

## \***\*Safari and other browsers\*\***

다른 브라우저(예: Safari)의 경우 react-devtools npm 패키지를 설치합니다:

```jsx
# Yarn
yarn global add react-devtools

# Npm
npm install -g react-devtools
```

그런 다음 터미널에서 개발자 도구를 엽니다:

```jsx
react - devtools;
```

그런 다음 웹 사이트의 <head> 시작 부분에 다음과 같은 <script> 태그를 추가하여 웹 사이트를 연결합니다:

```html
<html>
  <head>
    <script src="http://localhost:8097"></script>
  </head>
</html>
```

개발자 도구에서 보려면 지금 브라우저에서 웹 사이트를 다시 로드하십시오.

## \***\*Mobile (React Native)\*\***

React Developer Tools를 사용하여 React Native로 빌드된 앱을 검사할 수도 있습니다.

React Developer Tools를 사용하는 가장 쉬운 방법은 전역에 설치하는 것입니다:

```bash
# Yarn
yarn global add react-devtools

# Npm
npm install -g react-devtools
```

그런 다음 터미널에서 개발자 도구를 엽니다.

```bash
react-devtools
```

실행 중인 로컬 React Native 앱에 연결해야 합니다.

개발자 도구가 몇 초 후에 연결되지 않으면 앱을 다시 로드해 보십시오.
