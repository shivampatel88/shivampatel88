<div align="center">

<!-- HEADER — custom gradient banner, not the overused venom template -->
<img width="100%" src="https://capsule-render.vercel.app/api?type=cylinder&color=0:0d1117,40:0d1b2a,70:0a2540,100:163356&height=280&section=header&text=SHIVAM%20PATEL&fontSize=65&fontColor=58a6ff&animation=fadeIn&desc=Systems%20Thinker%20·%20Full-Stack%20Engineer%20·%20Curiosity-Driven%20Builder&descSize=16&descColor=79c0ff&descAlignY=68&fontAlignY=40&stroke=1c4580&strokeWidth=2" />

</div>

<div align="center">

<br/>

<!-- Typing SVG — 2 lines, punchy -->
<a href="https://github.com/shivampatel88">
  <img src="https://readme-typing-svg.demolab.com?font=JetBrains+Mono&weight=700&size=22&duration=3500&pause=1200&color=58A6FF&center=true&vCenter=true&multiline=false&repeat=true&width=700&lines=Building+things+to+understand+how+they+work.;Not+stopping+until+the+hard+parts+make+sense.;If+something+annoys+me+enough%2C+I+build+the+fix." alt="Typing SVG" />
</a>

<br/><br/>

<!-- Social badges -->
<a href="https://linkedin.com/in/shivampatel77">
  <img src="https://img.shields.io/badge/LinkedIn-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white"/>
</a>&nbsp;
<a href="mailto:shivamhp3084@gmail.com">
  <img src="https://img.shields.io/badge/Gmail-EA4335?style=for-the-badge&logo=gmail&logoColor=white"/>
</a>&nbsp;
<a href="https://github.com/shivampatel88">
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white"/>
</a>

<br/><br/>

<!-- Thin separator — ONE time only, not repeated -->
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">

</div>

<br/>

<!-- ══════════════════════════════════════════════════════════ -->
<!--  WHO AM I — terminal YAML, kept because it genuinely rocks -->
<!-- ══════════════════════════════════════════════════════════ -->

<img src="https://media2.giphy.com/media/QssGEmpkyEOhBCb7e1/giphy.gif?cid=ecf05e47a0n3gi1bfqntqmob8g9aid1oyj2wr3ds3mg700bl&rid=giphy.gif" width="26px" align="left">

## &nbsp;`$ whoami`

<img align="right" src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Gear.png" alt="Gear" width="110" />

```yaml
name: Shivam Patel
location: Vadodara, Gujarat, India
education: B.Tech CS — ITM SLS Baroda University (2022–2026) · CGPA 8.75

stack: MERN · Redis · Docker · BullMQ · RAG Pipelines · SSE

mindset: >
  I reverse-engineer production systems to understand them from the inside out.
  Atomic transactions, async job queues, RAG retrieval, race conditions —
  I don't move on until the internals click. Every project I've built started
  as a real problem I was personally frustrated with.

currently:
  - Open to full-stack developer roles (fresher — production-grade thinking from day one)
  - Exploring distributed systems and AI-native architectures
  - Building things no one asked me to because they annoyed me enough
```

<br/>

<!-- ══════════════════════════════════════════════════════════ -->
<!--  METRICS SHOWCASE — this is the section that was missing   -->
<!-- ══════════════════════════════════════════════════════════ -->

## &nbsp;`📐 By The Numbers`

<div align="center">

<table>
<tr>
<td align="center" width="200">
  <img src="https://img.shields.io/badge/80%25-perceived_wait_time_↓-58a6ff?style=for-the-badge&labelColor=0d1117"/>
  <br/><sub>SSE streaming — StudyBuddy</sub>
</td>
<td align="center" width="200">
  <img src="https://img.shields.io/badge/150ms→5ms-feed_latency-58a6ff?style=for-the-badge&labelColor=0d1117"/>
  <br/><sub>Redis caching — Blogsite</sub>
</td>
<td align="center" width="200">
  <img src="https://img.shields.io/badge/100%25-transaction_integrity-58a6ff?style=for-the-badge&labelColor=0d1117"/>
  <br/><sub>Atomic + idempotency — Rupay</sub>
</td>
<td align="center" width="200">
  <img src="https://img.shields.io/badge/350MB→95MB-docker_image-58a6ff?style=for-the-badge&labelColor=0d1117"/>
  <br/><sub>Multi-stage Nginx build — Blogsite</sub>
</td>
</tr>
</table>

</div>

<br/>

<!-- ══════════════════════════════════════════════════════════ -->
<!--  THINKING IN SYSTEMS — ASCII architecture block           -->
<!--  This is what makes a senior engineer lean forward        -->
<!-- ══════════════════════════════════════════════════════════ -->

## &nbsp;`🧠 How I Think About Systems`

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    StudyBuddy — RAG Architecture                         │
├─────────────────────────────────────────────────────────────────────────┤
│                                                                          │
│  PDF Upload                                                              │
│     │                                                                    │
│     ▼                                                                    │
│  [ Express API ] ──── 202 Accepted ────────────────────► [ Client ]     │
│     │                        ↑ SSE stream (chunk-by-chunk)              │
│     ▼                                                                    │
│  [ Redis / BullMQ Queue ]                                                │
│     │                                                                    │
│     ▼                                                                    │
│  [ BullMQ Worker ]                                                       │
│     ├── Semantic chunking                                                │
│     ├── Gemini embedding generation (3072-dim)                           │
│     └── MongoDB Atlas upsert                                             │
│                                                                          │
│  Query Flow:                                                             │
│  [ User Question ]                                                       │
│     ├── Vector Search (HNSW cosine) ──────┐                             │
│     ├── BM25 Keyword Search ──────────────┼──► RRF Fusion               │
│     │                                     │       │                      │
│     └─────────────────────────────────────┘       ▼                     │
│                                            [ Top 18 Candidates ]         │
│                                                    │                     │
│                                            Gemini Re-rank → Top 3        │
│                                                    │                     │
│                                            Cited Answer Generation       │
│                                                    │                     │
│                                         SHA-256 Hash Cache Check         │
│                                         (CDN-like deduplication)         │
└─────────────────────────────────────────────────────────────────────────┘
```

<br/>

<!-- ══════════════════════════════════════════════════════════ -->
<!--  TECH STACK                                               -->
<!-- ══════════════════════════════════════════════════════════ -->

<img src="https://media.giphy.com/media/iY8CRBdQXODJSCERIr/giphy.gif" width="26px" align="left">

## &nbsp;`⚙️ Tech Arsenal`

<div align="center">

<a href="https://skillicons.dev">
  <img src="https://skillicons.dev/icons?i=js,ts,react,nodejs,express,mongodb,redis,docker,nginx,github,python,cpp,tailwind,vite&perline=7&theme=dark" alt="Tech Stack" />
</a>

<br/><br/>

<!-- Languages -->
<img src="https://img.shields.io/badge/JavaScript-0d1117?style=for-the-badge&logo=javascript&logoColor=F7DF1E"/>
<img src="https://img.shields.io/badge/TypeScript-0d1117?style=for-the-badge&logo=typescript&logoColor=3178C6"/>
<img src="https://img.shields.io/badge/Python-0d1117?style=for-the-badge&logo=python&logoColor=3776AB"/>
<img src="https://img.shields.io/badge/C++-0d1117?style=for-the-badge&logo=cplusplus&logoColor=00599C"/>

<br/>

<!-- Frontend -->
<img src="https://img.shields.io/badge/React.js-0d1117?style=for-the-badge&logo=react&logoColor=61DAFB"/>
<img src="https://img.shields.io/badge/Tailwind_CSS-0d1117?style=for-the-badge&logo=tailwindcss&logoColor=06B6D4"/>
<img src="https://img.shields.io/badge/TanStack_Query-0d1117?style=for-the-badge&logo=reactquery&logoColor=FF4154"/>
<img src="https://img.shields.io/badge/Framer_Motion-0d1117?style=for-the-badge&logo=framer&logoColor=0055FF"/>

<br/>

<!-- Backend -->
<img src="https://img.shields.io/badge/Node.js-0d1117?style=for-the-badge&logo=nodedotjs&logoColor=339933"/>
<img src="https://img.shields.io/badge/Express.js-0d1117?style=for-the-badge&logo=express&logoColor=FFFFFF"/>
<img src="https://img.shields.io/badge/BullMQ-0d1117?style=for-the-badge&logoColor=E63946"/>
<img src="https://img.shields.io/badge/Zod-0d1117?style=for-the-badge&logo=zod&logoColor=3E67B1"/>
<img src="https://img.shields.io/badge/OAuth_2.0-0d1117?style=for-the-badge&logoColor=EB5424"/>

<br/>

<!-- Databases -->
<img src="https://img.shields.io/badge/MongoDB_Atlas-0d1117?style=for-the-badge&logo=mongodb&logoColor=47A248"/>
<img src="https://img.shields.io/badge/Redis-0d1117?style=for-the-badge&logo=redis&logoColor=DC382D"/>
<img src="https://img.shields.io/badge/MySQL-0d1117?style=for-the-badge&logo=mysql&logoColor=4479A1"/>
<img src="https://img.shields.io/badge/Vector_DB-0d1117?style=for-the-badge&logoColor=8B5CF6"/>

<br/>

<!-- DevOps & AI -->
<img src="https://img.shields.io/badge/Docker-0d1117?style=for-the-badge&logo=docker&logoColor=2496ED"/>
<img src="https://img.shields.io/badge/Nginx-0d1117?style=for-the-badge&logo=nginx&logoColor=009639"/>
<img src="https://img.shields.io/badge/GitHub_Actions-0d1117?style=for-the-badge&logo=githubactions&logoColor=2088FF"/>
<img src="https://img.shields.io/badge/Playwright-0d1117?style=for-the-badge&logo=playwright&logoColor=2EAD33"/>
<img src="https://img.shields.io/badge/RAG_Pipelines-0d1117?style=for-the-badge&logoColor=FF6F61"/>
<img src="https://img.shields.io/badge/Gemini_API-0d1117?style=for-the-badge&logo=googlegemini&logoColor=8E75B2"/>

</div>

<br/>

<!-- ══════════════════════════════════════════════════════════ -->
<!--  PROJECTS                                                  -->
<!-- ══════════════════════════════════════════════════════════ -->

<img src="https://media.giphy.com/media/ln7z2eWriiQAllfVcn/giphy.gif" width="26px" align="left">

## &nbsp;`🚀 What I've Built`

<!-- ─── STUDYBUDDY — FEATURED ─── -->

<div align="center">
  <img src="https://img.shields.io/badge/⭐_FEATURED_PROJECT-1c4580?style=for-the-badge&logoColor=58a6ff"/>
</div>

<br/>

<table>
<tr>
<td>

### <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Books.png" width="24"/> &nbsp;[StudyBuddy — AI Study Platform](https://github.com/shivampatel88/AI-buddy)

> _"200-page PDFs were killing my motivation to study. So I built the tool I wished existed."_

<div align="center">
<img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=000"/>
<img src="https://img.shields.io/badge/Node.js-339933?style=flat-square&logo=nodedotjs&logoColor=fff"/>
<img src="https://img.shields.io/badge/MongoDB_Vector_Search-47A248?style=flat-square&logo=mongodb&logoColor=fff"/>
<img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=fff"/>
<img src="https://img.shields.io/badge/BullMQ-E63946?style=flat-square"/>
<img src="https://img.shields.io/badge/Gemini_API-8E75B2?style=flat-square&logo=googlegemini&logoColor=fff"/>
<img src="https://img.shields.io/badge/SSE_Streaming-FF6F61?style=flat-square"/>
<img src="https://img.shields.io/badge/Docker_Compose-2496ED?style=flat-square&logo=docker&logoColor=fff"/>
</div>

<br/>

| Layer              | Engineering Decision                                                                                      |
| :----------------- | :-------------------------------------------------------------------------------------------------------- |
| 🔬 **Retrieval**   | Hybrid Vector (HNSW) + BM25 fused via **Reciprocal Rank Fusion** → Gemini re-ranking → top 3 cited chunks |
| ⚡ **Async Jobs**  | BullMQ worker handles chunking + embeddings — server returns **202 immediately**, never blocks            |
| 🌊 **Streaming**   | SSE chunk-by-chunk delivery → **80% reduction** in perceived wait time                                    |
| 🔒 **Caching**     | SHA-256 content hash → two students with the same PDF share one Gemini response _(CDN deduplication)_     |
| 🏁 **Concurrency** | XP race condition fixed with **MongoDB aggregation pipeline write** — zero read-modify-write window       |
| 💾 **Resilience**  | Dual-state reconciliation between Redis + MongoDB — crash-safe job recovery with stale detection          |

</td>
</tr>
</table>

<br/>

<!-- ─── RUPAY + BLOGSITE side by side ─── -->

<table>
<tr>
<td width="50%" valign="top">

### <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Money%20Bag.png" width="22"/> &nbsp;[Rupay — Digital Wallet](https://github.com/shivampatel88/Rupay_tm)

> _"Curious how Paytm prevents money from disappearing in a race condition. Built the answer."_

🔗 **[rupay-tm.vercel.app](https://rupay-tm.vercel.app)**

<div align="center">
<img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=000"/>
<img src="https://img.shields.io/badge/MongoDB-47A248?style=flat-square&logo=mongodb&logoColor=fff"/>
<img src="https://img.shields.io/badge/Razorpay-0C2451?style=flat-square&logo=razorpay&logoColor=fff"/>
<img src="https://img.shields.io/badge/JWT-000000?style=flat-square&logo=jsonwebtokens&logoColor=fff"/>
</div>

<br/>

- ⚛️ **Atomic MongoDB transactions** — debit & credit as one unit
- 🛡️ **2-layer idempotency** — pre-flight check + `$ne` atomic guard → concurrent duplicates = guaranteed safe no-op
- 🔐 **OTP inside the transaction** — server-enforced, cannot be bypassed client-side
- 🔑 **Token family + nonce replay detection** — compromised token wipes all sessions instantly
- 📊 **100% transfer success rate** — zero race conditions

</td>
<td width="50%" valign="top">

### <img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Memo.png" width="22"/> &nbsp;[Blogsite — Full-Stack Platform](https://github.com/shivampatel88/Blogsite)

> _"Built dev.to myself — from scratch, with real production constraints and no shortcuts."_

<div align="center">
<img src="https://img.shields.io/badge/React-61DAFB?style=flat-square&logo=react&logoColor=000"/>
<img src="https://img.shields.io/badge/Redis-DC382D?style=flat-square&logo=redis&logoColor=fff"/>
<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=docker&logoColor=fff"/>
<img src="https://img.shields.io/badge/Nginx-009639?style=flat-square&logo=nginx&logoColor=fff"/>
<img src="https://img.shields.io/badge/Playwright-2EAD33?style=flat-square&logo=playwright&logoColor=fff"/>
</div>

<br/>

- ⚡ Redis caching → feed latency **150ms → ~5ms**
- 🔒 JWT blacklisting in Redis — TTL-based auto-cleanup on logout
- 📦 Multi-stage Nginx build → Docker image **350MB → 95MB**
- 🤖 AI Refine: one Gemini call, returns refined HTML + diff — half the token cost
- 🧪 Playwright E2E test suite — deployment confidence without babysitting

</td>
</tr>
</table>

<br/>

<!-- ─── CHROME EXTENSION — upgraded wildcard card ─── -->

<table>
<tr>
<td>

### 🔥 &nbsp;Claude Chat Tracker — Chrome Extension &nbsp;`[personal tool]`

> _"I use multiple Claude accounts because of free-tier limits. Kept losing track of which chat was where. Built the fix in a weekend. Zero frameworks. Use it every day."_

<div align="center">
<img src="https://img.shields.io/badge/Vanilla_JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=000"/>
<img src="https://img.shields.io/badge/Chrome_Extension_API-4285F4?style=flat-square&logo=googlechrome&logoColor=fff"/>
<img src="https://img.shields.io/badge/chrome.storage.sync-34A853?style=flat-square&logo=googlechrome&logoColor=fff"/>
<img src="https://img.shields.io/badge/Content_Scripts-EA4335?style=flat-square&logo=googlechrome&logoColor=fff"/>
</div>

<br/>

```
Content Script              Popup UI                  Sync Layer
─────────────────           ──────────────────        ──────────────────────
Silently watches            Shows all tracked         chrome.storage.sync
claude.ai for chat          chats with search +       keeps chat list in sync
links + account info        filter by account         across devices & profiles
     │                           │                            │
     └───────────────────────────┴────────────────────────────┘
                                 │
                    One-click → opens chat in correct
                    Google account (auto session switch)
```

> **Why this exists here:** _I don't build things for resumes. I build things that solve problems I actually have. This one I use every single day._

</td>
</tr>
</table>

<br/>

<div align="center">
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">
</div>

<!-- ══════════════════════════════════════════════════════════ -->
<!--  EXPERIENCE                                               -->
<!-- ══════════════════════════════════════════════════════════ -->

<br/>

<img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Travel%20and%20places/Office%20Building.png" width="26" align="left">

## &nbsp;`🏢 Experience`

<table>
<tr>
<td>

**Software Developer Intern** &nbsp;·&nbsp; [**Protap Club**](https://protapclub.com), Vadodara &nbsp;·&nbsp; `Jan 2026 – May 2026`

- 🏗️ Architected **multi-tenant school ERP** from scratch — `15 domain modules` · `26 Mongoose models` · strict per-tenant data isolation via **7-layer Express middleware chain**
- 📡 Dual-mode NFC attendance with hardware device auth + teacher overrides · **Socket.io** real-time broadcasts · **Pino** structured logging
- 🚀 Shipped per-tenant feature flags, fee lifecycle management, and full-stack ERP features — directly with the founding team under real production pressure

</td>
</tr>
</table>

<br/>

<div align="center">
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">
</div>

<!-- ══════════════════════════════════════════════════════════ -->
<!--  GITHUB STATS                                             -->
<!-- ══════════════════════════════════════════════════════════ -->

<br/>

<img src="https://media.giphy.com/media/W5eoZHPpUx9sapR0eu/giphy.gif" width="26px" align="left">

## &nbsp;`📊 GitHub Analytics`

<div align="center">

<a href="https://github.com/shivampatel88">
  <img height="175em" src="https://github-readme-stats.vercel.app/api?username=shivampatel88&show_icons=true&theme=tokyonight&hide_border=true&count_private=true&include_all_commits=true&bg_color=0d1117&title_color=58a6ff&icon_color=58a6ff&text_color=c9d1d9&ring_color=58a6ff"/>
</a>&nbsp;
<a href="https://github.com/shivampatel88">
  <img height="175em" src="https://streak-stats.demolab.com/?user=shivampatel88&theme=tokyonight&hide_border=true&background=0D1117&ring=58A6FF&fire=58A6FF&currStreakLabel=58A6FF&sideLabels=C9D1D9&dates=8B949E"/>
</a>

<br/><br/>

<a href="https://github.com/shivampatel88">
  <img src="https://github-readme-stats.vercel.app/api/top-langs/?username=shivampatel88&layout=compact&theme=tokyonight&hide_border=true&langs_count=8&bg_color=0d1117&title_color=58a6ff&text_color=c9d1d9"/>
</a>

<br/><br/>

<a href="https://github.com/shivampatel88">
  <img src="https://github-profile-trophy.vercel.app/?username=shivampatel88&theme=tokyonight&no-frame=true&no-bg=true&row=1&column=6&margin-w=15"/>
</a>

<br/><br/>

<a href="https://github.com/shivampatel88">
  <img width="94%" src="https://github-readme-activity-graph.vercel.app/graph?username=shivampatel88&bg_color=0d1117&color=58a6ff&line=58a6ff&point=c9d1d9&area=true&area_color=58a6ff&hide_border=true&custom_title=Contribution%20Activity"/>
</a>

</div>

<br/>

<!-- Contribution snake -->
<div align="center">
<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/shivampatel88/shivampatel88/output/github-snake-dark.svg"/>
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/shivampatel88/shivampatel88/output/github-snake.svg"/>
  <img alt="github-snake" src="https://raw.githubusercontent.com/shivampatel88/shivampatel88/output/github-snake-dark.svg" width="100%"/>
</picture>
</div>

<br/>

<div align="center">
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif" width="100%">
</div>

<!-- ══════════════════════════════════════════════════════════ -->
<!--  CURRENTLY — personality section, upgraded                -->
<!-- ══════════════════════════════════════════════════════════ -->

<br/>

<img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Telescope.png" width="26" align="left">

## &nbsp;`🔭 What's On My Mind`

```rust
fn current_state() -> Developer {
    Developer {
        seeking     : "Full-stack developer roles — fresher, production-grade mindset",
        building    : "Something that solves a problem I currently have (always)",
        obsessing   : ["distributed systems", "AI-native architectures", "concurrency bugs"],
        belief      : "Every system has a reason it works the way it does. I just need to know what it is.",
        fun_fact    : "I built a Chrome extension to track my own AI chats because nothing else existed.",
    }
}
```

<br/>

<!-- ══════════════════════════════════════════════════════════ -->
<!--  FOOTER                                                   -->
<!-- ══════════════════════════════════════════════════════════ -->

<div align="center">

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:163356,50:0a2540,100:0d1117&height=110&section=footer" width="100%"/>

<br/>

![Visitor Count](https://komarev.com/ghpvc/?username=shivampatel88&color=58a6ff&style=for-the-badge&label=PROFILE+VIEWS)

<br/><br/>

<i>"Every system has a reason it works the way it does. I just need to know what it is."</i>

<br/>

</div>
