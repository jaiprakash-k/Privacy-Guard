# Privacy Guard  
### Automated PII Redaction Middleware for RAG Systems

Privacy Guard is a middleware solution that protects sensitive data before it reaches external Large Language Models (LLMs).  
It enables organizations to safely use AI and RAG pipelines without exposing Personally Identifiable Information (PII).

---

## 🚩 Problem

Organizations using AI systems often send raw internal documents (customer data, medical records, financial details, API keys, etc.) directly to external LLM providers.

This creates:

- Privacy violations  
- Regulatory non-compliance (DPDPA, GDPR, RBI norms)  
- Data breach risks  
- Financial and reputational damage  

There is no reliable, architecture-level mechanism to prevent sensitive data from leaving the organization while still preserving AI reasoning quality.

---

## 💡 Solution

Privacy Guard acts as a secure middleware layer between enterprise systems and AI models.

It:

1. Detects sensitive data (structured + unstructured)
2. Masks it using reversible anonymization
3. Sends only the safe version to the LLM
4. Restores original data after AI processing

The AI never sees real PII — but the final user response remains complete and accurate.

---

## 🏗️ Architecture Overview

User → RAG Retrieval → Detection Engine → Masking Engine → External LLM → Restoration Engine → Final Response

Key principle:
All sensitive data remains inside the secure enterprise environment.

---

## 🔍 Core Features

- Hybrid PII detection (Regex + NER)
- Reversible anonymization
- Session-based secure lookup table
- On-premise deployable
- RAG-native architecture
- LLM-agnostic integration
- Audit logging support
- Compliance-ready design

---

## 🛠️ Technologies Used

### Backend
- Node.js
- Express / Fastify

### PII Detection
- Custom Regex Engine
- Luhn Algorithm
- spaCy / Microsoft Presidio

### Storage
- Redis (Session-based lookup table)

### RAG
- Pinecone / Weaviate / pgvector

### Frontend
- React.js
- TypeScript

### Deployment
- Docker
- Kubernetes (Optional)

---

## 🔐 How It Works

1. User submits a query.
2. RAG retrieves relevant documents.
3. Middleware scans for sensitive data.
4. Sensitive values are replaced with placeholders.
5. Real values are stored securely in Redis (session-based).
6. Masked data is sent to the LLM.
7. Response is restored before reaching the user.

---

## 🎯 Target Use Cases

- BFSI
- Healthcare
- SaaS platforms
- Legal firms
- Government systems

---

## 📈 Future Scope

- Multilingual PII detection
- Enterprise compliance dashboard
- Advanced audit reporting
- On-premise AI model hosting
- GPU acceleration (AMD-based deployments)

---

## 📌 Estimated Implementation Cost

MVP Development: ₹3 – ₹6 Lakhs  
Monthly Prototype Infrastructure: ₹20,000 – ₹50,000  

Scalable to enterprise-grade deployment.

---

## 🧠 Key Advantage

Privacy Guard protects sensitive data without reducing AI performance.

The AI gets context.  
The organization keeps control.  
The data never leaves the building.

---

## 📜 License

MIT License (for open-source core version)

---

## 👥 Team

Team Name: Primestack  
Project: Privacy Guard  
Competition: AMD Slingshot  

---
