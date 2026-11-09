# Privacy

Foldline runs on your own computer. It has no accounts, no telemetry and no analytics, and nothing you make is sent to the author.

Your pages, frames, renders, voice lines and mixes stay in the folders you choose.

Some steps use the internet, and only when you run them:

- **Getting Foldline:** the skill clones Foldline from GitHub and installs its packages from npm. The optional MCP server installs from npm with `npx`.
- **Big assets (`fetch_assets`, or `setup.sh` and `tools/fetch.sh`):** downloads the voice model, HDRI skies or instrument libraries from GitHub releases of [lemo-opuscar](https://github.com/lemomo-ai/lemo-opuscar).
- **Checking voice lines (`check_voice` or `asr_check.py`):** the first run downloads a Whisper model from Hugging Face.
- **Edge voices (`make_voice` with `engine: "edge"`, or `tts_zh.py`):** sends the text of your lines to Microsoft's Edge text-to-speech service. The default engine, Kokoro, works offline.

Those services' own privacy policies apply to those requests.

Questions: open an issue at https://github.com/alireza12t/foldline/issues
