# AI - PhotoDewey Extension

AI-powered features for your photo library: an AI agent you can chat with about your library,
tag suggestions and descriptions from image analysis, and automatic tag-tree reorganization.
Works with Anthropic (Claude), OpenAI and Google Gemini.

> Requires PhotoDewey 1.1 or later.

---

## Features

- **AI agent:** a chat bubble in the bottom-right corner of the main window opens a chat panel.
  Ask about your library in plain language ("Which photos of Mormor have edits?") and the agent
  searches by tag, person, date, folder, rating, album, camera, place and more, reads metadata,
  faces and edits, and can look at photos to suggest improvements
- Pick the provider and model directly in the chat; switch mid-conversation without losing it
- Photo references in answers are clickable and reveal the photo in the gallery
- **Optional changes:** when you allow it in Settings (off by default), the agent can tag, rate,
  set titles and descriptions, sort photos into albums and apply non-destructive edits. By
  default every change waits for your OK on a confirmation card ("Don't ask again" available)
- **Improve with AI:** select 1 to 3 photos and click **Improve** in the chat. The agent analyses
  them, tries edits with the built-in tools without saving them, and saves the best result as a
  virtual copy next to the original. The original photo is not changed
- Every agent change is one entry in the History panel, prefixed "AI agent:", and is undone
  with Ctrl+Z. The agent can never delete, move or rename files, delete photos or tags, or
  change your settings
- **Estimated cost after every answer**, and a **Usage** section in Settings with monthly
  totals, a 30-day chart and breakdowns per model and feature (estimates in USD)
- One-click AI tag suggestions from the photo's image and metadata, as hierarchical tag paths
  (e.g. `nature/water/lake`) that reuse your existing tags
- AI image descriptions, written to the photo's Description field on request
- Analysed photos get an **AI** badge in the gallery and a **Has AI content / Missing AI
  content** filter
- AI-powered tag-tree reorganization from the Tag Hierarchy header, with full undo
- Your API keys are stored encrypted (Windows DPAPI), per user

---

## Supported providers

| Provider | Requires API key | Notes |
|----------|-----------------|-------|
| Anthropic (Claude) | Yes | Claude Haiku, Sonnet and Opus; rate limits shown in Settings |
| OpenAI | Yes | GPT-6 and GPT-4o models |
| Google Gemini | Yes | Gemini Flash, Flash-Lite and Gemini 4 models |

Ollama is no longer supported as of version 2.0.

A Claude Pro/Max or ChatGPT Plus/Pro subscription does not include API access. You need API
credits on the provider's developer website.

---

## Setup

1. Install the extension from the PhotoDewey **Extension Shop** (Help > Extension Shop), or drop
   `PhotoDewey.AI.dll` into `%AppData%\PhotoDewey\Extensions\` and restart.
2. Open **Tools > Settings > AI**.
3. Expand the provider you want to use, paste your API key and click elsewhere. The key is
   saved and the connection is checked.
4. Tick the checkbox in front of the provider name to make it active for tag suggestions.
5. Optionally choose the agent's default provider and model, and whether the agent may make
   changes.

---

## Chatting with the AI agent

1. Open a library and click the speech bubble in the bottom-right corner.
2. Choose a provider and model at the top of the panel.
3. Type a question and press **Enter**. Say "this photo" to mean the current selection.
4. Under each answer a muted line shows the estimated cost, for example
   `≈ $0.012 · 5,432 tokens in / 210 out · Claude Sonnet 5.5`.

The conversation is kept until you click **New conversation** or close PhotoDewey.

---

## Suggesting tags for a photo

1. Select a photo.
2. Click the sparkle icon next to the **Add Tag** box.
3. Tick the suggested tags you want and click **Apply Selected**.

---

## Reorganizing the tag tree

1. In the Tags panel, click the sparkle icon in the **Tag Hierarchy** header.
2. Review the proposed moves and renames.
3. Click **Apply Changes**. Ctrl+Z restores the previous tree.

---

## Privacy

Nothing is sent until you click a sparkle icon or send a question in the chat. Tag suggestions
send a small preview and some details of the photo. Tag-tree reorganization sends your tag paths
only. The agent sends your question and what it reads to answer it (file names, folders, tags,
people, albums, descriptions, places, face positions, edits), plus a preview of any photo it
looks at. Your API keys never leave your machine except as authentication headers on those
requests.

---

## Plugin Version

2.0
