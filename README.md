# 紫微斗数 Skill

> 作者：Linden | 版本：1.0.0 | 许可：MIT

基于 MCP 工具的专业紫微斗数命盘分析 skill，适用于 Claude Code。

## 功能

- 调用 `@mingai/mcp` MCP 服务自动排盘（支持阳历/农历/真太阳时）
- 结构化十二宫分析（命宫、官禄宫、财帛宫、夫妻宫等）
- 四化飞星与运限分析（大限、流年、流月）
- 经典格局自动识别
- 固定输出模板，每条解读有星曜或宫位依据

## 安装

### 前置条件：配置 MCP 服务

本 skill 依赖 `@mingai/mcp` MCP server 提供排盘工具。

**1. 在项目根目录创建 `.mcp.json`：**

```json
{
  "mcpServers": {
    "mingli": {
      "command": "npx",
      "args": ["-y", "@mingai/mcp"]
    }
  }
}
```

**2. 重启 Claude Code 使 MCP 配置生效。**

### 安装 Skill

```bash
# 项目级安装（仅当前项目可用）
git clone https://github.com/Linden-TR/ziwei-doushu-skill .claude/skills/ziwei-doushu

# 全局安装（所有项目可用）
git clone https://github.com/Linden-TR/ziwei-doushu-skill ~/.claude/skills/ziwei-doushu
```

## 使用

在 Claude Code 中输入以下任一触发词：

```
紫微斗数    排盘    命盘    看盘    算紫微
看运势      大限    流年    四化    飞星
```

然后按提示逐一输入出生信息即可。

## 项目结构

```
ziwei-doushu-skill/
├── SKILL.md                       # 核心：分析工作流与输入输出规范
├── references/
│   ├── xingyao.md                 # 十四主星 + 六吉六煞 + 杂曜速查
│   ├── gongwei.md                 # 十二宫含义与宫位互动规则
│   ├── sihua.md                   # 四化规则与天干四化表
│   ├── pattern-library.md         # 经典格局库
│   └── shichen.md                 # 时辰对照与推算
├── README.md
└── LICENSE
```

## 依赖

- Claude Code（或支持 skill 的 Claude 客户端）
- `@mingai/mcp` MCP server（通过 `.mcp.json` 配置）

## License

MIT
