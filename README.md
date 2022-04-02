# Sveltekit으로 Svelte 공부

해당 프로젝트는 다음의 링크를 통해 만들어졌습니다. [`create-svelte`](https://github.com/sveltejs/kit/tree/master/packages/create-svelte).

## Sveltekit으로 프로젝트 만들기

```bash
# 현재 작업중인 디렉토리에서 프로젝트 생성
npm init svelte@next

# my-app 디렉토리에서 프로젝트 생성
npm init svelte@next my-app
```

> Note: `@next` 는 임시 버전입니다. 현재 베타버전으로 계속 업데이트됩니다.

## Developing

프로젝트 생성후 반드시 `npm install` (or `pnpm install` or `yarn`)를 입력합니다.

개발용 서버를 아래와 같이 실행합니다.

```bash
npm run dev

# or start the server and open the app in a new browser tab
npm run dev -- --open
```

## Building

To create a production version of your app:

```bash
npm run build
```

`npm run preview` 로 빌드 결과물을 미리 볼 수 있습니다.

> [adapter](https://kit.svelte.dev/docs/adapters)로 배포 환경 설정이 가능합니다.
