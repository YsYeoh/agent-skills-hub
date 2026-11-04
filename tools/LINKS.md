# Tools (not skills)

Direct libraries, CLIs and frameworks an agent can install and drive — tools you call, rather than
`SKILL.md` procedures the agent follows. Same format: links only, no code copied in.

| Tool | Source | What it does |
|------|--------|--------------|
| moviepy | [zulko/moviepy](https://github.com/zulko/moviepy) | Python video editing library (v2.0, breaking changes from v1): cuts, concatenation, text overlays, compositing / non-linear editing, video processing and custom effects — GIF and all common audio/video formats, Python 3.9+. |
| auto-editor | [wyattblue/auto-editor](https://github.com/wyattblue/auto-editor) | Effort-free CLI editor: first-pass removal of silence and dead space by audio loudness or motion threshold (`--edit audio/motion`), with `--margin` padding to keep cuts natural. Ships an installable skill: `npx skills add WyattBlue/auto-editor`. |
| remotion | [remotion-dev/remotion](https://github.com/remotion-dev/remotion) | Make videos programmatically with React: design systems of animated assets, batch rendering millions of videos on your own infrastructure, video-editor apps, agent-driven creation. Ships Agent Skills docs and templates. Note: special license — company license may be required. |
| hex | [anomalyco/hex](https://github.com/anomalyco/hex) | Local voice dictation for macOS, Windows and Linux: hold a key, speak, it pastes into whatever app you are in. Transcribes on device, nothing leaves the machine after the first speech-model download. Rust app with a TypeScript SDK and an MCP server for meetings. Also ships the `hex-personal-commands` skill (see General / Meta Skills). MIT. |
| scrapling (framework) | [D4Vinci/Scrapling](https://github.com/D4Vinci/Scrapling) | The Python scraping framework behind the Scrapling agent skill: fast HTTP requests, stealth browser, JavaScript rendering, Cloudflare handling, adaptive selectors, proxy rotation, concurrent spiders with pause/resume and JSON/JSONL/CSV export. Usable from Python, the CLI, or an agent over its MCP server. The SKILL.md side is indexed under Research & Web. |
| whisperx | [m-bain/whisperx](https://github.com/m-bain/whisperx) | Automatic speech recognition at 70x realtime (whisper large-v2, batched, <8GB GPU) with word-level timestamps via wav2vec2 alignment, VAD preprocessing and pyannote-audio speaker diarization — the transcription/subtitle layer for video pipelines. |

## How to use them in a stack

These four line up into one video pipeline; each hands the next a clean artifact.

1. **Cut the raw footage — `auto-editor`.** Strip silence and dead air before anything else, so every
   later step works on a much shorter file.
   `auto-editor raw.mp4 --edit audio --margin 200ms -o cut.mp4`
2. **Transcribe — `whisperx`.** Run it on the cut audio to get word-level timestamps and speaker
   diarization, which become subtitles or a caption file for the edit.
   `whisperx cut.mp4 --model large-v2 --diarize`
3. **Assemble the edit — `moviepy`.** Do the actual non-linear edit in Python: trims, concatenation,
   text overlays, transitions, burn-in captions driven by the transcript from step 2.
4. **Render templated or batch video — `remotion`.** When the video is data-driven (one composition,
   many rows of data, branded templates, variants for A/B), drive it with React instead of hand-editing,
   then render on your own infrastructure.

Variants: for a quick social clip, steps 1→3 are enough. For programmatic marketing videos, skip 1→3
and feed data straight into Remotion, using whisperx only if you need captions from an existing voice
track.

## Other tools and where they fit

- **Scrapling** is the research arm rather than the video arm: it is the tool behind the
  `scrapling` skill in `skills/research-web/LINKS.md`, and it is what lets an agent reach the pages
  that block plain fetches before the writing stage of a research-to-article stack.
- **Hex** sits at the very front of any stack that needs spoken input: dictate a brief, a spec
  outline or a design note on-device, and the text lands in whatever editor or agent prompt you are
  working in. Nothing is uploaded.