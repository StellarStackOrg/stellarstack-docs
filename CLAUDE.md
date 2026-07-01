# stellarstack-docs — Contexte dépôt

> Documentation publique de StellarStack. Complète le `CLAUDE.md` racine du workspace.
> **Dépôt PUBLIC et visible des prospects.** Aucune info interne, aucun secret, aucun détail d'infrastructure sensible, aucun chiffre financier non public.
> Règle de tri : *« serais-je à l'aise si un client concurrent lisait ce document ? »*

## Rôle

Source de vérité de tout ce que StellarStack publie vers ses utilisateurs et prospects :
- **Référence de l'API publique** : endpoints, authentification, exemples de requêtes, codes d'erreur.
- **Guides d'onboarding** : premiers pas, déploiement d'un premier service, connexion d'un domaine, lecture de la facture.
- **Changelog public** : évolutions notables, langage clair et non technique quand possible.

C'est aussi la vitrine de crédibilité technique numéro un pour la cible développeurs.

## Structure cible

```
api/                 # référence API (endpoints, auth, exemples)
guides/              # guides d'onboarding, une tâche concrète par guide
  ├── premiers-pas.md
  ├── deployer-un-service.md
  ├── connecter-un-domaine.md
  └── comprendre-sa-facture.md
changelog/           # changelog public, par date ou version
```

## Conventions

- **Format** : Markdown partout.
- **Un guide = une tâche utilisateur concrète** (« Comment faire X »). Éviter les pages généralistes.
- **`api/` strictement synchro avec l'API réelle** de `stellarstack-platform`. Toute divergence est un bug de doc à corriger en priorité.
- **Voix de marque** : technique mais accessible, directe, honnête, **sans superlatifs marketing**.
- **Relecture avant merge** obligatoire (dépôt public visible des prospects).
- **Jamais** : infra physique, accès internes, identifiants, partenaires, chiffres financiers non publics.
- Toute réorganisation (nouvelle section, nouveau format) → répercutée dans le README.

## Découpage / interfaces

- Se cale sur ce que `stellarstack-platform` expose réellement ; la doc suit le code, pas l'inverse.
- Toute fonctionnalité livrée en prod → une entrée `changelog/` et, si pertinent, un guide créé ou mis à jour.