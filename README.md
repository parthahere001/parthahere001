<!--
  github.com/parthahere001/parthahere001 — profile README

  ONE SETUP STEP: add .github/workflows/snake.yml to THIS repo in the same commit.
  The snake image near the bottom fills in ~1 min after you push. Everything else
  renders instantly.
-->

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:1A1B27,50:7F5AF0,100:38BDAE&height=220&section=header&text=Partha%20Banerjee&fontSize=52&fontColor=ffffff&animation=fadeIn&desc=Consumer%20apps%20solo%20%C2%B7%20Payments%20infrastructure%20by%20day&descSize=18&descAlignY=62" alt="Partha Banerjee" />

<div align="center">

<img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=600&size=22&duration=3200&pause=900&color=BF91F3&center=true&vCenter=true&width=780&height=60&lines=5%2C000%2B+installs.+Zero+spent+on+ads.;Word-by-word+lyrics%2C+dead-reckoned+to+the+beat.;Consumer-powered+healthcare+for+gig+workers.;Agents+that+ship+finished+work%2C+not+demos." alt="5,000+ installs. Zero spent on ads." />

<p>
  <a href="https://play.google.com/store/apps/details?id=com.exodus.lyricglow"><img src="https://img.shields.io/badge/Play%20Store-5%2C000%2B%20installs-BF91F3?style=for-the-badge&logo=googleplay&logoColor=white&labelColor=1A1B27" alt="LyricGlow on Google Play — 5,000+ installs" /></a>
  <img src="https://img.shields.io/badge/Paid%20ads-zero-38BDAE?style=for-the-badge&labelColor=1A1B27" alt="Zero paid ads" />
  <a href="https://github.com/search?q=is%3Apr+author%3Aparthahere001+is%3Amerged&type=pullrequests"><img src="https://img.shields.io/badge/Pull%20requests-17%20of%2020%20merged-BF91F3?style=for-the-badge&logo=github&logoColor=white&labelColor=1A1B27" alt="17 of 20 pull requests merged" /></a>
</p>

</div>

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:1A1B27,50:7F5AF0,100:38BDAE&height=3&section=header" alt="" />

Android in Kotlin. PureScript on a checkout page millions of people pay through. Agent systems that produce finished artifacts instead of demos.

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:1A1B27,50:7F5AF0,100:38BDAE&height=3&section=header" alt="" />

## LyricGlow

**Word-by-word lyrics on your Android lock screen.** Any music player, any phone.

> [!TIP]
> **1,000+ installs in month one. 5,000+ today. Zero spent on ads.**

23,491 lines of Kotlin, 100% Compose, four months, one developer.

```mermaid
flowchart LR
  P["Any player"] --> L["One MediaSession listener"]
  L --> A["Anchor to monotonic clock"]
  A --> D["Dead-reckon at 30 Hz"]
  D --> S["Lock screen · AOD · widgets"]
```

<details>
<summary><b>How it stays in sync</b></summary>

<br/>

- **Dead-reckoned, not polled.** Position is anchored to `SystemClock.elapsedRealtime()` and extrapolated every frame — exact sync without hammering the player.
- **Word timing is modelled.** LRC gives only line stamps, so sing-time is estimated per character, clamped against the real line window, and scaled so the last word lights *on* the beat.
- **Widgets reuse the lock screen's draw code** through an off-screen `CanvasDrawScope` — no Compose runtime, just a bitmap.
- **Privacy is in the manifest, not the policy.** No `QUERY_ALL_PACKAGES`, no storage or media permissions at all.

</details>

<p>
  <a href="https://play.google.com/store/apps/details?id=com.exodus.lyricglow"><img src="https://img.shields.io/badge/Get%20it%20on%20Google%20Play-BF91F3?style=for-the-badge&logo=googleplay&logoColor=1A1B27" alt="Get it on Google Play" /></a>
  <a href="https://lyricglow.com"><img src="https://custom-icon-badges.demolab.com/badge/lyricglow.com-38BDAE?style=for-the-badge&logo=link-external&logoColor=1A1B27" alt="lyricglow.com" /></a>
</p>

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:1A1B27,50:7F5AF0,100:38BDAE&height=3&section=header" alt="" />

<!--
  NAMING NOTE — read once, then delete.
  "Aarokya" is unannounced Juspay work with no public footprint, so this page would
  be its first public mention. Worth a quick check with your team before pushing.
  To stay anonymous: drop the name from this heading and from the typing banner
  above, and the section still reads fine as "Building now".

  Everything here is intentionally limited to Aarokya's own positioning language —
  no stack, no architecture, no scale numbers.
-->

## Building now: Aarokya

**Consumer-powered healthcare for gig workers.** My main focus at Juspay right now.

Closed source, so this is deliberately all the detail there is — happy to talk about the engineering in a conversation.

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:1A1B27,50:7F5AF0,100:38BDAE&height=3&section=header" alt="" />

## An agent pipeline that makes videos while I sleep

A topic goes in, an upload-ready 1080p video comes out — researched, scripted, narrated, shot, cut and tagged. 26,543 lines of Python, 15 stages, one command.

<details>
<summary><b>The hard parts</b></summary>

<br/>

- **No API key anywhere.** Every model call shells out to the Claude Code CLI headless, with a JSON schema as the output contract.
- **Narration never leaves the machine.** Kokoro-82M runs locally on Apple Silicon under a prosody planner that derives rate and pitch from the scene's mood.
- **Relevant, or nothing.** Footage selection may return nothing; an empty pick becomes a typographic card, because a card beats misleading footage.
- **Every run stops at a human gate** with a claims table and source URLs. The editorial pass is a designed step.

</details>

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:1A1B27,50:7F5AF0,100:38BDAE&height=3&section=header" alt="" />

## Also at Juspay

I build features on **[Payment Page](https://docs.juspay.in/hyper-checkout/web)** — Juspay's hosted checkout, used by thousands of merchants and reaching millions of people paying for things.

It's written in **PureScript**. Strict purely-functional types, in production, on the checkout screen where a bug is somebody's money. Juspay open-sourced the framework underneath it as [purescript-presto](https://github.com/juspay/purescript-presto).

<sub>The repo is private, so there's nothing to link. PureScript, Payment Page and the scale figures are all from Juspay's public docs and marketing.</sub>

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:1A1B27,50:7F5AF0,100:38BDAE&height=3&section=header" alt="" />

## Open source you can read

| Repo | What it is |
| :--- | :--- |
| [**exolock**](https://github.com/parthahere001/exolock) | Android app locker. PBKDF2-HMAC-SHA256 at 120,000 iterations, constant-time compare, nothing in plaintext. 41 Kotlin files, zero Java. |
| [**Learner**](https://github.com/parthahere001/Learner) | MIT-licensed Django LMS, written because the one my college used was buggy. |
| [**Local-Music-Player**](https://github.com/parthahere001/Local-Music-Player) | Self-hosted FastAPI music server — ID3 tags, embedded cover art, playlists. |
| [**LottoBit**](https://github.com/parthahere001/LottoBit) | USD-priced ETH lottery in Solidity, tested three ways: mainnet fork, mocks, testnet. |

**20 pull requests authored, 17 merged — 15 into other people's repositories.**

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:1A1B27,50:7F5AF0,100:38BDAE&height=3&section=header" alt="" />

## Stack

<div align="center">

<p>
  <img src="https://img.shields.io/badge/PureScript-1A1B27?style=for-the-badge&logo=purescript&logoColor=BF91F3&labelColor=1A1B27" alt="PureScript" />
  <img src="https://img.shields.io/badge/Jetpack%20Compose-1A1B27?style=for-the-badge&logo=jetpackcompose&logoColor=4285F4&labelColor=1A1B27" alt="Jetpack Compose" />
  <img src="https://img.shields.io/badge/Claude%20Code-1A1B27?style=for-the-badge&logo=claude&logoColor=D97757&labelColor=1A1B27" alt="Claude Code" />
</p>

<a href="https://skillicons.dev"><img src="https://skillicons.dev/icons?i=kotlin,androidstudio,gradle,react,typescript,dart,flutter,firebase&theme=dark" alt="Mobile" /></a>
<a href="https://skillicons.dev"><img src="https://skillicons.dev/icons?i=python,django,fastapi,go,postgres,redis,docker,linux&theme=dark" alt="Backend" /></a>

<kbd>Coroutines</kbd> <kbd>Solidity</kbd> <kbd>ffmpeg</kbd> <kbd>GitHub Actions</kbd>

</div>

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:1A1B27,50:7F5AF0,100:38BDAE&height=3&section=header" alt="" />

<div align="center">

<!--
  Stats card points at a COMMUNITY MIRROR on purpose: the canonical
  github-readme-stats.vercel.app is 503 DEPLOYMENT_PAUSED, and both
  github-profile-trophy and github-readme-activity-graph are 402 (disabled).
  If this mirror dies too: fork anuraghazra/github-readme-stats -> import to
  Vercel -> swap the host below.
-->
<img height="180" src="https://github-readme-stats-salesp07.vercel.app/api?username=parthahere001&show_icons=true&count_private=true&include_all_commits=true&hide_border=true&theme=tokyonight&title_color=BF91F3&icon_color=38BDAE&text_color=A9B1D6&bg_color=1A1B27" alt="GitHub stats" />
<img height="180" src="https://streak-stats.demolab.com/?user=parthahere001&theme=tokyonight&hide_border=true&border_radius=10&background=1A1B27&ring=BF91F3&fire=BF91F3&currStreakLabel=38BDAE" alt="GitHub streak" />

</div>

<details>
<summary><b>More stats, and why the byte counts lie</b></summary>

<br/>

<div align="center">

<img width="100%" src="https://github-profile-summary-cards.vercel.app/api/cards/profile-details?username=parthahere001&theme=tokyonight" alt="Profile summary" />
<img height="200" src="https://github-profile-summary-cards.vercel.app/api/cards/repos-per-language?username=parthahere001&theme=tokyonight" alt="Top languages" />
<img height="200" src="https://github-profile-summary-cards.vercel.app/api/cards/most-commit-language?username=parthahere001&theme=tokyonight" alt="Most-committed language" />

</div>

<br/>

Three old repos of mine committed their virtualenvs, which alone account for tens of megabytes of "Python". Measured on code I actually wrote, my public GitHub is roughly **33% Kotlin, 19% JavaScript, 15% CSS, 10% Python** — the C and C++ entirely auto-generated Flutter desktop scaffolding.

</details>

<!--
  Snake is generated by .github/workflows/snake.yml in THIS repo.
  Blank until the workflow runs (~1 min after push). Delete this block to skip it.
-->
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/parthahere001/parthahere001/output/github-snake-purple.svg" />
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/parthahere001/parthahere001/output/github-contribution-grid-snake.svg" />
  <img width="100%" alt="Contribution snake" src="https://raw.githubusercontent.com/parthahere001/parthahere001/output/github-contribution-grid-snake.svg" />
</picture>

<img width="100%" src="https://capsule-render.vercel.app/api?type=rect&color=0:1A1B27,50:7F5AF0,100:38BDAE&height=3&section=header" alt="" />

<p align="center">
  <a href="https://linkedin.com/in/partha-banerjee-5a134b234/"><img src="https://custom-icon-badges.demolab.com/badge/LinkedIn-1A1B27?style=for-the-badge&logo=linkedin&logoColor=0A66C2&labelColor=1A1B27" alt="LinkedIn" /></a>&nbsp;
  <a href="https://dev.to/parthahere001"><img src="https://custom-icon-badges.demolab.com/badge/Dev.to-1A1B27?style=for-the-badge&logo=dev.to&logoColor=white&labelColor=1A1B27" alt="Dev.to" /></a>&nbsp;
  <a href="mailto:parthahere001@gmail.com"><img src="https://custom-icon-badges.demolab.com/badge/Email-1A1B27?style=for-the-badge&logo=gmail&logoColor=EA4335&labelColor=1A1B27" alt="Email" /></a>&nbsp;
  <a href="https://github.com/parthahere001?tab=followers"><img src="https://img.shields.io/github/followers/parthahere001?style=for-the-badge&color=BF91F3&labelColor=1A1B27&logo=github&logoColor=white&label=FOLLOW" alt="Follow" /></a>&nbsp;
  <img src="https://komarev.com/ghpvc/?username=parthahere001&label=PROFILE+VIEWS&color=BF91F3&style=for-the-badge" alt="Profile views" />
</p>

<div align="center">

**Building something that has to be correct at 3 a.m.? Let's talk.**

</div>

<img width="100%" src="https://capsule-render.vercel.app/api?type=waving&color=0:38BDAE,50:7F5AF0,100:1A1B27&height=120&section=footer" alt="" />
