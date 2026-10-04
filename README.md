<img src="https://capsule-render.vercel.app/api?type=waving&color=0:1f6feb,100:8957e5&height=200&section=header&text=Thybault%20Jallu&fontSize=54&fontColor=ffffff&fontAlignY=36&desc=Gameplay%20and%20Audio%20Programmer%20%C2%B7%20Kubernetes%20in%20production&descSize=18&descAlignY=58" width="100%" alt="Thybault Jallu: Gameplay & Audio Programmer, Kubernetes in production">

<p align="center">
  <a href="https://github.com/DenverCoder1/readme-typing-svg"><img src="https://readme-typing-svg.demolab.com?font=Fira+Code&weight=500&size=19&pause=1200&color=58A6FF&center=true&vCenter=true&width=640&lines=Gameplay+%26+audio+in+Unity+ECS+and+FMOD;Kubernetes+%C2%B7+Helm+%C2%B7+Flux+at+Ezytail;Talos+homelab+after+hours;Open+to+work%3A+France%2C+abroad+or+remote" alt="Gameplay & audio in Unity ECS and FMOD. Kubernetes, Helm, Flux at Ezytail. Talos homelab after hours. Open to work: France, abroad or remote."></a>
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/thybault-jallu-14a069319/"><img src="https://img.shields.io/badge/LinkedIn-Thybault%20Jallu-0A66C2?style=for-the-badge&logo=data%3Aimage%2Fsvg%2Bxml%3Bbase64%2CPHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHZpZXdCb3g9IjAgMCAyNCAyNCI%2BPHBhdGggZmlsbD0id2hpdGUiIGQ9Ik0yMC40NDcgMjAuNDUyaC0zLjU1NHYtNS41NjljMC0xLjMyOC0uMDI3LTMuMDM3LTEuODUyLTMuMDM3LTEuODUzIDAtMi4xMzYgMS40NDUtMi4xMzYgMi45Mzl2NS42NjdIOS4zNTFWOWgzLjQxNHYxLjU2MWguMDQ2Yy40NzctLjkgMS42MzctMS44NSAzLjM3LTEuODUgMy42MDEgMCA0LjI2NyAyLjM3IDQuMjY3IDUuNDU1djYuMjg2ek01LjMzNyA3LjQzM2EyLjA2MiAyLjA2MiAwIDEgMSAwLTQuMTI1IDIuMDYyIDIuMDYyIDAgMCAxIDAgNC4xMjV6bTEuNzgyIDEzLjAxOUgzLjU1NVY5aDMuNTY0djExLjQ1MnpNMjIuMjI1IDBIMS43NzFDLjc5MiAwIDAgLjc3NCAwIDEuNzI5djIwLjU0MkMwIDIzLjIyNy43OTIgMjQgMS43NzEgMjRoMjAuNDUxQzIzLjIgMjQgMjQgMjMuMjI3IDI0IDIyLjI3MVYxLjcyOUMyNCAuNzc0IDIzLjIgMCAyMi4yMjIgMGguMDAzeiIvPjwvc3ZnPg%3D%3D" alt="LinkedIn"></a>
  <a href="https://troupote.itch.io"><img src="https://img.shields.io/badge/itch.io-play%20my%20games-FA5C5C?style=for-the-badge&logo=itchdotio&logoColor=white" alt="itch.io"></a>
  <a href="https://github.com/ThybaultJallu"><img src="https://img.shields.io/badge/work%20GitHub-@ThybaultJallu-24292F?style=for-the-badge&logo=github&logoColor=white" alt="Work GitHub account"></a>
</p>

### Hi, I'm Thybault 👋

I'm a French game programmer who lives where **gameplay code meets sound**. I study computer science at **[Cnam-Enjmin](https://enjmin.cnam.fr/)**, France's national school of video games and interactive media, and I work as a **software developer at [Ezytail](https://www.ezytail.com/)** on a work-study contract.

I was a musician before I was a coder, so I care about how a system *feels* and *sounds*, and I like to measure it too. Latest example: I rewrote enemy avoidance in Crazy Planet Survivor and saved **~7 ms per frame with 5,000 entities** on screen.

The other half of my work is backend and platform. At Ezytail I build on **EzyFlow**, our event-driven integration platform (C#, NATS), and on the **Kubernetes** platform it runs on: **Helm** charts, **GitOps with Flux**, SSO, supply-chain security. After hours I run a **Talos Linux** homelab where I self-host whatever I need.

```csharp
var thybault = new Developer
{
    Role     = "Gameplay & Audio Programmer",
    Stack    = ["C#", "C++", "Unity ECS", "FMOD", ".NET", "SQL Server"],
    Ops      = ["Kubernetes", "Helm", "Flux (GitOps)", "Talos", "NATS", "Docker"],
    Studying = "Bachelor's in Computer Science, Video Games · Cnam-Enjmin (2024 → 2027)",
    Working  = "Software Developer · Ezytail (work-study)",
    Speaks   = ["French (native)", "English (professional)"],
    Based    = "Paris region & Angoulême, France",
    OpenTo   = ["gameplay", "audio", "tools", "backend", "devops"], // France, abroad or remote
};
```

## 💼 Experience

**Software Developer, work-study** · [Ezytail](https://www.ezytail.com/) · Paris region · 2025 → today
<br><sub>Ezytail is a B Corp certified e-commerce logistics and IT company: warehousing, transport and software for online retailers.</sub>

#### Production platform: Kubernetes, Helm, Flux

```mermaid
flowchart LR
    repo["Git<br/>Helm charts + values"] -->|pull| flux["Flux"]
    flux -->|HelmRelease| k8s
    subgraph k8s["Kubernetes => prod + staging"]
        ezyflow["EzyFlow connectors"] <--> nats[("NATS JetStream")]
        runners["GitHub Actions runners"] -->|SBOM| dt["Dependency-Track"]
        apps["EzyWizardus, dashboards"] --- sso["Authentik SSO"]
    end
```

- **GitOps on two clusters.** Production and staging run on Kubernetes and are driven from Git by Flux. I ship services as HelmReleases and keep them reconciled.
- **Helm charts.** I wrote the charts for EzyWizardus and the internal dependency dashboard, with Authentik SSO and a chart release workflow.
- **Platform services.** I deployed Dependency-Track on its own CloudNativePG PostgreSQL, the Radar Kubernetes UI with scoped RBAC for staff and engineering, and EzyFlow's analytics stream.
- **CI inside the cluster.** I moved GitHub Actions workflows (EzyManager, the EzyFlow framework, the canonical domain) to runners that live in Kubernetes.
- **Supply-chain security.** CycloneDX SBOMs built in CI and published to Dependency-Track, with policies, drift detection against internal libraries and release notifications to consuming repos.

#### EzyFlow: event-driven integration platform

EzyFlow moves Ezytail's orders, products and invoices between online stores, the ERP and logistics systems: C# connectors over **NATS JetStream**, deployed on the Kubernetes platform above.

- **Shopify connector.** Migrated it to the GraphQL Admin API (ShopifySharp), fixed order and product sync (IDs and GIDs, option serialisation) and masked secrets in error messages.
- **Framework releases.** SBOM and Dependency-Track publishing in the release pipeline of the shared EzyFlow packages, on Kubernetes runners.
- **Docs tooling.** An AI-docs CLI and corpus that help find the right connector.

#### Billing automation: Prefactra

```mermaid
flowchart LR
    carriers["Carrier invoices<br/>DPD, UPS, DHL, Chronopost,<br/>TNT, DB Schenker…"] --> prefac["Prefactra<br/>EzyManager => C# / SQL Server"]
    prefac --> clients["Client invoices<br/>B2B / B2C"]
```

- **Prefactra, billing automation (B2B / B2C).** The pre-invoicing side of EzyManager: it turns carrier costs into client invoices, so Ezytail stops acting as a financial buffer between carriers and clients.
- **A dozen carriers.** Invoice readers, models and stagers for DPD, UPS, DHL, Chronopost, TNT, DB Schenker and more, with overcharge calculation and matching to customer accounts and sub-accounts.
- **I own the project, not just the code.** I run its day-to-day and I'm the bridge between the business teams and R&D: gathering needs, reporting progress, shipping features.
- **SQL and architecture.** Optimised SQL Server queries that were too slow, and refactored the code around OOP principles and UML models.
- **Invoice tooling.** Wrote the first invoice generator ([.NET 9, ClosedXML](https://github.com/ThybaultJallu/EzyInvoiceMaker)), which splits the monthly billing ledger into one formatted invoice per client. The EzyManager CLI has since replaced it.

#### EzyWizardus: pricing grid injector

- **Main author** (130+ of its 157 commits) of a **Next.js** app that bulk-imports carriers' transport pricing grids from Excel into the Directus CMDB behind EzyPricing: parsing, company, carrier and contract matching, ISO country checks, live progress.
- Grew from a C# console prototype into a production web app with **Authentik SSO**, shipped on Kubernetes with its own Helm chart.

**61 merged pull requests** since February 2025 and **270+ contributions** over the last 12 months, all in Ezytail's private repositories, on my work account [@ThybaultJallu](https://github.com/ThybaultJallu).

> *"A very committed apprentice who fits easily into ongoing projects. Very organised, and communicates task progress very well."*
> <br>— my tutor at Ezytail (translated from French)

## 🎮 Featured game: Crazy Planet Survivor

<p align="center">
  <a href="https://troupote.itch.io/crazy-planet-survivor"><img src="assets/cps-logo.png" width="240" alt="Crazy Planet logo"></a>
</p>

<a href="https://troupote.itch.io/crazy-planet-survivor"><img src="assets/cps-hordes.jpg" width="100%" alt="Crazy Planet Survivor gameplay: hundreds of enemies swarm the player on a volcanic planet"></a>

A frantic **360° bullet heaven**: you fight hordes across the whole surface of spherical planets, with no screen edge to hide behind. Built on **Unity 6 and ECS** to push thousands of entities on **Windows and Android**. It's our year-long Cnam-Enjmin project, and it's still in development.

<p>
  <a href="https://troupote.itch.io/crazy-planet-survivor"><img src="https://img.shields.io/badge/play-itch.io-FA5C5C?style=flat-square&logo=itchdotio&logoColor=white" alt="Play on itch.io"></a>
  <a href="https://github.com/Athyrr/Crazy-Planet-Survivor"><img src="https://img.shields.io/badge/source-GitHub-24292F?style=flat-square&logo=github&logoColor=white" alt="Source on GitHub"></a>
  <img src="https://img.shields.io/badge/Unity%206-ECS-000000?style=flat-square&logo=unity&logoColor=white" alt="Unity 6 ECS">
  <img src="https://img.shields.io/badge/audio-FMOD-6E56CF?style=flat-square" alt="FMOD">
  <img src="https://img.shields.io/badge/platforms-Windows%20·%20Android-3DDC84?style=flat-square&logo=android&logoColor=white" alt="Windows and Android">
</p>

**Team:** 2 developers and 1 tech artist, with music by Baptiste Blanc. **Me:** 200+ commits across performance, gameplay, audio, mobile and tools.

| Area | What I built |
|---|---|
| **Performance** | Rewrote enemy avoidance for a native 3D map: **−7 ms per frame at 5,000 entities**, now **under 1 ms**. Spawner **~5 ms**, adaptive performance **~10 ms per frame**, faster targeting. |
| **Gameplay** | Movement, XP orbs, critical hits (with their shader), resistances, a global stat database with upgrades, wave loop and presets, difficulty scaling, the first boss. |
| **Audio** | FMOD from setup to ship: audio manager, SFX integration with buffering, mixer and volume settings. |
| **Mobile** | Android builds and **NFC**: tap a physical card on the phone to pick your character or amulet. |
| **Tools** | In-editor stats tool, camera preset editor, spawner inspector. |
| **UI** | HUD, lobby, pause and settings menus, shop animations. |

<p align="center">
  <img src="assets/cps-combat.jpg" width="32%" alt="Combat on the volcanic planet">
  <img src="assets/cps-forest.jpg" width="32%" alt="The forest planet">
  <img src="assets/cps-nfc.jpg" width="32%" alt="Prototyping the NFC cards, with the FMOD audio manager open in Unity">
</p>

## 🕹️ More games

<p align="center">
  <a href="https://github.com/Troupote/BlackHoleRun"><img src="https://gh-card.dev/repos/Troupote/BlackHoleRun.svg" alt="Troupote/BlackHoleRun"></a>
  <a href="https://github.com/Troupote/LaToutePetiteMiniville"><img src="https://gh-card.dev/repos/Troupote/LaToutePetiteMiniville.svg" alt="Troupote/LaToutePetiteMiniville"></a>
</p>

| Game | What it is | My part |
|---|---|---|
| [**BlackHoleRun**](https://github.com/Troupote/BlackHoleRun) | Unity space game, team of 5 (2025) | **Audio programmer.** Rebuilt the FMOD audio system on world positions, 5.1 surround with hardware detection, spatializer, EQ, panner and filter automation, music tempo driven by gameplay. |
| [**La Toute Petite Miniville**](https://github.com/Troupote/LaToutePetiteMiniville) | Two-player dice and city-building card game in Unity, team of 5 | Menus and UI, music and sound effects, UML design. |
| [**Fighting game**](https://github.com/Troupote/Jeu-de-combat) | Turn-based duel against an AI, 4 classes with special abilities | Duo project in C#, WPF and XAML. |
| **Game of Life** | Conway's cellular automaton in three flavours: [console](https://github.com/Troupote/JeuDeLaVieConsole), [graphical](https://github.com/Troupote/JeuDeLaVieGraphique) and [mutant cells](https://github.com/Troupote/CelluleMutante) | Solo, C#. |

Outside games, I also built [**ZendeskToSqlDatabase**](https://github.com/Troupote/ZendeskToSqlDatabase), a .NET console app that exports every Zendesk ticket and user into SQL Server so support data can be queried in SQL.

## 🧰 Toolbox

<p align="center">
  <img src="https://skillicons.dev/icons?i=cs,cpp,dotnet,unity,blender,python,ts,nodejs,nextjs,react,docker,kubernetes,githubactions,git,linux,arch,rider,visualstudio,vscode,neovim&perline=10" alt="C#, C++, .NET, Unity, Blender, Python, TypeScript, Node.js, Next.js, React, Docker, Kubernetes, GitHub Actions, Git, Linux, Arch Linux, Rider, Visual Studio, VS Code, Neovim">
</p>

| Area | Tools |
|---|---|
| **Games** | Unity 6 (ECS), C#, C++ (RAII, move semantics), FMOD Studio, Blender, rigging and skinning, game and level design, Android and NFC |
| **Software** | C# / .NET, SQL Server, NATS JetStream, TypeScript, Next.js / React, Directus, WPF / XAML, OOP and UML, Python, Turso |
| **Audio & video** | Music production, sound design, adaptive music, 5.1 mixing, Reaper, Premiere Pro, DaVinci Resolve |
| **DevOps & platform** | **Kubernetes** (in production at Ezytail, and on my Talos Linux homelab), **Helm** charts, **Flux** (GitOps), CloudNativePG, Authentik SSO, Dependency-Track and CycloneDX SBOMs, GitHub Actions on Kubernetes runners, Docker, Git, Linux (daily Arch user) |

## 📈 Activity

<p align="center">
  <a href="https://github.com/ThybaultJallu"><img src="https://streak-stats.demolab.com?user=ThybaultJallu&mode=weekly&theme=github-dark-blue&hide_border=true" width="49%" alt="Work account (@ThybaultJallu): contribution streak, mostly private Ezytail repositories"></a>
  <a href="https://github.com/Troupote"><img src="https://streak-stats.demolab.com?user=Troupote&mode=weekly&theme=github-dark-blue&hide_border=true" width="49%" alt="Personal account (@Troupote): contribution streak"></a>
  <br><sub>Left: work account, mostly private Ezytail repos. Right: this account, games and personal projects.</sub>
</p>

<picture>
  <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Troupote/Troupote/output/github-snake-dark.svg">
  <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Troupote/Troupote/output/github-snake.svg">
  <img alt="A snake eating my contribution graph" src="https://raw.githubusercontent.com/Troupote/Troupote/output/github-snake.svg">
</picture>

## 🌍 Let's work together

I'm looking for **game programming** roles (gameplay, audio, tools, engine), **DevOps / platform** roles (Kubernetes, GitOps) and **software engineering** roles, in France, abroad or remote. The quickest way to reach me is [LinkedIn](https://www.linkedin.com/in/thybault-jallu-14a069319/).

<details>
<summary>🇫🇷 <b>En français</b></summary>
<br>

Développeur jeu vidéo, en licence informatique parcours Jeu Vidéo au **Cnam-Enjmin** (2024 → 2027) et **développeur en alternance chez Ezytail**. J'y développe **Prefactra**, l'application C# / SQL Server qui automatise la facturation entre transporteurs et clients (B2B / B2C), et je fais le lien entre les équipes métier et la R&D. Je travaille aussi sur **EzyFlow**, la plateforme d'intégration événementielle d'Ezytail (C#, NATS), et sur la plateforme **Kubernetes** qui la fait tourner : charts **Helm**, GitOps avec **Flux**, SSO Authentik, Dependency-Track. Chez moi, je fais tourner un homelab sous **Talos Linux**.

Côté jeu : gameplay, performance (Unity ECS) et intégration audio (FMOD) sur **Crazy Planet Survivor** et **BlackHoleRun**. Musicien avant d'être développeur.

Ouvert aux opportunités en France, à l'étranger ou en remote : écrivez-moi sur [LinkedIn](https://www.linkedin.com/in/thybault-jallu-14a069319/).

</details>

<img src="https://capsule-render.vercel.app/api?type=waving&color=0:8957e5,100:1f6feb&height=110&section=footer" width="100%" alt="">
