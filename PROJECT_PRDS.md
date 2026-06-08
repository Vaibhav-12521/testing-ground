# Project Build Plans (PRDs) — Vaibhav Singh  
   
Three AI projects, specced for **portfolio + job impact**. Build priority: **1 → 2 → 3**.
Golden rule: each must end with a **live deployed link + a GitHub README with screenshots**. A deployed product beats a notebook every time.
  
--- 

# PRD 1 — "AskYourDocs": RAG Document Q&A Web App  ⭐ TOP PRIORITY
   
### 1. Problem & Value
People waste time hunting through long PDFs (manuals, papers, contracts, notes). AskYourDocs lets a user upload documents and ask questions in plain English, getting answers **with citations** to the source passage. This is the most in-demand AI pattern (RAG) — and built as a full web app, it proves you can do **AI + frontend + backend** together.

### 2. Target Users
Students, researchers, analysts, support teams — anyone with documents to query.

### 3. Goals / Success Metrics
- Answer a question over a 20-page PDF in **< 5 seconds**.
- Every answer shows the **source chunk(s)** it used (no hallucinated answers without citation).
- Deployed, public URL; works on mobile.

### 4. Tech Stack (resume-optimized)
- **Frontend:** React + Vite + Tailwind CSS (you already know this) — upload UI, chat UI, citation display.
- **Backend:** **FastAPI (Python)** REST API — `/upload`, `/query`. *(This is your chance to also show clean REST API design.)*
- **RAG:** LangChain + Hugging Face embeddings (`sentence-transformers/all-MiniLM-L6-v2`) + **FAISS** vector store.
- **LLM:** Groq API (LLaMA 3.1) for fast generation — you already use this.
- **Deploy:** Frontend on **Vercel**, backend on **Render/Railway** (free tier).

### 5. Core Features (MVP — build this first)
1. Upload a PDF → backend extracts text, chunks it (recursive splitter), embeds, stores in FAISS.
2. Ask a question → retrieve top-k chunks → RetrievalQA chain → LLM answer.
3. Display answer **+ the source snippets** it came from.
4. Handle errors gracefully (bad file, no answer found, rate limit).

### 6. Data Flow
`PDF upload → text extract → chunk → embed → FAISS index` then
`question → embed → similarity search (top-k) → prompt with context → LLM → answer + citations`

### 7. Milestones (≈ 1–2 weeks part-time)
- Day 1–2: FastAPI backend; PDF ingest + chunk + embed + FAISS.
- Day 3–4: RetrievalQA chain + Groq LLM; test via Postman.
- Day 5–7: React upload + chat UI; wire to API.
- Day 8–9: Citations display, error handling, polish.
- Day 10: Deploy + README with GIF demo.

### 8. Stretch (after MVP)
Multi-file support · chat history · swap FAISS → Pinecone/ChromaDB · "answer confidence" score · auth (reuse your Supabase skills).

### 9. Resume bullet this produces
> Built and deployed **AskYourDocs**, a full-stack RAG document-Q&A app (React + FastAPI) using LangChain, Hugging Face embeddings, and a FAISS vector store, with Groq/LLaMA 3.1 generation returning **cited, sub-5-second answers** over user-uploaded PDFs.

---

# PRD 2 — Cold Email Generator (AI Job-Outreach Tool)

### 1. Problem & Value
Job seekers and sales reps write slow, generic outreach. This tool takes a **job-posting URL** (or product info), extracts the key requirements, and generates a tailored cold email. Very demo-able — recruiters instantly understand the value.

### 2. Target Users
Job seekers, freelancers, sales/BD people.

### 3. Goals / Success Metrics
- Paste a job URL → get a tailored email in **< 10 seconds**.
- Email references the **actual role requirements** (not generic).
- Adjustable tone (formal / friendly / concise).

### 4. Tech Stack
- **App:** Streamlit (fast to ship) — OR upgrade to React + FastAPI for a stronger full-stack signal.
- **Orchestration:** LangChain.
- **LLM:** LLaMA 3.1 via Groq API.
- **Scraping/parsing:** requests + BeautifulSoup → structured JSON of the job post.
- **Vector store (optional):** ChromaDB to match your portfolio/skills to the role.
- **Deploy:** Streamlit Community Cloud (free) or Vercel+Render if React.

### 5. Core Features (MVP)
1. Input: job-posting URL or pasted text.
2. Scrape + parse into structured JSON (role, skills, company).
3. Prompt-engineer a tailored email using LangChain + LLaMA 3.1.
4. Tone selector + editable output + copy button.

### 6. Data Flow
`URL → scrape → parse to JSON → (optional) match user skills → prompt template → LLM → editable email`

### 7. Milestones (≈ 4–6 days)
- Day 1: Scrape + parse job posting to JSON.
- Day 2–3: LangChain prompt + Groq generation; tone control.
- Day 4: Streamlit UI; copy/edit.
- Day 5–6: Deploy + README with demo GIF.

### 8. Stretch
Save email history · resume-to-job match score · Gmail "create draft" integration · multiple email variants.

### 9. Resume bullet this produces
> Built and deployed a **Cold Email Generator** web app (Streamlit, LangChain, LLaMA 3.1 via Groq) that scrapes job postings into structured JSON and generates **role-tailored outreach emails** with adjustable tone via engineered prompts.

---

# PRD 3 — Word2Vec from Scratch (Research Implementation)

> Keep this lean. It's a strong **ML/research** signal but low priority for full-stack roles — make it a clean, well-documented repo, not a deployed app.

### 1. Problem & Value
Reimplement the Word2Vec paper (CBOW + Skip-Gram) in PyTorch from first principles. Demonstrates you understand embeddings, training loops, and can implement a research paper — valued for ML/Data roles and strong interview talking material.

### 2. Goals / Success Metrics
- Both **CBOW** and **Skip-Gram** train and converge.
- Learned embeddings pass **cosine-similarity sanity checks** (e.g., "king"–"queen").
- **t-SNE** visualization shows meaningful clusters.
- Fully **reproducible** (config files, seed, README).

### 3. Tech Stack
PyTorch · NumPy · scikit-learn (t-SNE) · Matplotlib · Jupyter.

### 4. Core Scope (MVP)
1. Preprocessing: tokenization, vocabulary build, context-target sampling.
2. CBOW + Skip-Gram models in PyTorch.
3. Training: Adam optimizer, cross-entropy loss, **negative sampling**.
4. Evaluation: cosine similarity tests + t-SNE plot.
5. Modular code: `src/` (data, model, train), `config.yaml`, notebook for results.

### 5. Milestones (≈ 4–5 days)
- Day 1: Preprocessing + vocab + sampling.
- Day 2–3: Models + training loop + negative sampling.
- Day 4: Evaluation + t-SNE viz.
- Day 5: README (theory summary + results plots), config, cleanup.

### 6. Resume bullet this produces
> Implemented **Word2Vec (CBOW & Skip-Gram) from scratch in PyTorch** with negative sampling, validated embeddings via cosine-similarity tests and **t-SNE** visualization, in a reproducible, modular codebase.

---

## How these change your CV
- After building **PRD 1 + 2 (deployed)**, swap them onto the CV (they're stronger than the Blockchain hackathon line).
- They add legitimately-earned keywords: **LangChain, RAG, FAISS, ChromaDB, Hugging Face, FastAPI, vector search, PyTorch** — all real and defensible in interviews.
- This makes your "AI / ML" skills line backed by *deployed products*, not just a training certificate.

## Suggested 3-week sprint
- **Week 1:** Node + Express + PostgreSQL API (close the backend gap) **+** start AskYourDocs.
- **Week 2:** Finish & deploy AskYourDocs (PRD 1).
- **Week 3:** Cold Email Generator (PRD 2) + polish GitHub READMEs. Apply daily throughout.
