# GitHub Profile View Counter

![Banner](assets/banner.png)

A self-hosted, fully customizable SVG view counter for your GitHub README. Built with **Vercel** + **Supabase** — free, fast, supports multiple users, supports repository visit count.

---

## ✨ Features

- **Profile visitor's count** — each GitHub user gets their own count
- **Repository visitor's count** — each GitHub repo gets its own count
- **No signup required** — just add your username to the URL
- **Fully customizable** — colors, styles, layout, font size, icon, etc
- **Multiple layouts** — horizontal, vertical, split
- **Multiple styles** — rounded, square, no background, invisible
- **Abbreviated counts** — 12345 → 12.3K
- **Base count** — add an offset to your counter
- **Invisible mode** — count silently without showing anything


---

## 🚀 Quick Start

### Add to GitHub Profile

Add this to your GitHub profile `README.md`:
```markdown
![](https://view-counter-livid.vercel.app/api?username=your-username)
```

> [!IMPORTANT]
> Replace `your-username` with your actual GitHub username.

---

### Add to a GitHub Repository

Add this to your repository's `README.md`:
```markdown
![](https://view-counter-livid.vercel.app/api?username=your-reponame)
```

> [!IMPORTANT]
> Since the counter tracks by username string, make your repo identifier unique to avoid accidentally sharing a count with someone else's repo of the same name. A good pattern is to append a random number:
>
> `your-reponame-5318` → unique, collision-free

> **Examples:**
> | Repo | Identifier to use |
> |------|-------------------|
> | `my-portfolio` | `my-portfolio-2947` |
> | `view-counter` | `view-counter-5318` |
> | `awesome-project` | `awesome-project-8821` |

---

## 🎨 Customization

### ● All Parameters

| Parameter | Default | Description |
|-----------|---------|-------------|
| `username` | *(required)* | Your GitHub username |
| `base` | `0` | Number added to the real count |
| `abbreviated` | `false` | `true` → shows `12.3K` instead of `12345` |
| `icon` | `true` | `false` to hide the eye icon |
| `iconSize` | `16` | Icon size in pixels |
| `iconColor` | same as `color` | Icon color (hex or rgba) |
| `label` | `Profile views:` | Label text. Set to `false` to hide |
| `labelColor` | same as `color` | Label text color |
| `color` | `#aaaaaa` | Count text color (fallback for all colors) |
| `size` | `13` | Font size in pixels |
| `style` | `rounded` | `rounded` · `square` · `nobg` · `invisible` |
| `layout` | `horizontal` | `horizontal` · `vertical` · `split` |
| `bgColor` | `rgba(255,255,255,0.08)` | Background color |
| `labelBgColor` | `rgba(255,255,255,0.05)` | Left section color in `split` layout |

---

### ● Colors

Both **hex** and **rgba** are supported for all color parameters.
```markdown
<!-- Hex (with or without #) -->
?color=58a6ff
?color=%2358a6ff

<!-- rgb or rgba -->
?color=rgb(88,166,255)
?color=rgba(30,30,30,0.9)
```

> [!TIP]
> Use `color` as your base color — it automatically applies to the icon, label, and count unless you override them individually with `iconColor` or `labelColor`.

> **Popular color themes:**
> 
> | Theme | Preview | `color` | `bgColor` |
> |-------|---------|---------|-----------|
> | GitHub Blue | ![](https://view-counter-livid.vercel.app/api?username=xyx&color=58a6ff&bgColor=rgba(56,139,253,0.1)) | `58a6ff` | `rgba(56,139,253,0.1)` |
> | GitHub Green | ![](https://view-counter-livid.vercel.app/api?username=xyx&color=3fb950&bgColor=rgba(46,160,67,0.1)) | `3fb950` | `rgba(46,160,67,0.1)` |
> | GitHub Orange | ![](https://view-counter-livid.vercel.app/api?username=xyx&color=f78166&bgColor=rgba(247,129,102,0.1)) | `f78166` | `rgba(247,129,102,0.1)` |
> | GitHub Purple | ![](https://view-counter-livid.vercel.app/api?username=xyx&color=bc8cff&bgColor=rgba(188,140,255,0.1)) | `bc8cff` | `rgba(188,140,255,0.1)` |
> | White on Dark | ![](https://view-counter-livid.vercel.app/api?username=xyx&color=ffffff&bgColor=rgba(30,30,30,0.9)) | `ffffff` | `rgba(30,30,30,0.9)` |
> | Minimal Grey | ![](https://view-counter-livid.vercel.app/api?username=xyx&color=aaaaaa&bgColor=rgba(255,255,255,0.05)) | `aaaaaa` | `rgba(255,255,255,0.05)` |

---

### ● Styles

Controls the shape and background of the badge (default: `rounded`).

| Style | Preview | Usage |
|-------|---------|-------|
| `rounded` | ![](https://view-counter-livid.vercel.app/api?username=xyx&style=rounded) | `?style=rounded` |
| `square` | ![](https://view-counter-livid.vercel.app/api?username=xyx&style=square) | `?style=square` |
| `nobg` | ![](https://view-counter-livid.vercel.app/api?username=xyx&style=nobg) | `?style=nobg` |
| `invisible` | *(renders nothing)* | `?style=invisible` |

> [!TIP]
> use "invisible" mode when you want to have counter without displaying it.

---

### ● Layouts

Controls the arrangement of the icon, label, and count (default: `horizontal`).

| Layout | Preview | Usage |
|--------|---------|-------|
| `horizontal` | ![](https://view-counter-livid.vercel.app/api?username=xyx&layout=horizontal) | `?layout=horizontal` |
| `vertical` | ![](https://view-counter-livid.vercel.app/api?username=xyx&layout=vertical) | `?layout=vertical` |
| `split` | ![](https://view-counter-livid.vercel.app/api?label=profile+views&username=xyx&layout=split) | `?layout=split` |


---

### ● Label

#### Custom text

| Preview | Usage |
|---------|-----|
| ![](https://view-counter-livid.vercel.app/api?username=xyx&label=visitors:) | `?label=visitors:` |
| ![](https://view-counter-livid.vercel.app/api?username=xyx&label=repo+views:) | `?label=repo+views:` |
| ![](https://view-counter-livid.vercel.app/api?username=xyx&label=profile+visits:) | `?label=profile+visits:` |

> [!NOTE]
> Use `+` for spaces in the URL -- `eg: ?label=profile+views`

> [!TIP]
> Otptional but Add `:` in end to make it look good -- `eg: ?label=visitors:`

---

#### Hide label

| Preview | Usage |
|---------|-----|
| ![](https://view-counter-livid.vercel.app/api?username=xyx&label=false) | `?label=false` |

---

#### Custom label color

| Color | Preview | Usage |
|---------|-------------|---------|
| Orange | ![](https://view-counter-livid.vercel.app/api?username=xyx&labelColor=f78166) | `?label=f78166` |
| Green | ![](https://view-counter-livid.vercel.app/api?username=xyx&labelColor=3fb950) | `?label=3fb950` |
| Blue | ![](https://view-counter-livid.vercel.app/api?username=xyx&labelColor=58a6ff) | `?label=58a6ff` |

---

### ● Icon

#### Hide icon

| Preview | Usage |
|---------|-----|
| ![](https://view-counter-livid.vercel.app/api?username=xyx&icon=false) | `?icon=false` |

---

#### Custom icon color

| Color | Preview | Usage |
|---------|-------------|-----|
| Orange | ![](https://view-counter-livid.vercel.app/api?username=xyx&iconColor=f78166) | `?iconColor=f78166` |
| Green | ![](https://view-counter-livid.vercel.app/api?username=xyx&iconColor=3fb950) | `?iconColor=3fb950` |
| Blue | ![](https://view-counter-livid.vercel.app/api?username=xyx&iconColor=58a6ff) | `?iconColor=58a6ff` |

---

#### Icon size

| iconSize | Preview | Usage |
|---------|------------|-----|
| `12` | ![](https://view-counter-livid.vercel.app/api?username=xyx&iconSize=12) | `?iconSize=12` |
| `16` *(default)* | ![](https://view-counter-livid.vercel.app/api?username=xyx&iconSize=16) | `?iconSize=16` |
| `24` | ![](https://view-counter-livid.vercel.app/api?username=xyx&iconSize=24) | `?iconSize=24` |

---

### ● Size

`size` controls the font size of `label` and `count`

| size | iconSize | Preview | Usage |
|--------|------------|---------|----------------|
| `11` | `13` | ![](https://view-counter-livid.vercel.app/api?username=xyx&size=11&iconSize=13) | `?size=11&iconSize=13` |
| `13` *(default)* | `16` *(default)* | ![](https://view-counter-livid.vercel.app/api?username=xyx&size=13&iconSize=16) | `?size=13&iconSize=16` |
| `16` | `20` | ![](https://view-counter-livid.vercel.app/api?username=xyx&size=16&iconSize=20) | `?size=16&iconSize=20` |

> [!NOTE]
> `iconSize` scales the icon independently.

---

### ● Count

#### Abbreviated

Shortens large numbers for a cleaner look. -- `eg: 1.000 → 1K`

| Preview | Usage |
|---------|-----|
| ![](https://view-counter-livid.vercel.app/api?username=xyx&abbreviated=false) | `?abbreviated=false` *(default)* |
| ![](https://view-counter-livid.vercel.app/api?username=xyx&abbreviated=true) | `?abbreviated=true` |

---

#### Base Count

Add an offset to the real count. Useful when migrating from another counter and you want to preserve your existing views.

| Preview | Usage |
|---------|-----|
| ![](https://view-counter-livid.vercel.app/api?username=xyx) | `?base=0` *(default)* |
| ![](https://view-counter-livid.vercel.app/api?username=xyx&base=1000) | `?base=1000` |

---

<details>
<summary><h3>🛠️ Self Hosting</h3></summary>

<br>

### 1. Supabase Setup

1. Go to [supabase.com](https://supabase.com) and create a free project
2. Open **SQL Editor** and run:
```sql
CREATE TABLE counters (
  username TEXT PRIMARY KEY,
  count    INTEGER DEFAULT 0
);

CREATE OR REPLACE FUNCTION increment_counter(uname TEXT)
RETURNS INTEGER AS $$
  INSERT INTO counters (username, count)
  VALUES (uname, 1)
  ON CONFLICT (username)
  DO UPDATE SET count = counters.count + 1
  RETURNING count;
$$ LANGUAGE SQL;
```

3. Go to **Settings → API** and copy your **Project URL** and **anon public key**

---

### 2. Project Setup
```bash
mkdir view-counter && cd view-counter
mkdir api
```

Create `package.json`:
```json
{
  "name": "view-counter",
  "version": "1.0.0",
  "dependencies": {
    "@supabase/supabase-js": "^2.0.0"
  }
}
```
```bash
npm install
```

---

### 3. Deploy to Vercel
```bash
npm i -g vercel
vercel login
vercel --prod
```

---

### 4. Add Environment Variables

In your Vercel dashboard → **Settings → Environment Variables**:

| Name | Value |
|------|-------|
| `SUPABASE_URL` | `https://your-project.supabase.co` |
| `SUPABASE_KEY` | `sb_publishable_xxxx...` |

Then redeploy:
```bash
vercel --prod
```

</details>

---

## 🔒 Privacy & Data

- No authentication or signup is needed
- Counts are public — anyone can see the count by loading the image
- Only the **username** and **view count** are stored — nothing else

---

## 🧰 Tech Stack

- **[Vercel](https://vercel.com)** — serverless API hosting (free tier)
- **[Supabase](https://supabase.com)** — PostgreSQL database (free tier)
- **SVG** — rendered inline as an image, no external dependencies

---

## 📄 License

<a href="https://github.com/piyush-kokane/view-counter/blob/main/LICENSE">MIT license</a> — free to use, fork, and self-host.

---

<div align="center">
  Made by <a href="https://github.com/piyush-kokane">piyush-kokane</a>
</div>
