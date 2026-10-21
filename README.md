# 学术裁缝 · Academic Tailor

一个从真实论文协作中提炼的 Codex 技能：把文献、代码、数据和实验记录组织成可追溯的论文证据，再完成写作、学术英译、科研图表、Word/WPS 排版和投稿核查。

**Evidence-grounded assistance for applied machine-learning papers, from research materials to a submission-ready manuscript.** Instructions are primarily in Chinese; Chinese and English manuscript work are supported.

## 适合什么任务

- 找公开数据集和相关论文，核对引用是否真实且支持正文。
- 核对基准与消融，区分训练、验证、测试及不同统计口径。
- 根据实际代码写方法，根据实验写结果、引言、摘要和结论。
- 中文稿转学术英文，保持术语、数值、公式和论证边界。
- 绘制结构图、混淆矩阵和训练曲线，按需生成可编辑 PPT。
- 处理拥挤表格、Word/WPS 兼容、原生公式与 MathType 对象。
- 投稿前检查图表引用、编号、文献、数值与全文表述的一致性。

它不预设某个模型、数据集、目标分数、随机种子或期刊，也不保证录用。研究的有效性取决于实际材料和验证。

## 安装

将本仓库中的 **`skills/academic-tailor` 整个文件夹**复制到 Codex 的技能目录：

- 默认位置：`~/.codex/skills/academic-tailor`
- 自定义了 `CODEX_HOME` 时：放入该目录下的 `skills/academic-tailor`

最终应能找到 `skills/academic-tailor/SKILL.md`，注意不要多套一层仓库文件夹。刷新技能列表或重新打开会话后使用。

这是供支持 `SKILL.md` 的代理读取的指令包，没有后台服务，也不自带文献数据库、GPU 或文档编辑程序。除技能入口外，所用工具由运行环境提供。

## 使用示例

```text
使用 $academic-tailor，检查我的最新版论文和结果目录。
先核对表格、混淆矩阵、摘要和结论的数据是否一致，
给出具体位置和可执行的修正，不使用旧版本数字。
```

```text
使用 $academic-tailor，根据数据说明、实际训练代码和结果写数据准备与增强。
区分原始图像、分类实例、在线增强与测试时增强；缺失信息标记待补充。
```

```text
使用 $academic-tailor，把这个中文方法章节改成自然的学术英文。
保留公式、引用和技术含义，并单独列出发现的事实冲突。
```

```text
使用 $academic-tailor，重新组织消融小节，让表格更清楚。
先检查每组实际配置和统计方式，再调整表头、表注与结果描述。
```

## 文件组织

```text
skills/academic-tailor/
  SKILL.md
  agents/openai.yaml
  references/
    literature-and-data.md
    experiments.md
    writing-and-translation.md
    figures.md
    documents-and-equations.md
    submission.md
    delivery-record.md
docs/
  design-notes.md
  evaluation-cases.md
```

主技能按任务加载专题，避免每次处理一个段落就读取全部流程。Zotero、MathType、Office、绘图与 GPU 工具均按需使用；缺少某项能力时必须说明可完成的范围。

## 来源与隐私

本技能根据一个应用型机器视觉论文项目中已检索的聊天片段和项目规范整理。提炼了反复出现的工作方法，也吸收了历史错误的修正，**没有逐字发布聊天记录**。长会话采用相关片段归纳，不宣称完整审计所有历史消息。

仓库不含论文正文、原始结果、私有文献库、数据集、作者信息、聊天标识、账号或本机路径。这里的通用指南不代表原始论文或数据的再分发授权。历史材料的具体模型和数字没有转化为默认参数。

## 验证与维护

发布前检查技能格式、文件链接、占位脚手架、包内文件和隐私信息。行为评估用例见 [evaluation-cases.md](docs/evaluation-cases.md)；这些是可重复评估的场景，不代表已运行训练、Office 或所有插件端到端测试。

具体期刊政策、引用格式和软件版本需在使用时重新核查。发现规则过度概括时，优先收窄适用范围。

## 许可证

技能原创说明和文档按 [MIT License](LICENSE) 分发。用户输入的稿件、数据、参考论文、工具和第三方资源保留各自权利与许可。
