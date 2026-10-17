# Match data format

`data/matches.json` is the source of match rows displayed by the site.

## Rules
- Add a row only after checking a reliable source (prefer league or club official records).
- Never invent scores, dates, or teams.
- An empty `matches` array means no records have been entered here yet; it does not mean no matches were played.
- Keep the source URL for each row whenever possible.
- `competition_id` should match the UI ID: `jfl`, `regional-<region-id>`, or `pref-<region-id>`.

## Match record fields
- `competition_id`: competition key used by the interface
- `season`: season year (number)
- `date`: match date in YYYY-MM-DD format
- `home_team`, `away_team`: team names as published by the source
- `home_score`, `away_score`: integer scores
- `source_url`: URL supporting the record

Example structure only (not a real result):
```json
{
  "schema_version": 1,
  "matches": [
    {
      "competition_id": "jfl",
      "season": 2026,
      "date": "YYYY-MM-DD",
      "home_team": "ホームチーム名",
      "home_score": 0,
      "away_score": 0,
      "away_team": "アウェイチーム名",
      "source_url": "https://example.com/"
    }
  ]
}
```
