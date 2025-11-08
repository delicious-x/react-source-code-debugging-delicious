### React 源码调试

#### 源码下载

从github [React](https://github.com/facebook/react) 官网选择需要调试的版本 

```bash
git clone https://github.com/facebook/react.git react17 
```

#### 安装JDK 17

```js
https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html
```

#### 源码编译

```js
cd react17
// 安装依赖
yarn
// 编译
yarn build react,shared,scheduler,react-reconciler,react-dom --type=NODE
```

<img width="1456" height="1504" alt="Image" src="https://github.com/user-attachments/assets/b019dedc-ff7b-4b30-9e7b-e6a5b0e07d8b" />


#### 源码调试

+ 创建项目

```js
// 创建项目
npx create-react-app react-app
```
+ 创建链接

```js
// link react
cd build/node_modules/react
yarn link

// link react-dom
cd ../react-dom
yarn link
```

+ 链接到本地项目

```js
// 进入 react-app 项目目录后
yarn link react react-dom
// 启动项目
npm run start
```