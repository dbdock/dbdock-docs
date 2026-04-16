# DBdock Docs

Source for the DBdock documentation site — [docs.dbdock.xyz](https://docs.dbdock.xyz).

Built with [Mintlify](https://mintlify.com/).

## Development

### Prerequisites

- Node.js 18+
- [Mintlify CLI](https://www.npmjs.com/package/mintlify)

### Install the Mintlify CLI

```bash
npm install -g mintlify
```

### Run locally

From the repo root:

```bash
mintlify dev
```

The docs site runs on [http://localhost:3000](http://localhost:3000) with live reload.

## Structure

```
.
├── docs.json                # Mintlify config (nav, theme, metadata)
├── global.css               # Global styles
├── index.mdx                # Home page
├── get-started/             # Installation, quickstart
├── core/                    # Concepts, configuration, security
├── cli/                     # CLI reference (one page per command)
├── migration/               # Cross-database migration
├── storage/                 # Storage provider setup
├── alerts/                  # Alerts & scheduling
├── guides/                  # Workflow guides
├── sdk/                     # Programmatic usage
├── help/                    # Troubleshooting, FAQ, changelog
├── images/                  # Logo, favicon, screenshots
└── snippets/                # Reusable content snippets
```

## Writing docs

- Each page is a `.mdx` file with frontmatter (`title`, `description`)
- Pages must be registered in `docs.json` under the correct group
- Use Mintlify components: `<Card>`, `<CardGroup>`, `<Steps>`, `<Tabs>`, `<AccordionGroup>`, `<Note>`, `<Warning>`, `<Tip>`
- Keep pages focused — one topic per page
- Cross-reference liberally with `[text](/path)`

## Deployment

Pushes to `main` auto-deploy to [docs.dbdock.xyz](https://docs.dbdock.xyz) via Mintlify's GitHub integration.

## Related repositories

- **[dbdock/dbdock](https://github.com/dbdock/dbdock)** — the CLI source code

## License

MIT — see [LICENSE](LICENSE).
