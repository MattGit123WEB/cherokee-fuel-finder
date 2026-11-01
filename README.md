# Cherokee Fuel Finder

A static, mobile-friendly Chevron and Texaco station locator for Cherokee County, Georgia.

## Files
- `index.html` — complete interactive website
- `stations.json` — editable station directory

## Publish with GitHub Pages
1. Create a new GitHub repository (or use an existing repository).
2. Upload `index.html` and `stations.json` to the repository root.
3. Open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select branch `main` and folder `/ (root)`, then save.
6. Wait for GitHub Pages to publish the site. The URL will look like `https://YOUR-USERNAME.github.io/REPOSITORY/`.

## How it works
- Leaflet renders the interactive map.
- OpenStreetMap supplies the map tiles.
- Address geocoding uses the public Nominatim service, one request at a time with a delay, and caches successful results in the browser.
- Google Maps links provide turn-by-turn navigation.
- Browser geolocation powers the **My location** button. Location permission generally requires HTTPS, which GitHub Pages provides.

## Editing stations
Edit `stations.json`. Each item uses:
`id`, `brand` (`Chevron` or `Texaco`), `name`, `address`, `phone`, and `source`.
Use unique IDs. Addresses are geocoded when the page loads; successful coordinates are cached in local storage. Clear the site's local storage if you change an address and need it geocoded again.

## Important data note
The included directory is a researched starter list, not a guaranteed complete or officially verified inventory. Listings, brands, phone numbers, and operating status can change. One listing (727 Hickory Rd) has inconsistent brand information in public directories and is flagged for verification. Check a station's branding before relying on it.

## Attribution and service limits
Map tiles and map data © OpenStreetMap contributors. Nominatim is a community geocoding service; it may be rate-limited or unavailable. This project intentionally geocodes sequentially and caches results. Do not turn this into a high-traffic geocoding service without arranging an appropriate provider.
