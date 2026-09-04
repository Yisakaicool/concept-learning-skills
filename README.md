# 概念学习资料生成 Skill

## 仓库用途
本仓库包含一个用于自动生成概念学习资料的 WorkBuddy Skill，以及使用该 Skill 生成的三份学习资料（Agent、大模型的上下文、Skill）。

## Skill 存放位置
`.workbuddy/skills/concept-tutor/SKILL.md`

## 如何在 WorkBuddy 中调用
1. 在 WorkBuddy 中打开本仓库。
2. 在对话中输入：`使用 concept-tutor Skill 学习概念：[概念名称]`
3. 例如：
   - `使用 concept-tutor Skill 学习概念：Agent`
   - `使用 concept-tutor Skill 学习概念：大模型的上下文`
   - `使用 concept-tutor Skill 学习概念：Skill`

## 已生成的学习资料
- `learning-materials/agent.md`：关于 Agent 的学习资料
- `learning-materials/llm-context.md`：关于大模型的上下文的学习资料
- `learning-materials/skill.md`：关于 Skill 的学习资料

## 人工核查和修改
我使用 AI（WorkBuddy）生成了 Skill 模板和三份概念学习资料的初稿，并做了以下人工核查和修改：

一、Skill 层面

将 AI 生成的通用 Skill 模板调整为符合作业要求的结构，增加了“自检要求”和“输出结构”两个章节，确保其能接收任意概念而非只针对本次的三个概念。

核查了 SKILL.md 的 YAML 元数据格式，补全了 name 和 description 字段。

二、学习资料层面

阅读并修改了三份概念资料中的术语表述，使其更符合课程中的定义（例如：统一了“上下文”的称呼，避免与“语境”“背景”混淆）。

补充了每个概念“容易混淆的问题/使用边界”部分的具体例子（原本 AI 只写了原则性说明）。

手动核对了所有资料来源链接，删除了两个无法访问的参考链接，替换为可查证的官方文档链接。

三、概念关系说明

将 AI 生成的抽象关系描述改写为“外卖员”类比，使三个概念的协作关系更直观。

添加了个人学习体会：结合之前使用 WorkBuddy 调用 Skill 时因上下文不完整导致出错的真实经历，说明上下文对 Agent 的实际影响。

四、目录结构与版本管理

手动调整了初始自动生成的目录结构，将 learning-materials 从错误的位置（.workbuddy/skills/concept-tutor/ 下）移至仓库根目录，使其与作业要求的规范一致。

在提交前逐条检查了 git status，确保没有误提交临时文件或敏感信息。

根据作业要求补充了 .gitignore 文件，排除了系统文件和密钥文件。

五、作业过程中的纠错记录

解决了 SSH 端口被屏蔽的问题（通过 HTTPS 方式完成克隆和推送）。

纠正了 VSCode 中 Python 环境变量识别问题（重启编辑器后重新选择解释器）。

修正了文件名拼写（将 l1m-context.md 重命名为 llm-context.md，将 skill1.md 重命名为 skill.md）。
