# Git 命名规范说明

本文档用于统一项目中的分支命名和提交信息命名，方便协作、版本管理和问题排查。

## 1. 分支命名规范

分支命名通常采用以下格式：

```bash
<type>/<short-description>
```

其中：
- type：分支类型
- short-description：简短的功能或修复描述

### 常见分支类型

- feat：新增功能
- fix：修复问题
- docs：文档更新
- chore：日常维护、配置、依赖、脚本等
- refactor：代码重构
- style：样式调整
- test：测试相关

### 分支命名示例

```bash
feat/add-login-page
fix/login-button-error
docs/git-naming-guide
chore/update-project-config
refactor/user-service
style/homepage-ui
```

### 中文说明

- 如果任务是“新增功能”，用 `feat/`
- 如果任务是“修复 bug”，用 `fix/`
- 如果任务是“整理文档”，用 `docs/`
- 如果任务是“项目配置或工具相关”，用 `chore/`
- 如果任务是“代码重构”，用 `refactor/`

### 命名建议

- 尽量使用小写字母
- 单词之间用 `-` 连接
- 描述尽量简短、清晰、可读
- 不要使用中文，避免编码和命令兼容性问题

---

## 2. 提交信息命名规范

提交信息通常采用以下格式：

```bash
<type>: <summary>
```

例如：

```bash
feat: add login page
fix: resolve form validation bug
docs: add git naming guide
chore: update project config
refactor: simplify user model
style: improve homepage layout
```

### 常见提交类型

- feat：新增功能
- fix：修复 bug
- docs：文档更新
- chore：例行维护
- refactor：重构
- style：样式调整
- test：测试相关

### 提交说明原则

- 提交信息必须简洁
- 必须说明这次改动的核心内容
- 尽量保持一个提交只做一个事情
- 不建议写成模糊描述，例如：`update`、`fix some bug`

---

## 3. Git 分支和提交的关系

- 分支用来管理任务
- 提交用来记录具体改动
- 一个功能任务通常会在一个功能分支上完成
- 完成后再合并到主分支

一个典型流程是：

```bash
git checkout -b feat/add-login-page
git add .
git commit -m "feat: add login page"
git checkout main
git merge feat/add-login-page
```

---

## 4. 实际项目使用建议

在这个项目中，我们建议统一采用下面几种最常见的前缀：

```bash
feat/
fix/
docs/
chore/
```

这四类最容易理解，也最适合团队协作。

> 说明：常见写法是 `feat`，不是 `fit`；`chore` 是常用前缀，代表例行维护和环境整理。

---

## 5. 总结

项目中统一命名规范的意义是：

- 提高可读性
- 方便团队协作
- 便于快速定位问题
- 让 Git 历史更清晰

保持命名规范化，可以让以后查看提交记录和分支管理变得非常轻松。
