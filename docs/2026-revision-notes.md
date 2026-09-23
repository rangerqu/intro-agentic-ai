# 2026 年内部分享修订初稿

修订日期：2026-09-23。基于 `rangerqu/intro-agentic-ai` 的 `8e2167970de7fc1ebaf14a4fcfafa276564267de`。原作署名川叶，原始项目为 [riverscn/intro-agentic-ai](https://github.com/riverscn/intro-agentic-ai)。

## 这一稿的定位

面向资管机构各岗位同事，重点照顾中后台与非技术听众。保留原版前八部分的递进结构、基础解释、交互示意和浅显语言，替换原医疗咨询、销售、履约等业务案例。原第九部分展开成第九至十一部分，讲清楚日常应用、任务边界与试用方法。

机构场景按内部工作设计，不套用零售客户咨询、客户转化或销售流程。所有具体任务与流程都是讨论示例，不表示公司已经实施或批准相应系统、政策和项目。演示材料全部虚构。

## 章节与讲授建议

| 部分 | 内容 | 本次处理 |
|---|---|---|
| 1 | AI 与神经网络 | 保留训练、梯度下降和图示，修正过强的生物类比与历史表述 |
| 2 | 生成式 AI | 保留 token 生成示意，补充训练、推理和工具的区别，以及 2026 年工作型 Agent 的交付方式 |
| 3 | 对话、提示词与 RAG | 保留基本讲法，改为内部意见整理与制度检索；澄清对话界面也可能包含 Agent 能力 |
| 4 | Agent 的循环与工具 | 用会议材料准备演示闭环，增加实际结果核验；不把内部思维展示等同于正确性 |
| 5 | 上下文工程 | 保留选择、压缩、隔离、写入，补充长任务交接与版本管理 |
| 6 | MCP、Skills、Subagents | 保留接口、说明书和分工类比，替换业务例子，补充 2026 年协议进展与权限区别 |
| 7 | Harness | 保留运行系统与工程思路，增加任务评估；去掉没有依据的倍数和效果保证 |
| 8 | 个人、团队、公司怎样用 | 保留层次与渐进路径，替换为制度比对助手；实际收益决定是否扩大 |
| 9 | 中后台与个人生产力 | 新增任务拆分、岗位候选任务、完整案例与专业经验的作用 |
| 10 | 可以交给 AI 的边界 | 新增动作级授权、常见误用、提示注入和讨论题 |
| 11 | 从小任务开始 | 新增试用安排、可复制提示词与现场演示 |

完整试讲可先按 75–90 分钟加讨论安排，实际时长需试讲后调整。第一至八部分保留内容深度，现场可减少交互停留；第九至十一部分建议留出约 25 分钟。若需要压缩，优先把产品进展、延伸阅读与部分讨论移到课后，不直接删除基础解释。

新增和重写的重要页面含 Slidev 讲者备注，可在 presenter 模式查看。第九部分“完整例子”展示主要差异；现场核对以 `docs/demo/expected-diff.md` 为完整参考，包含版本、生效日期和条号移动。

## 本次纠正的表述

- 2012 年 AlexNet 的表现改为大幅提高 ImageNet 竞赛成绩，不再写成当年“图像识别超过人类”。
- 神经网络与人脑的对应关系仅作类比。GPU 的优势取决于任务，不采用固定硬件换算。
- token 不是固定等于一个汉字，生成策略也并非总选概率最大的 token。原概率数字仅作示意。
- 语言模型能力还受训练、推理计算和工具影响，不用“只会猜字”解释全部能力。
- 对话与 Agent 区分的是任务推进方式，不把今天的对话产品笼统描述成不能调用工具。
- 推理模型可能不展示内部推理。验收需要来源、假设、计算和实际结果，而非长篇解释本身。
- MCP 提供接口规范，不自动赋予访问权限；Skills 不等于训练模型参数，多 Agent 也不保证更便宜、独立或正确。
- 移除“Harness 效果差 10 倍以上”“模型每 6 个月涨一轮”“个人效率翻倍”等无依据量化承诺。
- 数据使用与正式操作按机构授权设计，不把部署方式、脱敏或模型自报置信度当作充分条件。

## 来源与内容对应

以下为官方文档或原始论文。技术概念跨年份积累，2025 年的基础不标作 2026 年新发明。检索截至 2026-09-23。

| 来源 | 日期 | 本稿使用范围 |
|---|---|---|
| [ImageNet Classification with Deep Convolutional Neural Networks](https://papers.nips.cc/paper_files/paper/2012/hash/c399862d3b9d6b76c8436e924a68c45b-Abstract.html) | 2012 | AlexNet 竞赛表现的历史纠正 |
| [Effective context engineering for AI agents](https://www.anthropic.com/engineering/effective-context-engineering-for-ai-agents) | 2025-09-29 | 上下文选择、压缩与外部记录 |
| [Equipping agents for the real world with Agent Skills](https://www.anthropic.com/engineering/equipping-agents-for-the-real-world-with-agent-skills) | 2025-10-16；开放规范更新 2025-12-18 | 按需加载说明、参考资料和脚本 |
| [Effective harnesses for long-running agents](https://www.anthropic.com/engineering/effective-harnesses-for-long-running-agents) | 2025-11-26 | 进展记录、分步工作与结果验证 |
| [Demystifying evals for AI agents](https://www.anthropic.com/engineering/demystifying-evals-for-ai-agents) | 2026-01-09 | 验收任务结果，不能只看“已完成”的自述 |
| [How we contain Claude across products](https://www.anthropic.com/engineering/how-we-contain-claude) | 2026-05-25 | Cowork 知识工作实例，环境权限与外部内容风险 |
| [MCP Architecture overview](https://modelcontextprotocol.io/docs/learn/architecture) | 持续更新 | MCP 的基本定位与工具接口 |
| [The 2026-07-28 Specification](https://blog.modelcontextprotocol.io/posts/2026-07-28/) | 2026-07-28 | 协议连接、授权强化与扩展框架进展 |

产品能力例子说明已有实现，不构成产品采购建议或业务可靠性保证。本稿不采用模型排名、价格与未经本机构任务验证的效率数字。

## 演示材料

- [V1 输入](demo/policy-v1.md)
- [V2 输入](demo/policy-v2.md)
- [讲者参考核对表](demo/expected-diff.md)

现场使用讲义中的提示词，只提供两份输入。参考表用于讲者独立核对。演示不需要公司内部信息或正式系统权限。
