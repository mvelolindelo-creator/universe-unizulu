# UniVerse UNIZULU — Version 2 (account prototype)

Independent student community project. Not affiliated with or endorsed by UNIZULU.

## What's working
- Existing public opportunities, marketplace demo and local-only planner remain unchanged.
- New `account.html`: email sign-up, sign-in, email confirmation, password-reset request, sign-out, and private profile editing.
- Supabase `profiles` table protected with row-level security (RLS).

## Setup on Android
1. At https://supabase.com/dashboard create a free project. Keep your database password private.
2. Open SQL Editor > New query; paste `supabase-schema.sql`; Run.
3. In Supabase Authentication > Providers ensure Email is enabled. Keep email confirmation enabled.
4. In Authentication > URL Configuration set Site URL to `https://YOURUSERNAME.github.io/universe-unizulu/` and add redirect URL `https://YOURUSERNAME.github.io/universe-unizulu/account.html` (replace YOURUSERNAME).
5. Under Project Settings > API (or Connect > API keys, depending on dashboard) copy the Project URL and the public **publishable** key or legacy **anon** key. NEVER copy a `service_role` or `secret` key.
6. Edit `config.js` and replace the two PASTE values. These PUBLIC keys can be used in a browser only because RLS is enforced. Never disable RLS.
7. Upload the *contents* of this folder to the root of your existing `universe-unizulu` GitHub repository, replacing `index.html` and `README.md`, and adding `account.html`, `config.js`, `supabase-schema.sql`. GitHub Pages publishes from main/(root).
8. Open the public website, tap 'Student account', sign up with a test email, confirm the email, sign in, edit profile, sign out.
9. In Supabase Table Editor verify the new row in `profiles`. Test that unauthenticated visitors cannot access profile records.

## Important limits before a public launch
- This is a TEST prototype, not production-ready: add privacy notice/consent, retention and account deletion processes, POPIA compliance review, abuse protection, rate limits, moderation and monitoring.
- GitHub Pages is static. Supabase handles authentication and storage. Public publishable/anon key is normal; secret/service_role keys must NEVER be put in GitHub.
- Marketplace and opportunities still use demo content; no live listings or submissions.
- Planner tasks remain only on the device (localStorage), not linked to accounts.
- Password reset email requests work, but a dedicated password-update screen is not included yet; add this before public rollout.
- Email delivery quotas, free-tier limits and GitHub Pages terms may change.
