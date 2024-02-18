# REST API

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- les verbes HTTP ✔️
- les statuts HTTP ✔️
- les endpoints ✔️
- CORS ✔️
- la nomenclature recommandée pour les routes ✔️

## 💻 J'utilise

### Un exemple personnel commenté ✔️

```
// récupération d'une annonce par son id :

app.get("/ads/:id", async (req: Request, res: Response) => {
    // récupérer une annonce par son id
  try {
    const ad = await Ad.findOne({
      where: { id: parseInt(req.params.id, 10) },
      relations: { category: true, tags: true },
    });
    // si l'annonce n'existe pas, retourner un code 404
    if (!ad) return res.sendStatus(404);
    // sinon retourner l'annonce
    res.send(ad);
  } catch (err) {
    console.log(err);
    res.sendStatus(500);
  }
});
```

### Utilisation dans un projet ✔️

[lien github](https://github.com/ComicScrip/the-good-corner-nov23/blob/crud-categories/backend/src/index.ts)

Description : projet en formation visant à réaliser un clone de Le Bon Coin

## 🌐 J'utilise des ressources

### Repository de Prisma

- https://github.com/prisma/prisma-examples/tree/latest/typescript/rest-express
- Exemple d'API REST en utilisant Express JS et l'ORM Prisma

### HTTP Cat

- https://http.cat/
- Comprendre les codes HTTP avec humour

### REST API in 100s

- https://www.youtube.com/watch?v=-MTSQjw5DrM
- Vidéo youtube expliquant le principe d'une API REST et comment l'appliquer avec Express JS
