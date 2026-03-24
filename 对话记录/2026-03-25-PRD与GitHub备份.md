# 2026-03-25 PRD 与 GitHub 备份备忘

## 用户操作

- 要求：**备份到 GitHub**，并新增 **完整介绍类 PRD 文档** 一并入库。

## 本次新增/更新（yiyaowang）

| 路径 | 说明 |
|------|------|
| `智能组货/README.md` | 智能组货文档索引 |
| `智能组货/PRD-AI智能组货MVP.md` | **PRD 级**产品说明：背景、目标、功能、数据、非功能、验收、路线图 |
| 本文件 | 备份备忘 |

## 代码侧（zhinengzuhuo / zhinengzuhuo-backup）

- 与 PRD 对应的实现位于独立代码仓库；本次可一并提交：**`app/*.py`、`admin.html`、`.gitignore`（忽略 `app_runtime.db` 等）、`DEPLOY.md`、`DEPLOY_ALIYUN.md`、`API_EXAMPLES.md` 等**。

## 推送命令（本机执行）

```bash
# 文档仓
cd ~/yiyaowang
git add 智能组货/ 对话记录/
git status
git commit -m "docs: 智能组货 PRD + 备份备忘"
git push origin main

# 代码仓（在备份目录下）
cd ~/zhinengzuhuo-backup
git add app/ README.md DEPLOY.md DEPLOY_ALIYUN.md API_EXAMPLES.md .gitignore
git commit -m "feat: 智能组货 MVP 迭代（组货、话术、套餐名、导出、部署文档）"
git push origin main
```

若 `yiyaowang` 下尚有未提交的 `README.md`、`组件化/` 等改动，请用 `git status` 决定 **是否一并提交**。
