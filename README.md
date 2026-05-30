# 📝 TodoList — Composant React
> Composant React + TypeScript développé en autonomie : ajouter, cocher, modifier, supprimer et trier des tâches. Stylé en CSS natif imbriqué, sans framework UI.

![React](https://img.shields.io/badge/React-19-61DAFB?logo=react&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-5-3178C6?logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-7-646CFF?logo=vite&logoColor=white)

---

## Aperçu
Une todo list claire et fonctionnelle, pensée comme un composant autonome réutilisable. Initialement développée dans le cadre d'un projet collectif d'application d'organisateur d'évent pour préparer un titre RNCP, puis repris en projet personnel.

## Fonctionnalités
- ➕ Ajout d'une tâche au clic ou via la touche `Enter`
- ✅ Validation par checkbox personnalisée (style barré + italique)
- ✏️ Édition inline avec `textarea` multi-ligne
- 🗑️ Suppression individuelle
- 📊 Tri automatique : tâches non cochées en haut de la liste
- ♿ Conçu pour l'accessibilité (unités `rem`, focus géré)

## Stack technique
| Domaine | Choix | Pourquoi |
| Framework | React 19 | Composant et état réactif |
| Langage | TypeScript | Typage statique, fiabilité du code |
| Icônes | lucide-react | Légère, personnalisable |
| Style | CSS natif imbriqué | Pas de dépendance, lisibilité |
| Build | Vite | Rapidité et DX |

## Concepts mis en pratique
- **Gestion d'état** avec `useState` (4 états indépendants)
- **Inputs contrôlés** (synchronisation DOM / state)
- **Rendu conditionnel** via opérateur ternaire
- **Immuabilité** : `.map()`, `.filter()`, spread operator
- **Tri dynamique** avec `.sort()` sur un booléen converti en nombre
- **CSS scopé** sous un sélecteur racine pour éviter les conflits globaux

## Structure des données
```ts
type Task = {
  todo_id: number;
  todo_name: string;
  todo_is_done: boolean;
};
```

Simple et efficace. Nommage aligné sur une potentielle base de données pour anticiper l'intégration API.

## Pistes d'évolution
- Branchement à une API REST (Node + SQL)
- Date d'échéance par tâche (`todo_deadline`)
- Annulation de l'édition avec `Escape`
- Confirmation avant suppression
- Extraction du `<li>` en sous-composant `TaskItem` mémoïsé

## Démo
https://github.com/user-attachments/assets/e84f2205-a023-41aa-baf2-7f8d0f395a4d

