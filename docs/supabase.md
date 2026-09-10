# Cloud sync (Supabase)

Sign-in is optional. The timer works without it. This is only if you want the same sessions and settings on more than one Chrome profile.

The project already pointed at in the extension is:

`https://tiopzxojmnortiwbgfrx.supabase.co`

If that project is yours, skip to **Keys** and **SQL**. If it isn’t, make a new project and use that URL instead.

## 1. Project

1. Open [supabase.com/dashboard](https://supabase.com/dashboard) and sign in.
2. Open the existing project, or **New project**.
3. Wait until it is healthy.

## 2. Auth

1. **Authentication → Providers → Email** — turn it on.
2. For your own use, you can turn **Confirm email** off so Sign in works immediately. Leave it on if other people will create accounts.
3. **Authentication → URL configuration**
   - Site URL: `https://tiopzxojmnortiwbgfrx.supabase.co` (or your project URL)
   - Redirect URLs: add `https://tiopzxojmnortiwbgfrx.supabase.co/**`

Password reset opens in a browser. After they set a password, they come back to the extension and sign in.

## 3. SQL

1. **SQL Editor → New query**
2. Paste everything in `supabase/setup.sql`
3. **Run**

That creates `profiles`, `preferences`, and `sessions`, with row-level security so a user can only read their own rows. New signups get an empty profile and default preferences.

## 4. Keys

1. **Project Settings → API**
2. Copy **Project URL**
3. Copy the **anon / publishable** key (the public one). Not the service role key.

In the repo root, create `.env.local` (it is gitignored):

```
VITE_SUPABASE_URL=https://tiopzxojmnortiwbgfrx.supabase.co
VITE_SUPABASE_PUBLISHABLE_KEY=paste-the-anon-key-here
```

## 5. Rebuild

```bash
npm run build
```

Then **Reload** the unpacked extension on `dist`. Or `npm run package` and load the new zip.

Open Lahza → Settings → Account. Sign in should be amber. Create an account, then sign in on a second Chrome profile with the same email.

If the Account card says sign-in isn’t on this copy, `.env.local` was missing at build time, or you loaded an old `dist`.

## What syncs

- Display name
- Session lengths and the extras (long break, rounds, goal, auto-start, sound)
- Completed focus/break sessions

The running clock stays on the machine. Sync is for history and settings.
