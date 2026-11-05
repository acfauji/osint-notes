# Social Media Intelligence (SOCMINT)

## Profile Recon
- **Username search:** `sherlock` / `maigret` — check username across 300+ platforms
- **Email lookup:** `theHarvester -b all -d example.com` — gather associated emails
- **Reverse image search:** Google Images, TinEye — find other profiles using same photo

## Platform-Specific
| Platform | Techniques |
|---|---|
| LinkedIn | Company employees, job history, skills, location |
| GitHub | Repos, contribution graph, email in commits |
| Twitter/X | Handle chronology, engagement patterns, location hints |
| Instagram | Geotags, stories highlights, follower patterns |
| Facebook | Public groups, photos, check-ins |

## Profile Cross-Referencing
1. Collect identifiers: username, real name, email, phone, photo
2. Search each identifier across platforms
3. Correlate: same photo + same username = same person
4. Map connections: followers, follows, mentions

## Metadata Mining
- Download profile photos → check EXIF (GPS often stripped by platforms, but not always)
- Check public playlists, followers lists, groups

## Ethical Boundaries
- Only use **public** information
- Respect privacy laws (GDPR, local regulations)
- Do NOT attempt to access private accounts
- Document sources for every finding
