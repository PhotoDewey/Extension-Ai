# AI - PhotoDewey Extension

AI-powered features for your photo library: tag suggestions from image analysis and automatic
tag-tree reorganization. Works with Anthropic (Claude), OpenAI, Google Gemini, and local Ollama.

---

## Features

- One-click AI tag suggestions from the photo's image and metadata
- Hierarchical tag paths (e.g. `nature/water/lake`) that fit PhotoDewey's tag system
- Reuses your existing tags as context so suggestions match your library
- Image description generated alongside tags (shown in the Properties dialog)
- Token usage shown after each analysis
- Photos that have been analysed are marked with an **AI** badge in the gallery and can be
  filtered with the **Has AI content / Missing AI content** filter in the gallery toolbar
- Re-analysis confirmation with date of last analysis shown
- AI-powered tag-tree reorganization: click the sparkle button in the Tag Hierarchy header
  to have AI propose a cleaner hierarchy, review the proposed changes, then apply with one click
- Full undo support for tag-tree reorganization
- Per-provider **Active** toggle in Settings
- Your API keys are stored encrypted (Windows DPAPI), per user

---

## Supported providers

| Provider | Requires API key | Notes |
|----------|-----------------|-------|
| Anthropic (Claude) | Yes | Vision support; rate limits shown in Settings |
| OpenAI | Yes | GPT-4o vision |
| Google Gemini | Yes | Gemini 2.5 Flash / Pro |
| Ollama | No | Local models; set host URL in Settings |

When more than one provider is marked **Active**, a small picker appears when you click the
AI button so you can choose which one to use for that run.

---

## Setup

1. Install the extension from the PhotoDewey **Extension Shop** (Help > Extension Shop), or drop
   `PhotoDewey.AI.dll` into `%AppData%\PhotoDewey\Extensions\` and restart.
2. Open **Settings > AI**.
3. Expand the provider you want to use, paste your API key, and click **Save**.
4. Click **Test** (the connection test runs automatically when you save a key). If the check
   passes, tick the **Active** checkbox next to the provider name.

For Ollama, set the host URL (default `http://localhost:11434`) and tick **Active** - no API key
needed.

---

## Suggesting tags for a photo

1. Select a photo.
2. Click the sparkle icon next to the **Add Tag** box.
3. The panel analyzes the photo and lists up to 15 suggested tags. Tick the ones you want.
4. Click **Apply Selected** - tags are added to the photo.

The photo now shows an **AI** badge in the gallery, and the analysis (tags, description, token
usage) is recorded on the **AI** tab of its Properties dialog. If the photo already has AI data,
you will be asked whether to re-analyze, and the date of the last analysis is shown.

---

## Reorganizing the tag tree

1. Open the **Tags** panel (right-hand side) and expand **Tag Hierarchy**.
2. Click the sparkle icon next to the **+** button.
3. The dialog sends your full tag hierarchy to the AI and proposes a cleaner structure.
4. Review the list of proposed moves/renames and the AI's rationale.
5. Click **Apply Changes** to restructure the tree. All photos follow their tags automatically.

The entire operation is recorded as a single undo step - press Ctrl+Z to restore the previous
hierarchy.

---

## Privacy

Suggesting tags for a photo sends a small thumbnail and metadata (filename, date, camera, GPS
place name, title, description) to the chosen provider's API. Reorganizing the tag tree sends
your tag paths as plain text - no photos or metadata. Nothing is sent until you click an AI
button. Your API keys never leave your machine except as authentication headers on those requests.

---

## Plugin Version

1.1
