# Social Media Intelligence (SOCMINT)

## Profile Discovery
| Tool | Purpose | Command |
|---|---|---|
| `sherlock` | Username across 300+ platforms | `sherlock username` |
| `maigret` | Detailed dossier generation | `maigret username` |
| `theHarvester` | Email/domain enumeration | `theHarvester -d example.com -b all` |

## Platform Recon Guide

### LinkedIn
- Employee enumeration: `site:linkedin.com/in "Example Corp"`
- Job postings reveal tech stack
- Alumni pages show former employees

### GitHub
- Commits may leak emails: `git log --format="%ae" | sort -u`
- Repository descriptions reveal project names
- Fork history shows original author

### Twitter/X
- Handle chronology reveals account age
- Engagement patterns reveal active hours
- Location tags in media metadata

### Instagram
- Geotags reveal location history
- Stories highlights are publicly archived
- Tagged photos reveal associates

## Metadata Mining
- Download profile photos → `exiftool photo.jpg` for GPS
- Check `DateTimeOriginal` for activity windows
- Look for `Software` field for editing tools

## Verification Checklist
- [ ] Cross-reference with 2+ independent sources
- [ ] Verify timestamps match claimed activity
- [ ] Document source URL for each finding
- [ ] Note when data was collected (for staleness)

## Ethical Boundaries
- Public information only — no credentialed access
- Respect GDPR and local privacy laws
- Do not attempt account takeover or social engineering
- Document everything for audit trail
