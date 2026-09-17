# Mihir Mohite

**Pune, India** · B.Tech ECE (Electrical), AI & ML specialisation · MIT-WPU · CGPA 8.62

I work on LLM retrieval and evaluation, and on embedded sensor rigs. The common thread is
measurement — most of what I build exists to find out whether something actually works.

Founding Engineer at **ForeSites** · ML Intern at **BeyondBot** · President of **CoDeC**

[![Email](https://img.shields.io/badge/mihir.moe@gmail.com-D14836?style=flat-square&logo=gmail&logoColor=white)](mailto:mihir.moe@gmail.com)
<!-- TODO: paste your LinkedIn URL here and uncomment
[![LinkedIn](https://img.shields.io/badge/LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://linkedin.com/in/YOUR-HANDLE)
-->

---

## Repositories

### [lawmaster](https://github.com/lawn-mimower/lawmaster) — retrieval over Indian industrial law
`Python` · `FastAPI` · `LightRAG` · `Mistral OCR`

43 statutes, 1,210 pages, much of it Hindi and much of it tables. Uniform chunking
destroys legal text, so a router splits the corpus four ways — definitions, sections,
tables, amendments — and sends each to the store that suits it. Definitions become one
chunk per term; rate tables go to SQL because they are useless as prose; amendments are
resolved as diffs rather than retrieved. Answers cite back to the source page.

### [luna-reasoning-eval](https://github.com/lawn-mimower/luna-reasoning-eval) — how much reasoning a task actually needs
`Python` · `OpenAI` · `BFCL`

11 suites, 4 effort levels, ~9,000 API calls, a cost ledger on every one. Reasoning
transformed chained computation — multi-hop handover went 15% → 79% — but left retrieval
flat and made tool calling slightly worse for 34% more cost. The conclusion was to set
effort by task shape rather than globally. Ships with an adversarial audit of its own
results.

### [foresites](https://github.com/lawn-mimower/foresites) — construction snag management over WhatsApp
`Node` · `React` · `Python` · `AWS Lambda`

In a live client pilot. Multilingual, multimodal intake — English, Hindi and Marathi, as
text, voice or image. A vectorless retrieval skill queries PostgreSQL directly with no
embedding store, alongside a streaming NL-to-SQL agent over a 9-table schema. Both
serverless.

### [stereo-vergence-scanner](https://github.com/lawn-mimower/stereo-vergence-scanner) — 2D mapping on cheap parts
`C++` · `Python` · `ESP8266`

Two time-of-flight sensors on two servos, verging on a common point at each bearing. A
single sweeping sensor cannot tell a wall from the edge of a doorway; two verged ones can,
because the disagreement between them carries the information.

### [imu-drift-compensation](https://github.com/lawn-mimower/imu-drift-compensation) — measuring drift instead of assuming it
`C++` · `Python` · `scikit-learn`

Fits the drift of a stationary MPU6050 and subtracts it live, so the correction comes from
the sensor's own behaviour rather than a datasheet constant.

---

## Elsewhere

**AgroSense** — UAV RGB imagery into orthomosaics via a photogrammetry pipeline, with
ExG/VARI vegetation indices and K-Means zoning. An ESP32 ground module in embedded C
drives a Modbus soil sensor and GPS waypoint guidance, running on-device ML for NPK
estimation. Co-authored a review paper on low-cost precision-agriculture adoption.

**CoDeC** — ran Trifecta Challenge 2026, a three-day symposium with 350+ participants
across 87 teams, leading a core team of 15–20. Partnerships with GeeksforGeeks, HackerRank
and AlgoZenith.

---

## Tools

**Languages** `Python` `C++` `C` `Java` `SQL` `JavaScript`
**AI/ML** `PyTorch` `TensorFlow` `OpenCV` `scikit-learn` `RAG` `NL-to-SQL`
**Backend** `FastAPI` `Node.js` `Express` `REST` `SSE`
**Data** `PostgreSQL` `Supabase` `SQLite` `MongoDB` `Neo4j` `Pinecone`
**Cloud** `AWS Lambda` `S3` `GCP` `Azure` `Vercel` `Render`
**Hardware** `ESP32/ESP8266` `Arduino` `Modbus`

<sub>Certified: Azure Fundamentals (AZ-900) · AWS Academy Cloud Foundations · AWS Academy Cloud Security Foundations</sub>
