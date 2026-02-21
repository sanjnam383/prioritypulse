# ⚡ FeaturePulse — AI Feature Prioritisation Suite

> Score, rank and prioritise your features with AI. Built for PMs who are tired of gut-feel backlogs.

🔗 **Live Demo:** [featurepulse.vercel.app](https://featurepulse.vercel.app)

---

## 📌 The Problem

Every PM has a backlog full of features competing for limited engineering time. Most prioritisation happens on instinct, in a meeting, with whoever speaks loudest winning. RICE scoring exists but filling it in manually for every feature is tedious — and most PMs skip it.

FeaturePulse fixes that. Describe your features in plain English. AI scores them. You make the call.

---

## ✅ What It Does

Two modes — same powerful output:

**AI Mode** — describe features in plain English, AI scores all RICE dimensions automatically
**Manual Mode** — enter your own RICE scores if you prefer full control

Both modes produce:
- A ranked priority list with weighted scores and tier badges
- An effort vs impact scatter plot with quadrant logic
- A portfolio health grade (A–D) based on backlog balance
- An AI strategic recommendation — which features to build, cut, and why
- A downloadable PDF report to share with stakeholders

---

## 🎯 Who It Is For

- Product Managers prioritising a backlog before sprint planning or roadmap reviews
- Scrum Masters facilitating prioritisation sessions with engineering teams
- Early-stage founders making build vs defer decisions with limited capacity
- Anyone who wants a faster, more structured alternative to gut-feel prioritisation

---

## 🛠 Tech Stack

| Tool | Purpose |
|------|---------|
| HTML + CSS + JavaScript | Single file, no framework needed |
| Chart.js | Effort vs Impact scatter plot |
| jsPDF | In-browser PDF report generation |
| OpenRouter API | AI gateway — routes to best available free model |
| Llama 3.3 70B → Mistral 7B → Gemma 2 9B | Fallback model chain for reliability |
| Vercel | Hosting and deployment |

**Cost: 100% Free**

---

## 📐 How the Scoring Works

**RICE Score**
Standard formula: `(Reach × Impact × Confidence%) ÷ Effort`

**Weighted Priority Score**
`RICE (70%) + Strategic Alignment (30%)` — ensures strategically important features aren't buried by pure delivery metrics

**Feature Tiers**

| Tier | Logic |
|------|-------|
| ✅ Do Now | High impact (7+), low effort (≤4) — quick wins |
| 📅 Plan Next | High impact (7+), high effort (5+) — worth planning |
| 🔵 Do Later | Lower impact, low effort — nice to have |
| ⚠️ Reconsider | Low impact, high effort — question whether to build |

**Portfolio Health Grade**
A single A–D grade combining Do Now count, Reconsider count, average strategic alignment, and average confidence. Gives stakeholders one number to react to.

---

## 🤖 AI Features

**AI Scoring (AI Mode)**
Describe features in plain English with context — product stage, team size. AI scores Reach, Impact, Confidence, Effort, and Strategic Alignment for each feature. Strict and realistic — doesn't inflate scores.

**AI Strategic Recommendation**
A 3-paragraph no-fluff assessment from a strict senior PM persona covering:
1. What the prioritisation pattern reveals about your strategy
2. Which specific features to cut or defer — named directly
3. One actionable recommendation for your next sprint planning session

**Model Fallback Chain**
If the primary model (Llama 3.3 70B) is rate limited, the app automatically tries Mistral 7B, then Gemma 2 9B. No error, no waiting — just results.

---

## ⚠️ Current Limitations

- No data persistence — refreshing the page clears all inputs
- AI scoring quality depends on how descriptively features are written
- AI insight requires user to supply their own OpenRouter API key (free at openrouter.ai)
- Free tier models may occasionally be busy — the fallback chain handles this automatically
- Mobile layout functional but not fully optimised

---

## 🔮 Future Improvements

- [ ] Save and load feature sets via localStorage
- [ ] Team input mode — multiple stakeholders score and tool averages results
- [ ] Jira integration — import backlog items, export prioritised list back
- [ ] Sprint capacity input — factor in available story points
- [ ] Compare two prioritisation runs side by side

---

## 👩‍💻 Built By

**Sanjana M** · PM who builds what she wishes existed
