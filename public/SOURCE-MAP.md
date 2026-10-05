# Reviewer 网站内容来源映射

状态核对日期：2026-10-05（竞品资料核对日期仍为 2026-10-04）。实现基线：fc4cfe6；插件候选 0.7.0，74文件，tree digest 51bd9a9376debb1c7e8f82c17b02a632eaf89511ae08e706e82a37a59aec366e。Claude 最新复核已提交绑定，三组 evaluator 各 71/71，CP3 已关闭、manifest 已生成；日常安装未切换。

以下路径相对仓库根，正文中的术语是易读摘要，不改变产品语义。用户面统一称“你”或“Owner”；T0 原文中的 David 为单用户 Owner。

| 页面内容 | 核对依据 |
|---|---|
| 产品定位、四场景、两条Loop、非目标 | 技术评审/Reviewer-Plugin/Reviewer-Plugin产品设计.md §1–6；Reviewer-Plugin产品SSOT.md |
| 五Skill、四入口、工具和原生卡 | plugins/reviewer/skills/reviewer/SKILL.md；lib/server.mjs |
| 标准起草、独立审查、退修、账本 | skills/reviewer-align/SKILL.md；lib/alignment.mjs、ledger.mjs、server.mjs |
| 四单元、覆盖与依赖方向 | skills/reviewer-split/SKILL.md；lib/units.mjs |
| 五CR、B1–B4、独立复核、分歧和缺口 | skills/reviewer-verify/SKILL.md；lib/schemas.mjs、checks.mjs、loop2.mjs |
| 三轮、反向依赖闭包、TTL | skills/reviewer-recheck/SKILL.md；lib/recheck.mjs |
| SDK与持久化分层 | plugins/reviewer/README.md、SDK-DEPENDENCY.md；lib/persist.mjs、native.mjs、hook.mjs |
| 安装与hook | .agents/plugins/marketplace.json；plugins/reviewer/.codex-plugin/plugin.json、hooks/hooks.json、README.md |
| 成本口径 | plugins/reviewer/README.md；lib/usage.mjs、data/prices.json（不在网站报当前价格） |
| 修复候选、三组结果、限制 | docs/tasks/RV-06-D4-D6-claude-review.md §1–8；RV-06-CP3-closeout.md |
| 插件分发与安装尚未切换 | RV-06-CP3-closeout.md；evidence/RV06-CP3-20261005/installed-inventory.json 与当轮 git log/status |
| 人工/产品效果与旧数字合同边界 | 技术评审/Reviewer-Plugin/2026-10-03-新版验收与升级决定.md；tests/reviewer/product-effectiveness-contract.md；最新复核边界 |

方法文件的 skills/、lib/ 简写均相对 plugins/reviewer。架构图体现逻辑职责，不承诺严格的单向调用栈。SDK 可信性依赖消费者接线，不以结构有效代替语义正确。

信息结构参考：用户指定 matt-pocock-plugins/docs/site/index.html、architecture.html、guide.html、README.md；未复制其下载包、发布状态、上游能力或多宿主承诺。

页面没有公开原始评审日志、私人绝对路径、账号、认证信息或测试回执。发布静态网页不改变 Reviewer 候选包，亦不关闭 CP3。

## 竞品与任务范围增补

comparison.html 的五款产品能力已在 2026-10-04 核对官方资料，链接随对应段落列出。以 Recensa 官方产品页、Lenz About、Factiverse 主页、Prelint How reviews work、Patronus quickstart / evaluator reference 为依据。只概述任务、输入与输出，不采用厂商营销中的效果、速度、价格优势。

产品设计 §4 原竞品速览是历史未复核摘要，本页不沿用其“各自只覆盖一层”的排他断言：Recensa 已覆盖整份文档和来源；Lenz 可处理草稿和引用；Prelint 有后续 PR 评审；Patronus 支持自定义标准。页面不据“未公开”推断“不支持”。Reviewer 的区别写作组合流程，非功能独占或效果优越声明。

选用建议为公开定位加产品范围的归纳；六类任务与示例依据 T0 §1、§3–6，非实际成功案例。未修改 T0、语义合同或插件包。

2026-10-05 架构更新：收集与失败处置见 `plugins/reviewer/lib/collection.mjs`，Codex 证据见 `codex-evidence.mjs`；当前 76 文件候选、工程验证与历史宿主重放见 `docs/tasks/Architecture-collection-evidence-20261005.md` 和 `docs/tasks/Architecture-release-20261005.md`。旧 CP3 与 manifest 仅对应 `51bd9a93…`，不外推至本次候选。
