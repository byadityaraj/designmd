# FAQ

## What is DesignMD?

A platform that measures the design systems of production websites and turns them into structured, AI-ready specifications. Paste any URL, get back a `DESIGN.md` file with the real color palette, typography, spacing, and component patterns extracted from the live page.

## How do I use it?

Three ways:

- **CLI**: `npx @designmdcc/cli stripe.com > DESIGN.md` (zero-install) or `npm install -g @designmdcc/cli` then `dmd <url>`.
- **Web**: paste a URL into [designmd.cc](https://designmd.cc) and download the result.
- **Catalog**: browse [pre-generated benchmarks](https://designmd.cc/benchmarks) for 56 well-known sites.

## Is this an open-source project?

The CLI source and the showcase materials in **this repository** (sample outputs, documentation, screenshots) are MIT-licensed. The production source code — extraction pipeline, prompts, server, automation — is proprietary and not published here.

## How accurate are the extractions?

Every signal in a generated `DESIGN.md` is sourced from the live DOM and CSSOM at extraction time. Colors come from computed-style sampling, typography from the cascade, breakpoints from `@media` rule enumeration, hover states from CSSOM pseudo-class traversal. The LLM stage is a formatter — it organizes measured data into a readable spec, it doesn't invent values.

That said, some extractions are imperfect: WebGL-heavy pages may time out, and obscure CSS-in-JS frameworks sometimes obscure variable names. The extracted JSON (`/benchmarks/<slug>.json`, or `dmd <url> --json`) is the ground truth — the rendered markdown is a presentation layer on top.

## Why these 56 sites?

The current catalog was curated to balance:

- **Category coverage** — every major SaaS/consumer category represented
- **Design quality** — sites known for strong, distinctive visual systems
- **Recognizability** — brands people search for by name
- **Comparison value** — direct competitors in the same category enable "X vs Y" pages

Suggestions for additions are welcome — open an issue.

## Can I get a DESIGN.md for my own site?

Yes — run `dmd yourdomain.com` or paste it at [designmd.cc](https://designmd.cc). The result is generated on-demand. No login required. Free tier is rate-limited to 5 generations per day per IP-bucket.

## How does this differ from existing design-system catalogs?

Most catalogs (Awwwards, Land-book, etc.) are **inspiration galleries** — hand-curated screenshots with editorial commentary. DesignMD is a **measurement layer** — every page is parsed by an actual browser, every value is measured, every export is structured for machine consumption.

The intended use is different too: most galleries are read by designers seeking inspiration; DesignMD is consumed by AI coding agents (Claude, Cursor, Copilot) seeking ground truth about a specific brand.

## How do I use the output with Claude / Cursor / etc.?

After generating a `DESIGN.md`, drop it into your project root. Then point your agent at it via its rules file:

**Claude Code** — add to `CLAUDE.md`:
```
When building UI for this project, reference @DESIGN.md for exact colors,
typography, spacing, and component patterns.
```

**Cursor** — add to `.cursor/rules`:
```
Before writing UI code, read DESIGN.md and follow its specifications exactly.
Do not infer brand styles — measure from the file.
```

**Plain ChatGPT / others** — paste the file content as a system message or initial context message.

Full integration guide: [`docs/ai-workflows.md`](./ai-workflows.md).

## Will sites change over time?

Yes — that's the point of versioning. Each benchmark is stored in a version-tagged directory (`v0.5.1`, `v0.5.2`, etc.). Re-running the extractor produces a new version. The roadmap includes token-diff visualization so you can see how a site's design has evolved between snapshots.

## What about privacy?

DesignMD reads only public-web pages — there is no login, no cookie-jar, no scraping of authenticated content. URLs that resolve to private IPs (loopback, link-local, etc.) are blocked at the URL-guard layer.

## Cost / commercial use?

The live site and the CLI are free to use within the per-day rate limit. Commercial use of generated `DESIGN.md` outputs is permitted under the MIT license attached to the materials in this repo. The platform itself (production code, automation, hosting) is not commercially licensed; please reach out for inquiries.

## Where do I report bugs?

Open an issue on this repository for anything visible at [designmd.cc](https://designmd.cc) or via the CLI — broken extractions, wrong colors, missing categories, CLI failures, etc.
