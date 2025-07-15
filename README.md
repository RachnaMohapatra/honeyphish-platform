# 🛡️ HoneyPhish: Vendor Security Awareness & Cyber Risk Evaluation Platform

**HoneyPhish** is a secure, scalable web platform that empowers enterprises to assess and manage the cybersecurity posture of their third-party vendors. It combines a **Vendor Risk Assessment Portal** with a **Gamified Phishing Simulation System**, backed by real-time analytics, smart scoring, and dynamic feedback—all wrapped in a sleek **dark-glass UI with 3D particles**.
---

## 🎯 Objective

To build a full-stack, enterprise-grade solution that:

- Tracks and improves vendors' cybersecurity behavior  
- Delivers immersive phishing awareness training (HoneyPhish)  
- Provides internal teams with real-time vendor performance analytics  
- Offers badge-based gamification to drive security best practices  

---

## 1️⃣ Core Platform Features

### 🔐 User Authentication & Roles

- JWT/Supabase Auth for secure login  
- Role-based access control: **Admin** and **Vendor**

### 📝 Vendor Self-Service Portal

- HTTPS & SSL usage  
- MFA implementation  
- Data encryption (at rest & in transit)  
- Breach history  
- Retention and deletion policies  

### 📊 Automated Risk Scoring Engine

- Weighted scoring for form inputs  
- Generates **Trust Score** (Trusted, Caution, Risky)  
- Stores data in PostgreSQL/Supabase

### 🧑‍💻 Admin Dashboard

- View & filter all vendors with Trust Scores  
- Take action: Request Fix / Flag Risk / Send Email  
- Visual graphs: score timelines, risk factors, audit logs

### 🧾 Evidence Upload & Third-Party Checks

- Vendors upload documents and certificates  
- API Integration:  
  - [SSL Labs](https://www.ssllabs.com/)  
  - [HaveIBeenPwned](https://haveibeenpwned.com/)

### 🚨 Alerts & Recommendations

- Suggests improvements (e.g., "Enable MFA")  
- Real-time alerts on risk changes  
- Integrated AI Chatbot (OpenAI GPT) for vendor queries  

---

## 2️⃣ HoneyPhish: Phishing Awareness Simulation System

### 📬 Fake Mailbox UI (Mailbox.tsx)

- Simulated inbox with phishing & safe emails  
- "Click Link" → redirect to `/fail.html`, score −10  
- "Report as Suspicious":  
  - If phishing → reward email + score increase  
  - If safe → warning email (no score change)  
- Dynamic email feedback (no popups)

### ❌ Fail Page

- Large warning: **You failed the phishing simulation**  
- Score deduction notice + security tip  
- Navigation back to inbox  

### 📊 Admin Phishing Dashboard

- Logs: clicks vs reports  
- Score history chart (Chart.js)  
- Vendor activity overview  
- CSV Export Option  

### 🏆 Vendor Leaderboard

- Ranks vendors based on awareness score  
- Badges:  
  - 🏆 Platinum ≥ 90  
  - 🥇 Gold ≥ 80  
  - 🥈 Silver ≥ 70  
  - 🥉 Bronze ≥ 60  
- Animated tooltips + search by name  

---

## 3️⃣ UI & Visual Design

### 🌙 Glass UI Theme

- Glassmorphism (blurred, translucent cards)  
- Color scheme: **Black + Neon Blue/Purple**  
- Fonts: Inter / Poppins / Sora  
- Microinteractions & hover effects  

### 🌌 3D Particle Background

- Glowing particles & animated lines  
- Interaction: hover (connect/repel), click (pulse)  
- Powered by `tsParticles` / `three.js`  
- Full-screen, blurred & responsive  

---

## 4️⃣ Tech Stack

| Layer       | Technologies                                         |
|-------------|------------------------------------------------------|
| Frontend    | React (TypeScript), TailwindCSS, Vite, Radix UI      |
| Backend     | Node.js + Express / NestJS                           |
| Auth        | Supabase Auth / JWT                                  |
| DB          | PostgreSQL / Supabase                                |
| Storage     | AWS S3 / Supabase Storage                            |
| Charts      | Chart.js, Recharts                                   |
| Particles   | tsParticles, three.js                                |
| AI Assistant| OpenAI GPT API                                       |
| State Mgmt  | Context API / Redux                                  |
| Deployment  | Vercel, Netlify, Render, AWS                         |

---

## 🚀 Deployment

The project is live and hosted on **Netlify**:

🔗 **https://honeyphish-platform.netlify.app/**

Feel free to explore the platform and interact with the simulation to see all the features in action.

---

## 📜 Project Background

HoneyPhish was developed as part of a national-level cybersecurity innovation hackathon under the theme:

> 🛡️ **"Building Trust in Retail with Cybersecurity"**

The goal was to explore how retailers can strengthen their digital trust by proactively addressing third-party risk, phishing awareness, and vendor accountability. In modern retail, vendors often have access to customer data, supply chain systems, and transaction workflows — making them a critical point of potential compromise.

HoneyPhish addresses this gap by combining:
- 🧠 A **Vendor Risk Assessment System** that scores vendor practices like encryption, MFA usage, and breach history  
- 📬 A **Phishing Simulation Platform** that tests real-time awareness and rewards secure behavior  
- 📊 A comprehensive **Admin Dashboard** that gives internal security teams full visibility into vendor security posture  

This aligns directly with the hackathon’s focus on:
- Zero-trust security frameworks  
- Phishing resilience and fraud prevention  
- Transparent vendor scoring to enhance digital trust  
- Real-time, AI-enhanced threat mitigation strategies  

By merging automation, gamification, and educational awareness, HoneyPhish helps enterprises (like retailers) ensure that every vendor they work with is **verified, security-conscious, and continuously improving** — building trust in the supply chain from the ground up.

