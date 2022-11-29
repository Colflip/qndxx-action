# qndxx-action
用于广西区域的青年大学习的自动打卡
## ~~学习不用等~~

## 使用GitHub Actions实现自动化签到

1. Fork 这个仓库

2. 在仓库的 Settings -> Security -> Secrets -> Actions 中新建两条 repository secret：

   - `USERID`，青年大学习的学习编号

   - `USERNAME`，青年大学习的姓名

3. 启用 GitHub Actions

进入仓库的 Actions 页面，点击绿色的「I understand my workflows, go ahead and enable them」按钮

   - 出于安全考虑，GitHub 会对 Fork 时存在 Workflow 文件的仓库禁用 Actions，需要用户手动确认安全才会启用。

   - 如果仓库没有 Actions 页面，请进入仓库的 Settings -> Code and automation -> Actions -> General -> Actions permissions 检查是否允许运行 Actions。

默认每周一自动触发两次 Workflow （GitHub Actions 高负载时可能延迟）。如需修改为其他时间或条件下签到，可按照 GitHub [文档](https://docs.github.com/cn/actions/using-workflows/triggering-a-workflow)修改 `.github/workflows/gradle.yml`。

订阅 GitHub Actions 的 [Workflow 运行通知](https://docs.github.com/cn/actions/monitoring-and-troubleshooting-workflows/notifications-for-workflow-runs)，可在签到失败（Workflow 执行失败）时收到通知提醒。