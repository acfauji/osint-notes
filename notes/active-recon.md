# Active Reconnaissance

Active recon sends traffic to the target. **Only perform with authorization.**

## Host Discovery
| Tool | Command |
|---|---|
| `ping` | `ping -c 3 <ip>` |
| `nmap -sn` | `sudo nmap -sn 10.0.0.0/24` — ping sweep |
| `fping` | `fping -a -g 10.0.0.0/24` — fast sweep |

## Port Scanning
| Scan | Command | Use |
|---|---|---|
| TCP Connect | `nmap -sT <target>` | Stealth not required |
| SYN | `sudo nmap -sS <target>` | Faster, semi-stealthy |
| Service version | `nmap -sV <target>` | Identify software versions |
| OS detection | `sudo nmap -O <target>` | Fingerprint OS |
| Top 1000 | `nmap --top-ports 1000 <target>` | Common services |

Common sensitive ports to check: 22, 80, 443, 3306, 3389, 5432, 6379, 8080, 8443, 9200.

## Service Enumeration
After finding open ports, banner grab:
```bash
nc -nv <target> <port>
```
Or use nmap scripts:
```bash
nmap -sC -p <port> <target>   # default scripts
nmap --script=http-title -p 80,443 <target>
```

## Web App Discovery
| Tool | Purpose |
|---|---|
| `gobuster dir` | Directory brute-force |
| `ffuf` | Fast fuzzing (dirs, vhosts, params) |
| `nikto` | Web server scanner |
| `whatweb` | CMS/platform fingerprinting |
| `wappalyzer` (browser) | Tech stack detection |

## Network Mapping
- `traceroute` / `mtr` — path mapping
- `whois` on discovered IPs — ASN / hosting provider
- Reverse DNS — `dig -x <ip>`

## Methodology Checklist
1. [ ] Ping sweep to find live hosts
2. [ ] Port scan each live host (top 1000)
3. [ ] Service/version detection on open ports
4. [ ] Banner grabbing for additional details
5. [ ] Web app discovery on 80/443
6. [ ] Document findings with IP:port:service
