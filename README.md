# My Pretty Cain — Mood Check

A static mood-check page designed for GitHub Pages, with private responses stored in Supabase.

## 1. Create the database
1. Open your Supabase project.
2. Open **SQL Editor** and run `supabase.sql`.
3. In **Project Settings / API**, copy the Project URL and publishable/anon key.

## 2. Connect the website
Open `index.html` and replace:
- `YOUR_SUPABASE_URL`
- `YOUR_SUPABASE_PUBLISHABLE_KEY`

The publishable/anon key is designed to be used in a browser. Never put a Supabase service-role key or GitHub personal access token in this file.

## 3. Publish with GitHub Pages
1. Create a GitHub repository.
2. Upload `index.html`, `supabase.sql`, and this README.
3. In the repository, open **Settings → Pages**.
4. Under **Build and deployment**, choose **Deploy from a branch**.
5. Select `main` and `/ (root)`, then Save.

GitHub hosts the site. Supabase stores the responses.

## Privacy model
The SQL enables anonymous INSERT only. There is no anonymous SELECT policy, so visitors cannot query saved responses using the public browser key. Read the responses while signed into your Supabase project.
