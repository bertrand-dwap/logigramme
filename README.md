# Éditeur de Logigramme

Ce projet est une application web permettant de créer, modifier, sauvegarder et exporter des logigrammes (diagrammes de décision) de manière interactive. Elle est entièrement construite avec HTML, CSS (Bootstrap) et JavaScript, sans backend.

---

## ✨ Fonctionnalités

- 🎨 Interface utilisateur simple et épurée (grâce à Bootstrap).
- ➕ Ajout dynamique de **questions** et **résultats**.
- 🔀 Navigation conditionnelle selon les réponses (OUI/NON).
- 💾 Sauvegarde locale (sessionStorage) et export JSON.
- 📥 Import d'une structure de logigramme JSON.
- 📄 Génération d’un fichier HTML interactif autonome.
- 🔃 Réinitialisation et édition en continu des éléments.

---

## 🧩 Structure des données

```json
{
  "title": "Titre du logigramme",
  "questions": {
    "q0": {
      "text": "Question initiale ?",
      "yes": "q1",
      "no": "result_0"
    },
    ...
  },
  "results": {
    "result_0": {
      "result": "Ceci est un résultat."
    },
    ...
  }
}
```

Chaque question pointe vers un autre nœud par ses réponses "yes" et "no", qui peuvent être une autre question ou un résultat.

---

## 🚀 Utilisation

### En local

1. Ouvrir le fichier HTML principal dans un navigateur (`logigramme.html`).
2. Définir un titre pour le logigramme.
3. Ajouter des questions, enchaîner les options OUI/NON vers d'autres questions ou des résultats.
4. Sauvegarder la structure :
    - 💾 En session (sessionStorage)
    - 📄 En JSON (téléchargement)
    - 📄 En HTML interactif

### Structure JSON

Vous pouvez charger une structure existante via :
- le bouton `📄 Charger une structure de logigramme`
- ou `sessionStorage` (si une sauvegarde est présente)

---

## 🛠 Technologies utilisées

- **HTML5**
- **CSS3 (Bootstrap 5)**
- **JavaScript Vanilla**

Aucune dépendance externe n’est nécessaire côté backend.

---

## 📁 Fichiers générés

- `structure_logigramme.json` : export JSON de la structure
- `logigramme_interactif.html` : visualisation interactive autonome

---

## 🔒 Sécurité & Limitations

- Le stockage se fait uniquement en **sessionStorage** (pas de base de données).
- Le HTML exporté ne contient aucun script malveillant, mais reste statique.

---

## ✅ Validation

Avant export HTML, le système valide automatiquement que :
- le titre est défini
- toutes les liaisons (`yes`/`no`) pointent vers des nœuds valides
- les structures de questions/résultats respectent le format attendu

---

## 📬 Aide

Si vous rencontrez des erreurs :
- vérifiez les liaisons entre les questions et résultats
- assurez-vous que tous les champs requis sont remplis
- consultez la console du navigateur pour plus d’informations

---

## 🧑‍💻 Auteur

Développé pour permettre la création de logigrammes sans code.

---

## Licence

Ce projet est en open source, libre d’utilisation et de modification.
