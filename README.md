# component-library

## Getting Started

Install dependencies,

```bash
$ npm i
```

Start the dev server,

```bash
$ npm start
```

Build documentation,

```bash
$ npm run docs:build
```

Run test,

```bash
$ npm test
```

Build library via `father`,

```bash
$ npm run build
```

# 创建一个 button 组件

lerna create @keith/button packages/button --yes

在 tsconfig.json 文件中新加一个 paths "paths": { "@keith/button":["./packages/button/src/index.tsx"], }

修改 button 组件包中的 package.json { "name": "@keith/button", "version": "0.0.0", "keywords": [], "license": "MIT", "main": "lib/index.js", "module": "es/index.js", "types": "lib/index.d.ts", "files": [ "lib", "es", "dist" ], "peerDependencies": { "antd": "4.x", "react": ">=16.9.0", "react-dom": ">=16.9.0" }, "publishConfig": { "registry": "https://registry.npmjs.org" } } 在.fatherrc.ts 文件中，添加 button

const headPkgs: string[] = ['button']; // 添加 button
