# zh-dev-writing

中文代码注释与中文界面文案的写作规范，以 [Agent Skill](https://docs.claude.com/en/docs/claude-code/skills) 的形式提供给 Claude Code 等 AI 编程助手使用。

AI 写中文时常见的毛病：注释复述代码、引用文档章节号、满篇「把它」「搞」「坑」；界面提示写成「网络不太好，再试一次」「服务器开小差了」，或者直接甩出「请求失败（40001）」。这个 Skill 把这些问题整理成一份可执行的规范，在写或审查中文注释、中文 UI 文案时自动加载。

## 内容

- [`SKILL.md`](skills/zh-dev-writing/SKILL.md)：判断在写哪一类文字，两类共用的原则，两者的差别，落笔前自检。
- [`references/code-comments.md`](skills/zh-dev-writing/references/code-comments.md)：代码注释规约。注释分 What 与 Why 两类：What 写在读者会整体使用的地方，Why 只写代码里看不出来、能落到具体后果的理由。附改写示例。
- [`references/ui-copy.md`](skills/zh-dev-writing/references/ui-copy.md)：界面文案规约。引导类可以亲切，提示和报错用规范短句；按钮写清动作，同一动作全程一个叫法；数字、单位、时间、专名的格式。

## 安装

### Claude Code 插件

```
/plugin marketplace add FooFishes/zh-dev-writing
/plugin install zh-dev-writing@zh-dev-writing
```

### 手动安装

把 `skills/zh-dev-writing` 目录复制到个人或项目的 skills 目录：

```bash
git clone https://github.com/FooFishes/zh-dev-writing.git
cp -r zh-dev-writing/skills/zh-dev-writing ~/.claude/skills/
```

只想在某个项目里启用，就复制到该项目的 `.claude/skills/` 下。

## 使用

安装后不需要手动调用。写中文注释、改中文提示语、审查文案时，助手会根据 Skill 描述自动加载。也可以直接说「按 zh-dev-writing 改一下这段注释」。

项目自己的规范与本 Skill 冲突时，以项目规范为准。

## 许可证

[MIT](LICENSE)
