# Geolocation & Image Analysis

## EXIF Metadata
| Field | Value |
|---|---|
| GPSLatitude/GPSLongitude | Exact coordinates (if not stripped) |
| DateTimeOriginal | When photo was taken |
| Make/Model | Camera/device used |
| Software | Editing software used |

Tools: `exiftool`, `metadata_extract.py` (in security-toolkit)

## Reverse Image Search
- Google Images (images.google.com)
- TinEye (tineye.com)
- Yandex (yandex.com/images) — often best for people/landmarks

## Landmark Identification
- Compare photo with known landmarks via reverse search
- Look for: street signs, unique architecture, language on signage
- Use `Google Lens` for real-time identification

## Photo Context Analysis
- **Weather** — clouds, sun angle → approximate date/season
- **Time of day** — shadows direction → approximate time
- **Environment** — vegetation, vehicles, clothing → region estimate
- **Networks** — nearby Wi-Fi (via Wardriving databases, if applicable)

## Social Media Location Mining
- Check geotags on public posts
- Story locations (Instagram highlights)
- Check-in history (Foursquare/Swarm public check-ins)
- Photo backgrounds compared across profiles

## Verification
Cross-check multiple independent sources before concluding a location. One match is coincidence; multiple matches are evidence.
