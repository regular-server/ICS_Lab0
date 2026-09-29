# ICS Lab0 — Git 与 GitLab

本仓库为计算机系统基础课程 Lab0 的实验仓库，实验内容为学习 Git 的基本用法与分支管理，
并亲手制造、解决一次合并冲突。

## 实验产物

| 文件 | 说明 |
| --- | --- |
| `实验报告.md` | **实验报告**（任务 5 提交物），含文档问题解答、实验步骤、截图与建议 |
| `main.c` | 实验主程序，已完成 `TODO` 部分 |
| `Makefile` | 编译脚本 |
| `note.md` | 阅读 Commit Message 规范与 Git Flow 的学习笔记 |
| `graph/` | 实验过程截图 |
| `.github/workflows/classroom.yml` | 由 GitHub Classroom 提供的自动评分工作流 |

## 编译运行

```bash
make
./main
make clean
```

程序输出：

```text
Hello, world!
Git is powerful!
```

## 分支说明

- `main`：主分支，实验报告与最终结果提交于此；
- `feature`：实验用功能分支，修改 `main.c` 中的输出语句后合并回 `main`，
  合并时在 `main.c` 上产生了内容冲突并已解决。
