# Contributing

This repository is the public developer surface for DesignMD — CLI source, documentation, sample outputs, and screenshots. The extraction pipeline, prompts, server, and operational tooling live in a separate private repository and are not accepting outside contributions.

Within this repo, contributions are welcome in the following areas.

## What's in scope

- **Bug reports** on the live site ([designmd.cc](https://designmd.cc)) or the CLI ([`@designmdcc/cli`](https://www.npmjs.com/package/@designmdcc/cli)).
- **Benchmark suggestions** — a URL you'd like to see measured and added to the catalog.
- **Documentation improvements** — corrections, clearer phrasing, or additional integration recipes in `docs/`.
- **Better sample examples** — a more interesting `DESIGN.md` to swap into `examples/`.
- **CLI ergonomics** — small, well-scoped improvements to flags, error messages, or output formatting.

## What's out of scope

- New extraction algorithms or pipeline changes (proprietary).
- Prompt engineering or LLM logic (proprietary).
- Auth, billing, or account systems.
- Architectural redesigns of the platform.

If you have an idea in one of these areas, open an issue to discuss before writing code.

## How to file a bug

1. Open an issue with a clear, reproducible report.
2. Include the URL you tried, the command you ran (if CLI), the expected behavior, and the actual behavior.
3. For CLI bugs, paste the output of `dmd --version` and your Node version (`node --version`).

## How to suggest a benchmark

Open an issue titled `benchmark: <domain>` with one or two sentences on why the site is worth measuring (distinctive design system, strong category coverage, comparison value, etc.).

## How to send a PR

For small documentation or sample-quality changes:

1. Fork the repo.
2. Make the change on a feature branch.
3. Open a PR with a one-paragraph description of what changed and why.

For anything larger than a documentation tweak, please open an issue first so we can align on scope.

## Tone

We aim for technical, calm, editorial writing. Avoid hype, growth-marketing copy, and excessive emoji. Show, don't sell.

## License

By contributing, you agree that your contributions will be licensed under the [MIT License](./LICENSE) that covers the materials in this repository.
