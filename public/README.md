# Reviewer 发布页与使用指南

这是 Reviewer 0.7.0 的产品说明网站。正式入口：https://ww880412.github.io/reviewer-guide/ 。信息结构参考 matt-pocock-plugins 的 docs/site；视觉遵循 ~/.codex/DESIGN.md，独立编写 HTML/CSS/JavaScript，无运行依赖和构建步骤。

## 预览

从仓库根运行 `node docs/site/serve.mjs`，打开输出的 loopback 地址。服务只提供白名单中的页面、CSS、JS、图标与这两份维护文档，不暴露仓库、评审材料、会话或凭据。直接打开 index.html 也可阅读；浏览器剪贴板权限可能不同，文本复制失败会选中内容。

## 读者路径

- index.html：产品定位、四种场景、两条 Loop、交付物、适用范围。
- comparison.html：五款相邻产品与直接 Agent 评审的对照、差异、六类任务、反例和官方来源。
- architecture.html：五层职责的可点选说明、标准、可信绑定、复查、恢复、状态路径与模块索引；可复制架构 JSON。
- guide.html：本地安装、四种可复制启动示例、人的决定、结果、成本、数据与故障处理。
- release.html：候选 digest、实现/验收/发布/安装状态、本轮证据、未验证项与发布顺序。
- SOURCE-MAP.md：维护内容与源码/产品文档/验收记录的映射。

## 维护边界

这是纯说明网站，不会调用 Reviewer、启动模型、写评审状态、安装插件或发送决定。架构交互和首页报告明确为说明/示意。

没有公开下载 ZIP；release manifest 已生成，绑定已验收的 74 个包文件。不得把“页面完成”写成“插件已发布”。当前日常安装与修复候选不同；状态更新时核对包 digest、Claude 报告、evaluator、manifest 及实际安装，不能只改版本号。

仅部署这个目录中的公开页面和静态资源；不要发布本仓其他目录、私人轨迹或材料。2026-10-05 用户指定沿用 Matt 的 GitHub Pages 方式；公开网站仓库为 ww880412/reviewer-guide。仅上传公开静态白名单，插件包和验收原始材料留在私有工程仓。网站不进入 plugins/reviewer 包，避免改变刚验收的74文件候选。要携带包内指南须单独形成新候选并重新核验。

网站初次交付记录见 ../tasks/Reviewer-site-delivery.md；2026-10-05 状态更新与验收收尾见 ../tasks/RV-06-CP3-closeout.md。
