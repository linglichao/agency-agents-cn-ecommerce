# agency-agents-E-commerce

中国电商团队专属的 AI 角色库。

本仓库基于 [msitarzewski/agency-agents](https://github.com/msitarzewski/agency-agents) 和 [jnMetaCode/agency-agents-zh](https://github.com/jnMetaCode/agency-agents-zh) 做了定向裁剪，不再追求“大而全”，而是只保留适合中国电商业务直接落地的角色。

## 许可与署名

- 本仓库延续上游项目的 `MIT License`
- 保留了上游 `LICENSE` 文件中的版权与许可声明
- 当前仓库属于二次修改版本，主要工作是中国国内电商场景裁剪、角色收口和安装流程优化
- 上游来源：
  - 原始英文项目：[`msitarzewski/agency-agents`](https://github.com/msitarzewski/agency-agents)
  - 中文翻译与本地化项目：[`jnMetaCode/agency-agents-zh`](https://github.com/jnMetaCode/agency-agents-zh)
- 如果你继续基于本仓库二次分发，也应保留 `LICENSE` 和来源说明

## 这次收口后的定位

- 保留 `50` 个角色，覆盖 `10` 个国内电商高频部门
- 删除学术、游戏、HR、法务独立部门、空间计算、销售等不适合电商一线直接使用的角色
- 保留的平台与链路重点放在：淘宝/天猫、京东、拼多多、抖音、快手、小红书、微信生态、视频号、直播电商
- 保留的角色都服务于这几条主线：
  - 店铺运营与内容增长
  - 广告投放与归因分析
  - 商品、价格、库存、供应链
  - 客服、退货、日报周报
  - 电商系统开发与数据支持

## 适合谁用

- 国内品牌电商团队
- 淘系、京东、拼多多、抖音店播团队
- 私域和内容电商团队
- 电商产品、数据、技术、客服、供应链协作团队

## 保留的角色结构

### 营销与平台运营

- [中国电商运营专家](marketing/marketing-china-ecommerce-operator.md)
- [抖音策略师](marketing/marketing-douyin-strategist.md)
- [小红书运营专家](marketing/marketing-xiaohongshu-operator.md)
- [微信公众号运营](marketing/marketing-wechat-operator.md)
- [微信视频号运营策略师](marketing/marketing-weixin-channels-strategist.md)
- [快手策略师](marketing/marketing-kuaishou-strategist.md)
- [B站内容策略师](marketing/marketing-bilibili-strategist.md)
- [微博运营策略师](marketing/marketing-weibo-strategist.md)
- [私域流量运营师](marketing/marketing-private-domain-operator.md)
- [直播电商主播教练](marketing/marketing-livestream-commerce-coach.md)
- [短视频剪辑指导师](marketing/marketing-short-video-editing-coach.md)
- [百度 SEO 专家](marketing/marketing-baidu-seo-specialist.md)

### 付费投放

- [付费媒体审计师](paid-media/paid-media-auditor.md)
- [广告创意策略师](paid-media/paid-media-creative-strategist.md)
- [PPC 竞价策略师](paid-media/paid-media-ppc-strategist.md)
- [搜索词分析师](paid-media/paid-media-search-query-analyst.md)
- [追踪与归因专家](paid-media/paid-media-tracking-specialist.md)

### 供应链与经营

- [库存预测专家](supply-chain/supply-chain-inventory-forecaster.md)
- [物流路线优化师](supply-chain/supply-chain-route-optimizer.md)
- [供应商评估专家](supply-chain/supply-chain-vendor-evaluator.md)
- [动态定价策略师](specialized/specialized-pricing-optimizer.md)
- [零售退货专家](specialized/retail-customer-returns.md)

### 客服、分析与经营支持

- [客服响应者](support/support-support-responder.md)
- [数据分析师](support/support-analytics-reporter.md)
- [财务追踪员](support/support-finance-tracker.md)
- [法务合规员](support/support-legal-compliance-checker.md)
- [数据整合师](specialized/data-consolidation-agent.md)
- [报告分发师](specialized/report-distribution-agent.md)

### 产品、项目与质量

- [产品经理](product/product-manager.md)
- [反馈分析师](product/product-feedback-synthesizer.md)
- [趋势研究员](product/product-trend-researcher.md)
- [项目牧羊人](project-management/project-management-project-shepherd.md)
- [实验追踪员](project-management/project-management-experiment-tracker.md)
- [API 测试员](testing/testing-api-tester.md)
- [性能基准师](testing/testing-performance-benchmarker.md)
- [现实检验者](testing/testing-reality-checker.md)

### 电商技术与集成

- [前端开发者](engineering/engineering-frontend-developer.md)
- [后端架构师](engineering/engineering-backend-architect.md)
- [AI 工程师](engineering/engineering-ai-engineer.md)
- [数据工程师](engineering/engineering-data-engineer.md)
- [数据库优化师](engineering/engineering-database-optimizer.md)
- [代码审查员](engineering/engineering-code-reviewer.md)
- [飞书集成开发工程师](engineering/engineering-feishu-integration-developer.md)
- [微信小程序开发者](engineering/engineering-wechat-mini-program-developer.md)
- [UI 设计师](design/design-ui-designer.md)
- [UX 研究员](design/design-ux-researcher.md)
- [品牌守护者](design/design-brand-guardian.md)
- [图像提示词工程师](design/design-image-prompt-engineer.md)
- [视觉叙事师](design/design-visual-storyteller.md)
- [智能体编排者](specialized/agents-orchestrator.md)

完整文件索引见 [CATALOG.md](CATALOG.md)。

## 快速开始

### 1. 转换为目标工具格式

```bash
./scripts/convert.sh
```

### 2. 安装到你的工具

```bash
./scripts/install.sh --tool openclaw
./scripts/install.sh --tool claude-code
./scripts/install.sh --tool codex
./scripts/install.sh --tool cursor
./scripts/install.sh --tool hermes
```

### 3. 直接激活角色

```text
激活中国电商运营专家，帮我做一份 618 大促作战方案。
激活小红书运营专家，给这款新品做 7 天种草内容排期。
激活库存预测专家，根据近 90 天销量给出补货建议。
激活追踪与归因专家，帮我检查广告归因链路有没有断点。
```

## 推荐用法

### 单角色直用

适合一线员工直接提需求，例如：

- 店铺运营找 `中国电商运营专家`
- 平台内容找 `抖音策略师`、`小红书运营专家`
- 直播复盘找 `直播电商主播教练`
- 补货与库存找 `库存预测专家`
- 退货与售后找 `零售退货专家`、`客服响应者`

### 多角色协作

推荐几个电商常用组合：

- 新品上市：`趋势研究员` + `中国电商运营专家` + `小红书运营专家` + `广告创意策略师`
- 大促作战：`中国电商运营专家` + `库存预测专家` + `追踪与归因专家` + `数据分析师`
- 店播提效：`直播电商主播教练` + `短视频剪辑指导师` + `抖音策略师`
- 私域复购：`私域流量运营师` + `微信公众号运营` + `微信视频号运营策略师`
- 电商系统改造：`产品经理` + `前端开发者` + `后端架构师` + `API 测试员`

## 维护说明

- 新增或修改角色后，重新运行 `./scripts/convert.sh`
- 当前转换与安装脚本已经只面向本仓库保留的电商角色集
- 如果后续你还想继续收窄，比如只做“直播电商版”或“天猫旗舰店版”，可以再按部门继续拆分

## 来源说明

- 上游主项目：[`msitarzewski/agency-agents`](https://github.com/msitarzewski/agency-agents)
- 中文化基础：[`jnMetaCode/agency-agents-zh`](https://github.com/jnMetaCode/agency-agents-zh)
- 当前仓库：在中文化版本基础上做中国电商专属裁剪
