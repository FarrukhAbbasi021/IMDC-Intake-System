# IMDC Master Intake System

A fully offline-capable, static web application for the International Medical & Dental Council LLC intake process. Includes auto-propagating master form, sub-forms (Account Setup, Billing Agreement, BAA/HIPAA, PHI Release), document upload, camera capture, and a dynamic Form Manager.

---

## 🚀 Deploy on Render (Step-by-Step for Beginners)

### What You Need
- A free account on [GitHub](https://github.com) (free)
- A free account on [Render](https://render.com) (free)
- This project folder

---

### Step 1 — Create a GitHub Account (skip if you have one)

1. Go to **https://github.com**
2. Click **Sign up**
3. Enter your email, create a password, choose a username
4. Verify your email address

---

### Step 2 — Create a New GitHub Repository

1. Log into GitHub
2. Click the **+** button (top-right) → **New repository**
3. Name it: `imdc-intake-system`
4. Set it to **Public** (required for Render free tier)
5. Do NOT check "Add a README" (we already have one)
6. Click **Create repository**
7. GitHub will show you a page with upload instructions — keep it open

---

### Step 3 — Upload This Project to GitHub

**Option A — Upload via GitHub website (easiest for beginners):**

1. On your new empty repository page, click **uploading an existing file**
2. Drag and drop ALL files from this project folder:
   - `render.yaml`
   - `README.md`
   - `.gitignore`
   - The entire `public/` folder (drag the folder itself)
3. Scroll down, write a commit message like `Initial upload`
4. Click **Commit changes**

**Option B — Use Git on your computer (recommended long-term):**

```bash
# 1. Install Git from https://git-scm.com if not installed
# 2. Open a terminal/command prompt in this project folder, then:

git init
git add .
git commit -m "Initial commit - IMDC Intake System"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/imdc-intake-system.git
git push -u origin main
```
Replace `YOUR-USERNAME` with your actual GitHub username.

---

### Step 4 — Create a Render Account

1. Go to **https://render.com**
2. Click **Get Started for Free**
3. Sign up with your GitHub account (easiest — click "Sign up with GitHub")
4. Authorize Render to access your GitHub

---

### Step 5 — Create a New Static Site on Render

1. In the Render dashboard, click **New +** (top-right)
2. Select **Static Site**
3. Connect your GitHub account if prompted
4. Find and select your `imdc-intake-system` repository
5. Click **Connect**

---

### Step 6 — Configure the Static Site

Fill in these settings:

| Setting | Value |
|---|---|
| **Name** | `imdc-intake-system` (or any name you like) |
| **Branch** | `main` |
| **Root Directory** | *(leave blank)* |
| **Build Command** | *(leave blank — no build needed)* |
| **Publish Directory** | `public` |

6. Click **Create Static Site**

---

### Step 7 — Wait for Deployment (~1-2 minutes)

- Render will show a progress log
- When you see **"Your site is live"**, it's done!
- Your URL will be something like: `https://imdc-intake-system.onrender.com`

---

### Step 8 — Open Your Live Site

Click the URL shown in Render dashboard. Your IMDC form is now live on the internet! Share this URL with anyone who needs to fill out intake forms.

---

## 🔄 How to Update the Site Later

Whenever you update `public/index.html`:

**Via GitHub website:**
1. Go to your repository on GitHub
2. Navigate to `public/index.html`
3. Click the pencil ✏ (edit) icon
4. Make changes or click the upload icon to replace the file
5. Commit the change
6. Render automatically redeploys within ~1 minute

**Via Git terminal:**
```bash
git add .
git commit -m "Update form fields"
git push
```

---

## 📁 Project Structure

```
imdc-intake-system/
├── render.yaml          ← Render deployment configuration
├── README.md            ← This guide
├── .gitignore           ← Files to exclude from Git
└── public/
    ├── index.html       ← The entire application (single file)
    └── _redirects       ← URL routing rules
```

---

## 🌐 Custom Domain (Optional)

To use your own domain (e.g. `intake.yourclinic.com`):

1. In Render dashboard → your site → **Settings** → **Custom Domains**
2. Click **Add Custom Domain**
3. Enter your domain, e.g. `intake.yourclinic.com`
4. Render gives you a DNS record (usually a CNAME)
5. Log into your domain registrar (GoDaddy, Namecheap, etc.)
6. Add the CNAME record Render provided
7. Wait 10-60 minutes for DNS to propagate
8. Render auto-provisions an SSL certificate (HTTPS) for free

---

## ⚡ Features

- **Master Form** → auto-fills all sub-forms
- **Offline-first** → works without internet, syncs when back online
- **Form Manager** → add, remove, reorder, and customize forms
- **Document Upload** → upload PDFs, images, Word docs
- **Camera Capture** → photograph paper documents directly from phone
- **Export** → JSON backup, text export, email
- **Print** → print any individual form or all forms
- **localStorage** → all data persists in the browser across sessions

---

## 🔒 Privacy & Security Notes

- **No server-side storage** — all data stays in the user's browser (localStorage)
- No database, no backend, no data leaves the device unless explicitly exported/emailed
- HTTPS is automatically enabled by Render
- Suitable for internal use; for HIPAA-compliant cloud storage, a backend API would be needed

---

## 🆘 Troubleshooting

| Problem | Solution |
|---|---|
| Site shows "Not Found" | Make sure Publish Directory is set to `public` in Render settings |
| Changes not showing | Hard refresh: Ctrl+Shift+R (Windows) or Cmd+Shift+R (Mac) |
| Render build failing | Check that `public/index.html` exists in your repository |
| Can't upload to GitHub | Make sure the repository is set to Public |
| Camera not working | Camera requires HTTPS — works on Render, not on local `file://` |

---

## 📞 Support

For issues with the IMDC form system, contact your system administrator.
For Render platform issues: https://render.com/docs
For GitHub issues: https://docs.github.com
