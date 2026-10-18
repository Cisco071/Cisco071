### Hi, I'm Francisco 👋

MBA candidate at UC Berkeley Haas exploring applied AI and full-stack engineering. I build projects
end to end and test them honestly: each one below ships with its evaluation, the evidence, and a
written account of what didn't work.

**Working with:** Python · PyTorch · Claude API & multi-agent pipelines · local LLMs (Gemma, Ollama) · RAG and
retrieval · evals · reinforcement learning · TypeScript / Next.js · Postgres · Jupyter

### 🤖 AI / Machine Learning

**[spotify-multi-agent-pipeline](https://github.com/Cisco071/spotify-multi-agent-pipeline)** — A
multi-agent pipeline that turns **150,000 real Spotify Play Store reviews** (from a 660,622-row, 97 MB file) into a
traceable product recommendation. Code orchestrates parallel Claude Haiku agents (≤50 reviews per request) for
labeling, an independent Claude Sonnet verifier, code-owned grouping, ranking and anomaly detection, and a memo agent
whose every number is re-checked by code. 149,996 of 150,000 reviews were classified for about $12.70 in API spend,
with saved progress, crash recovery and a recorded interrupt-and-resume. Evaluated against 50 hand-labeled reviews,
a blind verifier, planted errors and prompt-injection tests. Results are served from Neon Postgres to a
[live Next.js dashboard](https://spotify-review-insights-dun.vercel.app) with period filters, event-annotated trends and
recurring-problem views. The README documents the failures and where the labels disagree.

**[personal-wiki-gemma-rag](https://github.com/Cisco071/personal-wiki-gemma-rag)** — A personal
knowledge assistant that runs **fully offline** on a MacBook Air. My own CLI and harness connect a local
Gemma 4 E4B model (4-bit, 3.1 GB on the GPU via Ollama) to my class notes, with three modes:
*ask* gives cited, grounded answers or reports insufficient evidence, *search* shows the original
passages, and *chat* is an assistant with conversation memory that looks up notes only when needed.
It uses hybrid retrieval (BM25 + EmbeddingGemma) and an Obsidian wiki that the model generates and links from the source notes.
All four ask-mode tests pass offline (1–6 s per answer), and the README documents seven failures I found and fixed.

**[mini-llm-class4](https://github.com/Cisco071/mini-llm-class4)** — A 122K-parameter nanoGPT
language model trained from scratch and evaluated before and after training on a fixed 48-case suite. On
the scorable cases, accuracy rose from 37.5% (untrained) to 83.3% on the starter corpus, and to 100% after
I extended the corpus with my own teaching sentences. The training data is checked for eval leakage, and the
repo includes an interactive training dashboard and a terminal chat interface.

**[class3-pacman-dqn](https://github.com/Cisco071/class3-pacman-dqn)** — Deep Q-Network trained on
`ALE/MsPacman-v5` (Atari) from raw pixels. Trained for 200 episodes (~30K learning updates), raising
mean evaluation score from 492 → 760 (+54%) over an untrained baseline. Full writeup covers
hyperparameter choices, training dynamics, and an honest limitations section (training was not
monotonic — score peaked around episode 140 before drifting down). Includes the executed notebook,
training dashboard, and gameplay GIFs at each checkpoint.

### 🛠️ Full-Stack Engineering

**[networking-tracker](https://github.com/Cisco071/networking-tracker)** — A secure contact-tracking
app built on Next.js and Neon Postgres, with Neon Managed Better Auth and the Neon Data API. The
frontend calls the database's REST API directly; Postgres Row Level Security (not application code)
enforces that every user can only ever see or modify their own rows. Includes a password-reset flow,
an automated test suite, and a README documenting the schema, security model, and deployment.

### ☁️ Cloud Computing

**[Cloud-computing-course-](https://github.com/Cisco071/Cloud-computing-course-)** — Exercises from a
cloud computing fundamentals course.
