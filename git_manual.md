# How to use git 

## 使用SSH同步GitHub

如果**本地没有仓库**，你可以直接从 GitHub 上**克隆（clone）**一个仓库到本地，这样本地就有了仓库。下面是详细步骤：

---

## 1. 本地没有仓库，如何从 GitHub 下载？

### 步骤一：克隆仓库

1. **在 GitHub 上找到你要下载的仓库**，比如 `https://github.com/用户名/仓库名`。
2. **点击绿色的 `Code` 按钮**，复制仓库的 HTTPS 地址（如 `https://github.com/用户名/仓库名.git`）。
3. **打开命令行（终端）**，输入：

   ```bash
   git clone https://github.com/用户名/仓库名.git
   ```

4. **克隆完成后，进入项目文件夹**：

   ```bash
   cd 仓库名
   ```

现在你本地就有了这个仓库的完整副本。

---

## 2. 本地修改、同步到远程

1. **用编辑器修改代码**。
2. **保存后，在命令行输入：**

   ```bash
   git add .
   git commit -m "你的修改说明"
   git pull origin main   # 推送前建议先拉取最新代码
   git push origin main
   ```

   > 注意：`main` 可能是 `master`，具体看你仓库的主分支名。

---

## 3. 如果你想新建一个本地仓库并推送到 GitHub

如果你**本地有代码，但还没有仓库，也没有远程仓库**，可以这样操作：

1. **在本地项目文件夹下初始化仓库：**

   ```bash
   git init
   ```

2. **添加所有文件并提交：**

   ```bash
   git add .
   git commit -m "首次提交"
   ```

3. **在 GitHub 上新建一个空仓库**，不要勾选初始化 README。
4. **将远程仓库地址添加到本地：**

   ```bash
   git remote add origin https://github.com/用户名/仓库名.git
   ```

5. **推送到远程仓库：**

   ```bash
   git push -u origin main
   ```

---

## 总结

- **本地没有仓库，直接 `git clone` 远程仓库即可。**
- **本地有代码但没仓库，先 `git init`，再关联远程仓库并推送。**

