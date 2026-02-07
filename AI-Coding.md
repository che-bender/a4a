- https://github.com/automata/aicodeguide
1. 使用ChatGPT 4.5，4o或o3按以下提示操作：
```
You're a senior software engineer. We're going to build the PRD of a project
together.

VERY IMPORTANT:
- Ask one question at a time
- Each question should be based on previous answers
- Go deeper on every important detail required

IDEA:
<paste here your idea>
```
您是一位资深软件工程师。我们将共同编写一个项目的产品需求文档 (PRD)。
非常重要：
- 一次只提一个问题
- 每个问题都应基于之前的回答
- 深入探讨每个重要的细节
想法：
- 针对中国大陆的高考资源填报,做一个历年高考成绩,各院校招生专业,人数,分数线的查询和分析系统
- 使用MERN技术栈
- 系统的用户界面除了满足正常的使用意外，做一些有特色的可视化呈现。期待柱状图和线型图意外的呈现。
```

2. 接下来几分钟，您将进入一个问答循环。请尽可能详细地回答所有问题。完成后（或您认为足够时），请发送以下提示，引导模型将其编译为产品需求文档 (PRD)：
# 这步我花了大概三十多分钟的时间。
```
Compile those findings into a PRD. Use markdown format. It should contain the
following sections:

- Project overview
- Core requirements
- Core features
- Core components
- App/user flow
- Techstack
- Implementation plan
```
将这些发现整理成一份产品需求文档 (PRD)。请使用 Markdown 格式。PRD 应包含以下部分：
- 项目概述
- 核心需求
- 核心功能
- 核心组件
- 应用/用户流程
- 技术栈
- 实现计划


3. 
```
根据生成的产品需求文档 (PRD)，制定一个详细的分步计划来构建此项目。
然后将其分解为相互衔接的小任务。
基于这些任务，再将其分解为更小的子任务。
确保每个步骤足够小，可以一次性完成，但又足够大，
以确保项目成功完成。
遵循软件开发和项目管理的最佳实践，避免复杂的跳跃式开发。将各个任务关联起来，创建依赖关系列表。
不应存在孤立任务。
非常重要：
- 使用 Markdown 或 AsciiDoc 格式
- 每个任务和子任务都应该是一个清单项
- 为每个任务提供足够的上下文信息，以便开发人员能够实现它
- 每个任务都应该有一个编号 ID
- 每个任务都应该列出依赖任务的 ID
```

4. 安装cursor，建了一个github工程，clone到本地。在cursorIDE中打开。输入下面的内容
```
你是一名高级软件工程师。请仔细阅读 @docs/specs.md，并实现 @docs/todo.md 中尚未完成的功能。每次都认真完成每个任务，并注意任务和子任务之间的依赖关系。完成一个任务后，在列表中勾选它，然后继续下一个任务。
```

- 之后cursor一通执行，期间按了几次run按钮。最后生成了一些代码和工程。
- 执行的时候没有完全跑起来，也许是因为我没有mongoDB。总之，cursor做了很多动作，没有什么结果。
- 更新了MongoDB的连接，正确的连接到了MongoDB。似乎是之前用了admin用户的原因。（参考testMongo.py）
- 之后让Cursor修复了后端的一些问题。正常的启动了项目。
- 基本上动起来了。但是目前没有数据。
- 下次做PRD的时候，把**数据移行**的问题考虑在内。

另外，在cursor中使用中文的话，对话的理解似乎没有问题。但是在执行命令的时候，画面上显示有一些乱码的部分。


# 整理
- 需要配置好环境，尤其是MongoDB
- 要考虑deploy的环境

# TBD
- MCP Sever起到什么作用？如何使用？
  - https://github.com/modelcontextprotocol/servers?tab=readme-ov-file
- 使用PRD+Cursor，做一个有实际生产价值的项目。接近bl4br的目的。
