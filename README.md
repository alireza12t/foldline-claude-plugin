# Foldline plugin for Claude

Adds a Foldline skill to Claude. [Foldline](https://github.com/alireza12t/foldline) renders HTML canvas animations to MP4 fast on a Mac, and ships 66 code-made film styles, review stills, reading-time checks, offline voice and loudness mastering. The skill tells Claude how to make a film with it: pick a style, build the page, check stills and text timing, render, and master the sound.

This is the copy listed in Anthropic's directory, so it holds the skill only. Foldline's code, docs and styles live in the [main repository](https://github.com/alireza12t/foldline).

## Needs

- macOS with Apple Silicon (Windows and Linux are untested and slower)
- Node 20+
- ffmpeg: `brew install ffmpeg`

The skill clones Foldline into `~/foldline` (or `$FOLDLINE_HOME`) the first time.

## Want the MCP tools too?

Foldline also has an MCP server with tools for styles, stills, renders, voice and mastering. In Claude Code, install the full plugin (skill plus server):

```sh
claude plugin install foldline --marketplace alireza12t/foldline
```

or add just the server: `claude mcp add --scope user foldline -- npx -y foldline-mcp`. When the tools are there, the skill uses them.

## Privacy

Foldline runs on your computer and collects nothing. A few steps use outside services, only when you run them: GitHub and npm (getting Foldline and its packages), GitHub releases (voice model, HDRIs, instruments), Hugging Face (the Whisper model for checking voice lines), and Microsoft's Edge text-to-speech if you choose it instead of the offline Kokoro voice, which sends the text of your lines. Details are in [PRIVACY.md](PRIVACY.md).

## Licence

Open source, free for non-commercial use ([PolyForm Noncommercial 1.0.0](LICENSE)). Making money with it needs a commercial licence: open an issue on the [main repository](https://github.com/alireza12t/foldline/issues) with "Commercial licence" in the title.
