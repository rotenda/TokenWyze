# TokenWyze

South Africa's leading voice on tokenisation and capital markets.

## Local Development

Just open `index.html` in your browser — no build step required.

## Deploying to GitHub Pages with Custom Domain

### Step 1: Create a GitHub Repository

1. Go to [github.com](https://github.com) and sign in
2. Click the **+** icon → **New repository**
3. Name it `tokenwyze`
4. Set it to **Public**
5. Click **Create repository**

### Step 2: Upload Your Files

**Option A — GitHub Web UI (easiest):**
1. In your new repo, click **Add file** → **Upload files**
2. Drag and drop ALL files: `index.html`, `post.html`, `CNAME`, `README.md`
3. Click **Commit changes**

**Option B — Git command line:**
```bash
cd /path/to/tokenwyze
git init
git add .
git commit -m "Initial launch — TokenWyze"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/tokenwyze.git
git push -u origin main
```

### Step 3: Enable GitHub Pages

1. In your repository, go to **Settings**
2. In the left sidebar, click **Pages**
3. Under **Source**, select **Deploy from a branch**
4. Choose branch: **main**, folder: **/ (root)**
5. Click **Save**

### Step 4: Configure Your Custom Domain (tokenwyze.co.za)

The `CNAME` file is already included and set to `tokenwyze.co.za`.

Now update your DNS settings with your domain registrar (e.g. Afrihost, Domains.co.za, Xneelo):

| Type  | Name | Value                          |
|-------|------|--------------------------------|
| A     | @    | 185.199.108.153                |
| A     | @    | 185.199.109.153                |
| A     | @    | 185.199.110.153                |
| A     | @    | 185.199.111.153                |
| CNAME | www  | YOUR_USERNAME.github.io        |

Then in GitHub → Settings → Pages → Custom domain, enter: `tokenwyze.co.za` and click **Save**.

Tick **Enforce HTTPS** once it appears (may take a few minutes after DNS propagates).

### Step 5: Your Site Is Live!

DNS propagation typically takes 15 minutes to a few hours. Once done, your blog will be live at:
```
https://tokenwyze.co.za
```

## Adding New Posts

1. Duplicate `post.html` → rename it (e.g. `fractional-property.html`)
2. Edit the content inside the HTML
3. Add a link to it from `index.html`
4. Commit and push — GitHub Pages auto-deploys within minutes

## File Structure

```
tokenwyze/
├── index.html      ← Homepage
├── post.html       ← Sample article (Project Khokha)
├── CNAME           ← Custom domain config (tokenwyze.co.za)
└── README.md       ← This file
```
