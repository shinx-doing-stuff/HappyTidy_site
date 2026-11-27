# Happy Tidy level tools (static site)

Three pages, plain HTML, no build step:

- `index.html`: landing page
- `editor.html`: level editor (gen level, bot v2 APS, level sequence, bot test lab)
- `playtest.html`: playtest tool for human testers. The designer opens `playtest.html?admin=1`.

## Deploy on GitHub Pages
1. Create a repo on GitHub (public, or private on a paid plan).
2. Upload everything in this folder to the repo root, including the hidden `.nojekyll` file.
3. Go to Settings > Pages > Source: "Deploy from a branch", choose branch `main` and folder `/ (root)`, then Save.
4. After about 1 minute the site is at `https://<user>.github.io/<repo>/`.

## How data is stored on the static site
There is no shared database:
- The editor's level library and drafts stay in each person's browser. Use Lưu > Tải JSON to keep files.
- Playtest levels come from `playtest-levels.json`. To change them, open `playtest.html?admin=1`, edit the list in Quản lý level, click "Tải playtest-levels.json", and replace the file in the repo.
- Tester results stay in the tester's browser. The tester clicks "Tải file kết quả" and sends the file. The designer imports it in Kết quả > Nhập file kết quả.

Background images for maps HT_BG_41 and later are not included yet. Add them as `bg/HT_BG_<n>.webp` and `bgthumb/HT_BG_<n>.webp`.
