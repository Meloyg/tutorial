# Github

---

### **GitHub 基础 CLI 教学**

本教程涵盖 GitHub 的基本命令行操作，帮助初学者掌握 Git 的基本概念。

---

## **1. 安装 Git**

在终端（Mac/Linux）或命令提示符（Windows）中运行：

```sh
git --version
```

如果没有安装 Git，可以从 [Git 官网](https://git-scm.com/downloads) 下载并安装。

---

## **2. 配置 Git**

首次使用 Git 需要配置用户名和邮箱：

```sh
git config --global user.name "你的用户名"
git config --global user.email "你的邮箱"
```

查看配置：

```sh
git config --list
```

---

## **3. 创建本地仓库**

新建一个项目文件夹，并初始化 Git：

```sh
mkdir my-github-project
cd my-github-project
git init
```

> 这会创建一个 Git 仓库（.git 目录）。

---

## **4. 连接到 GitHub**

先去 [GitHub 官网](https://github.com) 创建一个新的仓库（Repository）。
然后，在终端中将本地仓库连接到 GitHub：

```sh
git remote add origin https://github.com/你的用户名/你的仓库名.git
```

查看远程仓库：

```sh
git remote -v
```

---

## **5. 提交代码到 GitHub**

创建一个文件并提交：

```sh
echo "Hello GitHub!" > README.md
git add README.md
git commit -m "第一次提交"
git push -u origin main
```

> 第一次 push 可能需要使用 `git branch -M main` 设定默认分支。

---

## **6. 从 GitHub 克隆仓库**

```sh
git clone https://github.com/你的用户名/你的仓库名.git
```

---

## **7. 创建分支**

```sh
git branch new-feature
git checkout new-feature
```

或者：

```sh
git checkout -b new-feature
```

提交更改：

```sh
git add .
git commit -m "添加新功能"
git push origin new-feature
```

---

## **8. 进行 Pull Request（PR）**

在 GitHub 上，打开仓库，找到 `Pull requests` 选项，创建 PR 以合并 `new-feature` 分支。

---

## **9. Fork 和 Clone 其他人的仓库**

**Fork** 一个项目：

1. 在 GitHub 上找到想 Fork 的仓库，点击 `Fork` 按钮。

**Clone** Fork 后的仓库：

```sh
git clone https://github.com/你的用户名/别人仓库名.git
```

---

## **10. 解决冲突**

当多人修改同一文件，可能会出现冲突：

```sh
git pull origin main
git status
```

手动解决冲突后，提交更改：

```sh
git add .
git commit -m "解决冲突"
git push origin main
```

---

### **🎯 小游戏**

1. Fork 一个仓库并克隆到本地。
2. 在 `README.md` 里添加一句话。
3. 提交并 Push 代码。
4. 发起 Pull Request！

这样，你已经掌握了 GitHub 的基础 CLI 操作！ 🚀
