# 为什么要学习git?
## git-commit 规范
每一次在git上提交代码都需要填写提交说明，不然是不允许提交的。
Commit Message有它的规范，其分为三个部分，Header、Body和Footer。
### Header
Header是提交信息的标题，是必须填写的部分。
Header又分为type、scope和subject三部分,其中type和subject是必须的。
type: 用于说明提交的类型，常用的type有以下几种：
- feat: 新功能（feature）
- fix: 修补bug（fix）
- docs: 文档（documentation）
- style: 格式（不影响代码运行的变动）
- refactor: 重构（即不是新增功能，也不是修改bug的代码变动）
- test: 增加测试
- chore: 构建过程或辅助工具的变动
只用一个单词，我们就可以对本次改动有一个基本的认识。
scope用于描述本次commit的影响范围，而subject则是对本次commit的简短描述。
### Body与Footer
Body是对本次commit的详细描述，可以包含多行内容，主要用于解释为什么要进行本次提交，以及本次提交的具体内容。
Footer则是用于一些额外的信息，比如本次提交是否关闭了某个issue，或者是否有BREAKING CHANGE（破坏兼容性）等。
作者还介绍了一些工具，一个是Commitizen,它可以帮助我们规范化提交信息，还有一个是validate-commit-msg，它可以帮助我们验证提交信息是否符合规范。

## git flow
版本管理是协作开发中的关键问题。Git flow是一种分支管理模型，它定义了不同类型的分支及其用途，帮助团队更好地管理代码版本。
### 分支类型
Git flow定义了几种主要的分支类型，每种分支都有其特定的用途和生命周期：
- 主分支（master/main）：用于存放生产环境的代码，通常是稳定的版本。
- 开发分支（develop）：用于集成各个功能分支的代码，是开发过程中主要的工作分支。
- 功能分支（feature）：用于开发新功能，从develop分支创建，完成后合并回develop。
- 修复分支（hotfix）：用于修复生产环境中的紧急问题，从master分支创建，修复完成后合并回master和develop。
- 发布分支（release）：用于准备发布新版本，从develop分支创建，完成后合并回master和develop。
### 分支管理流程
1. 创建功能分支：当需要开发新功能时，从develop分支创建一个新的功能分支，命名通常为feature/功能名称。
2. 开发与提交：在功能分支上进行开发，完成后提交代码，并确保提交信息符合规范。
3. 合并功能分支：当功能开发完成后，将功能分支合并回develop分支，进行集成测试。

## 为什么要学习git？
如果只是从写代码的角度看，git连接着github，似乎只能当作一个快捷云盘，帮我们存储自己的项目，下载别人的仓库。然而在我看来，git更重要的作用是代码管理工具，每一次的git-commit都可以帮助我们快速了解本次提交的更新内容，这对于协作开发至关重要。git flow则提供了一个较为清晰的开发步骤，主分支用来发布项目、开发分支用来做新内容，具体的新功能在feature上做，做好了放回开发分支，release分支则预备发布新版本，如果发现严重bug，则要放到hotfix上。