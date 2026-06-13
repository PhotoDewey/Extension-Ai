# AI Tag Suggestions — PhotoDewey Extension

Suggest hierarchical tags for your photos using Claude AI vision. Select a photo, click the small
**AI** icon next to the tag box, review the suggestions, and apply the ones you want with a single
click.

---

## Features

- One-click tag suggestions from the photo's image and metadata
- Hierarchical paths (e.g. `nature/water/lake`) that fit PhotoDewey's tag system
- Reuses your existing tags as context so suggestions match your library
- Review checklist — you choose which suggestions to apply
- Applied tags go through PhotoDewey's normal tag creation (with undo)
- Photos that have been analysed are marked with an **AI** badge in the gallery
- Each analysis is shown on an **AI Tags** tab in the photo's Properties dialog
- Your API key is stored encrypted (Windows DPAPI), per user

---

## Setup

1. Install the extension from the PhotoDewey **Extension Shop** (Help → Extension Shop), or drop
   `PhotoDewey.AiTagSuggestions.dll` into `%AppData%\PhotoDewey\Extensions\` and restart.
2. Get an Anthropic API key from <https://console.anthropic.com>.
3. Open **Settings → AI Tags**, paste your key, and click **Save**. Optionally choose a model
   (default: `claude-haiku-4-5-20251001`).

---

## Using it

1. Select a photo.
2. Click the **AI** icon next to the **Add Tag** box.
3. A small panel appears and lists suggested tags. Tick the ones you want.
4. Click **Apply Selected** — the tags are added to the photo.

The photo now shows an **AI** badge in the gallery, and the suggestions are recorded on the
**AI Tags** tab of its Properties dialog.

---

## Privacy

Requesting suggestions sends a small thumbnail of the photo plus its metadata to Anthropic. Nothing
is sent until you click the AI icon. Your API key never leaves your machine except as the
authentication header on those requests.

---

## Plugin Version

1.0
