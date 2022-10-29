```json
{
  "name": "vue3-image-view",
  "private": false,
  "version": "0.1.2",
  "type": "module",
  "files": [
    "dist"
  ],
  "main": "./dist/vue3-image-view.umd.cjs",
  "module": "./dist/vue3-image-view.js",
  "types": "./dist/main.d.ts",
  "exports": {
    ".": {
      "import": "./dist/vue3-image-view.js",
      "require": "./dist/vue3-image-view.umd.js"
    },
    "./dist/style.css": "./dist/style.css"
  },
  "author": "o-h-y-o <khr157929@gmail.com> (https://github.com/O-h-y-o/vue3-image-view)",
  "license": "MIT",
  "description": "vue3-image-view",
  "repository": {
    "type": "git",
    "url": "git+https://github.com/O-h-y-o/vue3-image-view.git"
  },
  "bugs": {
    "url": "https://github.com/O-h-y-o/vue3-image-view/issues"
  },
  "homepage": "https://vue3-image-view-docs.netlify.app",
  "keywords": [
    "vue3-image-view",
    "vue3",
    "image-view",
    "image-viewer"
  ],
  "scripts": {
    "dev": "vite",
    "build": "vite build && vue-tsc --emitDeclarationOnly",
    "preview": "vite preview"
  },
  "devDependencies": {
    "@types/node": "^18.7.18",
    "@vitejs/plugin-vue": "^3.1.0",
    "path": "^0.12.7",
    "sass": "^1.55.0",
    "typescript": "^4.6.4",
    "vite": "^3.1.0",
    "vue-tsc": "^0.40.4",
  }
}
```

대충 이런식으로 해준다. 의존성 모듈과 개발의존성 모듈을 잘 구별해 놓자.

`--emitDeclarationOnly` 는 .d.ts 파일을 만들어서 운영하겠다는 명령어다.
