<div align="center">

# DBDock Docs

Source for the DBDock documentation site — **[docs.dbdock.xyz](https://docs.dbdock.xyz)**.

[![Mintlify](https://img.shields.io/badge/built%20with-Mintlify-23517c)](https://mintlify.com/)
[![Docs](https://img.shields.io/badge/docs-docs.dbdock.xyz-blue)](https://docs.dbdock.xyz)

</div>

---

A single knowledge base for both halves of DBDock: the open-source [CLI](https://github.com/dbdock/dbdock) and the managed [Cloud dashboard](https://dbdock.xyz), plus the [Cloud Sync](https://docs.dbdock.xyz/cloud-sync/overview) that links them. Built with [Mintlify](https://mintlify.com/).

## Development

### Prerequisites

- Node.js 18+ (an LTS release — the Mintlify CLI does not support Node 25+)
- [Mintlify CLI](https://www.npmjs.com/package/mintlify)

### Run locally

```bash
npm install -g mintlify   # once
mintlify dev              # from the repo root
```

The site runs on [http://localhost:3000](http://localhost:3000) with live reload.

### Validate before pushing

```bash
mintlify broken-links     # check internal links resolve
```

## Structure

```
.
├── docs.json                # Mintlify config (tabs, nav, theme, SEO, redirects)
├── global.css               # Global styles
├── index.mdx                # Home page
├── get-started/             # What is DBDock, cloud & CLI quickstarts, installation
├── core/                    # Concepts, configuration
├── cloud/                   # DBDock Cloud dashboard (connections, backups, storage, …)
├── cloud-sync/              # Linking the CLI to the cloud (auth, sync, data handling)
├── security/                # Encryption, cloud security, key management
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

The navigation is organized into three tabs — **Documentation**, **CLI Reference**, and **SDK** — configured in `docs.json`.

## Writing docs

- Each page is an `.mdx` file with frontmatter (`title`, `description`, optional `icon`)
- Register every page in `docs.json` under the correct tab and group
- Use Mintlify components: `<Card>`, `<CardGroup>`, `<Steps>`, `<Tabs>`, `<AccordionGroup>`, `<Note>`, `<Warning>`, `<Tip>`, `<CodeGroup>`
- Keep pages focused — one topic per page
- Write descriptive frontmatter — the `description` is the page's SEO meta description
- Cross-reference liberally with `[text](/path)`

## Deployment

Pushes to `main` auto-deploy to [docs.dbdock.xyz](https://docs.dbdock.xyz) via Mintlify's GitHub integration.

## Related repositories

- **[dbdock/dbdock](https://github.com/dbdock/dbdock)** — the CLI source and npm package
- **[DBDock Cloud](https://dbdock.xyz)** — the managed dashboard

## License

MIT — see [LICENSE](LICENSE).
