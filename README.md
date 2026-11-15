# KreatorFlow MCP server

Make Seedance videos, Seedream images, lip sync and voiceovers from Claude, ChatGPT, Cursor or VS Code. 33 tools, OAuth sign-in.

KreatorFlow connects your AI assistant to a full AI media studio. Ask for a video and it generates it with ByteDance's Seedance 2.5 or 2.0, makes images with Seedream 5.5, turns a photo and a voice track into a talking or singing video with OmniHuman lip sync, and runs Kitsune motion transfer, object swap and face swap on existing clips. It also reads text aloud, clones voices, makes music and sound effects, transcribes and translates speech, keeps saved characters consistent across a series, and plans scenes in Stage, the free 3D shot planner. It also talks to Kiryu, KreatorFlow's AI director, and uses templates.

KreatorFlow is an official partner of BytePlus, a ByteDance company.

This is a hosted (remote) MCP server. There is nothing to install or run locally, and this repository contains no code.

## Connect

- **Server URL:** `https://kreatorflow.ai/api/mcp` (Streamable HTTP)
- **Sign-in:** OAuth. Your app opens a KreatorFlow sign-in page; no API key to copy.
- **Plan:** a paid KreatorFlow plan (Creator, Pro, Max or Business) or the $3 48-hour trial on Creator, Pro or Max. Generations use your plan credits at 10% more than the studio price, and failed jobs are refunded automatically.

### Claude (web and desktop)
Open Customize, then Connectors, click + Add and choose Add custom connector. Name it KreatorFlow, paste `https://kreatorflow.ai/api/mcp`, click Continue and sign in with your KreatorFlow account.

### ChatGPT, Claude Code, Cursor, VS Code, Windsurf
Add a remote MCP server (custom connector) with the URL `https://kreatorflow.ai/api/mcp`. The app opens the KreatorFlow sign-in page for you. Clients that only run local servers can connect through the `mcp-remote` bridge.

Step-by-step setup with screenshots: https://kreatorflow.ai/mcp

## Tools

| Tool | What it does |
|---|---|
| `generate_video` | Text or image to video with Seedance 2.0, 2.0 Fast, 2.0 Mini or 2.5 |
| `generate_image` | Text to image with Seedream |
| `edit_image`, `edit_video` | Edit an existing image or clip with a prompt |
| `lip_sync` | Make the person in a photo speak or sing a voice track (OmniHuman 2.0) |
| `kitsune` | Motion transfer and object swap on a video |
| `face_swap` | Swap a face in an image |
| `generate_speech` | Text to speech |
| `generate_sound` | Music, sound effects or dialogue from a prompt |
| `clone_voice`, `list_voices` | Clone a voice and list available voices |
| `transcribe`, `translate_speech` | Speech to text and speech translation |
| `save_character`, `list_characters` | Keep a character consistent across a series |
| `upload_media` | Bring a public file URL into your workspace |
| `list_history`, `list_models`, `list_templates` | Browse past generations, models and templates |
| `get_template`, `use_template`, `save_template`, `publish_template` | Use, save and share templates |
| `create_upload`, `confirm_upload` | Upload a file from your computer |
| `ask_kiryu`, `get_kiryu_chat` | Let Kiryu, the AI director, drive the studio |
| `stage_create_scene`, `stage_edit_scene`, `stage_list_examples`, `stage_make_it_real` | Plan scenes in the free Stage 3D shot planner |
| `get_job`, `get_account` | Check a long job and see your credit balance |

Long jobs (video, image, edits, lip sync) return a job id; the assistant polls `get_job` until the result is ready.

## Developers

Prefer API keys and usage-based billing? See the KreatorFlow developer API and its MCP endpoint at https://kreatorflow.ai/seedance-api.

## Links

- Website: https://kreatorflow.ai
- MCP setup guide: https://kreatorflow.ai/mcp
- Support: https://kreatorflow.ai/support
