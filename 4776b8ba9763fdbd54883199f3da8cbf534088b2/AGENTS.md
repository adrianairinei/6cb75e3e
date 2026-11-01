# Fridge board — instructions for AI assistants (ChatGPT, Claude, etc.)

This folder is a public web page (GitHub Pages) shown on a family fridge touchscreen. The page reloads `data.json` every 10 seconds.

## How to update the board
1. Edit **only** `4776b8ba9763fdbd54883199f3da8cbf534088b2/data.json`. Do not touch `index.html`, this file, any other file, or any other repository.
2. Keep the schema exactly:
   ```json
   {
     "title": "Fridge board",
     "updated": "2026-11-01T09:40:00+01:00",
     "sections": [
       { "heading": "Section name", "items": ["line 1", "line 2"] }
     ]
   }
   ```
   - `title`: string. `updated`: ISO 8601 time **in Europe/Brussels** with its offset (+01:00 in winter, +02:00 in summer), set to the moment of your edit.
   - `sections`: array of `{heading: string, items: [strings]}`. Items are plain text only (no HTML).
3. Must stay valid JSON (double quotes, no trailing commas, no comments).
4. Commit directly to `main` with a short message, e.g. "Update fridge board". GitHub Pages deploys automatically; the fridge shows it within about 1 minute.

## Never
- Never add sensitive information: no addresses, phone numbers, health/medical details, passwords, codes, door/alarm info, schedules that reveal when the house is empty, financial info. **This page is public on the internet.**
- Never change the folder name, link to this page from elsewhere, or edit other files or repos.
