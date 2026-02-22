# 📊 ATTENDR — Attendance Dashboard

> A lightweight, browser-based attendance dashboard. Upload your weekly Excel file and instantly get a visual summary of office attendance, WFH days, leaves, and pending coverage days — no server, no login, no cost.

---

## 🌐 Live Demo

👉 **[View Dashboard] https://amitmishra86.github.io/attendence/**

> Replace the link above with your actual GitHub Pages URL after deployment.

---

## 📸 What It Does

| Feature | Description |
|---|---|
| 📂 Excel Upload | Drag & drop your SharePoint Excel file |
| 📅 Week View | See attendance week by week |
| 📆 Month View | See the full month at a glance |
| ⚠ WFH Pending | Who did WFH on Mon/Tue but hasn't covered it |
| 🚨 Zero Office Days | People with no office attendance |
| 🏖 Leave Summary | Leave count per person |
| 🏢 Team Breakdown | Office attendance % by team |
| ⬇ Export | Download processed dashboard as Excel |

---

## 🏢 Business Rules This Tool Understands

- **Monday & Tuesday** are mandatory office days
- If someone does **WFH on Mon/Tue**, they must complete those days from office **later in the same week** (Wed/Thu/Fri)
- The dashboard automatically calculates **pending WFH coverage** per employee

---

## 📁 Project Structure

```
attendr/
│
├── index.html        ← The entire app (single file!)
└── README.md         ← This file
```

That's it. The whole app is one HTML file.

---

## 🚀 How to Deploy on GitHub Pages (Step by Step)

### Step 1 — Create a GitHub Account
If you don't have one, sign up at [github.com](https://github.com)

### Step 2 — Create a New Repository
1. Click the **"+"** icon (top right) → **New repository**
2. Name it: `attendr`
3. Set visibility to: **Public**
4. ✅ Check **"Add a README file"** — then we'll replace it
5. Click **Create repository**

### Step 3 — Upload Your Files
1. Inside your new repo, click **"Add file"** → **"Upload files"**
2. Upload both files:
   - `index.html`
   - `README.md`
3. At the bottom, write a commit message like: `first commit — add attendance dashboard`
4. Click **Commit changes**

### Step 4 — Enable GitHub Pages
1. Go to your repo → click **Settings** (top tab)
2. Scroll down to **"Pages"** in the left sidebar
3. Under **Source**, select:
   - Branch: `main`
   - Folder: `/ (root)`
4. Click **Save**
5. Wait 1–2 minutes ⏳

### Step 5 — Get Your Link
GitHub will show you a green banner:
```
✅ Your site is live at https://YOUR-USERNAME.github.io/attendr
```
Copy that link and share it with your team!

---

## 📤 How to Use the Dashboard (Every Friday)

```
Step 1 → Download your Excel file from SharePoint
Step 2 → Open the dashboard link in your browser
Step 3 → Drag & drop the Excel file onto the page
Step 4 → Your dashboard is ready instantly! ✅
```

No login. No upload to any server. The file is read entirely in your browser.

---

## 📊 Excel Format Requirements

Your Excel file should follow this structure:

| Employee | Team | 05-Jan-2026 Monday | 06-Jan-2026 Tuesday | ... |
|---|---|---|---|---|
| John Doe | Programming | Yes | WFH | ... |
| Jane Smith | Design | Yes | Leave | ... |

**Accepted values in day columns:**
| Value | Meaning |
|---|---|
| `Yes` | Came to office ✅ |
| `WFH` | Worked from home 🏠 |
| `Leave` | On leave 🏖 |
| *(blank)* | No data |

The tool **auto-detects** your column headers — no formatting changes needed.

---

## 🔒 Password Protection

The dashboard is password protected. Default password is:
```
Attendr@2026
```

**To change the password:** open `index.html` in any text editor, find this line near the top of the `<script>` section and replace with your own:
```js
const CORRECT_PASSWORD = 'Attendr@2026'; // ← change this
```
Then re-upload the file to GitHub.

**How it works:**
- Anyone opening the link sees a password prompt first
- 5 wrong attempts locks the session (close & reopen tab to retry)
- Once unlocked, stays open until tab is closed

> ⚠️ Note: Password lives inside the HTML file. Anyone who downloads it can see it in source code. This is basic protection — enough to stop casual access.

---

## 🔄 How to Update the App in Future

If you want to make changes to the dashboard:

1. Edit `index.html` on your computer
2. Go to your GitHub repo
3. Click on `index.html` → click the **pencil icon** (Edit)
4. Paste your updated code
5. Click **Commit changes**

GitHub Pages will automatically update within 1–2 minutes.

---

## 🛠 Tech Stack

| Technology | Purpose |
|---|---|
| HTML / CSS / JavaScript | Entire app — no framework needed |
| [SheetJS (xlsx)](https://sheetjs.com/) | Reading Excel files in the browser |
| GitHub Pages | Free hosting |

**Zero dependencies to install. Zero cost. Works offline after first load.**

---

## 🙋 FAQ

**Q: Is my data safe? Does it upload anywhere?**
> No. The Excel file is read entirely inside your browser. Nothing is sent to any server.

**Q: Can my team members upload their own Excel files?**
> Yes! Anyone with the link can open the dashboard and upload any Excel file. Each person's session is independent.

**Q: What if my Excel column names are different?**
> The tool auto-detects date columns. As long as you have Employee, Team, and date columns with Yes/WFH/Leave values, it will work.

**Q: How do I share the dashboard?**
> Just share the GitHub Pages link: `https://YOUR-USERNAME.github.io/attendr`

**Q: Does it work on mobile?**
> Yes, it's responsive and works on mobile browsers.

---

## 👨‍💻 Built With Guidance From

This project was built as a first mini-project with step-by-step guidance from [Claude by Anthropic](https://claude.ai).

---

## 📅 Version History

| Version | Date | Changes |
|---|---|---|
| v1.0 | Feb 2026 | Initial release — Excel upload dashboard |

---

*Made with ❤️ — First mini project 🚀*
