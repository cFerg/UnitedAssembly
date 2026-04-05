# United Assembly — Website

**unitedassembly.us** | Jekyll + Decap CMS on GitHub Pages

---

## 🚀 Quick Deploy to GitHub Pages

### Step 1 — Create the Repository
1. Go to github.com and create a new repository named `unitedassembly.us`
2. Upload all files from this folder to the repo (drag & drop works)

### Step 2 — Enable GitHub Pages
1. Go to repo **Settings → Pages**
2. Source: **Deploy from a branch**
3. Branch: `main` / `root`
4. Click **Save**
5. Your site will be live at `username.github.io/unitedassembly.us` within a few minutes

### Step 3 — Connect Your Custom Domain
1. In repo Settings → Pages → Custom Domain, enter `unitedassembly.us`
2. With your domain registrar, add these DNS records:
   ```
   A     @     185.199.108.153
   A     @     185.199.109.153
   A     @     185.199.110.153
   A     @     185.199.111.153
   CNAME www   YOUR-USERNAME.github.io
   ```

---

## ✏️ Setting Up the CMS (Decap CMS)

This lets members edit content without touching code.

### Step 1 — Update the CMS config
Open `admin/config.yml` and change this line:
```yaml
repo: unitedassembly/unitedassembly.us  # Change to YOUR-USERNAME/YOUR-REPO-NAME
```

### Step 2 — Enable GitHub OAuth via Netlify Identity (free)
1. Create a free account at netlify.com
2. Create a new site → **Import existing project** → connect your GitHub repo
3. Go to **Site Settings → Identity → Enable Identity**
4. Under **Registration**, choose **Invite only**
5. Under **External Providers**, enable **GitHub**
6. Go to **Identity → Invite users** and invite your members by email

### Step 3 — Access the CMS
Members go to: `https://unitedassembly.us/admin/`  
They log in with their GitHub account (must be invited).

---

## 📝 How Members Use the CMS

Once logged in at `/admin/`, members can:
- **Blog Posts** — Write and publish posts with a rich text editor
- **Members & Board** — Add/edit their own profile and links
- **Programs & Bills** — Update program descriptions and status

No coding required. Changes go live within ~60 seconds.

---

## 🗂️ File Structure

```
├── _config.yml          # Site settings
├── _layouts/            # Page templates
├── _includes/           # Reusable components  
├── _posts/              # Blog posts (created via CMS)
├── _members/            # Member profiles (created via CMS)
├── admin/               # Decap CMS dashboard
│   ├── index.html
│   └── config.yml       # ← Update repo name here
├── assets/css/main.css  # All styles
├── index.html           # Homepage
├── about/               # About page
├── blog/                # Blog index
├── members/             # Members directory
└── programs/            # Programs & bills
```

---

## 🔒 Should You Privatize the Repo?

**Recommendation: Keep it public.**
- Transparency aligns with your nonprofit mission
- GitHub Pages is free on public repos; private repos require a paid plan
- Never store sensitive data (API keys, donor info) in the repo regardless

---

## Questions?
Contact: contact@unitedassembly.us
