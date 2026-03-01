
# Sarkari Saathi

An open-source, deterministic rule engine and semantic search platform designed to solve information asymmetry in Indian government scheme distribution. Built for FOSS Hack 2026.

## System Architecture



Sarkari Saathi abandons standard CRUD architecture in favor of a Retrieval-Augmented Generation (RAG) pipeline to ensure zero-hallucination, deterministic eligibility matching.

### Tech Stack
* **Frontend:** Next.js, TypeScript, Tailwind CSS (Server-Side Rendered for SEO and low-latency interaction).
* **Backend:** Node.js, Express.js (Handles ETL ingestion scripts and API routing).
* **Database:** MongoDB Atlas with Vector Search (Stores high-dimensional embeddings of scheme criteria).
* **Deployment (Target):** Dockerized Node.js backend on AWS EC2, static Next.js assets on AWS S3/CloudFront.

## Engineering Objectives
1. **Data Ingestion:** Automated ETL pipelines to scrape, clean, and vectorize raw scheme data.
2. **Semantic Matching:** Map complex user demographic JSON payloads against vectorized scheme constraints.
3. **Deterministic Output:** Utilize hard boolean logic to verify final eligibility, bypassing LLM hallucination risks.

## Local Development Setup

### Prerequisites
* Node.js (v18+)
* MongoDB Atlas Cluster (with Vector Search enabled)

### Installation
1. Clone the repository:
   \`git clone https://github.com/someshsinha/sarkari-saathi-foss.git\`
2. Install Frontend Dependencies:
   \`cd frontend && npm install\`
3. Install Backend Dependencies:
   \`cd ../backend && npm install\`
4. Configure environment variables in `backend/.env` (MongoDB URI, LLM API Keys).
5. Start development servers:
   * Frontend: \`npm run dev\`
   * Backend: \`node server.js\` (or setup nodemon)

## License
MIT License. See `LICENSE` for details.
