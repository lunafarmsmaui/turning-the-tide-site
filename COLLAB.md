# Collaboration guide — Turning the Tides website

Two people work on this repo. To avoid stepping on each other:

## One-time setup (per machine)

1. Open **PowerShell** and install GitHub CLI:
   ```
   winget install GitHub.cli
   ```
   Close and reopen PowerShell when done.

2. Authenticate as `lunafarmsmaui`:
   ```
   gh auth login
   ```
   Choose **GitHub.com** → **HTTPS** → **Yes** (browser auth) → press Enter → authorize in browser.

3. Clone the repo wherever you want it:
   ```
   git clone https://github.com/lunafarmsmaui/turning-the-tide-site.git
   ```

4. Open the folder in VS Code (File → Open Folder).

## Daily workflow

**Always start a session with:**
> "Claude, pull latest from main before we start"

**Always end a session with:**
> "Claude, commit this with message X and push"

Vercel auto-deploys ~30 sec after each push.

## Live URLs

- Production: `https://turning-the-tide-site.vercel.app`
- Custom domain: `https://trningthetides.org` (once DNS finishes propagating)

## If git complains about a conflict

That means we both edited the same file before pulling. Tell Claude:
> "There's a merge conflict — fix it, keeping the most recent change to the conflicting section."

Then commit + push as usual.

## The one rule

**Pull before editing.** It's the only way to avoid conflicts.
