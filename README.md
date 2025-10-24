# CrewIA Dropshipper

Système d'automatisation e-commerce multi-boutiques avec intelligence artificielle et architecture distribuée.

## Vue d'ensemble

Plateforme d'automatisation complète pour la gestion de boutiques en ligne, intégrant web scraping intelligent, traitement de données massif, génération de contenu par IA et publication multi-canal.

## Stack technique

**Backend & Core**
- Python 3.11+ (asyncio, async/await)
- FastAPI (API REST asynchrone)
- MongoDB + Beanie ODM (base de données NoSQL)
- Redis (cache & queue)
- Celery (task queue distribuée)

**Intelligence Artificielle**
- Agents IA multi-spécialisés (analyse, rédaction, stratégie)
- Modèles LLM (OpenSource + API routing)
- NLP pour génération de contenu optimisé
- Système de scoring intelligent des produits

**Scraping & Automation**
- Playwright (browser automation headless)
- Architecture multi-proxy avec rotation
- Anti-détection & fingerprinting
- Traitement asynchrone haute performance

**Infrastructure**
- Architecture microservices
- Docker containerization
- Système de checkpoint/resume pour résilience
- Monitoring avec health checks

## Architecture

```
┌─────────────────┐
│  Input Handler  │  → Validation, scoring, multi-format support
└────────┬────────┘
         │
┌────────▼────────┐
│   AI Enterprise │  → Agents autonomes, workflow routing
└────────┬────────┘
         │
┌────────▼────────┐
│    Extractor    │  → Web scraping, data enrichment
└────────┬────────┘
         │
┌────────▼────────┐
│ Content Gen     │  → Optimisation SEO, génération contenu
└────────┬────────┘
         │
┌────────▼────────┐
│   Publisher     │  → API SP-API Amazon, batch processing
└─────────────────┘
```

## Modules principaux

### Input Handler
- Lecture multi-format (CSV, JSON, XLSX, URL)
- Validation Pydantic V2 avec règles métier
- Système de scoring 0-100 (5 métriques)
- Checkpoint manager (file & Redis backends)

### AI Enterprise
- Manager d'agents avec capability detection
- Workflow router intelligent
- Celery bridge pour intégration legacy
- API Gateway avec métriques temps réel

### Publisher
- Intégration Amazon SP-API avec gestion quotas
- Traitement par lot (batch) optimisé
- Feed builder XML conforme
- Error handling & retry logic
- Image processing avec optimisation

### Interface
- CLI interactif (Rich)
- Dashboard Streamlit avec visualisations
- Système de navigation par menus
- Formatters pour affichage structuré

## Points techniques notables

- **Async-first**: Architecture entièrement asynchrone pour performances optimales
- **Type safety**: Utilisation intensive de Pydantic V2 pour validation runtime
- **Resilience**: Checkpoint/resume, retry mechanisms, graceful shutdown
- **Testing**: Suite de tests complète (unit + integration) avec pytest-asyncio
- **Code quality**: Black, isort, mypy, pre-commit hooks
- **Logging**: Loguru avec contexte structuré
- **Scalabilité**: Design multi-instance avec état partagé Redis

## Structure du projet

```
crewia-dropshipper/
├── src/
│   ├── input_handler/      # Validation & scoring produits
│   ├── ai_enterprise/      # Système d'agents IA
│   ├── extractor/          # Web scraping
│   ├── content_generator/  # Génération contenu
│   ├── publisher/          # Publication Amazon SP-API
│   ├── interface/          # CLI & dashboard
│   ├── batch/              # Traitement par lot
│   ├── database/           # MongoDB models & client
│   └── config/             # Configuration & settings
├── tests/
│   ├── unit/
│   └── integration/
└── pyproject.toml          # Poetry dependencies
```

## Technologies clés

`Python` `FastAPI` `MongoDB` `Redis` `Celery` `Playwright` `Pydantic` `asyncio` `Docker` `Pytest` `AI/LLM` `REST API` `Web Scraping` `Microservices`

---
