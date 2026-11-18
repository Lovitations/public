# Lovitations

Skills for the paperwork of a wedding: the words, the guests and the day.
They work in Claude (the Claude app and Claude Code), ChatGPT and Codex,
Gemini CLI and Grok Build.

| Area | Skill | What it does |
|---|---|---|
| Words | `invitation-wording` | The text for a save-the-date or invitation, with a separate version per guest group (for example day and evening guests). |
| Words | `wedding-website-copy` | The pages of a wedding website: welcome, story, programme, travel, dress code, gifts, RSVP and FAQ. |
| Words | `wedding-speech` | A speech or toast from the speaker's own stories, timed to the minutes they have. |
| Guests | `guest-list` | A guest list with households, parts of the day, plus-ones, children and dietary needs, with real headcounts. |
| Guests | `rsvp-followup` | Who is coming, who hasn't answered, the numbers and dietary needs for the caterer, and reminder drafts. |
| Guests | `seating-plan` | A table-by-table seating plan that keeps every hard rule and says which wishes it could not meet. |
| The day | `wedding-day-schedule` | A minute-by-minute schedule with travel time, buffers and an owner per moment, plus a short programme for guests. |
| The day | `wedding-budget` | A budget from the couple's quotes, split into fixed costs and costs per guest, with what each extra guest costs. |

Ask in plain language, for example "write our wedding invitation", "how many
evening guests do we have" or "maak een draaiboek voor onze trouwdag".

## Install

| Where | How |
|---|---|
| Claude (app) | Download `lovitations-<version>.zip` from the [latest release](https://github.com/lovitations/public/releases/latest) and upload it under Customize → Plugins. |
| Claude Code | `/plugin marketplace add lovitations/public`, then `/plugin install lovitations@lovitations` |
| Codex | `codex plugin marketplace add lovitations/public`, then `codex plugin add lovitations@lovitations` |
| Gemini CLI | `gemini extensions install https://github.com/lovitations/public` |
| Grok Build | Grok Build reads Claude Code marketplaces: add this repository as a marketplace source, then install `lovitations` from the Marketplace tab. |

## Languages

The skills answer in the language you write in (Dutch, English, Spanish,
German or any other) and follow the customs of the country you marry in.

## What these skills do and do not do

- **They work from what you give them** in the conversation: lists, quotes,
  notes, replies, spreadsheets. They don't search your mail or files on their
  own.
- **Missing facts are marked as missing.** The skills are written to flag a
  date, amount, name or story that isn't in your material rather than make it
  up. Check the output before you rely on it.
- **They draft, you send.** The plugin has no way to send email, messages or
  invitations. Reminders and texts come back as drafts.
- **They ask before creating or changing a file**, and only where the
  environment allows it. A spreadsheet you share is left as it is; a new
  version is saved as a new file.
- **No network calls, no data collection, no credentials.** The plugin is
  plain instructions. Your data goes only where your Claude or ChatGPT setup
  already sends it.

## Optional tools

Creating and reading `.xlsx` files works where the environment can run Python
(for example with `openpyxl`). Without that, the skills give you a table to
paste instead.

## About Lovitations

These skills come from [Lovitations](https://lovitations.nl): digital
save-the-dates, invitations and wedding websites with a personal link per
guest, a live RSVP dashboard and day and evening guests built in.

## Support and privacy

- Free wedding tools: https://lovitations.nl/gratis-bruiloft-tools
- Support: https://lovitations.nl/contact
- Privacy statement: https://lovitations.nl/policies/privacy-policy
- Mail: info@lovitations.nl

## License

MIT. See `LICENSE`.
