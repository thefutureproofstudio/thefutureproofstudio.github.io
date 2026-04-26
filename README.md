# The Futureproof Studio — Website

**futureproofstudio.co**

---

## Site Structure

```
futureproof-site/
├── index.html          ← Homepage (main entry point)
├── course.html         ← AI Literacy Course sales page
├── workshops.html      ← Workshop & institutional training info
├── contact.html        ← Contact form, booking, newsletter
├── favicon.svg         ← Browser tab icon
├── styles.css          ← Shared styles (reference — styles are inline per page)
├── nav-footer-snippet.html  ← Copy/paste nav & footer for new pages
└── README.md           ← This file
```

---

## Deploying to GitHub Pages

### Step 1: Create your GitHub repository

1. Go to [github.com](https://github.com) and sign in
2. Click **+** → **New repository**
3. Name it: `futureproofstudio` (or any name you like)
4. Set to **Public**
5. Click **Create repository**

### Step 2: Upload your files

**Option A — Drag and drop (easiest):**
1. Open your repository on GitHub
2. Click **uploading an existing file**
3. Drag all files from this folder into the upload area
4. Click **Commit changes**

**Option B — GitHub Desktop app:**
1. Download [GitHub Desktop](https://desktop.github.com)
2. Clone your repository
3. Copy files into the cloned folder
4. Commit and push

### Step 3: Enable GitHub Pages

1. Go to your repository → **Settings** → **Pages**
2. Under **Source**, select **Deploy from a branch**
3. Select **main** branch, **/ (root)** folder
4. Click **Save**
5. Wait 2–3 minutes — your site will be live at:
   `https://yourusername.github.io/futureproofstudio`

### Step 4: Connect your custom domain (futureproofstudio.co)

**In GitHub:**
1. Settings → Pages → Custom domain
2. Enter: `futureproofstudio.co`
3. Click Save
4. Check "Enforce HTTPS" once it activates

**In your domain registrar (Namecheap, GoDaddy, etc.):**

Add these DNS records:

| Type  | Host | Value                  |
|-------|------|------------------------|
| A     | @    | 185.199.108.153        |
| A     | @    | 185.199.109.153        |
| A     | @    | 185.199.110.153        |
| A     | @    | 185.199.111.153        |
| CNAME | www  | yourusername.github.io |

DNS propagation takes 15 min to 24 hours. Once done, `futureproofstudio.co` will point to your GitHub Pages site.

---

## Setting Up Contact Forms (Formspree)

The contact page uses [Formspree](https://formspree.io) for form submissions.

### Setup:
1. Go to [formspree.io](https://formspree.io) and create a **free account**
2. Click **New Form** — give it a name (e.g. "Workshop Inquiry")
3. Copy your **form ID** (looks like: `xyzabcde`)
4. Open `contact.html` in VS Code
5. Find these placeholders and replace with your form IDs:

```html
<!-- Main proposal form -->
action="https://formspree.io/f/YOUR_FORMSPREE_ID"

<!-- General contact form -->
action="https://formspree.io/f/YOUR_FORMSPREE_ID_2"

<!-- Newsletter form -->
action="https://formspree.io/f/YOUR_NEWSLETTER_FORMSPREE_ID"
```

You can use the same form ID for all three, or create separate forms for each.

**Free tier:** 50 submissions/month — plenty to start.
**Paid tier:** $10/month for unlimited submissions.

Submissions are emailed directly to the email address on your Formspree account.

---

## Connecting to Teachable

In all files, find and replace `YOUR-TEACHABLE-URL` with your actual Teachable school URL.

Search for: `YOUR-TEACHABLE-URL.teachable.com`

Examples of where it appears:
- Nav "Enroll Now" buttons
- Course page CTA buttons
- Homepage hero buttons

To find all instances in VS Code: **Cmd+Shift+F** (Mac) or **Ctrl+Shift+F** (Windows)

---

## Making Edits

### Recommended workflow:

1. Open any `.html` file in **VS Code**
2. Use **Cmd+F / Ctrl+F** to find text you want to change
3. Edit the readable text between `>` and `<` tags
4. Save the file
5. Go to GitHub → your repository → click the file → click the pencil icon → paste new content → Commit

Or use **GitHub Desktop** for a more visual drag-and-drop experience.

### Finding your contact details to update:

Search for these placeholders across all files:
- `hello@futureproofstudio.co` → your actual email
- `linkedin.com/company/thefutureproofstudio` → your LinkedIn URL
- `YOUR-TEACHABLE-URL` → your Teachable school URL
- `YOUR_FORMSPREE_ID` → your Formspree form IDs

---

## Adding New Pages

1. Copy `nav-footer-snippet.html` as your starting point
2. Add the full HTML structure around it
3. Update the `class="active"` on the correct nav link for that page
4. Add SEO `<meta>` tags in the `<head>`
5. Save as a new `.html` file in the same folder
6. Upload to GitHub

---

## Page Descriptions

| Page | Purpose | Key CTA |
|------|---------|---------|
| `index.html` | Brand homepage, introduces studio and flows into course | → Course page |
| `course.html` | Full AI Literacy course sales page with pricing | → Teachable enroll |
| `workshops.html` | Institutional workshop one-pager with formats and pricing | → Contact for proposal |
| `contact.html` | Proposal request form, general contact, newsletter signup | → Submit form |

---

## Brand Reference

**Colors:**
- Teal (primary): `#0d9488`
- Ink (text): `#1a1f2e`
- Slate (body): `#3d4a5c`
- Background: `#f8fafc`

**Fonts (Google Fonts — already linked in each page):**
- Display/headings: DM Serif Display
- Body/UI: Outfit

**Logo:** See `favicon.svg` — the same icon is inline SVG in each page's nav.

---

*The Futureproof Studio · futureproofstudio.co*
