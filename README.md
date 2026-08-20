# Alliance Layout Planner

**Alliance Layout Planner** — a free, browser-based territory/layout planner for **Kingshot** (Century Games). Unlike single-alliance planners, this one puts **several alliances on one shared kingdom map**, each color-coded, so you can plan KvK positioning, castle sieges, and kingdom-wide territory splits.

Inspired by the WOS Nerds layout planner for Whiteout Survival.

## Features

- **Multiple alliances on one map** — add as many as you need, each with its own name, color, and visibility toggle
- **Alliance buildings**: HQ (shows the alliance name on the map), banners, member cities, traps/rally points, alliance resource nodes
- **Player names on cities** — double-click a member city and type the player's name; it renders inside the city square (and below it when zoomed out). Century Games removed their public player-lookup API in July 2026, so automatic name/avatar verification is not possible — names are entered manually.
- **March times** — select a trap (or place one) to see dashed march lines with travel times from every member city of that alliance (a grouped trap shows only its own hive); calibrate the speed in Settings
- **Quick layouts: bear-trap hives** — one-click placement of two imported hive configurations: the **swirl** (50 cities, 7 banners) and the **banner-pad** (50 cities, 10 banners). Your original banners are kept and extra banners added so every TC sits fully in territory. Each hive is placed as a group — drag anywhere as one unit, Ungroup to customize.
- **Grouping** — shift-click to multi-select, Group to make any buildings move as one, Ungroup to break apart; clicking any grouped building selects its whole group
- **Alliance award statues** — Golden Guardian, Pioneer, Sword of Kings, Horn of Victory, and Champion's Will (2×2 each) placeable in territory
- **Real Kingshot map overlay** (toggleable) — the actual 1200×1200 map baked in: 67k mountain tiles and 23k lake tiles (unbuildable), King's Castle + turrets, all 90 permanent structures (4 fortresses, 12 sanctuaries, outposts, frontier lodges) with their no-build zones. In-game placement rules are enforced: nothing on terrain/structures/King's zone, no alliance buildings, nodes or traps in the Ruins ring, HQs only in Plains/Badlands, banners blocked in structure forbidden zones (cities exempt at fortresses/sanctuaries). Map data extracted from the community ksmapper dataset.
- **Resource levels view** — shades the concentric zone rings (Badlands → Plains → Fertile → Ruins → Forbidden) with a legend of which ring holds which node quality
- **Per-alliance caps** — 285 banners and 100 TCs per alliance, enforced on placement; each alliance row shows a live `TC x/100 · B x/285` count
- **Real resource node spawns** — all 6,499 map nodes (Bread / Wood / Stone / Iron) drawn in place and unbuildable
- **Legend** — collapsible sidebar reference for every symbol: your buildings, all structure abbreviations (F, SA, BG, DO, RO, AO, GO, PO, TO, FL…), terrain, nodes, and overlays
- **Box select & grouping** — drag a box over buildings to select them all, Group/Ungroup, erasing any grouped building removes the whole group (undo restores it)
- **TC block stamp** — pick columns × rows and place that many member cities in one click as a movable group
- **Auto-config (full alliance)** — pick a bear layout and drop a complete alliance in one click: 1 HQ, 2 bear traps, all 100 TCs, and its banners. Both styles are built from your imported hives, mirrored into a twin-trap alliance around a central HQ whose 15×15 territory helps cover the interior: **Swirl** (100 TCs, 14 banners), **Banner-pad** (100 TCs, 18 banners). Every TC sits fully in territory. Select a layout and a spot to preview a green/red ghost on the map, then "Place here" to commit. The 4 spots are ranked by closeness to the King's Castle, respecting the rule that HQs may only sit in the Plains ring, never Fertile. Placed as a group on an empty alliance.
- **Neutral landmarks**: King's Castle, turrets, fortresses, resource nodes, obstacles — place them wherever they sit on your server's map
- **Territory coverage** — HQ and banners auto-draw their coverage area in the alliance color so you can see connections and gaps
- **Editing QoL** — undo/redo, drag to move, mouse-wheel zoom, pan, erase, double-click to name a building
- **PNG export** with an alliance legend, ready to post in alliance chat or Discord
- **Save / Load** layouts as `.json` files to share with co-leads; work also auto-saves in your browser
- **Adjustable sizes** — building footprints and coverage radii are estimates and vary by server generation, so everything is editable in Settings

Everything runs client-side in a single HTML file. No server, no accounts, no tracking.

## Host it on GitHub Pages (free)

1. Sign in to [github.com](https://github.com) and click **New repository**.
2. Name it anything (e.g. `alliance-layout-planner`). Keep it **Public**. Click **Create repository**.
3. On the new repo page, click **uploading an existing file**, drag in `index.html` (and this `README.md`), and click **Commit changes**.
4. Go to **Settings → Pages** (left sidebar).
5. Under **Build and deployment → Source**, choose **Deploy from a branch**; set Branch to `main` and folder to `/ (root)`. Click **Save**.
6. Wait a minute or two, then refresh — GitHub shows your site URL at the top of the Pages settings:
   `https://<your-username>.github.io/alliance-layout-planner/`

Share that link with your alliance. Any update you push to `index.html` goes live automatically within a minute or so.

### Optional: custom domain

In **Settings → Pages → Custom domain**, enter your domain and add a CNAME record at your DNS provider pointing to `<your-username>.github.io`.

## Usage tips

- Click an alliance row in the sidebar to make it **active** — new buildings belong to it.
- Click a building type, then click the map to place. Keep clicking to place more; `Esc` or right-click to stop.
- Drag empty ground (or middle-mouse drag) to pan; mouse wheel zooms.
- `V` select · `H` pan · `E` erase · `Del` delete selected · `Ctrl+Z` / `Ctrl+Y` undo/redo.
- Check **Settings** to correct footprint sizes and banner/HQ coverage for your server generation — defaults are estimates.

## License

MIT — do whatever you like with it.
