<h1 align="center">🩺 dabetai — Ecosistema Preventivo Impulsado por IA para la Diabetes</h1>

<p align="center">
  <em>Una plataforma basada en wearables que predice complicaciones de la diabetes antes de que sean irreversibles.</em>
</p>

<p align="center">
  <a href="https://github.com/dabetai-org/mobile-app"><img src="https://img.shields.io/badge/App_M%C3%B3vil-React_Native_0.79-61DAFB?logo=react&logoColor=white" alt="App Móvil"></a>
  <a href="https://github.com/dabetai-org/web-app"><img src="https://img.shields.io/badge/Portal_Web-Angular_19-DD0031?logo=angular&logoColor=white" alt="Portal Web"></a>
  <a href="https://github.com/dabetai-org/api"><img src="https://img.shields.io/badge/Core_API-NestJS_11-E0234E?logo=nestjs&logoColor=white" alt="Core API"></a>
  <a href="https://github.com/dabetai-org/ai-api"><img src="https://img.shields.io/badge/AI_API-FastAPI-009688?logo=fastapi&logoColor=white" alt="AI API"></a>
  <a href="https://github.com/dabetai-org/ai-models"><img src="https://img.shields.io/badge/AI_Models-scikit_learn-F7931E?logo=scikitlearn&logoColor=white" alt="AI Models"></a>
  <a href="https://github.com/dabetai-org/landing"><img src="https://img.shields.io/badge/Landing-Astro-BC52EE?logo=astro&logoColor=white" alt="Landing"></a>
</p>

<p align="center">
  <a href="README.md">🇬🇧 English</a> · <a href="README.es.md">🇪🇸 Español</a>
</p>

---

## 🎯 El desafío

El manejo de la diabetes suele ser reactivo. Los pacientes no tienen visibilidad de la progresión silenciosa de complicaciones peligrosas — retinopatía, nefropatía, neuropatía y pie diabético — mientras que los médicos carecen de datos continuos en tiempo real para intervenir a tiempo. **dabetai** resuelve esto proporcionando un **ecosistema preventivo** que fusiona datos biológicos en tiempo real de wearables con supervisión clínica y predicción de riesgos mediante IA, transformando el cuidado de la diabetes de reactivo a proactivo.

## 🏗 Arquitectura

```
┌─────────────────────────────────────────────────┐
│           App Móvil (Paciente)                   │
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
│  Portal Web  │  │  AI Inference   │
│  (Médicos)   │  │  API            │
│  Angular 19  │  │  FastAPI +      │
│  Tailwind    │  │  scikit-learn   │
└──────────────┘  │  XGBoost        │
                  └────────┬─────────┘
                           │
                  ┌────────▼─────────┐
                  │  AI Models Core  │
                  │  Python/PyTorch  │
                  └──────────────────┘
```

## 📦 Repositorios

| Repositorio | Propósito | Stack | Estado |
|-------------|-----------|-------|--------|
| [mobile-app](https://github.com/dabetai-org/mobile-app) | Centro del paciente para monitoreo de glucosa, sincronización con wearables y alertas de riesgo IA | React Native 0.79, Expo 53, Tailwind CSS | ✅ Activo |
| [web-app](https://github.com/dabetai-org/web-app) | Portal médico para supervisión remota de pacientes e insights clínicos | Angular 19, Tailwind CSS | ✅ Activo |
| [api](https://github.com/dabetai-org/api) | API REST principal: auth, usuarios, datos médicos, comunicación con IA | NestJS 11, PostgreSQL, Prisma | ✅ Activo |
| [ai-api](https://github.com/dabetai-org/ai-api) | API de inferencia IA para predicción de riesgo de complicaciones en tiempo real | FastAPI, Python 3.11, MongoDB | ✅ Activo |
| [ai-models](https://github.com/dabetai-org/ai-models) | Pipelines de ML: entrenamiento, evaluación y serialización de modelos predictivos | Python, scikit-learn, XGBoost, PyTorch | ✅ Activo |
| [landing](https://github.com/dabetai-org/landing) | Página educativa que presenta el ecosistema | Astro, Tailwind CSS | ✅ Activo |

## 🧠 ¿Cómo funciona?

1. **Pacientes** usan la **App Móvil** para registrar glucosa, comidas, medicación y actividad física — o sincronizan con wearables (MCG) para obtener biomarcadores en tiempo real como ritmo cardíaco y calidad del sueño
2. **Médicos** se conectan vía el **Portal Web** para monitorear pacientes de forma remota, revisar tendencias clínicas y recibir alertas generadas por IA
3. La **API de Inferencia IA** procesa los datos del paciente mediante modelos de machine learning entrenados para pronosticar el riesgo de complicaciones específicas: retinopatía, nefropatía, neuropatía y pie diabético
4. Tanto pacientes como médicos reciben alertas tempranas, permitiendo una intervención oportuna antes de que las complicaciones se vuelvan irreversibles

## 🔬 Investigación

Artículo publicado: *"Prevención de Riesgos de la Diabetes Mediante una Plataforma Inteligente de Monitorización y Predicción de Complicaciones con Inteligencia Artificial"* — [Leer el artículo completo](https://chrisssp.vercel.app/assets/docs/papers/Prevenci%C3%B3n-de-Riesgos-de-la-Diabetes-Mediante-una-Plataforma-Inteligente-de-Monitorizaci%C3%B3n-y-Predicci%C3%B3n-de-Complicaciones-con-Inteligencia-Artificial.pdf)

## 🛡 Privacidad y seguridad

- Autenticación JWT de extremo a extremo
- Control de Acceso Basado en Roles (RBAC)
- Almacenamiento encriptado de datos médicos
- Integración segura con dispositivos wearables

## 🤝 Contribuciones

Seguimos un flujo de trabajo estricto basado en PRs. Revisa el `CONTRIBUTING.md` de cada repositorio para lineamientos.

---

<p align="center">
  <sub>Hecho con ❤️ por el equipo dabetai · 2025</sub>
</p>
