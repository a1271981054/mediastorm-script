# mediastorm-script

一个用于中文视频口播稿写作、润色和重写的 Agent Skill。它把影视飓风（B站 UID 946974）最近 **100 期完整逐字稿**（409,956 汉字 / 45,720 句断句 / 27 小时 45 分钟音频）的叙事方式，整理成可复用的写作步骤与量化词表，适合硬件评测、技术科普、AI 工作流、极限企划、深度纪实、旅行对话与商业复盘等题材。

本项目为独立的学习与写作工具，与影视飓风无官方关联。参考材料中的作品名称及引用内容属于其各自权利人。

## 特点

- **分赛道骨架**：8 大赛道、16 种细分流派，各有一套论证动力，不套用同一模板。
- **三层辩证拉扯**：先让步还原对方逻辑，再实测反折，留缝给例外，关键处收紧定性，避免单向吹黑。
- **实测呼吸节奏**：气口均值 9.18 字、九成断句不超过 15 字，按题材控制语气词温度。
- **零虚构事实**：不编造数据、测试结果或个人经历，素材缺口以占位标注。
- **去爹味视角**：多用 `我觉得`、少用 `我认为`，以“替你踩过坑的朋友”口吻说话。
- **可查的量化底稿**：词频矩阵、控温红线、标题公式、商单植入公式与改稿诊所全部附在 `references/`。

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
├── SKILL.md                          # 技能入口：人设红线、六步创作法、时长配比、交稿自检
├── references/
│   ├── patterns.md                   # 一页纸速查：核心数据铁律、赛道速选表、救命句型
│   ├── tracks.md                     # 八大赛道与 16 流派骨架 + 100 期原片时间戳案例
│   ├── rhetoric-and-dialectics.md    # 辩证微语法、10 大叙事机关、7 种商单公式、标题公式
│   └── lexicon-and-prosody.md        # 41 万字词频矩阵、按题材控温表、呼吸韵律、改稿诊所
└── README.md
```

## 更新记录

- **2026-11-20**：升级为 100 期 / 41 万字全量蒸馏版，新增 `tracks.md`、`rhetoric-and-dialectics.md`、`lexicon-and-prosody.md` 三份专项手册，重写 `SKILL.md` 与 `patterns.md`。
