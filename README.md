# 解禁冲击评估

`laogu-unlock`

限售解禁冲击评估 skill：输入公司名称或股票代码，输出解禁抛压评估报告。

## 一键安装

仓库地址（点击复制）：

`https://github.com/laogu-caibao/laogu-unlock`

**方式一：克隆**

```bash
git clone https://github.com/laogu-caibao/laogu-unlock.git
```

**方式二：下载 ZIP**

https://github.com/laogu-caibao/laogu-unlock/archive/refs/heads/main.zip

**导入使用**

- Claude Code / Muse：把仓库中的 `SKILL.md` 放到 `~/.claude/skills/laogu-unlock/` 下即可调用。
- 豆包智能体 / Workbuddy 等：按各平台的 skill 上传流程导入 `SKILL.md`。
- 扣子 Coze：扣子编程 → 技能面板 → 创建技能 → 本地上传，上传本仓库打包的 zip（仓库根目录已有 SKILL.md，直接压缩仓库文件夹即可）；如页面要求 `.skill` 后缀，由扣子导入后自动生成，不要只改扩展名。
- Trae：设置 → 技能 → 上传技能，上传同上 zip；或手动放到 `~/.trae/skills/laogu-unlock/`（项目级用 `.trae/skills/laogu-unlock/`）。Trae 也支持 MCP：把 `uvx laogu-mcp` 配进 MCP 设置即可获得 16 个工具（skill 负责流程指导、MCP 负责工具调用）。
- 一次装好全部 16 个：用 [laogu-mcp](https://github.com/laogu-caibao/laogu-mcp)，`uvx laogu-mcp` 一键安装。
## 文件结构

- `SKILL.md` — 主流程（平台中立，需用户输入公司，无自动运行）
- `references/sources.md` — 数据源：解禁信息以网页搜索为主力路径、交叉核对规则、历史案例搜索模板

## 输出结构

- 解禁基本信息：日期、股数、占总股本/流通股比、股份性质、主要解禁股东
- 抛压分级：轻微（<5%）/ 中等（5–20%）/ 重度（>20%），经验分级
- 解禁结构解读：股东性质与一般性减持意愿常识
- 历史案例参照：可比案例事实陈述（不做预测）
- 风险提示：解禁 ≠ 减持，实际减持看后续公告

## 使用方式

- 输入：公司名称或股票代码（如"海通发展"、"603616"）
- 可与 `laogu-morning` 联动：早报中的"今日看点·限售解禁"条目可直接丢进来做深度评估
- 可与 `laogu-announcements` 联动：解禁提示性公告出现后自动触发评估

---
## 出品

**老谷拆财报** —— 以数据为刃，剖市场真相

- 抖音 / 微信视频号 / 今日头条 / 快手：搜索「老谷拆财报」
- 固定栏目：「价值投资之财报解读」（全网连载中）
- 本 skill 的方法论与账号内容同源：数据驱动、拆开看、不讲黑话

### 扫码关注

| 微信视频号 | 抖音 |
|---|---|
| ![视频号二维码](docs/qrcode-shipinhao.jpg) | ![抖音二维码](docs/qrcode-douyin.png) |
| 扫一扫，关注视频号 | 抖音号：gubaobao22 |

> 作者声明：个人观点，仅供参考，不构成投资建议。
