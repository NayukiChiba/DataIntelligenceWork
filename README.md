# DataIntelligenceWork

「从数据到智能」课程结课实践项目。

## 结课要求

**任务**：完成一个完整的"从数据到智能"实践项目。

**项目流程**：

> 数据获取与理解 → 数据质量分析 → 数据处理与样本构造 → 数据分析 → 基线方法（可选）→ 模型设计、训练或调用 → 结果与评价 → 对比实验（可选）→ 错误案例分析 → 从数据到智能过程分析

**项目汇报**：

- 每名学生以项目汇报的形式制作 PPT 进行介绍，能够解释项目的数据来源、数据处理、模型选择或设计、实验结果和失败分析（5 分钟左右）。
- 可采用录屏软件或腾讯会议，自行讲解 PPT，录制成视频文件（压缩）。

**最终提交**：一个文件夹的压缩包，包含：

```text
2026XXXX学号-姓名/
├── data/                    # 数据文件夹（如直接调用在线开源数据集或数据太大，提供数据集链接）
├── 完整代码/                # 代码文件夹
├── 实验报告2026XXXX.docx
├── 介绍PPT2026XXXX.pptx
└── 演讲录屏2026XXXX.mp4
```

> [!WARNING]
> 只提交**一个 zip 压缩包**文件，文件名为 `2026XXXXXX-张三.zip`（学号-姓名），不要搞错了！！

**提交方式**：暂定为百度网盘收集。由于百度网盘收集有效期为 30 天，收集链接将在课程结束后发布，**截止日期：12 月 31 日**。

## 开发环境

项目限定使用 Python 3.12，`.python-version`、Ruff 和 pre-commit 配置与之保持一致。

## 文档

文档源码位于 `docs/`，使用基于 Vite 的 VitePress 构建。
文档的 npm 配置、锁文件和依赖均位于 `docs/`。
安装 Node.js 22 或更高版本后，在仓库根目录执行：

```bash
cd docs
npm ci
npm run docs:dev
```

在 `docs/` 目录构建检查：`npm run docs:build`，构建后预览：`npm run docs:preview`。

更新 `main` 分支的文档或相关配置会自动发布到
[GitHub Pages](https://nayukichiba.github.io/DataIntelligenceWork/)；
Pull Request 会检查文档构建，也可以在 Actions 页面手动运行"发布文档" workflow。
