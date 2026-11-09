# Foldline plugin for Claude

Adds the [Foldline](https://github.com/alireza12t/foldline) MCP server to Claude. Foldline renders HTML canvas animations to MP4 fast on a Mac, and gives agents 66 code-made film styles, review stills, full renders, reading-time checks, TTS and loudness mastering.

The server comes from npm (`npx -y foldline-mcp`), so this repo only holds the plugin manifest. Foldline's code, docs and styles live in the [main repository](https://github.com/alireza12t/foldline).

## Needs

- Node 20+
- ffmpeg: `brew install ffmpeg`
- Chrome's headless shell: `npx playwright-core@1.63.0 install chromium-headless-shell`

The server tells you if one is missing.

## Install in Claude Code

```sh
claude plugin install foldline --marketplace alireza12t/foldline
```

## Licence

Open source, free for non-commercial use ([PolyForm Noncommercial 1.0.0](LICENSE)). Making money with it needs a commercial licence: open an issue on the [main repository](https://github.com/alireza12t/foldline/issues) with "Commercial licence" in the title.
