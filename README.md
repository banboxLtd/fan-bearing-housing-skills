# Banbox 风机轴承座 Skill
# Fan Bearing Housing Procurement Skill

> Banbox 官方 AI 采购助手 Skill —— 选型 / 库存 / 报价一站搞定
> Official Banbox AI procurement skill — product search, stock check, and quote generation in one place.

---

## 快速安装 / Quick Install

直接把下面这句话发给你的 AI 助手：

> 帮我安装 Banbox 风机轴承座 Skill，仓库地址：`https://github.com/banbox/banbox-fan-bearing-housing-skill`

Agent 会自动克隆仓库、读取 `skill.json` 连接 MCP server，下次启动即可使用。

Send this to your AI agent:

> Install the Banbox fan bearing housing skill from: `https://github.com/banbox/banbox-fan-bearing-housing-skill`

---

## 手动安装 / Manual Install

### Claude Code

```bash
git clone https://github.com/banbox/banbox-fan-bearing-housing-skill.git \
  ~/.claude/skills/banbox-fan-bearing-housing-skill
```

### Cursor / 其他支持 MCP Streamable HTTP 的客户端

在 MCP 配置文件中添加：

```json
{
  "mcpServers": {
    "banbox": {
      "type": "streamable-http",
      "url": "https://ai.fanbearinghousing.com/mcp"
    }
  }
}
```

---

## 配置 API Key（可选）/ Configure API Key (Optional)

查看价格需要免费注册账户。注册方式：

1. **推荐**：直接告诉 AI 助手"我想查价格"，助手会自动引导你完成注册并获取 API Key。
2. **手动**：注册成功后将 `apiKey` 填入 `skill.json` 的 `env.BANBOX_API_KEY` 字段：

```json
{
  "env": {
    "BANBOX_API_KEY": "your-api-key-here"
  }
}
```

Pricing requires a free account. The AI assistant will guide you through registration automatically when you first ask for prices. Or fill in `skill.json` → `env.BANBOX_API_KEY` manually after registering.

---

## 支持的能力 / Capabilities

| 功能 | Function |
|---|---|
| 按轴径 / 冷却方式搜索产品 | Search by shaft diameter / cooling method |
| 查看产品规格和尺寸图 | View specs and dimension drawings |
| 下载产品目录 PDF | Download product catalogue |
| 查询库存和交期 | Check stock and lead time |
| 查看阶梯报价（需注册）| View tiered pricing (registration required) |
| 在线生成报价单 | Generate formal quote online |
| 常见问题解答（12项）| FAQ (12 topics) |

---

## MCP Server 信息 / MCP Server Info

- **Transport**: Streamable HTTP
- **Endpoint**: `https://mcp.banbox.cn/mcp`
- **Auth**: 无需额外鉴权，apiKey 通过工具 `context` 字段传入

---

## 联系我们 / Contact

- 网站 / Website: [www.fanbearinghousing.ccom](https://www.fanbearinghousing.com)
- 邮箱 / Email: sales@fanbearinghousing.com
