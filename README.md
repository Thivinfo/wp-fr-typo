<p align="center">
  <img src="banner.svg" alt="wp-fr-typo — Skill Claude Code" width="100%"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Claude%20Code-Skill-5865F2?style=flat-square&logo=anthropic&logoColor=white" alt="Claude Code Skill"/>
  <img src="https://img.shields.io/badge/WordPress-6.0%2B-0073aa?style=flat-square&logo=wordpress&logoColor=white" alt="WordPress 6.0+"/>
  <img src="https://img.shields.io/badge/Polyglots%20FR-Conforme-00a32a?style=flat-square" alt="Polyglots FR Conforme"/>
  <img src="https://img.shields.io/badge/Glossaire-602%20termes-f0b849?style=flat-square" alt="Glossaire 602 termes"/>
  <img src="https://img.shields.io/badge/Licence-MIT-lightgrey?style=flat-square" alt="Licence MIT"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Glossaire%20mis%20à%20jour%20le-31%2F03%2F2026-ff6b35?style=flat-square" alt="Glossaire mis à jour le 31/03/2026"/>
</p>

> [!NOTE]
> **Version du glossaire intégré : 31/03/2026**
> Le glossaire officiel WordPress FR ([translate.wordpress.org](https://translate.wordpress.org/locale/fr/default/glossary/)) est mis à jour régulièrement par l'équipe Polyglots. Si tu constates un écart entre ce skill et le glossaire en ligne, la version en ligne fait foi. N'hésite pas à [ouvrir une issue](https://github.com/thierrypigot/wp-fr-typo/issues) pour signaler un terme à mettre à jour.

---

> **Vous soumettez une traduction sur GlotPress. Refusée.**
> Apostrophe droite. Espace insécable manquante. Terme hors glossaire…

Les règles de l'équipe **Polyglots WordPress Francophone** sont strictes, et pour une bonne raison : la cohérence de l'interface WordPress en français en dépend. Mais les maîtriser toutes simultanément (602 termes officiels, typographie, encodage .po, écriture épicène…) relève du parcours du combattant.

**wp-fr-typo** est un skill [Claude Code](https://claude.ai/code) qui applique automatiquement l'intégralité de ces règles à chaque traduction.

---

> [!WARNING]
> **Ce skill est un assistant, pas un remplaçant.**
> Une relecture humaine reste indispensable avant toute soumission sur translate.wordpress.org.
> L'IA peut se tromper sur le contexte d'une chaîne, sur un nom propre à conserver, ou sur une formulation épicène. Les blocs `[DOUTE]` signalent les cas incertains, ils ne les résolvent pas.
> **Toujours relire le fichier .po avant d'importer.**

---

## Ce que ça change concrètement

| Sans wp-fr-typo | Avec wp-fr-typo |
|-----------------|-----------------|
| `plugin` dans le texte traduit | `extension` — terme officiel |
| `l'extension` (apostrophe droite) | `l'extension` — U+2019 courbe |
| `Erreur: message` | `Erreur : message` — espace insécable |
| `"guillemets anglais"` | `« guillemets français »` |
| `\u2019` dans le .po | `'` — vrai caractère UTF-8 |
| Doute silencieux sur un terme | Bloc `[DOUTE]` explicite avec alternatives |

---

## Fonctionnalités

- **Glossaire officiel intégré** : 602 termes issus de [translate.wordpress.org](https://translate.wordpress.org/locale/fr/default/glossary/)
- **Typographie française complète** : apostrophes courbes, espaces insécables, guillemets « », points de suspension U+2026, majuscules accentuées
- **Fichiers .po / GlotPress** : encodage UTF-8 strict, variables gettext intactes, aucun artefact `\uXXXX`
- **Garde-fous intelligents** : le skill signale ses doutes avec des alternatives plutôt que de choisir silencieusement
- **Mémoire d'apprentissage** : tes corrections sont mémorisées projet par projet dans `memory/`
- **Checklist de validation** : passage point par point avant chaque livraison

---

## Workflow

### 1. Exporter depuis GlotPress

Sur [translate.wordpress.org](https://translate.wordpress.org), ouvre ton projet, sélectionne la langue, puis en bas de page : **Export** › format **Portable Object Message Catalog (.po/.pot)**.

<p align="center">
  <img src="docs/step1-export.svg" alt="Export .po depuis GlotPress" width="100%"/>
</p>

---

### 2. Traduire avec Claude Code + wp-fr-typo

Lance Claude Code dans le dossier contenant ton fichier `.po` et invoque le skill :

```
/wp-fr-typo mon-extension-readme-fr.po
```

Le skill analyse les chaînes existantes, corrige les erreurs typographiques et terminologiques, traduit les chaînes vides, puis livre le fichier prêt à importer.

<p align="center">
  <img src="docs/step2-claude.svg" alt="Traduction avec Claude Code + wp-fr-typo" width="100%"/>
</p>

---

### 3. Relire avant publication

> [!IMPORTANT]
> **Ne pas sauter cette étape.**
> Parcourir le fichier `.po` généré, vérifier les blocs `[DOUTE]` signalés, contrôler les chaînes à contexte spécifique (noms propres, contenu marketing, formulations épicènes).

Ouvre le fichier dans [Poedit](https://poedit.net/), VS Code ou tout éditeur texte, et valide chaque traduction produite avant de soumettre.

---

### 4. Importer dans GlotPress

De retour sur translate.wordpress.org, ouvre **Import Translations**, choisis ton `.po` relu et clique **Import**.

<p align="center">
  <img src="docs/step4-import.svg" alt="Import dans GlotPress" width="40%"/>
</p>

---

## Installation du skill

```bash
npx skills add thierrypigot/wp-fr-typo
```

## Utilisation

Mentionne l'une de ces expressions dans Claude Code pour déclencher le skill :

`traduis` · `traduire` · `traduction WordPress` · `GlotPress` · `fichier .po` · `translate WP`

Le skill fonctionne aussi pour **vérifier ou corriger** une traduction française existante.

---

## Mémoire d'apprentissage

Le skill maintient deux fichiers dans `memory/` qui persistent entre les sessions :

| Fichier | Rôle |
|---------|------|
| `memory/corrections.md` | Historique des traductions que tu as corrigées |
| `memory/project-glossary.md` | Termes spécifiques à ton projet (ex : nom de l'extension, variantes retenues) |

Ces fichiers sont lus automatiquement au démarrage. Tes préférences sont respectées projet par projet.

---

## Sources officielles

- [Règles typographiques Polyglots WP FR](https://fr.wordpress.org/team/handbook/polyglots/les-regles-typographiques-utilisees-pour-la-traduction-de-wp-en-francais/)
- [Glossaire officiel](https://translate.wordpress.org/locale/fr/default/glossary/)
- [Erreurs de traduction fréquentes](https://fr.wordpress.org/team/handbook/polyglots/le-glossaire-et-les-erreurs-de-traduction-les-plus-frequentes/)
- [Recommandations Polyglots](https://fr.wordpress.org/team/handbook/traduire-wordpress-en-francais/recommandations/)

---

## À propos

Ce skill est développé par **[Thierry Pigot](https://profiles.wordpress.org/thierrypigot/)**, fondateur de WeAre[WP], [agence WordPress](https://wearewp.pro) experte basée à Laval.

**20+ ans de WordPress.** Contributeur traductions WordPress FR, co-fondateur du Meetup WP Paris (1 700 membres), speaker à 16 WordCamps dont [WordCamp Nice 2026](https://www.wp-assistance.fr/support-wordpress/wordcamp-nice-2026-programme-conferences-et-compositions-wordpress/). Badges WordPress.org : Translation Contributor, Plugin Developer, WordCamp Organizer, WordCamp Speaker…

Ce skill est né d'un besoin concret rencontré lors de soumissions sur translate.wordpress.org et partagé avec la communauté francophone pour que personne n'ait à réapprendre les mêmes règles à la dure.

<p align="center">
  <a href="https://wearewp.pro">
    <img src="https://img.shields.io/badge/WeAre%5BWP%5D-Agence%20WordPress-0073aa?style=for-the-badge&logo=wordpress&logoColor=white" alt="WeAre[WP]"/>
  </a>
  &nbsp;
  <a href="https://profiles.wordpress.org/thierrypigot/">
    <img src="https://img.shields.io/badge/WordPress.org-thierrypigot-21759b?style=for-the-badge&logo=wordpress&logoColor=white" alt="Profil WordPress.org"/>
  </a>
  &nbsp;
  <a href="https://github.com/thierrypigot">
    <img src="https://img.shields.io/badge/GitHub-thierrypigot-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"/>
  </a>
</p>

---

<p align="center">
  Conçu pour la communauté <strong>WordPress Francophone</strong> · Skill <a href="https://claude.ai/code">Claude Code</a> · Licence MIT
</p>
