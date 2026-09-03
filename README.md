# AI Educator Showcase

A single-page, static showcase of the apps, simulations, labs, notes, and experiments produced during and around the AI for Educators workshop — one place to browse everything, sorted by status (live vs. experimental) and grouped by category.

Live at: **https://clarkngo.github.io/ai-educator-showcase/**

## What's in it

- [`index.html`](index.html) — the entire site: layout, styling, and the data array of every linked project, in one file.

No build step, no dependencies, no backend — it's plain HTML/CSS/JS. Every project card is an entry in a JS array (`title`, `kicker`, `status`, `url`, `tags`, `desc`) grouped into sections:

| Section | What it covers |
|---|---|
| Start Here | Personal site, portfolio, courses, playground hub |
| AI Tools & Apps | Prompt builder, agentic blueprints, speech/writing tools |
| Simulations & 3D | Maritime, volleyball, and network simulators |
| Technical & System Design | Architecture walkthroughs, capacity calculators, security labs |
| Notes & Learning | Learning notes, class notes, conference notes |
| Writing & Publishing | Blog, eBooks, vibe-coding log |
| Games & Creative | Mini-games and personal creative builds |

Each card carries a `live` or `exp` (experimental) status badge, so visitors can tell finished tools apart from in-progress ones at a glance.

## Adding a new project

Open [`index.html`](index.html) and add an entry to the relevant section's array:

```js
{ title: "Name", kicker: "Short subtitle", status: "live", url: "https://...", tags: "Tag · Tag", desc: "One or two sentences describing what it does and why it exists." }
```

## Deploying it

### GitHub Pages

1. In the repo, go to **Settings → Pages**.
2. Under **Build and deployment**, set **Source** to `Deploy from a branch`.
3. Set **Branch** to `main` and the folder to `/ (root)`.
4. Save. The site will publish at `https://<your-username>.github.io/ai-educator-showcase/`.

That's the whole setup — every path in the site is relative, so it works unmodified from a repo subpath.

### Running it locally

Any static file server works:

```bash
python3 -m http.server 8123
```

Then open `http://localhost:8123`.

## License

[MIT](LICENSE).
