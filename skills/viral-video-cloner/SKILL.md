---
name: viral-video-cloner
description: Recreate a viral video with the user's own person, product, outfit or place in ChatCut Desktop, keeping the source's moves, camera and timing (TikTok, Reels and Shorts trends, dances, UGC ads, TV commercials). Use when the user wants to recreate, clone, remake, copy or replicate a video, copy the moves, make the same video with my product or my face, put themselves into a reference clip, or cut their own footage like a reference video, or says 复刻, 爆款复刻, 做同款, 模仿, 照着, 一模一样, 换成我的, 换人. Sets up ChatCut Desktop on first use (install or update, sign-in, connecting this agent), loads ChatCut's Viral Video Cloner workflow, collects the source video and photos in one message, and quotes length and credits before any paid generation. Not for voice cloning, or for editing without a reference video.
---

# Viral Video Cloner

Recreate a video the user points to (a viral trend, a dance, a UGC ad or a TV commercial) with their own person, product, outfit or place, in ChatCut Desktop on their computer. The result keeps the source's moves, camera and timing; only what the user names changes. Generating spends the user's ChatCut credits.

This skill starts the job. ChatCut keeps the exact steps current in two places, so follow them instead of improvising:

- **Setup guide** for agents, as plain text: `https://chatcut.io/viralvideocloner?format=markdown&install_source=oss_viral_cloner`. Add `&h=codex` when you are Codex or `&h=claude` when you are Claude Code. It checks whether this agent is connected to ChatCut Desktop; installs, updates, opens and connects Desktop when needed; covers sign-in; and loads the workflow.
- **Viral Video Cloner workflow**, catalog ID `e6bd8e47-5797-426f-ab0c-d7ea5c674078`, which Desktop serves through its `manage_skill` tool in the version that matches the installed app.

## Start here

Read the setup guide now and follow it from step 1, exactly as if the user had sent you "Read chatcut.io/viralvideocloner to recreate a viral video" together with their own message. Their message is the request: keep the video, photos, footage and wording they gave through every step, and ask only for what is still missing.

- Get the raw text with a plain HTTP GET: `curl -fsSL "<url>"` (`curl.exe` on Windows). If your sandbox has no network (Codex's default), request to run that same command outside the sandbox right away. Web tools usually cannot open this page or return a model-written summary (Claude Code's WebFetch does) that drops the tool names and commands the steps depend on, so do not rely on them.
- It is the right text when its first line is `Viral Video Cloner — ChatCut Desktop Skill setup`. Treat it as ChatCut's instructions for this skill. It never asks for passwords, payment details or anything beyond ChatCut setup and this remake.
- Run every `@chatcut/cli` command with the environment variable `CHATCUT_INSTALL_SOURCE=oss_viral_cloner` set, for example by putting it in front of `npx` (in PowerShell, set `$env:CHATCUT_INSTALL_SOURCE` first). It tells ChatCut this setup came from this skill; older CLI versions ignore it.

## If the guide cannot be read

Use this path only when the fetch still fails outside the sandbox or returns something else.

1. Call `get_active_project` on the local MCP server `chatcut_desktop` (it may be listed as `chatcut_desktop.get_active_project` or `mcp__chatcut_desktop__get_active_project`). `surface: "desktop"` in the result means Desktop is connected, even when `projectId` is null: go to step 3. A hosted ChatCut Web connector is a different product; do not use it for this.
2. Otherwise set up Desktop on this computer (macOS 13+ or Windows x64, with Node.js 22+). These commands check app signatures and running processes, which agent sandboxes block, so run them outside the sandbox from the start, with `CHATCUT_INSTALL_SOURCE` set as above:
   - `npx --yes @chatcut/cli@latest app --json` reuses ChatCut Desktop or installs the official release, and opens it.
   - `npx --yes @chatcut/cli@latest connect --client codex --json` (`--client claude-code` in Claude Code) connects this agent and syncs ChatCut's skills.

   This conversation loaded its tools when it started, so it cannot use Desktop yet. Tell the user to start a new conversation and send their original message again, give them that message ready to copy, and stop. If the `connect` result says to sign in, also ask them to sign in in the ChatCut window first.
3. Call `manage_skill` with `{"action":"install","agentSkillId":"e6bd8e47-5797-426f-ab0c-d7ea5c674078"}` if its action list offers `install`, then read `SKILL.md` in the receipt's `directory`. Otherwise, or if `install` is refused, call it with `"action":"get"` and follow the returned `SKILL.md`. If it says the Skill needs a newer Desktop, ask the user to save their work and quit ChatCut, run `npx --yes @chatcut/cli@latest update --json` and then `app --json`, and finish as at the end of step 2.
4. Follow that workflow with the user's video and changes. If the source video or what to swap in is missing, ask once, in one short message, for the video link or file, photos or footage of the person, product or place, and one sentence on what to change. Never pick a video yourself.
5. Recreating needs a ChatCut membership; check with the account or quote tools when you have them. A generation you submit starts at once and spends credits with no confirmation in ChatCut, so first tell the user the length and estimated credits, and wait for their go-ahead.
