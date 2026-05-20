# Example `DESIGN.md` outputs

Eight curated samples from the live DesignMD catalog, showing the kind of structured design specification you get for any URL. Each `.md` file is paired with the source-site thumbnail used during extraction.

| Sample                                       | Category     | Live page                                                  |
| -------------------------------------------- | ------------ | ---------------------------------------------------------- |
| [`DESIGN-stripe.md`](./DESIGN-stripe.md)     | Fintech      | [/benchmarks/stripe](https://designmd.cc/benchmarks/stripe)       |
| [`DESIGN-mercury.md`](./DESIGN-mercury.md)   | Fintech      | [/benchmarks/mercury](https://designmd.cc/benchmarks/mercury)     |
| [`DESIGN-linear.md`](./DESIGN-linear.md)     | Productivity | [/benchmarks/linear](https://designmd.cc/benchmarks/linear)       |
| [`DESIGN-notion.md`](./DESIGN-notion.md)     | Productivity | [/benchmarks/notion](https://designmd.cc/benchmarks/notion)       |
| [`DESIGN-vercel.md`](./DESIGN-vercel.md)     | Hosting      | [/benchmarks/vercel](https://designmd.cc/benchmarks/vercel)       |
| [`DESIGN-anthropic.md`](./DESIGN-anthropic.md) | AI         | [/benchmarks/anthropic](https://designmd.cc/benchmarks/anthropic) |
| [`DESIGN-figma.md`](./DESIGN-figma.md)       | Design       | [/benchmarks/figma](https://designmd.cc/benchmarks/figma)         |
| [`DESIGN-airbnb.md`](./DESIGN-airbnb.md)     | Consumer     | [/benchmarks/airbnb](https://designmd.cc/benchmarks/airbnb)       |

## Generate your own

```bash
npx @designmdcc/cli <your-url> > DESIGN.md
```

Same pipeline as the examples in this folder — measured live against the source page, no human editing.

## What's in a sample

Every generated `DESIGN.md` follows a consistent 10-section structure:

1. **Visual Theme & Atmosphere** — high-level character of the brand
2. **Color Palette & Roles** — primary, accent, surface, text, with measured hex values
3. **Typography Rules** — families, size scale, weights, line-heights
4. **Component Stylings** — buttons, inputs, cards, navigation
5. **Spacing & Layout** — spacing scale, container widths, grid systems
6. **Iconography & Imagery** — icon styles, illustration patterns
7. **Motion & Interaction** — transitions, easing, hover states
8. **Responsive Behavior** — measured breakpoints, mobile patterns
9. **Accessibility** — measured contrast pairs, focus styles
10. **Implementation Notes** — practical guidance for AI agents

## How these were generated

Each file is the unedited output from the live DesignMD pipeline at the date stamped on the corresponding `/benchmarks/<slug>` page. The pipeline:

1. Loads the source URL in a headless browser
2. Extracts CSS variables, computed styles, breakpoints, and component selectors
3. Captures multiple-fold screenshots
4. Streams the extracted token JSON + screenshots into a vision LLM
5. Saves the markdown response unchanged

No human editing has been applied to these examples.

## How to use them

See [`/docs/ai-workflows.md`](../docs/ai-workflows.md) for instructions on integrating these files with Claude Code, Cursor, Copilot, Windsurf, and other AI coding tools.
