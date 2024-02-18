# Docker

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- la création d'une image docker ✔️
- l'éxécution d'un container ✔️
- l'orchestration de containers avec docker-compose ✔️

## 💻 J'utilise

### Un exemple personnel commenté ✔️

```
// on déclare les différents services
services:
    // mon service s'appelle "db", il utilise une image officielle postgres stockée dans docker hub
  db:
    image: postgres:15-alpine
    environment:
      POSTGRES_PASSWORD: postgres
    // on vérifie l'etat de la base de données
    healthcheck:
      test: ["CMD-SHELL", "pg_isready"]
      interval: 20s
      timeout: 5s
      retries: 5

  // mon service s'appelle "api" et c'est mon application
  api:
    // si jamais la base de données n'est pas en état, l'application ne se lance pas
    depends_on:
      db:
        condition: service_healthy
    build: .
    // je rend l'application disponible sur le port 4000
    ports:
      - "4000:4000"
    // je stock les données dans un volume
    volumes:
      - ./src:/app/src
```

### Utilisation dans un projet ✔️

[lien github](https://github.com/096benjaminbenoit/graphql-api-starter)

Description : Un projet personnel visant à créer un starter pack pour une API GrapQL, le tout dockerisé.

## 🌐 J'utilise des ressources

### Documentation officielle de Docker

- https://docs.docker.com/
- documentation officielle de Docker

### Cours de David Elbaze

- https://delbaze.notion.site/Docker-b3778e65ac284f29a3b722a8bb93bcb9
- cours Notion d'un des formateurs de la WildCode School

### Docker illustré

- https://www.youtube.com/watch?v=caXHwYC3tq8&t=2s
- vidéo illustrant Docker