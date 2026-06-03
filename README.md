# growth-trajectory-research

A Claude Code skill for deep research and analysis of successful people's growth trajectories.

## What It Does

This skill enables Claude Code to perform evidence-backed analysis of public figures' growth trajectories, focusing on:

- Career breakthroughs and adversity turning points
- Key choices and their consequences
- How experiences shaped abilities, personality, and decision patterns
- Long-term growth systems: ability stacks, environment choices, networks, key bets, compounding loops
- Transferable principles and action insights

## What It Prevents

- Generic inspirational biographies ("hagiography")
- Unsupported cause-and-effect claims
- Survivorship bias
- PR/narrative repetition as fact
- Timeline hallucination
- Overgeneralized lessons

## Installation

### For Claude Code (Personal Skills)

Copy or clone this repository to your personal skills directory:

```bash
# Clone to your skills directory
git clone https://github.com/San-Y108/growth-trajectory-research.git ~/.claude/skills/growth-trajectory-research

# Or copy manually
cp -r growth-trajectory-research ~/.claude/skills/
```

### For Claude Code (Project Skills)

If you want to use this skill in a specific project:

```bash
# Clone into your project's .claude/skills directory
git clone https://github.com/San-Y108/growth-trajectory-research.git .claude/skills/growth-trajectory-research
```

## Usage

Once installed, the skill will automatically trigger when you ask Claude Code to analyze a successful person's growth trajectory. Examples:

- "告诉我 Elon Musk 是怎么成功的"
- "分析 Oprah 的成长轨迹和关键转折"
- "成功辍学生有什么共同特质？"
- "Tell me how Steve Jobs succeeded"
- "Analyze Taylor Swift's career choices and turning points"

## Skill Features

### Research Workflow

1. **Identity Confirmation** - Disambiguates common names, confirms success domain
2. **Multi-Source Deep Search** - 8-15 credible sources across 3+ source types
3. **Chronology First** - Dated timeline with confidence levels before analysis
4. **Turning Point Analysis** - Constraints, alternatives, risks, opportunity costs
5. **Experience Shaping** - How experiences shaped abilities with confidence labels (supported/plausible/speculative)
6. **Bias Audit** - Survivorship bias, hindsight bias, PR bias, base rate blindness
7. **Long-Term Growth System** - Ability stack, environment, networks, key bets, compounding loops

### Output Elements

Every analysis must include:

1. Source/credibility overview
2. Identity and success domain confirmation
3. Growth timeline with confidence levels
4. Important turning points and choices
5. Experience shaping analysis with confidence labels
6. Long-term growth system breakdown
7. Good/bad/not-to-imitate choices
8. Action insight (transferable principles, training directions, risk warnings)
9. Uncertainty and what not to conclude
10. Interactive follow-up questions (FAQ/AMA)

### Anti-Hagiography Rules

The skill actively prevents:

- Treating sequence as causality
- Generalizing elite outcomes
- Romanticizing adversity
- Ignoring failures, privilege, luck, timing, institutional support
- Presenting self-narratives as facts
- Omitting base rate data when analyzing groups

## Files

- `SKILL.md` - Main skill instructions (157 lines)
- `tests/pressure-scenarios.md` - 7 pressure test scenarios with pass/fail criteria (130 lines)
- `README.md` - This file

## Testing

The skill was validated using TDD (Test-Driven Development) methodology:

1. **RED Phase**: Identified baseline failure modes through spec review
2. **GREEN Phase**: Wrote minimal skill addressing observed failures
3. **REFACTOR Phase**: Ran 4 pressure scenarios, identified and fixed base rate data gap

### Test Results

| Scenario | Result |
|----------|--------|
| Oprah adversity | ✅ Passed |
| Steve Jobs controversy | ✅ Passed |
| Michael Jordan ambiguity | ✅ Passed |
| Successful dropouts bias | ❌→✅ Fixed (added base rate requirement) |

## License

MIT

## Contributing

Contributions welcome! Please open an issue or PR.

## Author

Created by [San-Y108](https://github.com/San-Y108)
