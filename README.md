<h1 align="center">Viral Video Cloner</h1>

<p align="center"><b>Recreate viral videos with your AI agent.</b><br>
1 clip, 1 photo, 0 reshoots.<br>
Keep the moves, the camera and every cut. Swap in your people, products and world.</p>

<p align="center">
  <a href="https://chatcut.io/viralvideocloner?utm_source=github&utm_medium=readme&utm_campaign=oss_viral_cloner&utm_content=nav"><b>Website</b></a>
  &nbsp;&bull;&nbsp;
  <a href="#examples"><b>Examples</b></a>
  &nbsp;&bull;&nbsp;
  <a href="docs/how-it-works.md"><b>How it works</b></a>
  &nbsp;&bull;&nbsp;
  <a href="README.zh-CN.md"><b>简体中文</b></a>
</p>

<p align="center">
  <img alt="Works with Claude Code" src="https://img.shields.io/badge/Claude%20Code-supported-D97757?style=flat-square">
  <img alt="Works with Codex" src="https://img.shields.io/badge/Codex-supported-111111?style=flat-square">
  <a href="LICENSE"><img alt="License: Apache-2.0" src="https://img.shields.io/badge/License-Apache--2.0-blue?style=flat-square"></a>
  <a href="https://discord.com/invite/sMjQPvwZTT"><img alt="Discord" src="https://img.shields.io/badge/Discord-join-5865F2?style=flat-square&logo=discord&logoColor=white"></a>
</p>

<p align="center">
  <img src="docs/media/hero.webp" width="960" alt="One skateboarding take recreated twice. Left: the original. Right: the same push, ollie and grind recreated in a Seoul spring lane and in an anime seaside town.">
</p>
<p align="center"><sub>Left: the original. Right: two recreations, one reference photo each. Same push, ollie, grind and camera. <a href="examples/skate-one-take-two-worlds">See the plans</a>.</sub></p>

**Hypit clones a video's edit: the script, captions and B-roll. Viral Video Cloner keeps the footage itself.** The motion, the camera move and every cut stay as filmed, and the people, products and world become yours.

## Install

```bash
npx skills add ChatCut-Inc/viral-video-cloner -g
```

Then ask your agent in plain words:

```text
Recreate this video with me as the skater: https://www.tiktok.com/@creator/video/123  (attach me.jpg)
```

On first use, the skill sets up [ChatCut Desktop](https://chatcut.io/viralvideocloner?utm_source=github&utm_medium=readme&utm_campaign=oss_viral_cloner&utm_content=install) (free, macOS and Windows) and connects it to your agent. If sign-in is needed, your agent guides you through it and continues in the same conversation. If tools or Skills have not loaded, it follows your agent app's requirements to refresh, restart and resume, or start a new conversation. When a new conversation is needed, it gives you a complete prompt to copy, carrying your request, media and setup progress forward. Recreations need a ChatCut membership. Before anything renders, your agent tells you how long the result will be and roughly how many credits it costs. Nothing starts until you say go.

## Examples

### Motion transfer: new cast, new world, same stunt

<video src="UPLOAD:truck-compare" controls muted></video>

A man on a camp chair in a golden field becomes a woman in white on a snowy plain at sunrise, and the black pickup becomes an orange rally truck. The jump, the landing and the camera are untouched. `16:9 · 8 s · 1080p · ≈21 credits` · [plan](examples/truck-jump-snowfield)

### Object swap: change one thing, keep every other pixel

<video src="UPLOAD:toycar-compare" controls muted></video>

A model car on a train windowsill grows into a real car in the tunnel. Only the car changes: the sill, the forest and the tunnel lights stay as filmed. `16:9 · 8 s · 720p · ≈8.5 credits` · [plan](examples/toy-car-train-tunnel)

<video src="UPLOAD:swap-strip" controls muted></video>

Each clip wipes from the original to the recreation. A creator's tumbler becomes your moka pot while her face, words and room stay. A poodle barista becomes a British shorthair. A canister on a back seat becomes a gift box. `9:16 · 8 s · 720p · ≈9 credits each` · plans: [moka pot](examples/ugc-moka-pot), [cat barista and gift box](examples/showcase)

### Batch: one ad, many creators

<video src="UPLOAD:batch-strip" controls muted></video>

One UGC ad recreated with four creators in four settings: a café, a parked car, a rooftop and a study. Same tumbler, same pitch, same timing. `9:16 · 8 s each · 4 versions` · [plans](examples/ugc-four-creators)

**More:** a crowd dance in three worlds, an activewear brand film and seven short recreations (a cat barista, a giant's boot, a ceiling-fan outfit change...) are in [examples/](examples/README.md).

## What people make with it

- **Ads.** Take an ad that already performs and recreate it shot for shot with your product. Same pacing, same camera, new product.
- **UGC.** Keep a creator's delivery and put your product in their hand, or run one script through several creators and settings.
- **Choreography.** Put yourself, your mascot or your character into a trending dance with the original moves and cuts.
- **Brand films.** Restage a cinematic shot in your brand's world: your colors, your locations, your cast.

## How it works

1. **Your agent studies the source.** It reads every shot and cut and writes a plan: who plays which role, what to swap, what must stay.
2. **You confirm length and cost.** Recreations run from 4 to 30 seconds.
3. **ChatCut renders it.** The source's motion guides the new video, so moves, camera work and cut points follow the original. The source audio is kept.
4. **The result lands in a ChatCut project,** ready to edit further or export.

Three ways to recreate:

| Mode | What changes | What stays |
| --- | --- | --- |
| **Motion transfer** | People, setting and style, rebuilt from your reference photos | Movement, camera and timing |
| **Object swap** | Only the person, product or outfit you name | Every other pixel of the shot |
| **Batch** | A new cast or product per version | The shot, the pitch and the timing |

Have your own footage instead? The agent can also cut it to the source's rhythm, captions and effects. Details: [docs/how-it-works.md](docs/how-it-works.md).

## Pricing

- The skill is free and open source. ChatCut Desktop is free to download.
- Recreations are generated in the cloud and need a ChatCut membership; they use the membership's credits ([pricing](https://chatcut.io/pricing?utm_source=github&utm_medium=readme&utm_campaign=oss_viral_cloner&utm_content=pricing)). As a guide: 8 seconds at 720p is about 10 credits, at 1080p about 26.
- Your agent quotes the length and estimated credits before every render. See [docs/pricing.md](docs/pricing.md).

## Use it responsibly

- **Only recast people who agreed.** Yourself, people who gave you permission, or characters you created.
- **No public figures.** Don't recreate celebrities, politicians or other real people you don't have rights to.
- **Mind the source.** A recreation keeps the source audio and follows its choreography and shots. If you publish it, make sure you may use them, or replace the audio.
- **Label AI content** where your platform asks for it, and never use a recreation to fake an endorsement.

Full policy: [docs/responsible-use.md](docs/responsible-use.md). Report misuse to team@chatcut.io.

## FAQ

**Which agents work?** Claude Code and Codex, running on your computer (macOS 13+ or Windows x64). Browser-only chats and cloud sandboxes can't reach ChatCut Desktop.

**What can I use as the source?** A link or a local file. Each recreation covers 4 to 30 seconds; for longer videos your agent picks the strongest part and tells you which.

**How many reference photos?** Up to 6 per recreation: people, products, outfits or places.

**How is it different from other recreation tools?** You ask in plain words inside Claude Code or Codex: no ComfyUI graph and no NVIDIA GPU, because rendering runs in the cloud. The agent writes a shot-by-shot plan first, so cut points line up with the source, and the result opens in an editor where you can keep cutting.

**No agent?** Download [ChatCut Desktop](https://chatcut.io/viralvideocloner?utm_source=github&utm_medium=readme&utm_campaign=oss_viral_cloner&utm_content=faq), open Viral Video Cloner under Skills, and add the video and your photos.

## Repository

```text
skills/viral-video-cloner/   the skill (also linked from .claude/skills and .agents/skills)
examples/                    every example: plan, reference images, cost, what changed
docs/                        how it works, pricing, responsible use
```

## Contributing

Made something good with it? [Share your recreation](https://github.com/ChatCut-Inc/viral-video-cloner/issues/new?template=showcase.yml): the best ones join the examples. Bug reports and skill improvements are welcome too. See [CONTRIBUTING.md](CONTRIBUTING.md).

## License

The skill, plans and docs are released under the [Apache License 2.0](LICENSE). Example media is licensed separately, mostly under CC BY 4.0; see [examples/MEDIA-LICENSE.md](examples/MEDIA-LICENSE.md). ChatCut and Viral Video Cloner are trademarks of ChatCut; see [TRADEMARK.md](TRADEMARK.md).

<p align="center"><sub>Built by <a href="https://chatcut.io/?utm_source=github&utm_medium=readme&utm_campaign=oss_viral_cloner&utm_content=footer">ChatCut</a>, the AI video editor your agent can drive.</sub></p>
