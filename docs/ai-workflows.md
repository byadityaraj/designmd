# Using DesignMD output with AI coding tools

The `DESIGN.md` files produced by DesignMD are purpose-built for LLM context windows. Drop one into your project, reference it from your coding agent's rules file, and the assistant will build UI that matches the real design system of the source brand — colors, typography, spacing, all measured live.

## Step 0 — generate the file

The fastest path is the CLI:

```bash
npx @designmdcc/cli stripe.com > DESIGN.md
```

Or, installed globally:

```bash
npm install -g @designmdcc/cli
dmd stripe.com > DESIGN.md
```

You can also paste a URL into [designmd.cc](https://designmd.cc) and download the result. Same output either way.

## Claude Code

### Project-level reference

Add to your project's `CLAUDE.md`:

```markdown
# Design context

When building any UI in this project, reference the design specification at
@DESIGN.md.

That file contains the exact colors, typography, spacing scale, breakpoints,
and component patterns extracted from the source URL. Do not invent brand
values — read them from the file.
```

### Per-task usage

When you need to build a specific component:

```
@DESIGN.md — build me a pricing card that matches the primary button style
and uses the body typography from §3.
```

## Cursor

Add to `.cursor/rules` at project root:

```
Before writing any UI code:

1. Read DESIGN.md (in the project root).
2. Use its color palette, typography scale, and spacing values exactly.
3. Match the component patterns described in §4.
4. Do NOT infer brand styles — every value should trace back to the file.
```

Cursor loads this rule into every chat session in the project.

## GitHub Copilot

Copilot reads open files. The pattern:

1. Keep `DESIGN.md` open in a sidebar tab.
2. In your code comment, reference the spec:

```js
// Per DESIGN.md §2.3, use the brand-indigo (#0a2540) for primary
// CTA buttons. Border-radius 6px, padding 12px 18px.
function PrimaryButton({ children }) {
  // Copilot will now suggest button styles matching the spec.
}
```

## Windsurf, Aider, Cline, Continue

Same pattern as Cursor — every modern AI coding tool supports a project-root rules file:

| Tool             | Config file                                      |
| ---------------- | ------------------------------------------------ |
| Cursor           | `.cursor/rules` or `.cursorrules`                |
| Windsurf         | `.windsurfrules`                                 |
| Aider            | `CONVENTIONS.md` or `.aider.conf.yml`            |
| Cline (VS Code)  | `.clinerules`                                    |
| Continue         | `~/.continue/config.json` → `customCommands`     |

Reference `DESIGN.md` from any of them.

## Plain ChatGPT / Claude.ai web

If you're not in a coding tool:

1. Open the generated `.md` file in a text editor
2. Copy the entire contents
3. Paste as the first message in a new conversation, prefaced with:
   > Use this design specification for all UI code you generate in this conversation. Do not infer values; reference the file.
4. Then ask for components, screens, layouts, etc.

The model will adhere to the measured values for the rest of the conversation.

## Best practices

### Keep the file in the repo

Don't reference a URL — paste the `DESIGN.md` content into your repository as a file. AI tools work better with local file context than fetched URLs, and the file becomes a stable snapshot you can version-control.

### Regenerate when the brand changes

If the source brand redesigns, regenerate the `DESIGN.md`. The old version becomes stale immediately.

```bash
dmd stripe.com --force > DESIGN.md
```

`--force` bypasses the cache and re-extracts from the live page.

### Cite the source in PRs

When using a measured design system, reference it in pull-request descriptions:

> *Design tokens sourced from `DESIGN.md` (extracted via DesignMD from stripe.com on 2026-05-10).*

This makes design decisions auditable.

### Mix and match

You can use multiple `DESIGN.md` files in the same project — e.g., reference Stripe's button styling and Linear's typography in the same component. The files compose cleanly.

```bash
dmd stripe.com > ./design/stripe.md
dmd linear.app > ./design/linear.md
```

Then point your agent at the relevant file per task.

## Examples in this repository

See [`/examples`](../examples) for 8 production `DESIGN.md` outputs covering:

- **Fintech** — [Stripe](../examples/DESIGN-stripe.md), [Mercury](../examples/DESIGN-mercury.md)
- **AI** — [Anthropic](../examples/DESIGN-anthropic.md)
- **Productivity** — [Linear](../examples/DESIGN-linear.md), [Notion](../examples/DESIGN-notion.md)
- **Hosting** — [Vercel](../examples/DESIGN-vercel.md)
- **Design tools** — [Figma](../examples/DESIGN-figma.md)
- **Consumer** — [Airbnb](../examples/DESIGN-airbnb.md)

Use any of these directly, or generate one for a brand you actually need with `dmd <url>` or at [designmd.cc](https://designmd.cc).
