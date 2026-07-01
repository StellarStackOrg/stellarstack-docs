# stellarstack-docs

Documentation publique de StellarStack : référence de l'API, guides d'onboarding, changelog public.

> **Dépôt public.** Contrairement aux autres dépôts de l'organisation, celui-ci est ouvert : il ne doit contenir aucune information interne, aucun secret, aucun détail d'infrastructure sensible. En cas de doute sur ce qui peut y figurer, se référer au principe : *"est-ce que je serais à l'aise si un client concurrent lisait ce document ?"*
>
> **Statut : temporaire sur GitHub**, le temps que `git.stellarstack.fr` (GitLab CE) soit opérationnel. Voir [Migration](#migration-vers-gitlab-ce).

## Objet

Ce dépôt est la source de vérité de tout ce que StellarStack publie à destination de ses utilisateurs et prospects :

- **Documentation de l'API publique** : endpoints, authentification, exemples de requêtes, codes d'erreur.
- **Guides d'onboarding** : premiers pas, déploiement d'un premier service, connexion d'un domaine, lecture de la facture.
- **Changelog public** : historique des évolutions notables de la plateforme, dans un langage clair, non technique quand possible.

C'est aussi, indirectement, un outil de crédibilité technique (cf. stratégie de communication : la présence GitHub/documentation est la vitrine de confiance numéro un pour la cible développeurs).

## Structure du dépôt

```
stellarstack-docs/
├── api/                 # Référence API (endpoints, auth, exemples)
├── guides/              # Guides d'onboarding et tutoriels
│   ├── premiers-pas.md
│   ├── deployer-un-service.md
│   ├── connecter-un-domaine.md
│   └── comprendre-sa-facture.md
├── changelog/            # Changelog public, par date ou version
└── README.md
```

## Comment l'utiliser / contribuer

- Toute nouvelle fonctionnalité livrée en production doit s'accompagner d'une entrée dans `changelog/` et, si pertinent, d'une mise à jour d'un guide existant ou d'un nouveau guide.
- La documentation de l'API (`api/`) doit rester strictement synchronisée avec l'API réellement exposée (`stellarstack-platform`) — toute divergence est un bug de documentation à corriger en priorité.
- Rédaction : ton technique mais accessible, cohérent avec la voix de marque StellarStack (direct, honnête, sans superlatifs marketing).

## Conventions

- **Format** : Markdown pour tous les documents.
- **Un guide = une tâche utilisateur concrète.** Éviter les pages généralistes ; préférer des guides actionnables ("Comment faire X").
- **Relecture avant publication** : toute PR sur ce dépôt doit être relue avant merge, ce dépôt étant public et visible par les prospects.
- **Pas de données sensibles** : aucune information sur l'infrastructure physique, les accès internes, les identifiants, les partenaires ou les chiffres financiers non publics.

## Migration vers GitLab CE

Même trajectoire que les autres dépôts : ce dépôt sera à terme hébergé sur `git.stellarstack.fr`. Étant public, un miroir en lecture seule pourra être maintenu plus longtemps si la documentation doit rester consultable largement (à trancher en fonction de la stratégie de distribution du contenu au moment de la bascule).

## Mise à jour de ce document

Document vivant. Toute réorganisation de la documentation (nouvelle section, nouveau format) doit être reflétée ici.

---
*StellarStack — Cloud PaaS/SaaS Simple, Transparent, Souverain*
