# AGENTS.md

「从数据到智能」课程结课实践项目。Python 3.12，用 uv 管理依赖，Ruff 负责 lint 与格式化，文档位于 `docs/`（VitePress）。

## Git 提交规范

遵循 [Conventional Commits](https://www.conventionalcommits.org/zh-hans/)，格式：

```text
<type>(<scope>): <主题>

<正文>

<页脚>
```

**规则：**

- `type`：英文小写。常用 `feat` / `fix` / `docs` / `style` / `refactor` / `perf` / `test` / `build` / `ci` / `chore` / `revert`
- `scope`：英文小写，可选，表示改动范围，如 `data`、`model`、`docs`、`ci`
- 主题与正文：**中文**，简洁明确；主题不超过 50 字，结尾不加句号；主题与正文之间空一行
- 正文：用 Markdown 列表逐条说明改动点与原因，**至少 2 条**，每条一行保持简洁
- 页脚：关联 issue 用英文关键词，如 `Closes #123`、`Refs #45`；破坏性变更写 `BREAKING CHANGE: ...`

**写法（二选一，保证提交信息显示为分段落、带列表的结构）：**

```bash
# 1. 多个 -m，每个 -m 是一个段落
git commit -m "feat(data): 添加链家二手房数据爬取脚本" -m "- 支持按城市分区批量抓取房源列表页
- 增加请求间隔与重试机制，避免触发反爬

Closes #12"

# 2. heredoc 写入完整 Markdown 格式
git commit -F - <<'EOF'
feat(data): 添加链家二手房数据爬取脚本

- 支持按城市分区批量抓取房源列表页
- 增加请求间隔与重试机制，避免触发反爬

Closes #12
EOF
```

**示例：**

```text
fix(model): 修复特征分箱后评估指标异常的问题

- 分箱边界含 NaN 导致测试集编码越界，统一用 -1 填充
- 补充分箱逻辑的单测

Refs #34
```

保持简洁：正文只写"为什么"和必要的细节，每条一句话说清。
