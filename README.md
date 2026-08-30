# suns-story

一个面向 Codex 的中文故事写作 Skill。

只需提供**主题**与**篇幅**，它会生成原创的第一人称故事，主要采用以下叙事技法：

- 克制、冷静的叙述语气
- 精确数字与日常小动作之间的反差
- 短对白和未被说破的潜台词
- 非线性时间跳转
- 行政、账单、路线和操作流程等后台细节
- 普通物件的多次出现与意义变化
- 回扣开头但不直接升华的留白结尾

## 使用方法

安装后，可以显式调用：

```text
使用 $suns-story，主题：我的女友大A，大A指代中国A股市场；篇幅：1000字。
```

也可以直接描述需求：

```text
用冷峻克制、数字与细节形成反差的口吻，写一篇关于成年人告别的故事，2000字。
```

默认只输出标题和正文。若只提供主题与篇幅，Skill 会自行完成叙述者、人物关系、地点、时间线、核心物件和结尾设计。

## 安装

将仓库克隆到 Codex 的 Skills 目录：

```bash
git clone https://github.com/waffle105/suns-story.git ~/.codex/skills/suns-story
```

Windows PowerShell：

```powershell
git clone https://github.com/waffle105/suns-story.git "$env:USERPROFILE\.codex\skills\suns-story"
```

重新打开 Codex 会话后，即可通过 `$suns-story` 调用。

## 项目结构

```text
suns-story/
├── SKILL.md                    # 技能入口、工作流与交付检查
├── agents/
│   └── openai.yaml            # Codex 界面信息与调用策略
└── references/
    └── style-profile.md        # 详细风格谱、结构与修订指南
```

## 设计原则

`suns-story` 提炼的是可迁移的高层叙事技法，不是换名仿写模板：

- 不复制参考作品的原句、情节链、人物关系或标志性细节。
- 不以真实公众人物第一人称发布虚构自白。
- 不把未经证实的现实人物私生活写成事实。
- 涉及现实人物时，应改成明确的虚构角色、架空故事或寓言。

本仓库不包含用于风格研究的源 PDF，也不收录参考文章原文。

## License

[MIT](LICENSE)

