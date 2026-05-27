# video-creator

AI Video Full-Stack Creation Skill — generate scripts, storyboards, prompt packs, and compliance docs in one shot.

[![License](https://img.shields.io/badge/license-MIT-blue.svg)](LICENSE)
[![Version](https://img.shields.io/badge/version-1.1.0-green.svg)](SKILL.md)

> [中文版](README.md)

## What Is This

A complete methodology and executable scaffold for AI video creation. From a single creative idea, follow an 8-stage pipeline to produce deliverable scripts, storyboards, AI prompt packs, and compliance documents.

It can be installed directly as a **Marvis AI Assistant** Skill, or used as a standalone methodology reference for any AI video creator.

## 8-Stage Pipeline

```
Topic Config → Full Story → Script Table → Storyboard Table → Segment Storyboard → Prompt Packs → Compliance & Quality Review → Final Assembly
```

| Stage | Output | Description |
|-------|--------|-------------|
| Stage 0 Topic Config | Topic Confirmation | Parse user intent, determine video type, duration, style |
| Stage 1 Full Story | Complete Story | Storytelling by 4 narrative dimensions (Setup / Escalation / Conflict-Twist / Payoff) |
| Stage 2 Script Table | Standardized Script | VO, dialogue, voice tone annotations, duration estimates |
| Stage 3 Storyboard Table | Storyboard Script | Shot numbers, shot sizes, camera moves, durations, transitions |
| Stage 3.5 Segment Storyboard | 15s Segment Storyboards | `{{}}` placeholders, voice tone, sound effects, continuity annotations |
| Stage 4 Prompt Packs | AI Prompt Packs | Characters / Scenes / Props / Easter eggs — 4 categories |
| Stage 5 Compliance & Quality | Review Reports | Political / violence / NSFW / copyright / platform taboos + creative quality scoring |
| Stage 6 Final Assembly | Word Doc + TXT Log | All creative materials compiled and exported |

## Key Features

- **Fixed Format Constants**: F1-F5 format constants eliminate output inconsistency
- **Duration-Adaptive**: 1 min to 90+ min, auto-matches narrative structure, word count, shot count
- **Hard Constraint Validation**: Python scripts check volume/completeness at each stage, auto-block on failure
- **Mandatory Compliance Review**: Full checks for political, violence, NSFW, copyright, and platform taboo content
- **Creative Quality Scoring**: 60-point system across 4 narrative + 4 directorial dimensions
- **Series Linking**: Supports prequel continuity + sequel hooks, easter egg & foreshadowing tracking

## Installation & Usage

### For Marvis Users

```bash
# 1. Clone the repo
git clone https://github.com/Wsal4/video-creator.git

# 2. Copy to Marvis skills directory
cp -r video-creator ~/.agents/skills/custom/video-creator/

# 3. Use in conversation
/video A 30-second cyberpunk short film
```

Trigger words:
- `/video`
- `/生成视频` (generate video)
- `/做分镜` (create storyboard)
- `/写脚本` (write script)
- `/视频创作` (video creation)

### As a Standalone Methodology Reference

`SKILL.md` is pure Markdown — readable and usable by anyone:

- **F1-F5 Format Constants**: Standardized templates for scripts, storyboards, story segments, prompt packs, and output declarations
- **Duration-Narrative Matching Table**: Volume requirements and narrative structure by duration
- **8-Stage Pipeline Architecture**: Complete workflow from ideation to final assembly
- **Python Validation Scripts**: Runnable volume check scripts
- **Compliance Checklist**: Itemized rules for political / violence / NSFW / copyright / platform taboo review
- **Creative Quality Scoring Rubric**: 60-point system across 8 dimensions

## Example Use Cases

```
Generate a 1-minute short video script about a cat detective with a sequel hook
/video Create a cyberpunk-style 30-second short
Turn this synopsis into a full AI video storyboard and prompt set
Generate an AI video script based on current trending topics
Write an AI-video-ready storyboard and prompts
```

## Project Structure

```
video-creator/
├── SKILL.md       # Main Skill file (49KB), complete creation pipeline
├── meta.json      # Metadata (name, description, version, use cases)
├── README.md      # Chinese readme
├── README_EN.md   # English readme (this file)
├── LICENSE        # MIT License
├── CONTRIBUTING.md # Contribution guide
└── .gitignore
```

## Contributing

Contributions welcome — no coding required:

- **Open an Issue**: Bug reports, feature requests, feedback
- **Tweak a line, open a PR**: Fix typos, polish docs, optimize wording
- **Deep refactor**: New platform support, expanded scoring dimensions, pipeline restructure

Read [CONTRIBUTING.md](CONTRIBUTING.md) first.

> `SKILL.md` is plain Markdown — editing it is editing prompts. No build environment needed. PR diffs are pure text comparisons.

## License

MIT License — see [LICENSE](LICENSE)

## Related Projects

- [Marvis](https://github.com/your-org/marvis) — AI assistant platform compatible with this Skill
- [AI HOT](https://aihot.virxact.com) — AI news source (used in Stage 0 topic discovery)