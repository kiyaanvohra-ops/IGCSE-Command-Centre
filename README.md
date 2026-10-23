# IGCSE Command Centre

A responsive study planner for Cambridge IGCSE subjects with subject selection, syllabus/topic tracking, a revision calendar, study logs, revision tips, and Supabase cloud sync.

## Publish with GitHub Pages

1. Open this repository on GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**.
4. Choose branch **main** and folder **/(root)**, then click **Save**.
5. Wait for GitHub Pages to publish. The URL should be:

   https://kiyaanvohra-ops.github.io/IGCSE-Command-Centre/

6. In Supabase, open **Authentication → URL Configuration** and set **Site URL** to the published site URL. Add the same URL to **Redirect URLs**.

## Supabase setup

- The site has a **Cloud sync** section where you enter the Supabase Project URL and browser-safe publishable key.
- Run the supplied `supabase_schema.sql` in the Supabase SQL Editor if the table and policies have not already been created.
- Keep Row Level Security enabled and ensure policies restrict each row to `auth.uid()`.
- Never put a Supabase service-role or secret key in this public website.
- Configure SMTP in Supabase if you want reliable account confirmation email delivery.

## Privacy

The main planner is hidden while signed out. Cloud progress should be tested after signing in on two separate browsers. Do not rely on browser-local storage as a substitute for the authenticated Supabase record.
