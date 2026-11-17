# Changelog - AI Extension

## v2.0 - 2026-11-17
- New: AI agent. A chat bubble in the bottom-right corner opens a chat panel where you can ask about your library (tags, people, dates, albums, edits, metadata, file locations) and have the agent look at photos and suggest improvements.
- Pick the provider and model directly in the chat.
- Optional changes (off by default, enable in Settings, AI tab): the agent can tag, rate, set titles and descriptions, manage album membership and apply non-destructive edits. Every change asks first by default, and each one is a single undoable History entry prefixed "AI agent:".
- Estimated cost line under every answer, and a new Usage section in Settings with monthly totals, a 30-day chart and breakdowns per model and feature.
- Updated model lists and prices for Anthropic, OpenAI and Google Gemini.
- Removed: Ollama support.
- Requires PhotoDewey 1.1 or later.

## v1.2 - 2026-11-16
- Added a user manual (Help > Extensions > AI).

## v1.1 - 2026-07-31

## v1.0 - 2026-07-18

## 1.1

- **Multi-provider support:** Anthropic (Claude), OpenAI (GPT-4o), Google Gemini 2.5, and
  local Ollama. Per-provider **Active** checkbox in Settings; a picker appears when more than
  one provider is active.
- **Image description:** each analysis now returns a short description of what is visible in the
  photo, shown on the AI Properties tab alongside the suggested tags.
- **Token usage:** input and output tokens are shown in the flyout after each analysis.
- **Re-analysis confirmation:** if a photo already has AI data, you are asked to confirm before
  re-running; the date of the last analysis is shown.
- **Tag-tree reorganization:** new sparkle button in the Tag Hierarchy header. Click to have AI
  propose a cleaner hierarchy; review the changes, then apply with one click. Full undo support.
- **Gallery filter:** the filter bar gains **Has AI content / Missing AI content** options
  (visible only when the AI module is installed and active).
- **Rate limit display:** Anthropic rate-limit headers are read after each call and shown in the
  Settings panel.
- **Provider-level error display:** API errors show an icon next to the provider name in Settings;
  the full error (including billing guidance for 400/402 responses) is in the expanded section.
- **Updated Gemini model IDs:** updated to `gemini-2.5-flash` / `gemini-2.5-pro` (1.5 retired).
- **Bug fix:** AI tag button stayed disabled even when a provider was active. Fixed by
  re-evaluating `CanExecute` on every selection change.
- **Bug fix:** clearing the API key field had no effect. Fixed by distinguishing an untouched
  masked field from an intentionally empty one.

## v1.0 - 2026-07-18

## 1.0

- Initial release.
- Suggest hierarchical tags for a photo using the Claude vision API.
- AI icon next to the tag input opens a review-and-apply suggestion panel.
- Per-photo analysis stored in the library; shown on an **AI** Properties tab.
- Analysed photos marked with an **AI** badge in the gallery.
- API key configured in **Settings > AI** (stored encrypted with Windows DPAPI).
