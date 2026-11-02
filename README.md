# 📦 Stock Management

> Application web fullstack de gestion de stock : API Spring Boot et interface React.

[![CI](https://github.com/tameze-prince/FullStack_Stock_Management_WebSite/actions/workflows/ci.yml/badge.svg)](https://github.com/tameze-prince/FullStack_Stock_Management_WebSite/actions/workflows/ci.yml)
![Spring Boot](https://img.shields.io/badge/Spring%20Boot-6DB33F?logo=springboot&logoColor=white)
![React](https://img.shields.io/badge/React-61DAFB?logo=react&logoColor=black)
![TypeScript](https://img.shields.io/badge/TypeScript-3178C6?logo=typescript&logoColor=white)
![PostgreSQL](https://img.shields.io/badge/PostgreSQL-336791?logo=postgresql&logoColor=white)
[![License: MIT](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)

<!-- À compléter : captures d'écran de l'application et lien de démo -->

## Structure

```
.
├── Stock-app-backend/   API Spring Boot (Maven, Dockerfile)
├── Stock-app-front/     Interface React (TypeScript)
├── render.yaml          Blueprint de déploiement Render
└── docs/DEPLOYMENT.md   Checklist de déploiement et réglages JVM
```

## Démarrage rapide

```bash
# API
cd Stock-app-backend
./mvnw spring-boot:run

# Interface
cd Stock-app-front
npm install
npm run dev
```

## Déploiement

Déployé sur Render via `render.yaml` (service Docker + base PostgreSQL). Le point de contrôle de santé est `/actuator/health`.
La checklist complète et l'explication des options JVM sont dans [`docs/DEPLOYMENT.md`](docs/DEPLOYMENT.md).

## Licence

[MIT](LICENSE) © ZEUFACK TAMEZE Prince