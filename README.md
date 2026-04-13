# Seedance 2.0 Prompt Skill for Claude Code

[中文文档](README_CN.md)

> Turn Claude Code into your Seedance 2.0 video prompt expert

A [Claude Code](https://docs.anthropic.com/en/docs/claude-code) Skill that generates high-quality Chinese video prompts ready to paste directly into ByteDance's [Jimeng Platform](https://jimeng.jianying.com/) (Seedance 2.0 video generation model).

Distilled from **400+ battle-tested Seedance 2.0 prompts**, featuring storyboard timeline methodology, reinforcement keyword constraint system, and writing guides for 18+ scene categories.

## Features

- **10 Creation Modes** — Text-to-video, character consistency, camera replication, effect mimicry, story completion, video extension, sound design, one-take long shot, video editing, music beat sync
- **Reinforcement Keyword System** — A quality insurance mechanism extracted from real-world prompts, ensuring stable generation (resolution, facial stability, motion fluidity, lighting, atmosphere)
- **Storyboard Timeline Method** — Precise per-segment control of shot scales, camera movements, and frame content, flexible from 4 to 15 seconds
- **18+ Scene Writing Guides** — Each scene category has dedicated writing focus, reinforcement keyword recipes, and style references
- **Long Video Segmentation** — Videos exceeding 15 seconds are automatically split into segments with transition point descriptions
- **Multimodal Asset References** — Full `@图片`/`@视频`/`@音频` reference specification
- **8-Dimension Writing Standards** — Granular standards covering facial expressions, actions, lighting, materials, camera work, transitions, physics, and sound effects

## Scene Coverage

| Category | Scenes |
|----------|--------|
| Portraits & Culture | Aesthetic portraits, Chinese traditional culture (Peking opera / calligraphy / tea ceremony / shadow puppetry / guqin...), daily life & emotions |
| Action & Fantasy | Action combat, sci-fi & fantasy, cinematic quality, creative mashups |
| Nature & Animals | Atmospheric landscapes, cute animals & pets |
| Sports | Basketball, swimming, boxing, skiing, F1, surfing, rock climbing... |
| Commercial | Product showcase videos, e-commerce ads, automotive displays |
| Content Creation | Educational/knowledge content, local life/store reviews, short drama dialogue, MV/music beat sync |
| Product Showcase Subcategories | Beauty & skincare, fashion & apparel, food & beverage, electronics, home goods, sports & outdoor, pet supplies, jewelry & accessories |

## Quick Start

### 1. Install the Skill

Place `seedance2.md` into your Claude Code skills directory:

```bash
# Option A: Project-level (current project only)
mkdir -p .claude/skills
cp seedance2.md .claude/skills/

# Option B: Global (available across all projects)
mkdir -p ~/.claude/skills
cp seedance2.md ~/.claude/skills/
```

### 2. Usage

Describe the video you want in Claude Code — the skill triggers automatically:

```
> Write a cyberpunk future city video prompt

> Generate a 15-second Peking opera performance prompt

> Create a lipstick product showcase prompt, 9:16 vertical

> I need a 30-second xianxia battle short film
```

**Trigger keywords**: `seedance`, `sd2`, `视频提示词`, `video prompt`, `生成视频`, `AI视频`, `即梦`, `短剧`, `广告视频`, `视频延长`, `带货视频`, etc.

## Examples

### Example 1: Aesthetic Portrait

**Input**: `Write a video prompt about a boy under cherry blossoms`

**Output**:

```
16:9横屏，15秒，日系青春电影质感。0-3秒：全景俯拍，樱花花瓣纷纷扬扬飘落，
神社古老的石板路铺满粉色花毯，镜头缓慢下降穿过层层樱花。3-7秒：中景跟拍，
一位穿白色校服的男生从远处走来，发丝随步伐轻轻晃动，脚步轻盈踩在落花上。
7-11秒：近景侧拍，男生突然停下抬头，樱花花瓣从镜头前划过形成虚影，他嘴角
微微上扬露出温柔的笑容，逆光中发丝边缘泛起金色光晕。11-15秒：特写侧脸，
背景虚化成粉白色的樱花散景，镜头缓缓推进直到占满整个面部。【强化词】4K超高清，
日系小清新色调，暖黄逆光效果，景深感强，面部清晰稳定，五官全程一致不变形，
动作流畅连贯无跳帧。
```

### Example 2: Product Showcase

**Input**: `Write a lipstick try-on product video prompt`

**Output**:

```
9:16竖屏，15秒，化妆品广告质感。0-3秒：特写唇膏旋转出壳，金属外壳在聚光灯下
闪烁高级光泽，色号清晰可见。3-7秒：中景美妆博主手持口红展示膏体，丝绒雾面质地
显色饱满，旋转展示不同角度。7-11秒：特写唇部试色，博主用口红均匀涂抹双唇，
动作轻柔专业，色彩从裸色渐变为复古红。11-15秒：特写最终妆效，唇色饱满显白
显气质，博主对镜微笑自信大方。【强化词】口红试色，高级丝绒质感，色彩还原度高，
唇部特写稳定，4K高清。
```

### Example 3: Long Video (Auto-segmented)

**Input**: `Write a 30-second xianxia battle short film`

**Output**: Automatically split into 2 segments of 15 seconds each, with transition point descriptions for sequential generation and stitching on the Jimeng platform.

## Core Methodology

### Golden Formula

```
Subject + Action + Scene + Lighting + Camera Language + Style + Quality + 【Reinforcement Keywords】
```

### Storyboard Timeline

| Time Segment | Shot Scale | Narrative Function |
|-------------|------------|-------------------|
| 0-3s | Wide / Establishing | Build the world: environment, atmosphere, sense of space |
| 3-7s | Medium | Subject entrance: character actions, interactions, narrative progression |
| 7-11s | Close-up / Detail | Emotional peak: expression details, key actions, texture showcase |
| 11-15s | Close-up ↔ Wide | Resolution: freeze frame / pull back, emotional resonance, lingering imagery |

### Reinforcement Keyword System

Quality constraints appended to each prompt, marked with `【强化词】`:

```
【强化词】4K超高清，电影质感，面部清晰稳定，五官全程一致不变形，
人体比例自然协调，动作流畅连贯无跳帧，暖黄逆光效果，景深感强。
```

> **Note**: The generated prompts are in **Chinese** — this is required by the Seedance 2.0 platform for optimal results. You can describe your ideas in any language, and the skill will produce Chinese prompts automatically.

## Repository Structure

```
.
├── README.md               # This file (English)
├── README_CN.md            # Chinese README
├── seedance2.md            # Skill file (place in .claude/skills/ to use)

```

## Acknowledgments

- Prompt materials sourced from community-shared Seedance 2.0 practical prompt collections
- Platform capabilities referenced from the [Jimeng Platform](https://jimeng.jianying.com/) official documentation

## License

MIT
