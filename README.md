# 紫微斗数 (Ziwei Doushu) — Claude Code Skill

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Version](https://img.shields.io/badge/version-1.0.0-blue)](SKILL.md)
[![Claude Code](https://img.shields.io/badge/Claude%20Code-Skill-orange)](https://claude.ai/code)

> Purple Star Astrology chart reading & destiny analysis skill for Claude Code. Multi-school methodology: Zhongzhou (primary), San He, Fei Xing, Qin Tian Si Hua, He Luo. Powered by `@mingai/mcp`.

**中文命理分析 · Chinese Metaphysics · Taoist Astrology · 东方占星**

---

## Features

- **Full chart casting** — 十二宫 (12 palaces), 十四主星 (14 major stars), 辅星/杂曜, 四化 (4 transformations), 大限 (decadal cycles)
- **Structured analysis** — 命盘骨架 → 星系全局 → 逐宫分析 → 四化追踪 → 大限解读 → 格局识别 → 徵验讯号
- **Multi-school integration** — Zhongzhou school as primary methodology, backed by San He, Fei Xing, Qin Tian Si Hua, and He Luo
- **Horoscope support** — 大限 / 流年 / 流月 / 流日 / 流时 analysis via `ziwei_horoscope`
- **Flying star analysis** — 宫干四化飞渡, 忌转忌/禄转禄 path tracking via `ziwei_flying_star`
- **45 classic patterns** — Pattern recognition with break/rescue analysis
- **International timezone support** — True solar time correction, DST handling, cross-timezone conversion

## Quick Start

```bash
git clone https://github.com/Linden-TR/ziwei-doushu-skill.git
```

Copy the skill into your Claude Code skills folder:

```
~/.claude/skills/ziwei-doushu/
├── SKILL.md
└── references/
    ├── xingyao.md          # Star reference (14 major + minor stars)
    ├── gongwei.md          # Palace reference (12 palaces + interactions)
    ├── sihua.md            # Four transformations (Qin Tian + Fei Xing)
    ├── pattern-library.md  # 45 classic patterns
    ├── shichen.md          # Time conversion & timezone reference
    └── zhengyan.md         # Empirical verification signals
```

## Usage

Once installed, simply ask Claude Code:

> "帮我排盘，1990年5月15日上午9点出生，男性"

> "分析一下我的事业运和财运"

> "Cast my Ziwei Doushu chart, born Feb 14 1990 at 3pm in San Francisco"

The skill auto-triggers on keywords like 紫微斗数, 排盘, 命盘, 看运势, Ziwei Doushu, Purple Star Astrology, and more.

## Analysis Framework

| Phase | Description |
|-------|-------------|
| **Phase 1** | Collect birth info (gender, date, time, birthplace) |
| **Phase 2** | Call MCP tools for chart casting |
| **Phase 3** | Structured analysis: skeleton → galaxy overview → palace-by-palace → four transformations → decadal cycle → pattern recognition |
| **Phase 4** | Output in academic Chinese style with evidence-linked judgments |

## Analysis Styles

- **精简版 (Compact)** — Core palaces + current decadal cycle, suitable for quick readings
- **详细版 (Detailed)** — Full 12-palace analysis + flying stars + pattern breakdown + verification signals

## Methodology

This skill follows the **Zhongzhou School (中州派)** tradition, tracing back to 陆斌兆 (Lu Binzhao) and 王亭之 (Wang Tingzhi):

1. **Wholeness over isolated signals** — Cross-palace integrated inference, not fragmented omens
2. **Logic over intuition** — Every judgment grounded in star-palace-transformation logic chains
3. **Scholarship over mysticism** — Ziwei Doushu as an academic knowledge system, not secret arts
4. **Empirical signals as supplement** — High-verification signals from the Lu-Wang corpus used as references, not absolutes

Other schools (San He, Fei Xing, Qin Tian, He Luo) serve as auxiliary perspectives.

## References

| File | Content |
|------|---------|
| `references/xingyao.md` | 14 major stars, brightness table, dual-star combos, 6 auspicious / 6 inauspicious / miscellaneous stars, star interaction principles |
| `references/gongwei.md` | 12 palaces, 三方四正, He Luo numerology, palace-stem-branch interactions, palace overlap rules |
| `references/sihua.md` | Qin Tian four transformations, flying star palace-stem technique, self-transformation, dual-化 analysis |
| `references/pattern-library.md` | 45 patterns (7 imperial + 8 literati + 10 career + 6 wealth + 8 special + 6 relational), break/rescue logic |
| `references/shichen.md` | Time period chart, true solar time correction, international timezone conversion, DST handling |
| `references/zhengyan.md` | Lu-Wang corpus empirical verification signals, organized by star and category |

## Requirements

- Claude Code (latest version recommended)
- `@mingai/mcp` MCP server configured for `ziwei`, `ziwei_horoscope`, `ziwei_flying_star` tools

## Author

**Linden** — [github.com/Linden-TR](https://github.com/Linden-TR)

## License

MIT © 2026 Linden
