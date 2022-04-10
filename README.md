
# svelte를 공부해봅니다. Let's begin to learn Svelte

### svelte Template으로 만들어졌습니다. 다음과 같이 만들 수 있습니다.

```bash
npx degit sveltejs/template [만들고자 하는 디렉토리명/working directory]
cd [만든 디렉토리명/working directory]
```

### [Node.js](https://nodejs.org)가 설치되어 있어야 합니다.
- Note that you will need to have [Node.js](https://nodejs.org) installed.


## 시작해 봅시다! Let's Get started!

### 프로젝트 실행에 필요한 파일들 설치
- Install the dependencies...

```bash
cd [프로젝트가 설치된 위치/working directory]
npm install
```

### [Rollup](https://rollupjs.org)으로 작동합니다.
- ...then start [Rollup](https://rollupjs.org):

```bash
npm run dev
```

### localhost:8080에서 실행됩니다. src 폴더 내의 소스코드를 수정하면 바로 적용됩니다. `package.json`파일 내의 환경설정으로 `--host 0.0.0.0`을 통해 host 주소를 변경하는 것이 가능합니다.
- Navigate to [localhost:8080](http://localhost:8080). You should see your app running. Edit a component file in `src`, save it, and reload the page to see your changes.

By default, the server will only respond to requests from localhost. To allow connections from other computers, edit the `sirv` commands in package.json to include the option `--host 0.0.0.0`.

## 배포 모드로 작동시키기 Building and running in production mode

### 애플리케이션을 빌드합니다.
- To create an optimised version of the app:

```bash
npm run build
```
### `npm run start`로 빌드하여 배포가 가능합니다
- You can run the newly built app with `npm run start`. This uses [sirv](https://github.com/lukeed/sirv), which is included in your package.json's `dependencies` so that the app will work when you deploy to platforms like [Heroku](https://heroku.com).


## SPA모드  Single-page app mode

### 애플리케이션을 구동하는 역할을 하는 `sirv`는 `public` 폴더내에 만들어진 파일을 확인하고 애플리케이션을 구동합니다.
- By default, sirv will only respond to requests that match files in `public`. This is to maximise compatibility with static fileservers, allowing you to deploy your app anywhere.

### 다양한 경로가 필요한 SPA인 경우에는 반드시 경로를 명시해주셔야 합니다.
- If you're building a single-page app (SPA) with multiple routes, sirv needs to be able to respond to requests for *any* path. You can make it so by editing the `"start"` command in package.json:

```js
"start": "sirv public --single"
```

## Typescript 사용이 가능합니다. Using TypeScript

### Typescript를 사용하려면 다음 명령어를 입력해주세요.
- This template comes with a script to set up a TypeScript development environment, you can run it immediately after cloning the template with:

```bash
node scripts/setupTypeScript.js
```

### 지우려면 다음과 같이 해주세요.
- Or remove the script via:

```bash
rm scripts/setupTypeScript.js
```

### Typescript를 사용할 떄 환경설정 수정은 `tsconfig.json`에서 수정해주세요.
If you want to use `baseUrl` or `path` aliases within your `tsconfig`, you need to set up `@rollup/plugin-alias` to tell Rollup to resolve the aliases. For more info, see [this StackOverflow question](https://stackoverflow.com/questions/63427935/setup-tsconfig-path-in-svelte).
