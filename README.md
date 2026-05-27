# video-creator

AI 视频全流程创作技能 —— 一键生成脚本、分镜、提示词包与合规文档。

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.1.0-green.svg)](SKILL.md)

> [English](README_EN.md)

## 这是什么

一个面向 AI 视频创作的全流程方法论与可执行脚手架。帮助你从一句话创意出发，按 8 步流水线输出可交付的脚本、分镜、AI 提示词包和合规文档。

它可以作为 **Marvis AI 助手** 的 Skill 直接安装使用，也可以作为独立的方法论文档供任何 AI 视频创作者参考。

## 8 步流水线

```
选题配置 → 故事正文 → 脚本表 → 分镜表 → 段落故事板 → 提示词包 → 合规质量审查 → 产出汇总
```

| 阶段 | 产出 | 说明 |
|------|------|------|
| 阶段0 选题配置 | 选题确认 | 解析用户意图，确定视频类型、时长、风格 |
| 阶段1 故事正文 | 完整故事 | 按编剧叙事四维（建立/放大/冲突/兑现期待）创作 |
| 阶段2 脚本表 | 标准化脚本 | 含画外音、台词、音色标注、时长估算 |
| 阶段3 分镜表 | 分镜脚本 | 含镜头号、景别、运镜、时长、转场 |
| 阶段3.5 段落故事板 | 15秒段落故事板 | 含占位符 `{{}}`、台词音色、音效、衔接标注 |
| 阶段4 提示词包 | AI 提示词包 | 人物/场景/道具/彩蛋四类提示词 |
| 阶段5 合规质量 | 审核报告 | 政治/暴力/低俗/侵权/平台禁忌 + 创作质量评分 |
| 阶段6 产出汇总 | Word 文档 + TXT 日志 | 全部创作物料整合导出 |

## 核心特性

- **格式常量固化**：F1-F5 五套格式常量，杜绝输出不一致
- **时长自适应**：1 分钟到 90 分钟+，自动匹配叙事结构、字数、分镜数
- **硬约束验证**：Python 脚本逐阶段检查体量/完整性，不达标自动阻断
- **强制合规审核**：政治/暴力/低俗/侵权/平台禁忌全量检查
- **创作质量评分**：60 分制，编剧叙事四维 + 导演审美四维
- **剧集联动**：支持前集承接 + 续集悬念，伏笔 + 彩蛋全链路标注

## 安装与使用

### 方式一：Marvis 用户直接安装

```bash
# 1. 克隆仓库
git clone https://github.com/YOUR_USERNAME/video-creator.git

# 2. 复制到 Marvis skills 目录
cp -r video-creator ~/.agents/skills/custom/video-creator/

# 3. 在对话中使用
/video 赛博朋克风格的30秒短片
```

或者直接在 Marvis 中输入触发词：
- `/video`
- `/生成视频`
- `/做分镜`
- `/写脚本`
- `/视频创作`

### 方式二：作为方法论文档独立使用

`SKILL.md` 是纯 Markdown 文件，可以直接阅读和参考：

- **F1-F5 格式常量**：标准化脚本、分镜、故事板、提示词包、产出物声明的格式模板
- **时长-叙事结构匹配表**：不同时长的体量要求和叙事结构选择
- **8 步流水线架构**：从选题到产出汇总的完整工作流
- **Python 验证脚本**：可直接运行的体量检查脚本
- **合规审查清单**：政治/暴力/低俗/侵权/平台禁忌的逐项检查规则
- **创作质量评分细则**：60 分制，编剧叙事四维 + 导演审美四维

## 示例用例

```
帮我生成一个关于猫咪侦探的1分钟短视频脚本，要有续集
/video 做一个赛博朋克风格的30秒短片
用这个梗概写完整的AI视频分镜脚本和提示词
生成一个贴合当前热点的AI视频脚本
帮我写一个AI视频可用的分镜和prompt
```

## 样品输出

`samples/` 目录包含一个完整示例项目的全部产出物——都市心理悬疑短片《7楼半》（3分钟，20镜，60/60满分评分）：

| 文件 | 内容 | 大小 |
|------|------|------|
| [story.md](samples/story.md) | 故事正文（约1650字，三章结构） | 5KB |
| [script.md](samples/script.md) | 故事脚本表 | 2.6KB |
| [storyboard.md](samples/storyboard.md) | 分镜脚本表（20个分镜，13列格式） | 13KB |
| [characters.md](samples/characters.md) | 人物设定提示词包 | 2.7KB |
| [scenes.md](samples/scenes.md) | 场景设定提示词包 | 4.8KB |
| [sound.md](samples/sound.md) | 声音设计（4层音轨） | 2.4KB |
| [props-eastereggs.md](samples/props-eastereggs.md) | 道具与彩蛋提示词包 | 3KB |
| [segments.md](samples/segments.md) | 15秒段落故事板（P1-P12） | 12.6KB |
| [compliance.md](samples/compliance.md) | 合规审核报告 | 1.7KB |
| [scoring.md](samples/scoring.md) | 质量评分报告（60/60优秀） | 3.2KB |

## 项目结构

```
video-creator/
├── SKILL.md       # 主 Skill 文件（49KB），包含完整创作流水线
├── meta.json      # 元数据（名称、描述、版本、用例）
├── README.md      # 本文件
├── README_EN.md   # 英文版
├── LICENSE        # MIT 许可证
├── CONTRIBUTING.md # 贡献指南
├── .gitignore
└── samples/       # 示例产出物（《7楼半》完整项目）
    ├── story.md
    ├── script.md
    ├── storyboard.md
    ├── characters.md
    ├── scenes.md
    ├── sound.md
    ├── props-eastereggs.md
    ├── segments.md
    ├── compliance.md
    └── scoring.md
```

## 贡献

欢迎贡献！无论你是：

- **提 Issue**：发现 bug、建议新功能、反馈使用体验
- **改一行提 PR**：修正格式错误、补充文档、优化措辞
- **深度改造**：新增平台适配、扩展评分维度、优化流水线架构

请先阅读 [CONTRIBUTING.md](CONTRIBUTING.md)。

> `SKILL.md` 是纯 Markdown 文本文件，改它就是改提示词，不需要编程环境。PR 的 diff 就是纯文本对比，一目了然。

## 许可

MIT License - 详见 [LICENSE](LICENSE)

## 相关项目

- [Marvis](https://github.com/your-org/marvis) - 兼容本 Skill 的 AI 助手平台
- [AI HOT](https://aihot.virxact.com) - AI 资讯来源（阶段0 选题时使用）