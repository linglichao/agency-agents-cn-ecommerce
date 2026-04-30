# OpenCode 桌面版使用国内电商角色库指南（Windows）

适用对象：日常在 Windows 上使用 OpenCode 桌面版的运营同事。

## 一、先拿到项目

项目地址：

- GitHub：<https://github.com/linglichao/agency-agents-cn-ecommerce>

建议做法：

1. 把仓库下载为 ZIP 并解压到一个固定目录
2. 或者用 Git 克隆到本地

示例目录：

- `D:\AI\agency-agents-cn-ecommerce`

## 二、打开 PowerShell

进入项目目录，例如：

```powershell
cd D:\AI\agency-agents-cn-ecommerce
```

## 三、最简单的用法

如果员工已经把这个项目下载好了，并且是让 OpenCode 自己帮忙操作，那么最简单可以直接对 AI 说：

- `请先帮我在当前项目安装这个国内电商角色库，然后激活中国电商运营专家。`
- `请先检查当前项目有没有安装电商角色库，没有的话帮我安装，再用小红书运营专家帮我写方案。`

AI 正常会做这两步：

1. 运行角色安装命令
2. 安装完成后直接按你说的角色开始工作

如果员工想自己手动安装，再看下面标准步骤。

## 四、标准安装步骤：生成 OpenCode 可用角色文件

首次使用先运行：

```powershell
.\scripts\convert.ps1 --tool opencode
```

这一步会生成：

- `integrations\opencode\agents\`

## 五、安装到当前项目

继续运行：

```powershell
.\scripts\install.ps1 --tool opencode
```

安装完成后，项目目录下会出现：

- `.opencode\agents\`

说明：

- OpenCode 这里是“项目级安装”
- 也就是哪个项目里放了 `.opencode\agents\`，OpenCode 在那个项目里就能用这些角色

如果想一步做完，也可以直接连续执行：

```powershell
.\scripts\convert.ps1 --tool opencode
.\scripts\install.ps1 --tool opencode
```

## 六、在 OpenCode 桌面版里怎么用

1. 用 OpenCode 打开你的工作项目目录
2. 确认这个项目目录里已经有 `.opencode\agents\`
3. 在对话里直接说出角色名和任务

示例：

- `激活中国电商运营专家，帮我做一份 618 大促作战方案。`
- `激活小红书运营专家，给这款新品做 7 天种草内容排期。`
- `激活抖音策略师，给这个短视频脚本做优化。`
- `激活库存预测专家，根据近 90 天销量给出补货建议。`
- `激活客服响应者，帮我整理一套售后回复话术。`

更适合普通员工的一句话说法：

- `请用中国电商运营专家帮我做这个活动方案。`
- `请用小红书运营专家帮我写 5 篇种草笔记。`
- `请用抖音策略师帮我优化这个短视频脚本。`
- `请用客服响应者帮我整理售后回复模板。`

## 七、推荐优先使用的角色

日常运营高频：

- 中国电商运营专家
- 小红书运营专家
- 抖音策略师
- 微信视频号运营策略师
- 直播电商主播教练
- 私域流量运营师
- 库存预测专家
- 动态定价策略师
- 客服响应者
- 数据分析师

## 八、更新角色库

如果仓库有新版本，进入项目目录后重新运行：

```powershell
.\scripts\convert.ps1 --tool opencode
.\scripts\install.ps1 --tool opencode
```

## 九、常见问题

### 1. 提示找不到脚本

先确认你在项目根目录下，再执行命令。

### 2. PowerShell 不允许执行脚本

可以先在当前窗口执行：

```powershell
Set-ExecutionPolicy -Scope Process Bypass
```

然后重新运行上面的 `convert.ps1` 和 `install.ps1`。

### 3. OpenCode 里没有看到角色生效

按下面顺序排查：

1. 确认项目目录里已经有 `.opencode\agents\`
2. 确认 `.opencode\agents\` 里面有很多 `.md` 文件
3. 关闭并重新打开 OpenCode 当前项目
4. 提问时直接写出角色名，不要只描述岗位

### 4. 不知道该用哪个角色

优先按任务类型选：

- 做平台运营方案：`中国电商运营专家`
- 做小红书内容：`小红书运营专家`
- 做抖音内容或投流思路：`抖音策略师`
- 做直播复盘或话术：`直播电商主播教练`
- 做补货和库存：`库存预测专家`
- 做客服话术：`客服响应者`
- 做经营分析：`数据分析师`

## 十、仓库说明

这个角色库是基于开源项目二次裁剪的国内电商版，已经收口成更适合运营团队直接使用的版本。
