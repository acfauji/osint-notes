# Tools Quick Reference

## Amass
```bash
# Passive enum
amass enum -passive -d example.com

# Active enum (authorized only)
amass enum -active -d example.com

# Output to file
amass enum -passive -d example.com -o subdomains.txt
```

## Subfinder
```bash
subfinder -d example.com -silent
subfinder -d example.com -o subs.txt
```

## Shodan
```bash
# Search by host
shodan host <ip>

# Search by service
shodan search "port:22 country:ID"

# Search by organization
shodan search "org:\"Example Corp\""
```

## theHarvester
```bash
theHarvester -d example.com -b all -f report.html
```

## Sherlock (username search)
```bash
sherlock username
sherlock --timeout 5 username1 username2
```

## Amass + Subfinder integration
```bash
subfinder -d example.com -silent | amass enum -passive -d example.com -config config.ini
```

## Gitleaks (secret scanning)
```bash
gitleaks detect --source /path/to/repo --report-path report.json
```
