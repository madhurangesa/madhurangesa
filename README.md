# madhurangesa.com

Personal website — 3 pages: Home, Interests, and Pride & Prejudice Bookshelf.

---

## STEP 1 — Fill in your files before uploading anything

### Your photo
- Take or choose a portrait photo of yourself
- Rename it exactly: `photo.jpg`
- Place it in the `assets/` folder

### Your CV
- Export or save your CV as a PDF
- Rename it exactly: `cv.pdf`
- Place it in the `assets/` folder

### Your book cover photos
- Take photos of each of your P&P editions (any angle, portrait orientation works best)
- Rename each file to match what's in `bookshelf.html`, e.g. `penguin-clothbound.jpg`
- Place them all in the `covers/` folder
- If you don't have a photo for a book yet, that's fine — a styled placeholder shows automatically

Your folder should look like this when ready:

```
madhurangesa/
├── index.html
├── interests.html
├── bookshelf.html
├── style.css
├── assets/
│   ├── photo.jpg       ← your headshot
│   └── cv.pdf          ← your CV
└── covers/
    ├── penguin-clothbound.jpg
    ├── folio-society.jpg
    └── ... (one per book)
```

---

## STEP 2 — Edit the text

Open each HTML file in any text editor (TextEdit on Mac, Notepad on Windows, or VS Code).
Search for `✏️ EDIT` — every line that says that is something you should change.

### index.html
- Your subtitle line (Researcher · Writer · Collector)
- Your bio paragraphs
- Your quote and attribution
- Your LinkedIn URL
- Your email address

### interests.html
- The lead sentence under the heading
- Your Substack name and description
- Your Substack URL
- The four interest tiles — edit or delete any

### bookshelf.html
- The book cards are already filled in with real editions; edit them to match what you actually own
- See the "ADD MORE BOOKS" comment block at the bottom to add new ones

---

## STEP 3 — Put it on GitHub

1. Go to https://github.com and sign in (or create a free account)
2. Click the **+** icon → **New repository**
3. Name it `madhurangesa` (or anything you like)
4. Set it to **Public**
5. Click **Create repository**

Then, on your computer, open **Terminal** (Mac) or **Command Prompt** (Windows) and run:

```bash
cd path/to/this/folder
git init
git add .
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/YOUR-GITHUB-USERNAME/madhurangesa.git
git push -u origin main
```

Replace `YOUR-GITHUB-USERNAME` with your actual GitHub username.
GitHub will ask you to log in the first time.

---

## STEP 4 — Deploy on Vercel

1. Go to https://vercel.com
2. Click **Sign Up** → choose **Continue with GitHub**
3. Click **Add New Project**
4. Find and click **Import** next to your `madhurangesa` repository
5. Leave all settings as they are — no build command needed
6. Click **Deploy**

Your site will be live in about 30 seconds at a temporary URL like:
`https://madhurangesa.vercel.app`

---

## STEP 5 — Connect madhurangesa.com

1. In your Vercel project, click **Settings** → **Domains**
2. Type `madhurangesa.com` and click **Add**
3. Vercel will show you DNS records to add. They look like:

   | Type  | Name | Value               |
   |-------|------|---------------------|
   | A     | @    | 76.76.21.21         |
   | CNAME | www  | cname.vercel-dns.com |

4. Go to wherever you registered your domain (GoDaddy, Namecheap, Google Domains, etc.)
5. Find **DNS Settings** or **Manage DNS**
6. Add both records exactly as shown
7. Wait 5–30 minutes for DNS to propagate

Your site will then be live at **https://madhurangesa.com** with free HTTPS. ✅

---

## STEP 6 — Updating the site later

Whenever you want to change something:
1. Edit the file on your computer
2. To add a new book: add the image to `covers/`, edit `bookshelf.html`
3. Then run:

```bash
git add .
git commit -m "Describe what you changed"
git push
```

Vercel picks up the change automatically and redeploys in seconds.

---

## Quick reference — what each file does

| File             | What it is                          |
|------------------|-------------------------------------|
| `index.html`     | Home page — your bio and photo      |
| `interests.html` | Interests page — Substack + tiles   |
| `bookshelf.html` | P&P collection page                 |
| `style.css`      | All the visual styling (shared)     |
| `assets/`        | Your photo and CV go here           |
| `covers/`        | Book cover photos go here           |
