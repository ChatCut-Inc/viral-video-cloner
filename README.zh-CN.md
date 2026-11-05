<h1 align="center">爆款视频复刻 · Viral Video Cloner</h1>

<p align="center"><b>让你的 AI 助手复刻任何爆款视频。</b><br>
一句话，把爆款视频换成你的人、产品和场景。</p>

<p align="center">
  <a href="https://chatcut.io/zh/viralvideocloner?utm_source=github&utm_medium=readme&utm_campaign=oss_viral_cloner&utm_content=nav_zh"><b>官网</b></a>
  &nbsp;&bull;&nbsp;
  <a href="#能换成什么样"><b>示例</b></a>
  &nbsp;&bull;&nbsp;
  <a href="docs/how-it-works.md"><b>原理</b></a>
  &nbsp;&bull;&nbsp;
  <a href="README.md"><b>English</b></a>
</p>

<p align="center">
  <img alt="支持 Claude Code" src="https://img.shields.io/badge/Claude%20Code-supported-D97757?style=flat-square">
  <img alt="支持 Codex" src="https://img.shields.io/badge/Codex-supported-111111?style=flat-square">
  <a href="LICENSE"><img alt="License: Apache-2.0" src="https://img.shields.io/badge/License-Apache--2.0-blue?style=flat-square"></a>
</p>

<p align="center">
  <img src="docs/media/hero.webp" width="960" alt="同一段群舞复刻成三个不同的世界：白色哥特宫廷、红羽歌舞秀和 1930 年代水上芭蕾，踩着节拍切换">
</p>
<p align="center"><sub>同一段群舞，复刻成三个不同的世界：白色哥特宫廷、红羽歌舞秀和 1930 年代水上芭蕾。<a href="https://chatcut.io/zh/viralvideocloner?utm_source=github&utm_medium=readme&utm_campaign=oss_viral_cloner&utm_content=hero_zh">看完整视频</a>。</sub></p>

## 安装

```bash
npx skills add ChatCut-Inc/viral-video-cloner -g
```

## 三步开始

1. **选一个想复刻的视频。** 链接或本地文件都行。
2. **把需求发给你的 AI 助手。** 它会装好 ChatCut，再问你要原视频和素材。
3. **AI 生成你的版本。** 成片可以继续剪辑或导出。

```text
用我当领舞，复刻这段舞：<视频链接或本地文件>（附上 me.jpg）
```

第一次用时，技能会帮你装好 [ChatCut 桌面端](https://chatcut.io/zh/viralvideocloner?utm_source=github&utm_medium=readme&utm_campaign=oss_viral_cloner&utm_content=install_zh)（免费，支持 macOS 和 Windows），并接到你的 AI 助手上。需要登录时，AI 助手会引导你完成登录，再在原对话继续。如果工具或 Skill 尚未加载，它会按当前 AI 助手应用的要求，选择刷新、重启后恢复原对话，或新开对话。需要新对话时，它会提供一段完整的可复制提示语，带上你的需求、素材和已完成的安装状态。复刻需要 ChatCut 会员。开始生成前，AI 助手会先告诉你成片多长、大约花多少积分，你同意了才开始。

## 能做什么

**爆款、UGC、TVC，都能复刻。** 已经验证过的好内容，换成你的品牌。

| 爆款短视频 | UGC 广告 | TVC 广告 | 商品展示 |
| --- | --- | --- | --- |
| <video src="UPLOAD:usecase-viral" controls muted width="200"></video> | <video src="UPLOAD:usecase-ugc" controls muted width="200"></video> | <video src="UPLOAD:usecase-tvc" controls muted width="200"></video> | <video src="UPLOAD:usecase-fashion" controls muted width="200"></video> |
| 热门舞蹈和段子，换你来演 | 同一段真人自拍种草，手里换成你的产品 | 同样的大片镜头，主角换成你的产品 | 同一条上身视频，换上你的新款 |

## 能换成什么样

### 动作迁移

动作和运镜照原片来，出镜的人和场景都换成你的。

<video src="UPLOAD:truck-compare" controls muted></video>

金色荒野里坐在折叠椅上的男人，换成雪原日出里的白衣女生；黑色皮卡换成橙色拉力皮卡。`16:9 · 8 秒 · 1080p · 约 21 积分` · [规划](examples/truck-jump-snowfield)

### 局部替换

说出要换的人、产品或衣服，镜头里其余部分原样不动。

<video src="UPLOAD:toycar-compare" controls muted></video>

火车窗台上的模型车，进隧道后变成真车。`16:9 · 8 秒 · 720p · 约 8.5 积分` · [规划](examples/toy-car-train-tunnel)

<video src="UPLOAD:swap-strip" controls muted></video>

博主手里的吸管杯换成你的摩卡壶，贵宾犬咖啡师换成英短猫，后座上的塑料桶换成礼盒。`9:16 · 8 秒 · 720p · 每条约 9 积分` · 规划：[摩卡壶](examples/ugc-moka-pot)、[猫咖啡师和礼盒](examples/showcase)

### 批量出片

同一条 UGC 广告，换 4 位模特、4 个场景，产品和讲法不变。

<video src="UPLOAD:batch-strip" controls muted></video>

`9:16 · 每条 8 秒 · 4 个版本` · [规划](examples/ugc-four-creators)

## 作品

**一条视频，变成任何世界。** [7 条短复刻](examples/showcase)和更多示例都在 [examples/](examples/README.md)，每个都附规划。

## 怎么做到的

1. **AI 助手先看片**：读出每个镜头和切点，写一份规划：谁演哪个角色、换什么、什么必须保留。
2. **你确认时长和费用**：每次复刻 4–30 秒。
3. **ChatCut 生成**：用原片的动作引导新画面，动作、运镜和切点都跟着原片走，原声保留。
4. **成片进 ChatCut 项目**：可以接着剪，也可以直接导出。

手上有自己的素材？AI 助手也可以照原片的节奏、字幕和特效来剪你的素材。详见 [docs/how-it-works.md](docs/how-it-works.md)。

## 怎么收费

- 技能免费、开源；ChatCut 桌面端免费下载。
- 复刻在云端生成，需要 ChatCut 会员，用会员积分支付（[价格](https://chatcut.io/zh/pricing?utm_source=github&utm_medium=readme&utm_campaign=oss_viral_cloner&utm_content=pricing_zh)）。参考：8 秒 720p 约 10 积分，1080p 约 26 积分。
- 每次生成前，AI 助手都会先报时长和预估积分。详见 [docs/pricing.md](docs/pricing.md)。

## 安全与授权

- **只换得到同意的人**：你自己、授权给你的人，或你自己创作的角色。
- **不做公众人物**：明星、政要，以及你没有权利使用的真人，都不要复刻。
- **注意原片权利**：复刻会保留原片的声音，也沿用它的编舞和镜头。要发布的话，先确认你有权使用，或者换掉原声。
- **按平台要求标注 AI 生成**，不要用复刻伪造代言。

完整说明：[docs/responsible-use.md](docs/responsible-use.md)。发现滥用请发邮件到 team@chatcut.io。

## 常见问题

**爆款视频复刻是什么？** ChatCut 的一个 Skill，帮你复刻喜欢的视频。给 AI 助手原视频和你的照片或素材，它会保留原片的动作和运镜，把人、产品或场景换成你的。

**支持哪些 AI 助手？** 能在你电脑上运行的 AI 助手，比如 Claude Code 和 Codex（macOS 13 及以上或 Windows x64）。纯网页聊天和云端沙箱连不到 ChatCut 桌面端。第一次用时，助手会帮你装好 ChatCut。

**没有 AI 助手也能用吗？** 能。下载 [ChatCut 桌面端](https://chatcut.io/zh/viralvideocloner?utm_source=github&utm_medium=readme&utm_campaign=oss_viral_cloner&utm_content=faq_zh)，在 Skills 里打开爆款视频复刻，填上原视频和你的照片或素材就行。

**动作迁移和局部替换有什么区别？** 动作迁移保留动作、运镜和节奏，人物和场景按你的照片重建；局部替换保留整个镜头，只换你点名的人、产品或衣服。

**需要自己选用哪种方式吗？** 不用。说清想怎么改，AI 助手会自己判断。

**可以用什么视频？** 视频链接或本地文件都行。每次复刻 4 到 30 秒；视频更长时，助手会挑动作最完整的那段，并告诉你。

**需要会剪辑吗？** 不需要。说清想怎么改，剩下的交给 AI 助手。

**最多能放几张照片？** 每次最多 6 张，可以是人物、产品、服装或地点。

**怎么收费？** 复刻消耗 ChatCut 积分。生成前会先告诉你做多长、大约多少积分，你确认后才开始。

**会保留原视频的声音吗？** 会。成片保留原片的声音；原片没有声音时，保留模型生成的声音。

**成片在哪里？** 在 ChatCut 的项目里，可以继续剪辑，也可以直接导出。

**和其他复刻工具有什么不同？** 在 Claude Code 或 Codex 里用一句话说清要换什么就行，不用搭 ComfyUI，也不需要 NVIDIA 显卡，生成在云端跑。AI 助手会先写逐镜头的规划，切点和原片对得上；成片直接进剪辑器，还能接着剪。

## 仓库结构

```text
skills/viral-video-cloner/   技能本体（.claude/skills 和 .agents/skills 里有链接）
examples/                    每个示例：规划、参考图说明、费用、换了什么
docs/                        原理、计费、安全与授权
```

## 参与贡献

用它做出了好东西？[分享你的复刻](https://github.com/ChatCut-Inc/viral-video-cloner/issues/new?template=showcase.yml)，好的作品会收进示例。也欢迎报 bug、改进技能，见 [CONTRIBUTING.md](CONTRIBUTING.md)。

## 许可

技能、规划和文档以 [Apache License 2.0](LICENSE) 发布。示例素材单独授权，大部分是 CC BY 4.0，见 [examples/MEDIA-LICENSE.md](examples/MEDIA-LICENSE.md)。ChatCut 和 Viral Video Cloner 是 ChatCut 的商标，见 [TRADEMARK.md](TRADEMARK.md)。

<p align="center"><sub>由 <a href="https://chatcut.io/zh/?utm_source=github&utm_medium=readme&utm_campaign=oss_viral_cloner&utm_content=footer_zh">ChatCut</a> 出品：能让 AI 助手直接上手剪辑的 AI 视频编辑器。</sub></p>
