# NIVORA — Think before you pay

> **Hyderabad iQOO Hackathon Entry Prototype**  
> *Bringing personally relevant spending context into the crucial moment right before payment confirmation.*

---

## 📌 Executive Summary

NIVORA addresses impulse spending at point-of-sale by inserting a **Smart Pause** before payment confirmation. Rather than acting as a traditional post-facto budgeting dashboard, NIVORA calculates exact projected remaining budget metrics in real-time, presents one actionable observation, and leaves the final decision with the user.

### 👥 Team Credentials
- **Rohith** — Team Lead & Product Design
- **Siddik** — Android Experience & Mobile Development
- **Chandu** — Decision Intelligence & Prompting

---

## 🛠️ Technology Stack

| Layer | Choice | Purpose |
| :--- | :--- | :--- |
| **Application** | React 19 + TypeScript + Vite | Fast, typed client SPA |
| **Styling** | Tailwind CSS v4 + Tokens CSS | Semantic dark mode system (`#0B0D0F` dark theme, primary amber `#FFBF1A`) |
| **Motion** | Framer Motion | Signature aperture contraction and pause mark choreography |
| **State** | Zustand + Integer Paise Math | Lightweight persistent state stores with integer paise arithmetic |
| **QR Engine** | Zod + `qrcode` + `jsqr` | Typed schema validation, demo QR generator, and canvas camera/file scanner |
| **Testing** | Vitest + React Testing Library | Unit tests for paise arithmetic, local rules, and idempotency guards |

---

## 🚀 Quick Start Guide

### 1. Installation
```bash
npm install
```

### 2. Development Preview
```bash
npm run dev
```
Open [http://localhost:5173](http://localhost:5173) in your browser.

### 3. Production Build
```bash
npm run build
```

### 4. Run Automated Test Suite
```bash
npx vitest run
```

---

## 🧪 Evaluator Demo Scenarios

Evaluators can test the 7 pre-seeded scenarios directly using the **Demo Scenario Presets** drawer in the desktop side panel or mobile menu:

1. **Primary Café Demo (₹650)**: Seeded dining budget ₹820 remaining $\rightarrow$ Smart Pause projects **₹170 remaining**.
2. **Small Purchase (₹120)**: ₹820 remaining $\rightarrow$ Calm teal insight with **₹700 remaining**.
3. **Over-Budget (₹900)**: Exceeds remaining ₹820 budget by **₹80** (Muted coral warning highlight).
4. **Review & Cancel**: User inspects comparative before/after balances and cancels (budget remains ₹820, logged in decision history).
5. **Context Unavailable**: Context toggled off in settings $\rightarrow$ Honest "No context available" message.
6. **Camera Fallback**: Camera permission rejection fallback with working file upload & sample QR paths.
7. **Invalid QR Payload**: Non-NIVORA QR payload rejected cleanly by Zod validator.

---

## 🔒 Disclaimers & Ethics

- **Concept Prototype · Simulated Payments**: No money is transferred.
- **Privacy First**: No real bank credentials, UPI PINs, Aadhaar numbers, or account balances are ever requested.
- **Hardware Boundary Disclosure**: The prototype runs client-side local rules (`LocalRulesProvider`). Snapdragon NPU acceleration and cross-app Android system payment interception are documented as future Android explorations.
