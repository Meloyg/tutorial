# NextJS

---

## **Next.js 基础 CLI 教学**

---

## **1. 安装 Node.js**

Next.js 依赖于 Node.js，先检查是否已安装：

```sh
node -v
```

如果没有安装，可以从 [Node.js 官网](https://nodejs.org) 下载并安装。

---

## **2. 创建 Next.js 项目**

在终端运行：

```sh
npx create-next-app@latest my-app
```

如果没有 `npx`，可以使用：

```sh
npm install -g create-next-app
create-next-app my-app
```

或者使用 `yarn`：

```sh
yarn create next-app my-app
```

---

## **3. 进入项目并运行**

```sh
cd my-app
npm run dev
```

> 打开浏览器，访问 [http://localhost:3000](http://localhost:3000)，就能看到 Next.js 默认页面。

---

## **4. 修改首页**

打开 `pages/index.js`，找到：

```jsx
<h1>Welcome to Next.js!</h1>
```

修改为：

```jsx
<h1>你好，世界！</h1>
```

保存后，浏览器会自动更新页面。

---

## **5. 添加样式**

修改 `styles/globals.css`，增加：

```css
body {
  background-color: lightblue;
  color: darkblue;
  text-align: center;
  font-family: Arial, sans-serif;
}
```

刷新网页，观察变化！

---

## **6. 加入图片**

在 `public` 目录中放入一张图片，比如 `hello.png`，然后修改 `pages/index.js`：

```jsx
import Image from "next/image";

export default function Home() {
  return (
    <div>
      <h1>你好，世界！</h1>
      <Image src="/hello.png" alt="Hello" width={300} height={200} />
    </div>
  );
}
```

---

## **7. 添加新页面**

创建 `pages/about.js`，并写入：

```jsx
export default function About() {
  return <h1>这是一个关于页面</h1>;
}
```

然后在 `pages/index.js` 里加个链接：

```jsx
import Link from "next/link";

export default function Home() {
  return (
    <div>
      <h1>你好，世界！</h1>
      <Link href="/about">关于我们</Link>
    </div>
  );
}
```

点击链接，即可跳转到新页面。

---

## **🎯 小游戏**

1. 修改 `index.js`，让页面展示你的名字。
2. 改变背景颜色，让网站更好看！
3. 添加一个新页面，介绍你的兴趣爱好。
4. 分享你的网页，让大家来看看！

这样，你已经学会了 Next.js 的基础操作！ 🚀
