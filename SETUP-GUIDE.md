# 🚀 Full Setup Guide — Your Animated ML Profile

Everything you need to get the profile live, end to end.

---

## ❓ Do I need to delete the repo I already made?

**No — don't delete it.** You already created the `misbahee/misbahee` repo and the
snake is already working there. Deleting it would throw away the snake's `output`
branch and your commit history. Instead, you'll just **overwrite the files** with
this updated set. Git handles that cleanly.

---

## 📁 Final Repo Structure

Your `misbahee` repo should end up looking exactly like this:

```
misbahee/                         ← repo name = your username (the "magic" repo)
├── README.md                     ← the profile (ML Systems, personalized)
├── assets/
│   └── banner.svg                ← your custom animated hero banner 🎨
└── .github/
    └── workflows/
        ├── snake.yml             ← generates the contribution snake 🐍
        └── profile-3d.yml        ← generates the 3D contribution city 🌆
```

That's it — 4 files. Everything else (the snake images on the `output` branch,
the `profile-3d-contrib/` folder on `main`) is created **automatically** by the
workflows. You never add those by hand.

> ⚠️ **The `assets/banner.svg` path matters.** The README loads the banner from
> `raw.githubusercontent.com/misbahee/misbahee/main/assets/banner.svg`. Keep the
> file at `assets/banner.svg` on the `main` branch or the banner won't show.

---

## 🛠️ Setup — Step by Step

### Step 1 — Replace the files in your repo
Upload/replace these three files, keeping the folder structure above:
- `README.md`
- `.github/workflows/snake.yml`
- `.github/workflows/profile-3d.yml`

**Easiest way (web):** open your repo → click a file → pencil ✏️ icon → paste the
new contents → **Commit changes**. Repeat for each file. To add a new file in a
folder, click **Add file → Create new file** and type `.github/workflows/snake.yml`
as the name — GitHub creates the folders for you.

### Step 2 — Fill in the last few blanks in `README.md`
Most of it is already filled from your LinkedIn (name, location, education, Cafe
Kithabi, skills, LinkedIn link). Only two things left — search for `[YOUR-EMAIL]`
and `[ADD:`:
- `[YOUR-EMAIL]` — your email in the Connect section (once, e.g. `mailto:you@gmail.com`)
- `[ADD: ...]` — the project bullets: your real metrics, models used, results, and a
  one-line description of **BroWorld**. Fill these in when you can — they make the
  projects hit much harder than generic text.

_(Name, location, B.Sc. Mathematics, Cafe Kithabi background, LinkedIn `misbahtv`,
and your skills are all already in.)_

### Step 3 — Turn on write permission for Actions
Repo → **Settings → Actions → General → Workflow permissions** →
select **"Read and write permissions"** → **Save**.
(Your snake already committed, so this is likely on — but confirm.)

### Step 4 — Run the two workflows once
Repo → **Actions** tab:
1. Click **"Generate Contribution Snake"** → **Run workflow** (it may already be done).
2. Click **"Generate 3D Contribution Graph"** → **Run workflow**.

Wait ~1–2 minutes each. When they finish (green ✓), refresh your profile —
the snake 🐍 and the 3D city 🌆 will both show. They auto-refresh daily after this.

---

## ✅ How to know it worked
- Go to `github.com/misbahee` — the README renders with header wave, typing text,
  stats cards, snake, and 3D graph.
- If the snake or 3D image is a broken icon, its workflow hasn't finished a
  successful run yet → re-check **Step 3 & 4**.

---

## 🐞 Troubleshooting
| Problem | Fix |
|---|---|
| 3D / snake image broken | Run the workflow (Step 4); confirm write permission (Step 3) |
| Workflow run shows red ✗ | Open the run → read logs. Usually "read and write permissions" is off |
| Stats cards blank sometimes | The vercel services rate-limit occasionally; they recover on their own |
| Placeholders showing on profile | You missed a `[YOUR ...]` / `[ADD: ...]` — search the README again |

---

## 🎨 Optional upgrades (whenever you want)
- **lowlighter/metrics** — a big dashboard SVG (isometric calendar, language & habit
  breakdowns). Needs one extra workflow + a personal access token. Ask me and I'll set it up.
- **WakaTime** — real weekly coding-time stats by language.
- **Custom hand-coded SVG banner** — a unique glowing animated header no template offers.
