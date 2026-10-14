# UniVerse — UNIZULU student community (independent)

A zero-dependency mobile-first website and installable Progressive Web App (PWA) prototype.

## Features
- Opportunities board with demo-labeled example cards, search, filtering, and campus selection.
- Marketplace with demo-labeled example listings, category search, and form to prepare a listing for operator review (no server or email receiver yet).
- Academic task planner: add, complete, remove, filter, export tasks; saved in browser localStorage.
- Responsive layout, installable PWA manifest and basic offline caching after hosted visit.
- Explicit disclaimer: not affiliated with or endorsed by UNIZULU.

## Test locally
Run `python3 -m http.server 8000` inside this folder, then visit `http://localhost:8000`. Static double-clicking index.html also works for most features, but PWA installation requires HTTPS or localhost.

## Publish at R0
1. Create an account on GitHub. Create a public repository and upload the files in this folder to its root.
2. In repository Settings > Pages, choose Deploy from branch, main, root. Your site will be available under the GitHub Pages URL after publishing.
3. On a compatible Android browser, open the HTTPS URL and choose `Install app` or `Add to Home screen`. iOS Safari supports `Add to Home Screen` for web apps, but installation behavior varies.
4. Before public promotion, replace example cards with real opportunities and manually reviewed listings; add operator contact email, privacy and moderation policies. The form currently DOES NOT send messages or submit them to any server. Don't collect ID numbers or other sensitive data in the early MVP.
5. Free tiers have limits; consult provider terms. Avoid using official university logos and any claim of partnership without permission.

## Next features requiring backend
Moderated submissions, user identities, reporting and abuse handling, notification preferences, cloud sync, security/privacy governance, payment provider (only once validated). Consider Supabase free tier after initial demand.

## Independent project
UNIZULU is a location/community descriptor only. This is not an official University of Zululand app.
