# Ultimate O & X — Five in a Row
By Y Pengly · v1.1.0

## Run locally
Open `index.html` in any modern browser (Chrome, Edge, Firefox, Safari). No install or internet needed.
Optional local server: `python3 -m http.server 8000` then visit http://localhost:8000

## Deploy online
Upload the folder to Netlify Drop, GitHub Pages, Vercel or Cloudflare Pages. It is a static site (just `index.html`).

## Features
Unlimited board (drag, wheel/pinch zoom), vs AI (8 levels), Friendly Match (names, scores, undo, rematch), Hint button,
8 themes, statistics and history, sound/music/animation settings, responsive for phone, tablet and desktop. Data is stored in localStorage.

## AI system
1 Beginner: random near stones. 2 Easy: wins/blocks fours, else random. 3-4: pattern scoring of every candidate (offense + defense).
5-8: minimax + alpha-beta over the best-ranked candidates, depth 2/2/3/4, with open/closed three and four evaluation.
All levels 3+ take immediate wins and block immediate losses.

## Testing checklist
- Horizontal, vertical and both diagonal 5-in-a-row wins; 4 does not win; 6 wins
- Occupied cells rejected; board panned far away keeps working
- AI wins when it can and blocks open fours (levels 3-8)
- Undo (both modes), Hint, pause/resume/restart/draw/exit
- Reload: theme, settings, stats, history persist
- Phone: pinch zoom, one-finger drag, tap to place, no page scroll
