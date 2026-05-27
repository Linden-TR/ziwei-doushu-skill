# 紫微斗数 Skill · Ziwei Doushu

> **Author:** Linden（[Linden-TR](https://github.com/Linden-TR)） | **Version:** 1.0.0 | **License:** MIT

**中文** | [English](#english)

---

## 简介

**紫微斗数**是中国传统命理学两大支柱之一，与八字并称"命学双璧"。它起源于宋代，通过十四主星在十二宫的分布、四化飞星的能量流转，推演人一生的性格、事业、财运、婚姻、健康等各方面的走势。

本 Skill 将紫微斗数排盘与分析能力带入 Claude Code，基于 `@mingai/mcp` 提供的专业排盘引擎，结合结构化的分析框架与丰富的参考文库，帮助任何人——从命理初学者到资深研究者——快速获得专业级的紫微斗数命盘解读。

### 亮点

- **一键排盘** — 无需手动查表，输入出生信息直接出盘
- **多流派融合** — 整合三合、飞星、河洛、钦天四化等多流派分析视角
- **限流叠宫** — 大限、流年、流月、流日、流时层层叠加，精确定位时间节点
- **经典格局识别** — 自动匹配紫府同宫、杀破狼、月朗天门等数十种经典格局
- **结构化输出** — 每条解读有明确的星曜和宫位依据，不凭空断言
- **真太阳时校正** — 支持出生地经度，自动修正时区偏差

---

## 快速开始

### 1. 配置 MCP 服务

在项目根目录创建 `.mcp.json`：

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

重启 Claude Code 使配置生效。

### 2. 安装 Skill

```bash
# 项目级安装（仅当前项目可用）
git clone https://github.com/Linden-TR/ziwei-doushu-skill .claude/skills/ziwei-doushu

# 全局安装（所有项目可用）
git clone https://github.com/Linden-TR/ziwei-doushu-skill ~/.claude/skills/ziwei-doushu
```

### 3. 开始使用

在 Claude Code 中输入以下任一触发词：

```
紫微斗数    排盘    命盘    看盘    算紫微
看运势      大限    流年    四化    飞星
```

然后按提示逐一输入出生信息（性别、出生日期、时辰、地点）。Skill 会自动完成排盘并输出结构化分析报告。

---

## 项目结构

```
ziwei-doushu-skill/
├── SKILL.md                       # 核心工作流 · Core workflow
├── references/
│   ├── xingyao.md                 # 星曜速查 · Star reference
│   ├── gongwei.md                 # 十二宫互动 · Palace reference
│   ├── sihua.md                   # 四化规则 · Four Transformations
│   ├── pattern-library.md         # 经典格局库 · Pattern library
│   └── shichen.md                 # 时辰对照 · Time conversion
├── README.md
└── LICENSE
```

---

## 依赖

- [Claude Code](https://claude.ai/code)（或支持 Skill 的 Claude 客户端）
- [`@mingai/mcp`](https://www.npmjs.com/package/@mingai/mcp) — 排盘引擎

---

## 贡献

欢迎提交 Issue 和 Pull Request。参考库的扩充、新格局的添加、分析框架的优化都是欢迎的方向。

---

## License

MIT © 2026 Linden

---

<a name="english"></a>

## Introduction

**Ziwei Doushu** (紫微斗数, literally "Purple Star Astrology") is one of the two pillars of traditional Chinese destiny analysis, alongside BaZi (Eight Characters). Originating in the Song Dynasty (~10th century), it maps 14 major stars across 12 palaces to reveal a person's life trajectory — personality, career, wealth, relationships, health, and more.

This Skill brings Ziwei Doushu charting and analysis into Claude Code. Powered by the `@mingai/mcp` chart calculation engine and guided by a structured analytical framework with an extensive reference library, it enables anyone — from curious beginners to seasoned practitioners — to obtain professional-grade Ziwei chart readings.

### Highlights

- **One-click chart generation** — No manual table lookup. Input birth details, get a full chart.
- **Multi-school synthesis** — Integrates San He (三合), Fei Xing (飞星), He Luo (河洛), and Qin Tian Si Hua (钦天四化) perspectives.
- **Time-layered analysis** — Decadal luck, annual luck, monthly luck, daily luck, and bi-hourly luck stacked with precision.
- **Pattern recognition** — Automatically identifies dozens of classical configurations (Zi-Fu same palace, Sha-Po-Lang, Moon Over Heaven's Gate, etc.).
- **Evidence-based output** — Every interpretation is anchored to specific stars and palaces. No empty assertions.
- **True solar time** — Supports birthplace longitude for automatic timezone correction.

## Quick Start

### 1. Configure MCP

Create `.mcp.json` in your project root:

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

Restart Claude Code.

### 2. Install

```bash
# Project-level
git clone https://github.com/Linden-TR/ziwei-doushu-skill .claude/skills/ziwei-doushu

# Global (all projects)
git clone https://github.com/Linden-TR/ziwei-doushu-skill ~/.claude/skills/ziwei-doushu
```

### 3. Use

Type any of these trigger words in Claude Code and follow the prompts:

```
紫微斗数    chart    horoscope    fortune    destiny
排盘        ziwei    astrology    luck       flying star
```

## What is Ziwei Doushu? (A 30-Second Primer)

Your birth time determines which stars fall into which of the 12 palaces (Self, Career, Wealth, Spouse, Health, Travel, etc.). Each star carries a specific energy — Ziwei (紫微) is the Emperor star, Po Jun (破军) is the Vanguard, Tan Lang (贪狼) is desire and charisma. The Four Transformations (四化: Lu 禄 / Quan 权 / Ke 科 / Ji 忌) act as the dynamic engine, redirecting and amplifying these energies across palaces as time unfolds.

The result is a map — not of fate, but of tendencies, opportunities, and challenges. Think of it as a weather forecast for your life: it doesn't tell you what will happen, but it tells you when to carry an umbrella.

---

## Dependencies

- [Claude Code](https://claude.ai/code)
- [`@mingai/mcp`](https://www.npmjs.com/package/@mingai/mcp) — Chart calculation engine

## Contributing

Issues and PRs welcome. Expanding the reference library, adding new patterns, and refining the analytical framework are all encouraged.

## License

MIT © 2026 Linden
