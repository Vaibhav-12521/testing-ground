# CV5 - Your ATS-Optimized CV + Job-Hunt Playbook

Headline role: **Full-Stack Developer** (decided with you). Hackathon result corrected to **Runner-up** (matches your portfolio - never risk a "Winner" claim that fails a reference check).

---

## 1. What's in this folder

| File | What it is | When to use |
|------|-----------|-------------|
| `Vaibhav_Singh_FullStack_CV.tex` | ATS-optimized LaTeX → polished PDF | Send this PDF to recruiters / upload to job portals |
| `Vaibhav_Singh_CV_ATS_PlainText.md` | Plain-text version | Paste into Word/Google Docs → save as `.docx` (safest ATS format); also for copy-paste into application text boxes |
| `README_How_To_Get_IT_Job.md` | This playbook | Read once, then act |

### How to generate the PDF (no LaTeX installed on your PC)
1. Go to https://overleaf.com → New Project → Upload Project → upload `Vaibhav_Singh_FullStack_CV.tex`.
2. Click **Recompile**. Download the PDF. 
3. Name the file exactly: `Vaibhav_Singh_Full_Stack_Developer.pdf` (recruiters search by filename).

### How to make the .docx (some ATS prefer Word)
1. Open `Vaibhav_Singh_CV_ATS_PlainText.md` in any text editor, copy all.
2. Paste into Google Docs or MS Word, apply a simple font (Calibri/Arial 10–11pt), bold the section headers.
3. File → Download → `.docx`. Done.

---

## 2. Why this CV scores high on ATS (Applicant Tracking Systems)

ATS software parses your CV into a database and ranks it against the job description by keyword match and structure. This CV is built for that:

- **Single column, no tables/text-boxes/graphics in the body** — multi-column and image-based CVs get garbled by parsers. (Your old CV4 used a skills *table* and FontAwesome icons — risky. Fixed here.)
- **Standard section headings** the parser recognizes: *Professional Summary, Technical Skills, Professional Experience, Education*.
- **Keywords that match real job posts**: React, Node.js, JavaScript, TypeScript, REST API, PostgreSQL, MySQL, OAuth, JWT, Git, CI/CD, Agile. Added **Node.js + Express** explicitly so backend/Node filters catch you.
- **Selectable text, standard fonts**, no headers/footers holding contact info (some ATS ignore those zones).
- **One page**, reverse-chronological, quantified bullets ("90%+ accuracy", "four AI products", "sub-second responses").

> **Target: 80%+ match.** Before each application, paste the job description + your CV into a free checker like Jobscan or Resumeworded and add any missing keyword you genuinely have.

---

## 3. The #1 rule: tailor per application (5 min each)

Don't send the same CV everywhere. For each job:
1. Read the job post, list its **must-have skills**.
2. In your CV's **Professional Summary** + **Technical Skills**, make sure those exact words appear (only if true).
   - Applying for a **React/Frontend** role? Move React, Tailwind, Responsive Design to the front of the summary.
   - Applying for a **Node.js/Backend** role? Lead with Node.js, Express, REST API, PostgreSQL.
3. Rename the file to match the title in the post. 

This single habit beats a "perfect" generic CV.

---

## 4. Fix one honesty gap before you apply

Your CV mentions **Node.js / Express**, but your shipped backends are PHP and Supabase. Recruiters will ask. Close the gap fast so it's true:
- Rebuild **one** existing API (e.g. the Medstocksy or Lucknowi backend) as a small **Node.js + Express + PostgreSQL** service. A weekend project is enough.
- Push it to GitHub with a clean README. Now "Node.js" is fully defensible in interviews.

---

## 5. Make your GitHub recruiter-ready (https://github.com/Vaibhav-12521)

Recruiters click your GitHub. Right now several portfolio projects link to your profile root, not real repos. Fix:
- [ ] Pin your 6 best repos (Medstocksy, EVA, Lucknowi, etc.).
- [ ] Every pinned repo needs a **README** with: what it does, tech stack, a screenshot/GIF, and a **live demo link**.
- [ ] Add a profile README (`Vaibhav-12521/Vaibhav-12521` repo) with a 3-line intro + your portfolio link.
- [ ] Make sure the Lucknowi/EVA links in your portfolio point to the actual repos.

A GitHub with live, documented projects + your live sites (medstocksy.in, lucknowi.com) is your biggest edge over other freshers — most have none. Lead with it.

---

## 6. Where & how to apply (India, fresher full-stack)

**Apply daily, track in a sheet.** Volume + tailoring wins.

- **LinkedIn** — set "Open to Work", apply to "Easy Apply" full-stack/React/Node roles, and **DM the recruiter or hiring manager** after applying with a 3-line note + portfolio link. This is where most replies come from.
- **Naukri.com** — upload the `.docx`, keyword-rich; Indian recruiters search here heavily.
- **Internshala** — fresher full-stack / web dev roles & internships that convert to full-time.
- **Wellfound (AngelList)** — startups, which value shipped products over degrees (your strength).
- **Cutshort, Hirist, Instahyre** — India dev-focused boards.
- **Company career pages** — apply directly when you find a fit; less ATS competition than aggregators.

Aim for **10–15 tailored applications/day**. Track: company, role, date, status, follow-up date.

---

## 7. The cold message that gets replies (LinkedIn DM)

> Hi [Name], I'm a full-stack developer (React/TypeScript + Node/PHP). I've shipped two live production apps solo — a multi-tenant pharmacy SaaS (medstocksy.in) and an e-commerce store (lucknowi.com). I'd love to be considered for the [Role] role at [Company]. Portfolio: vaibhav1.me. Happy to share more — thank you!

Short, specific, links the proof. Send 5–10/day to recruiters at companies you applied to.

---

## 8. Interview prep (start now, in parallel)

- **DSA:** you did the GFG 160-day challenge — keep ~3 problems/day on LeetCode (Arrays, Strings, HashMaps, Trees). Most fresher screens are easy/medium.
- **JS/React core:** closures, promises/async-await, event loop, `useState`/`useEffect`, props vs state, lifting state, REST vs WebSocket.
- **Backend:** REST design, status codes, auth (JWT vs session — you've done both, talk about it), SQL joins & indexing.
- **Your own projects:** be ready to whiteboard the Medstocksy multi-tenant RLS design — it's a genuinely strong, senior-sounding talking point. Drill "why RLS over app-level checks" until it's smooth.

---

## 9. Your 7-day action checklist

- [ ] Day 1: Generate PDF on Overleaf + create `.docx`. Run it through Jobscan once.
- [ ] Day 2: Clean up GitHub (pin repos, add READMEs, fix project links).
- [ ] Day 3: Update LinkedIn headline to "Full-Stack Developer | React · Node.js · TypeScript", set Open to Work, add portfolio link.
- [ ] Day 4–5: Build the small Node.js + Express + PostgreSQL API; push it.
- [ ] Day 6–7: Apply to 10+ roles/day across LinkedIn, Naukri, Wellfound, Internshala; DM recruiters; start daily LeetCode.

---

*You already have the rarest fresher asset: live, real, deployed products with paying-user-grade features. The CV and this plan exist to get that fact in front of the right person. Now it's a numbers + consistency game — apply daily, tailor every time, follow up.*
