# superagent-demo
Super-agent demo playground (dsh-superagent research prototype)

## 这个仓库是干什么的

这个仓库是 **Super-agent 架构**（`dsh-superagent` 参考原型）的试验场。

它不承载业务代码，存在的意义是验证和演示一条完整的协作链路：人提出需求，agent 自动开工，最后把可审查的产物交回来。

在这套架构里：

- 人只在一个地方提需求，并用 @ 提到 agent，不需要自己拆任务、开分支、跑测试；
- 编排层把需求切成工单，交给独立的 worker 在自己的会话和目录里完成——读上下文、判断范围、定方案、改代码、自测；
- worker 把结果（例如一个 Pull Request）连同验证证据交回原线程，人只需要 review 和决定。

所以，这个仓库里出现的改动和 PR 本身就是这套架构的行为样本：它们展示 agent 如何理解一个请求、如何控制改动范围，以及如何把「做完了」说得可验证。

**怎么用**：在本仓库的 Issue 下评论，形如 `@muzhi93-agent 在 README 里加一节「这个仓库是干什么的」，然后开一个 PR`。显式的 @ 请求会直接开工，并在原线程交付结果。
