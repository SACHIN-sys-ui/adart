# AdArt — Deployment Guide

## Project Structure
```
adart/
├── api/
│   └── generate.js       ← Secure backend (your API key lives here)
├── public/
│   └── index.html        ← Your full website
├── vercel.json           ← Vercel config
└── README.md
```

---

## Deploy to Vercel (Free) — Step by Step

### Step 1: Create a GitHub account
Go to https://github.com and sign up (free).

### Step 2: Create a new repository
1. Click the **+** button → **New repository**
2. Name it: `adart`
3. Set it to **Public**
4. Click **Create repository**

### Step 3: Upload your files
In your new repo, click **"uploading an existing file"** and upload:
- `api/generate.js`
- `public/index.html`
- `vercel.json`

Make sure to keep the folder structure (api/ and public/ folders).

### Step 4: Create a Vercel account
Go to https://vercel.com and sign up with your GitHub account (free).

### Step 5: Import your project
1. In Vercel dashboard → click **"Add New Project"**
2. Select your `adart` GitHub repo
3. Click **Deploy** (leave all settings default)

### Step 6: Add your Anthropic API key (THE IMPORTANT STEP)
1. In Vercel dashboard → go to your project → **Settings**
2. Click **Environment Variables**
3. Add a new variable:
   - **Name:** `ANTHROPIC_API_KEY`
   - **Value:** your key from https://console.anthropic.com
4. Click **Save**
5. Go to **Deployments** → click **Redeploy** (so it picks up the new key)

### Step 7: Your site is live! 🎉
Vercel gives you a free URL like: `adart.vercel.app`

---

## Get Your Anthropic API Key
1. Go to https://console.anthropic.com
2. Sign up / log in
3. Click **API Keys** → **Create Key**
4. Copy it and paste into Vercel (Step 6 above)
5. Add a few dollars of credit (new accounts get free credits)

---

## Custom Domain (Optional)
Want `adart.in` instead of `adart.vercel.app`?
1. Buy the domain at https://godaddy.com or https://namecheap.com
2. In Vercel → **Settings** → **Domains** → add your domain
3. Follow Vercel's DNS instructions (takes ~10 minutes)

---

## Cost
- Vercel hosting: **FREE** (Hobby plan)
- Anthropic API: ~₹0.10–0.50 per brief generated (very cheap)
- Domain: ~₹800–1200/year (optional)

---

## Need Help?
The Vercel docs are excellent: https://vercel.com/docs
