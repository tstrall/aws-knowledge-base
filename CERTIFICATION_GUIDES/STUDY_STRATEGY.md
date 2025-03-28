# 🎯 AWS Certification Study Strategy

This file outlines a repeatable process for preparing for AWS certification exams in parallel with building and reviewing a personal AWS knowledge base.

It’s designed to promote **long-term retention**, not just short-term memorization — using **active learning, test feedback, and content refinement**.

---

## 🧪 Step 1: Use Practice Exams as a Compass

Start by taking a **timed practice exam** or a set of exam-like questions.  
For each question:

1. ✅ If you got it right, move on.
2. ❌ If you missed it or guessed:
   - ⏸️ Pause before reading the full answer.
   - 🔎 Try to find the answer in your knowledge base (`.md` files).
   - ✍️ If it's missing or unclear, add it or improve the existing entry.

> This builds contextual memory and reinforces the habit of connecting real-world reasoning to your notes.

---

## 📚 Step 2: Maintain a Test Review Log

Log any missed or fuzzy questions in [`TEST_REVIEW.md`](./TEST_REVIEW.md) with:

- A brief summary of what confused you
- A link to the `.md` file that covers (or should cover) it
- A follow-up action (e.g., re-read, write diagram, update notes)

This file becomes your **targeted re-review list**.

---

## 📋 Step 3: Use Descriptive Checklists for Review

Each cert has a checklist (e.g., [`CHECKLIST_SAA.md`](./CHECKLIST_SAA.md)) that:

- ✅ Tracks what topics are written
- 📎 Links to content for easy navigation
- 📝 Includes a short description for scanning
- 🔁 Can include optional review flags like:

```markdown
| ✅ | [S3](../storage/s3.md) | Object storage (🔁 review storage classes) |
```

---

## 🔁 Step 4: Weekly Rotation Plan

Split your study into two types of sessions:

### A. 📖 Knowledge Review (Writing & Refinement)
- Re-read or improve `.md` files you wrote earlier
- Add missing details, diagrams, or examples
- Compare services, draw decision trees, spot gaps

### B. 🧪 Practice & Feedback
- Take 10–30 practice questions (timed or untimed)
- Log issues in `TEST_REVIEW.md`
- Immediately follow up with notebook review

> 💡 Pro tip: Rewriting a section in your own words after missing a test question is one of the best ways to lock it in.

---

## 🧱 Why This Works

This approach blends:

- 📘 Passive study → Reading your notes
- 🧠 Active recall → Practice questions
- ✍️ Elaboration → Writing & refining knowledge
- 🔁 Feedback loops → Test-based gaps

It avoids cramming and builds a **durable mental model of AWS** — ideal for exams and real-world design work.

---

## 🛠 Tools Used

- ✅ Markdown-based knowledge base in GitHub
- ✅ Autolinked checklists per certification
- ✅ `TEST_REVIEW.md` log to capture confusion
- ✅ This strategy file to keep it all grounded

---

## ✅ Optional: Daily/Weekly Tracker

You can add a `STUDY_LOG.md` to track what you did each day (like a mini journal), or just keep a running note like:

```markdown
- [x] Reviewed IAM and KMS
- [x] Added S3 retrieval class chart
- [ ] Follow up on NAT Gateway pricing (TEST_REVIEW.md)
```
