# soul2-prompt

**One line in Korean or English, and you get an editorial-grade prompt.** A prompting skill for Higgsfield Soul 2.0.

- Type `Make me a Soul shot. A rainy night outside a convenience store.` — that's the whole interface.
- Location, subject, wardrobe, lighting and color palette are all decided for you. The skill does not interrogate you.
- You get three things back: **a settings label, a full English prompt (typically 1,200–2,200 characters), and a translation.**

![soul2-prompt demo — from one line of input to finished images](docs/demo-v2.gif)

<sub>▶ [Higher quality video (mp4)](docs/demo-v2.mp4) · The English prompt scrolling on screen is the real, unedited output that produced that photograph.</sub>

<br>

## ⬇️ Download

### **[👉 Get the latest release](../../releases/latest)**

Grab the `.skill` file from that page. **A `.zip` with identical contents is attached too** — pick that one if Claude's upload dialog won't show `.skill`. (Or skip the download entirely — see below.)

<br>

## Install

### The easy way: just ask your AI

Paste this one line into whatever agent you already use (Claude Code, Codex, Claude with Chrome, …):

```
https://github.com/promptwhat/promptwhat-soul2-skill  install this skill
```

Using its browser tool, the agent opens the repo, fetches the latest release and puts it where it belongs. **You can stop reading here.**

<br>

<details>
<summary><b>Prefer to do it by hand? (expand)</b></summary>

<br>

**Claude**

1. First enable **code execution** under **Settings → Capabilities**.
   *Without it the Skills menu will not appear at all.*
2. Go to **Customize → Skills** ([claude.ai/customize/skills](https://claude.ai/customize/skills)).
3. **+** → **Create skill** → **Upload a skill**
4. Upload the `.skill` file.

**Codex**

- Fastest: hand the repo URL above to `$skill-installer`.
- By hand: unzip the `.skill` and drop the `soul2-prompt-public` folder into `~/.codex/skills/` (`~/.agents/skills/` works too). It then triggers on its own — no need to point at it each time.

**Any other agent**

Unzip it, drop `soul2-prompt-public` into your working directory, and tell the agent: **"Read soul2-prompt-public/SKILL.md all the way through, then write Soul prompts by those rules."**

</details>

<br>

## How to use it

```
Make me a Soul shot. A rainy night outside a convenience store.
```
```
Make me a Soul shot. A summer night at an amusement park, crisp and cool — a set of 6.
```
```
Make me a Soul shot.
```
> The third one works too. With nothing to go on, the skill invents the concept itself.

<br>

## Not sure what to type?

The first wall after installing is knowing what to say. Every common phrase sits on one page.

### **[👉 Phrase cheat sheet](docs/명령어-모음.md)** (Korean)

Nine short sections. Don't read them all, just find the one you need.

| What you want | Where |
|---|---|
| Your first single image | 1. Getting started |
| A multi-image set | 2. Multiple images |
| Change the subject or framing | 3~4 |
| Change the preset and colors | 5~7 |
| Fix what came back | 8. Fixing results |
| What to copy into Higgsfield | 9. Using the output |

Each section is a table. Copy the left column as-is. Nothing to memorize.

<br>

## What it can do

![12 concepts, three results each](docs/gallery.jpg)

**Twelve concepts, three shots each — 36 images.** Everyday snapshots like a neighborhood stationery shop, surreal scenes like a flooded corridor or a room-sized teacup, male subjects, close-ups. Same skill throughout. **Only one line of input changed.**

<br>

![A set of six with consistent subject and wardrobe](docs/demo-set.jpg)

Add `as a set` and you get several images at once. **The default is one person in one outfit** — the identity and wardrobe sentences are carried over verbatim to every shot, and only the scene and framing change. The palette travels with them as fixed HEX values.

<sub>Want the face tighter? Two options. **Generating the first shot and attaching it as a reference image** costs nothing extra and raises the likeness, but per Higgsfield it drifts as the count grows. **For real consistency across many shots and sessions, use Higgsfield's Soul ID (Character tab)** — train a person on 20+ photos once, then pick them at generation time. Availability depends on your plan. The skill explains both at the end of its output.</sub>

<sub>Want a lookbook where each shot is a different person instead? Add `with different people`.</sub>

<br>

## Real prompts, not samples

**[→ Three complete examples: input line, full prompt, resulting photo](docs/examples.md)**

Every English prompt in that document is the exact text that produced the photograph shown beside it.

<br>

## What it is built on

Every rule comes from a full analysis of **all 136 generations** in Higgsfield's official **Soul Carousels** project. Anything not confirmed by that survey is marked `[제안값]` (proposed value) inside the document.

The package also ships `golden-prompts.md` — 12 measured originals, unedited.

<br>

## Removing it

**Delete one folder and it is gone.** This skill creates no other files, registers with no service, and schedules no background tasks.

- **Claude** — `Customize → Skills`, select the skill, toggle it off, then **Delete** from the `…` menu
- **Codex and other agents** — delete the `soul2-prompt-public` folder you dropped in

Discard the downloaded `.skill` file too and nothing is left behind.

<br>

## Credits

**promptwhat** — Instagram [@prompt_what](https://instagram.com/prompt_what)

License: [MIT](LICENSE)

<sub>MIT covers **the skill itself** — its rules, structure and commentary. The twelve English source prompts bundled in `golden-prompts.md` are generations from Higgsfield's official account ([@skxqw](https://higgsfield.ai/@skxqw/projects/soul-carousels)), included as reference material for gauging prompt density; they are **not** covered by MIT and their rights remain with the original author.</sub>

<sub>Korean README: [README.md](README.md)</sub>
