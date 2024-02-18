# Titre de la compétence

> ❌ A travailler

> ✔️ Auto validation par l'étudiant

## 🎓 J'ai compris et je peux expliquer

- l'état (_state_) pour contrôler l'affichage d'un composant ✔️
- les composants enfants et les _props_ qu'on leur passe ✔️
- le déclenchement d'instructions en fonction des actions de l'utilisateur ✔️
- le déclenchement d'instructions en fonction de l'étape du cycle de vie du composant ou du changement de valeur de ses props ✔️
- l'usage d'un reducer (_useReducer_) pour gérer un état composé dans un composant ❌
- l'état stocké dans un composant avec un _context provider_ et accessible dans ses descendants via `useContext` ❌

## 💻 J'utilise

### Un exemple personnel commenté ✔️

```
// composant React //

export default function MapInformations({ selectedFactory }) {
    // rendu conditionnel
  if (!selectedFactory) {
    return (
      <div className="text-xl text-center py-20 px-5">
        Sélectionnez un point sur la carte pour voir les détails
      </div>
    );
  }

  return (
    <div className="bg-slate-100 p-10">
      <div className="border-t-4 border-rose-600 bg-white h-full">
        <h2 className="text-center text-xl font-bold py-2">
            // récupération des données reçu d'un composant parent
          {selectedFactory.factoryName}
        </h2>
        <div className="flex justify-center gap-5">
          <FaMapMarkerAlt className="text-rose-600" />
          <p>
            {selectedFactory.address}, {selectedFactory.postCode}
          </p>
        </div>
        // passage de props dans un composant enfant
        <Meteo selectedFactory={selectedFactory} />
      </div>
    </div>
  );
}
```

### Utilisation dans un projet ✔️

[lien github](https://github.com/096benjaminbenoit/meteo-simplon)

Description : projet d'étude visant à intégrer dans une petit app React, une carte avec des informations dynamiques

### Utilisation en production si applicable ✔️

[lien du projet](https://github.com/096benjaminbenoit/percuson-vitrine)

Description : Vitrine réalisée en React et déployée dans le cadre de mon alternance

## 🌐 J'utilise des ressources

### Documentation officielle React

- https://fr.react.dev/
- documentation React

### Série vidéos apprendre React

- https://www.youtube.com/watch?v=hhe6Xb4Em5U&list=PLjwdMgw5TTLUEOKPg5Z5TgwAOeWkjGL69
- série de vidéos youtube pour apprendre React