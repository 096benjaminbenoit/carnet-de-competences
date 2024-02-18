# GraphQL

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- la différence entre REST et GraphQL ✔️
- les besoins auxquels répond GraphQL ✔️
- la définition d'un schéma
- Query ✔️
- Mutation ✔️
- Subscription ❌

## 💻 J'utilise

### Un exemple personnel commenté ✔️

```
// suppression d'un livre par son id :
  
  @Mutation(() => String)
  async deleteBook(@Arg("bookId") id: number) {
    // récupération du livre par son id
    const book = await Book.findOne({ where: { id } });
    // si le livre n'est pas trouvé, on renvoie une erreur
    if (!book) throw new GraphQLError("not found");
    // sinon, on supprime le livre
    await book.remove();
    return "deleted";
  }
```

### Utilisation dans un projet ✔️

[lien github](https://github.com/096benjaminbenoit/graphql-api-starter)

Description : Un projet personnel visant à créer un starter pack pour une API GrapQL.

## 🌐 J'utilise des ressources

### Documentation officielle de GraphQL

- https://graphql.org/