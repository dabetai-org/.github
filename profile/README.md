<h1 align="center">🩺 dabetai — AI-Powered Preventive Ecosystem for Diabetes</h1>

<p align="center">
  <em>A wearable-driven platform that predicts diabetes complications before they become irreversible.</em>
</p>

<p align="center">
  <a href="https://github.com/dabetai-org/mobile-app"><img src="https://img.shields.io/badge/Mobile_App-React_Native_0.79-61DAFB?logo=react&logoColor=white" alt="Mobile App"></a>
  <a href="https://github.com/dabetai-org/web-app"><img src="https://img.shields.io/badge/Web_Portal-Angular_19-DD0031?logo=angular&logoColor=white" alt="Web Portal"></a>
  <a href="https://github.com/dabetai-org/api"><img src="https://img.shields.io/badge/Core_API-NestJS_11-E0234E?logo=nestjs&logoColor=white" alt="Core API"></a>
  <a href="https://github.com/dabetai-org/ai-api"><img src="https://img.shields.io/badge/AI_API-FastAPI-009688?logo=fastapi&logoColor=white" alt="AI API"></a>
  <a href="https://github.com/dabetai-org/ai-models"><img src="https://img.shields.io/badge/AI_Models-scikit_learn-F7931E?logo=scikitlearn&logoColor=white" alt="AI Models"></a>
  <a href="https://github.com/dabetai-org/landing"><img src="https://img.shields.io/badge/Landing-Astro-BC52EE?logo=astro&logoColor=white" alt="Landing"></a>
</p>

<p align="center">
  <a href="README.md">🇬🇧 English</a> · <a href="README.es.md">🇪🇸 Español</a>
</p>

---

## 🎯 The Challenge

Diabetes management is often reactive. Patients lack visibility into the silent progression of dangerous complications — retinopathy, nephropathy, neuropathy, and diabetic foot — while healthcare providers suffer from a lack of continuous, real-time data to intervene early. **dabetai** solves this by providing a **preventive ecosystem** that fuses real-time biological data from wearables with clinical oversight and AI-powered risk prediction, shifting diabetes care from reactive to proactive.

## 🏗 Architecture

```
┌─────────────────────────────────────────────────┐
│              Mobile App (Patient Hub)            │
│     React Native + Expo + Tailwind CSS           │
└───────────────────────┬─────────────────────────┘
                        │ HTTPS / JWT
┌───────────────────────▼─────────────────────────┐
│              Core API (NestJS)                   │
│         PostgreSQL + Prisma + JWT Auth           │
└────┬──────────────────────┬─────────────────────┘
     │                      │
     ▼                      ▼
┌──────────────┐  ┌──────────────────┐
│  Web Portal  │  │  AI Inference    │
│  (Medical)   │  │  API             │
│  Angular 19  │  │  FastAPI +       │
│  Tailwind    │  │  scikit-learn    │
└──────────────┘  │  XGBoost         │
                  └────────┬─────────┘
                           │
                  ┌────────▼─────────┐
                  │  AI Models Core  │
                  │  Python/PyTorch  │
                  └──────────────────┘
```

## 📦 Repositories

| Repository | Purpose | Stack | Status |
|------------|---------|-------|--------|
| [mobile-app](https://github.com/dabetai-org/mobile-app) | Patient hub for glucose monitoring, wearable sync, and AI risk alerts | React Native 0.79, Expo 53, Tailwind CSS | ✅ Active |
| [web-app](https://github.com/dabetai-org/web-app) | Medical portal for remote patient oversight and clinical insights | Angular 19, Tailwind CSS | ✅ Active |
| [api](https://github.com/dabetai-org/api) | Core REST API: auth, users, medical data, AI communication | NestJS 11, PostgreSQL, Prisma | ✅ Active |
| [ai-api](https://github.com/dabetai-org/ai-api) | AI inference API for real-time complication risk prediction | FastAPI, Python 3.11, MongoDB | ✅ Active |
| [ai-models](https://github.com/dabetai-org/ai-models) | ML pipelines: training, evaluation, and serialization of predictive models | Python, scikit-learn, XGBoost, PyTorch | ✅ Active |
| [landing](https://github.com/dabetai-org/landing) | Educational landing page presenting the ecosystem | Astro, Tailwind CSS | ✅ Active |

## 🧠 How It Works

1. **Patients** use the **Mobile App** to log glucose, food, medication, and physical activity — or sync with wearables (CGMs) for real-time biomarkers like heart rate and sleep quality
2. **Healthcare providers** connect via the **Web Portal** to monitor patients remotely, review clinical trends, and receive AI-driven alerts
3. The **AI Inference API** processes patient data through trained machine learning models to forecast the risk of specific complications: retinopathy, nephropathy, neuropathy, and diabetic foot
4. Both patients and doctors receive early warnings, enabling timely intervention before complications become irreversible

## 🔬 Research

Published paper: *"Prevención de Riesgos de la Diabetes Mediante una Plataforma Inteligente de Monitorización y Predicción de Complicaciones con Inteligencia Artificial"* — [Read the full paper](https://chrisssp.vercel.app/assets/docs/papers/Prevenci%C3%B3n-de-Riesgos-de-la-Diabetes-Mediante-una-Plataforma-Inteligente-de-Monitorizaci%C3%B3n-y-Predicci%C3%B3n-de-Complicaciones-con-Inteligencia-Artificial.pdf)

## 🛡 Privacy & Security

- End-to-end JWT authentication
- Role-Based Access Control (RBAC)
- Encrypted medical data storage
- Secure wearable device integration

## 🤝 Contributing

We follow a strict PR-based workflow. Check each repository's `CONTRIBUTING.md` for guidelines.

---

<p align="center">
  <sub>Built with ❤️ by the dabetai team · 2025</sub>
</p>
