---
layout: article
titles:
  # @start locale config
  en      : &EN       About
  en-GB   : *EN
  en-US   : *EN
  en-CA   : *EN
  en-AU   : *EN
  zh-Hans : &ZH_HANS  关于
  zh      : *ZH_HANS
  zh-CN   : *ZH_HANS
  zh-SG   : *ZH_HANS
  zh-Hant : &ZH_HANT  關於
  zh-TW   : *ZH_HANT
  zh-HK   : *ZH_HANT
  ko      : &KO       소개
  ko-KR   : *KO
  fr      : &FR       À propos
  fr-BE   : *FR
  fr-CA   : *FR
  fr-CH   : *FR
  fr-FR   : *FR
  fr-LU   : *FR
  # @end locale config
key: page-about
---

随着汽车电子电气架构（E/E 架构）向智能化与网联化深度演进，功能安全已超越早期以机械系统为主的工程保障范畴，演变为覆盖软硬件协同设计的系统化安全工程体系，成为自动驾驶技术落地与量产的关键基石。在此体系中，**危害分析与风险评估** (HARA, Hazard Analysis and Risk Assessment) 承担着风险识别与顶层安全需求定义的核心职能。该过程通过对车辆运行场景、潜在功能失效模式及环境要素的系统化建模，提取车辆运动状态、道路拓扑及交通参与者分布等关键特征，并基于严重度 (S)、曝光率 (E) 和可控性 (C) 三个维度对风险进行量化评估，确定汽车安全完整性等级 (ASIL)，并将评估结果转化为顶层安全目标 (Safety Goals)，进而分解为可验证的软硬件安全需求，指导系统设计与工程实施。

为推动大模型与人工智能技术在预期功能安全 (Safety of The Intended Functionality, SOTIF) 及功能安全领域的落地应用，提升 HARA 流程的自动化与智能化水平，我们提出“面向自动驾驶的自动化危害分析与风险评估评测任务” 并构建了一个专注于评估自动驾驶安全逻辑推理与需求生成的结构化数据集。该数据集源自脱敏的真实工业项目数据，聚焦于动力系统核心高危失效模式——“非预期驱动力/扭矩输出”，共包含 3,000 条高质量标注数据。本任务旨在多维度评估模型在安全领域的场景理解、因果推理与风险决策能力，包含以下两个子任务：

- **子任务 1：危害事件识别与场景描述生成。**该任务要求模型基于给定的车辆运行工况与环境参数，精准识别潜在的危害事件 (Hazard Event)，并生成符合工程规范的危害场景结构化描述。
- **子任务 2：风险参数评定与等级推理。**该任务要求模型基于场景特征，推理并输出 HARA 分析的关键风险指标 (S/E/C)，并据此判定相应的安全完整性等级 (ASIL)。
