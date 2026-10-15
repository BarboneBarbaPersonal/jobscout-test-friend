# JobScout-Template - spec

Date: 2026-10-15. The shareable version of JobScout. Andrea's own version
(`BarboneBarbaPersonal/JobScout`, with Like and CV insights) stays as it is.

## Goal
A non-technical person gets their own job board in about 8 minutes, with a Google
account and a free GitHub account, and no knowledge of GitHub.

## What a new user does (the whole guide)
Part 1 - Google Sheet
1. Copy the template sheet, fill in Preferences and Companies.
2. Share it: "Anyone with the link", Viewer. Copy the link.

Part 2 - GitHub
3. Click "Create my JobScout" -> GitHub's "create from template" page -> name, Public, Create.
4. Type your GitHub username on the guide page, click "Add my sheet link" -> GitHub's
   "New secret" page: name `SHEET_URL`, value = the sheet link, Add secret.
5. Click "Start my first scan" (or wait: it runs every hour by itself).
   Your page: `https://<username>.github.io/<repo>/`.

Nothing else: no "enable Actions", no Pages settings, if GitHub allows the workflow to
switch Pages on by itself (to be tested; if not, one extra step with a direct link).

## Differences from Andrea's version
- No Like, no CV insights, no CV add-on setting, no shared hidden list (Hide is kept
  in the browser only).
- Pages are published by GitHub Actions directly (no gh-pages branch). The previous
  board is read back from the live page to keep each job's "found" date.
- When something is missing (no secret, sheet not shared), the page itself says so
  in plain words instead of showing a 404.
- The template project's own page is the setup guide:
  `https://barbonebarbapersonal.github.io/JobScout-Template/` - this is the link to share.

## Unchanged
Same scanner (`scout/`), same sheet format, same matching rules, same tests.

## Done means
- A test project created from the template by following the guide works end to end:
  status page before the secret, board after the first scan.
- Guide checked on phone width. Tests pass.
