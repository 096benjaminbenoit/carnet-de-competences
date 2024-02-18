# TypeScript

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'intéret de TypeScript dans l'IDE ✔️
- les types de bases ✔️
- comment et pourquoi étendre une interface ✔️
- les classes et les decorators ✔️

## 💻 J'utilise

### Un exemple personnel commenté ✔️

```
// typage d'une requête axios //

// je type mon state pour qu'il reçoit un tableau de catégories
  const [categories, setCategories] = useState<Category[]>([]);

  useEffect(() => {
    axios
    // la requête doit récupérer un tableau de catégories
      .get<Category[]>("http://localhost:4000/categories")
      .then((res) => setCategories(res.data))
      .catch(console.error);
  }, []);

  const router = useRouter();

    // je type les événements
  const handleSubmit = async (e: FormEvent<HTMLFormElement>) => {
    e.preventDefault();
    const formData = new FormData(e.target as HTMLFormElement);
    const formJSON: any = Object.fromEntries(formData.entries());
    formJSON.price = parseFloat(formJSON.price);

    axios
      .post("http://localhost:4000/ads", formJSON)
      .then((res) => {
        router.push(`/ads/${res.data.id}`);
      })
      .catch(console.error);
  };
```

### Utilisation dans un projet ✔️

[lien github](https://github.com/096benjaminbenoit/graphql-api-starter)

Description : Un projet personnel visant à créer un starter pack pour une API GrapQL écrit en Typescript

## 🌐 J'utilise des ressources

### Documentation officielle Typescript

- https://www.typescriptlang.org/docs/
- documentation officielle de Typescript

### Tutoriel et exercices Typescript

- https://www.totaltypescript.com/tutorials/beginners-typescript
- tuto et exercice pour voir les concepts en typescript (type, interface, etc)