### 1. 프로젝트 생성

#### create-react-app 설치

```bash
yarn global add create-react-app
```

#### 프로젝트 생성

```bash
create-react-app project-name
```

> 프로젝트 이름에 대문자는 사용할 수 없다.

#### 폴더구조

- 생성한 프로젝트는 아래와 같은 폴더 구조를 가지고 있고, 딱 필수로 필요한 것들만을 포함하고 있다.

![Alt 폴더구조](./img/create-react-app1.png)

#### Dependency

```json
  "dependencies": {
    "react": "^16.8.6",
    "react-dom": "^16.8.6",
    "react-scripts": "3.0.1"
  }
```

### 2. Prettier 연동

#### Prettier?

- 자동으로 코드 스타일을 관리해주는 도구
- 에디터와 연동해서 사용 할 수 있다.

#### 적용

1. 루트 디렉터리에 .prettierrc 파일 생성

```json
{
  "trailingComma": "all",
  "tabWidth": 2,
  "semi": true,
  "singleQuote": true
}
```

2. Prettier 익스텐션 설치

### 3. ESLint

#### ESLint?

- ESLint 는 자바스크립트의 문법을 확인해주는 도구
- CRA로 만든 프로젝트에는 기본적으로 적용된다.
- 대표 규칙(여러 Lint 규칙들을 묶어서 라이브러리로 제공)
  - eslint-config-airbnb
  - eslint-config-google
  - eslint-config-standard

#### airbnb 설치

```bash
npm install eslint-config-airbnb
```

#### 설정

```json
"eslintConfig": {
    "extends": [
      "react-app",
      "airbnb"
    ]
},
```

#### Prettier 연동

- Prettier에서 관리하는 스타일이 ESLint에서 비활성화 되도록한다.

```bash
npm install eslint-config-prettier
```

```json
 "eslintConfig": {
    "extends": [
      "react-app",
      "airbnb",
      "prettier"
    ]
  },
```

### 3. 실행

```bash
yarn start
```
