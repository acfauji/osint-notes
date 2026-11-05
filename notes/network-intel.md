# Network Intelligence

## DNS Zone Walking
```bash
# AXFR attempt (may fail if restricted)
dig axfr example.com @ns1.example.com

# DNS enumeration
dnsenum --enum example.com
fierce --domain example.com
```

## Certificate Intelligence
- CT logs reveal historical subdomains
- Expired certificates may reveal retired services
- SAN certificates reveal related domains
- `certspotter` API for continuous monitoring

## IP Intelligence
- Reverse DNS: `dig -x <ip>`
- ASN lookup: `whois -h whois.radb.io -i origin <asn>`
- GeoIP: `geoiplookup <ip>`
- Shodan host lookup: `shodan host <ip>`

## Email Infrastructure
- MX records reveal mail providers
- SPF/DMARC reveal email security posture
- DKIM selectors reveal signing domains
- DMARC policy reveals alignment strictness

## SSL/TLS Intelligence
- Certificate SAN fields reveal related domains
- Certificate transparency logs reveal historical certs
- Certificate issuer reveals CA preferences
- Certificate expiration reveals maintenance cadence
