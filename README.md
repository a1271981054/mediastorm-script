# mediastorm-script

一个用于中文视频口播稿写作、润色和重写的 Agent Skill。它将影视飓风视频口播中的叙事方式整理成可复用的写作步骤，适合技术科普、AI 工作流介绍、产品讲解和纪录片式叙事。

本项目为独立的学习与写作工具，与影视飓风无官方关联。参考材料中的作品名称及引用内容属于其各自权利人。

## 特点

- 用具体问题或现象开场，尽快交代观众为什么需要了解这个主题。
- 把技术概念翻译成日常例子，用工作流前后对比说明变化。
- 使用短句、自然转场和观众可能提出的问题组织讲解。
- 明确适用条件和局限，不编造测试结果、数据或个人经历。
- 附带写作模式、案例和中短视频压缩方法。

## 安装

在项目中安装，将仓库克隆到项目的技能目录：

```bash
mkdir -p .agents/skills
git clone https://github.com/a1271981054/mediastorm-script.git .agents/skills/mediastorm-script
```

也可以安装到当前用户的共享技能目录：

```bash
mkdir -p ~/.agents/skills
git clone https://github.com/a1271981054/mediastorm-script.git ~/.agents/skills/mediastorm-script
```

需要支持读取 `SKILL.md` 的 Agent 客户端；具体技能目录和重新加载方式请以客户端文档为准。

## 使用

在支持 Agent Skills 的客户端中，可以直接指定技能和任务，例如：

```text
用 $mediastorm-script 把下面的技术说明改写成 3 分钟中文口播稿：
……
```

也可以提供主题、目标观众、时长、已有材料和希望保留的事实，让 Agent 从头组织讲解。时效性事实与外部资料应在使用前核实。

## 文件结构

```text
mediastorm-script/
├── SKILL.md                 # 技能入口与写作流程
├── references/
│   └── patterns.md          # 写作模式、案例与句式参考
└── README.md
```
