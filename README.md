# Game privacy policies

One repo for the privacy policy of every game. Each game has its own folder, so
each game gets its own URL on GitHub Pages:

| Game | Folder | URL to paste into Play Console |
|---|---|---|
| Color Lab: Kids Painting | `color-lab/` | `https://<github-username>.github.io/game-privacy-policies/color-lab/` |
| Color Sort | `color-sort/` | `https://<github-username>.github.io/game-privacy-policies/color-sort/` |
| Grow Runner | `grow-runner/` | `https://<github-username>.github.io/game-privacy-policies/grow-runner/` |

Preview locally with MAMP: http://localhost:8888/game-privacy-policies/

## Publish (one time)

1. Create an empty **public** repo named `game-privacy-policies` on GitHub.
2. Push this folder:
   ```bash
   cd /Applications/MAMP/htdocs/game-privacy-policies
   git remote add origin git@github.com:<github-username>/game-privacy-policies.git
   git push -u origin main
   ```
3. On GitHub: Settings → Pages → Source **Deploy from a branch** → `main` / `/ (root)` → Save.
4. Wait a minute, then open the URLs above to check them.

## Add a new game

1. Make a folder named after the game in lowercase with dashes, for example `can-smash/`.
2. Put the policy in it as `index.html` (copy the game's `store/privacy-policy.html`).
3. Add a link to it in the list in the top-level `index.html`, and a row in the table above.
4. Commit and push. The new URL is live about a minute later.

## Change a policy

Edit that game's `index.html`, change the "Last updated" date at the top, commit and push.
The copy in this repo is the published one. Keep the game's own `store/privacy-policy.html` the same.

## Moving a game that is already on Google Play

The old privacy policy URL must keep working until Play Console points to the new one:

1. Publish this repo and check the game's new URL opens.
2. Play Console → the app → Policy and programs → App content → Privacy policy → paste the new URL → Save, then send the change for review.
3. Only after that change is live, archive or delete the game's old privacy policy repo.
