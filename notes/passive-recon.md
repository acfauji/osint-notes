# Passive Reconnaissance

Passive recon gathers information **without directly touching the target's systems** — no packets sent to their infrastructure.

## DNS Intelligence
| Tool | Purpose | Command |
|---|---|---|
| `dig` | Query DNS records | `dig +short A example.com` |
| `dnsrecon` | Comprehensive DNS sweep | `dnsrecon -d example.com` |
| `amass enum` | Passive subdomain collection | `amass enum -passive -d example.com` |
| `subfinder` | Fast subdomain discovery | `subfinder -d example.com` |

Key records to collect:
- **A/AAAA** — resolved IPs
- **MX** — mail servers (useful for phishing surface mapping)
- **TXT/SPF** — email security posture
- **CNAME** — hosted services (often reveals underlying providers)

## Certificate Transparency (CT Logs)
Public CT logs are a goldmine for subdomains. Anyone can query them without touching the target:
- `crt.sh` — web UI / JSON API: `https://crt.sh/?q=%25.example.com&output=json`
- `certspotter` — API-based monitoring
- `censys.io` — certificate + service search

## WHOIS
Reveals registration details: registrar, dates, registrant org (often redacted).
- `whois example.com`
- Look for: registrar, expiry, nameservers, historical changes (WHOIS history services)

## Search Engine Dorking
| Dork | Finds |
|---|---|
| `site:example.com` | All indexed pages |
| `site:example.com filetype:pdf` | Public PDFs |
| `site:github.com "example.com"` | Leaked code references |
| `inurl:admin site:example.com` | Admin panels |

## GitHub / Code Search
- `github.com/search` — search for company name, domain, key strings
- Look for: API keys, internal IPs, config files accidentally committed
- Use `trufflehog` / `gitleaks` on public repos

## Methodology Checklist
1. [ ] Enumerate root domain DNS records
2. [ ] Query CT logs for subdomains
3. [ ] Check WHOIS for registration details
4. [ ] Dork search engines for exposed assets
5. [ ] Search GitHub for leaked credentials
6. [ ] Document everything in a structured report
