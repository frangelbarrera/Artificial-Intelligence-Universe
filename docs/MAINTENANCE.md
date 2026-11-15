# Catalog Maintenance

This repository is curated, not merely collected. Every update should improve discovery, accuracy, and reader trust.

## Review before adding or changing an entry

- Use a direct official product page, official documentation, or canonical repository URL.
- Confirm the destination is publicly available and relevant to the category.
- Use one factual sentence, end it with a period, and keep it within 120 characters.
- Search the README for duplicates and place the entry in the most specific category.
- Do not accept listings whose primary value is a backlink, referral placement, or dofollow link.

## Link-health review

Run a link-health review before large catalog updates and at least once per quarter. Treat HTTP 404 and 410 responses as confirmed breakage; replace them with a verified official destination or remove the entry. Treat timeouts, TLS failures, 403 responses, and rate limits as manual-review candidates, not automatic deletions.

## Frontier model snapshot

The frontier model section is a dated editorial snapshot, not a universal leaderboard. Each row must link to a primary source and use descriptive language. Do not add a ranking, price, or benchmark score unless its source, metric context, and verification date are explicit.

## Release checklist

1. Check changed Markdown links and anchors.
2. Confirm all changed descriptions follow the canonical format.
3. Update the dated model snapshot only after checking each primary source.
4. Review the diff for duplicate entries, marketing language, and stale product names.
5. Record the scope of the update in a concise English commit message.
