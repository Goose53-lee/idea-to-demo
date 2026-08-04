# Idea to Demo

> 把模糊需求收紧成一条能点通、能拿来做决定的后台 Demo。

多数 Demo 的问题，不是页面少，而是看完之后仍然不知道：这个方向该不该继续做。

`idea-to-demo` 不从画页面开始。它先找清谁在用、要处理什么、最重要的判断是什么，再选出一条最小但完整的路径。最后交付的不是一组孤立界面，而是一个能运行、能操作、能验证方向的前端 Demo。

![OrderFlow 订单管理 Demo](assets/order-management-desktop.png)

## 快速开始

安装：

```bash
npx skills add Goose53-lee/idea-to-demo -g -y
```

调用：

```text
用 $idea-to-demo，把这份需求做成一个可以操作的后台 Demo。
```

只有一句想法也可以：

```text
用 $idea-to-demo 做一个门店售后管理后台。
主要给店长使用，他们需要快速发现异常订单并完成处理。
```

## 它怎么工作

### 1. 先找准要验证的问题

Skill 会先确定主要用户、核心业务对象和最重要的任务。缺少的信息如果会改变主流程，就问；只影响文案或样例数据，就写清假设后继续。

### 2. 只选一条完整路径

它不会为了显得完整而铺满模块。默认选择一条能从入口走到结果的路径，通常包含概览、列表或队列、详情，以及一次有意义的处理动作。

### 3. 让页面围绕任务组织

工作台用来判断，列表用来查找和筛选，详情说明对象当前发生了什么，表单承接下一步操作。每个页面都有一个视觉中心，不把所有模块做成同样重的卡片。

### 4. 做成真的可以操作

当任务包含代码，Skill 会沿用现有技术栈和组件，补上连贯的 Mock 数据、筛选、搜索、抽屉、表单、反馈和必要状态。主路径需要从头点到尾，不用静态截图冒充交互。

### 5. 在交付前跑一遍

构建成功只是起点。Skill 还会检查浏览器中的主流程、桌面端与窄屏、空状态或错误状态，以及是否误改了任务之外的文件。

## 你会得到什么

- 一条明确的产品验证目标；
- 一组彼此连接的后台页面；
- 自洽的 Mock 数据和业务状态；
- 可以实际点击的核心交互；
- 桌面端与窄屏的代表性响应式行为；
- 一份诚实的交付说明：哪些是真的，哪些是模拟的，哪些留给生产开发。

这仍然是 Demo。除非明确扩大范围，它不代表真实 API、数据库、登录与权限、安全审计、自动化测试、CI/CD 或上线准备已经完成。

## 示例

### OrderFlow：列表、详情与移动端

首页展示的桌面列表把异常提醒、核心指标、筛选和订单处理放进同一条工作路径。

详情用抽屉保留列表上下文，让用户查看状态、风险、收货信息、金额和订单动态后继续处理。

![OrderFlow 订单详情抽屉](assets/order-management-detail.png)

窄屏不压缩桌面表格，而是重新组织成订单卡片和移动导航。

<p align="center">
  <img src="assets/order-management-mobile.png" alt="OrderFlow 移动端订单卡片" width="390" />
</p>

### 退税通 ERP：工作台、列表与详情

工作台先给判断，再让用户进入数据。

![退税通 ERP 工作台](assets/erp-dashboard.png)

列表保留扫描效率和关键操作。

![退税申请列表](assets/erp-refund-list.png)

详情把对象、状态和下一步动作放在一起。

![退税申请详情](assets/erp-refund-detail.png)

> 示例使用 Mock 数据，只展示信息结构、状态关系、交互路径和响应式处理。

## 适合用在

- ERP、CRM、订单管理、运营平台和企业工作台；
- 列表、详情、表单、审批和异常处理流程；
- 从一句想法、PRD 或参考图快速验证产品方向；
- 在现有前端项目中补出一条可评审的新流程；
- 需要给团队演示，但还没到生产开发阶段的功能。

如果任务的核心是后端架构、数据库、安全、权限、部署或生产验收，这个 Skill 不是终点。

## 更多调用方式

有 PRD：

```text
用 $idea-to-demo 阅读这份 PRD。
先确定主要用户和最值得验证的路径，再做一个可运行的后台 Demo。
```

有参考图：

```text
用 $idea-to-demo 提取这些参考图的布局、层级和交互方法，
结合我的业务重新设计。不要复制原品牌和业务内容。
```

已有项目：

```text
用 $idea-to-demo 改造当前项目的订单列表和详情流程。
先检查现有组件、Token 和运行页面，复用当前技术栈；
完成后检查构建、主流程、桌面端和窄屏。
```

## 其他安装方式

<details>
<summary>手动安装到个人目录</summary>

把整个仓库复制到：

```text
~/.agents/skills/idea-to-demo
```

</details>

<details>
<summary>安装到单个项目</summary>

把 Skill 放进项目：

```text
your-project/
└── .agents/
    └── skills/
        └── idea-to-demo/
```

这样它只服务当前仓库，也可以跟随项目提交给团队。

</details>

如果安装后没有出现在 Skill 列表中，请重新启动 Codex。

## 仓库结构

```text
idea-to-demo/
├── SKILL.md
├── agents/
│   └── openai.yaml
├── references/
│   ├── discovery-and-scope.md
│   ├── ui-foundations.md
│   ├── page-patterns.md
│   ├── states-responsive-and-content.md
│   └── implementation-and-acceptance.md
└── assets/
    ├── demo-brief.md
    ├── demo-handoff.md
    └── example screenshots
```

`SKILL.md` 保存核心流程。页面模式、视觉基础、状态、响应式和验收规则按任务需要从 `references/` 读取。

## License

[MIT](LICENSE)
