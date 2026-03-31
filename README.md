# wp-fr-typo — Skill Claude Code

**Traduction WordPress de l'anglais vers le français** — conforme à 100 % aux règles officielles de l'équipe Polyglots WordPress Francophone.

## Ce que fait ce skill

- Applique le **glossaire officiel WordPress FR** (602 termes — source : translate.wordpress.org)
- Respecte toutes les **règles typographiques Polyglots** (apostrophes courbes, espaces insécables, guillemets français, majuscules accentuées, écriture épicène…)
- Gère les **fichiers .po / GlotPress** : encodage UTF-8 strict, variables gettext intactes
- Signale les **doutes** explicitement plutôt que de silencieusement choisir
- Apprend de tes **corrections** grâce à un système de mémoire par projet

## Prérequis

[Claude Code](https://claude.ai/claude-code) installé.

## Installation

```bash
npx skills add thierrypigot/wp-fr-typo
```

## Utilisation

Déclenche le skill en mentionnant : `traduis`, `traduire`, `traduction WordPress`, `GlotPress`, `po/pot/mo`, `translate WP`, `chaine a traduire`, ou `wordpress.org/translate`.

Fonctionne aussi pour **vérifier ou corriger** une traduction française existante.

## Mémoire d'apprentissage

Le skill maintient deux fichiers dans `memory/` :

| Fichier | Rôle |
|---------|------|
| `memory/corrections.md` | Log des traductions corrigées par l'utilisateur |
| `memory/project-glossary.md` | Termes spécifiques au projet courant |

Ces fichiers sont lus au démarrage de chaque session et mis à jour automatiquement quand tu corriges une traduction.

## Sources officielles

- [Règles typographiques Polyglots WP FR](https://fr.wordpress.org/team/handbook/polyglots/les-regles-typographiques-utilisees-pour-la-traduction-de-wp-en-francais/)
- [Glossaire officiel](https://translate.wordpress.org/locale/fr/default/glossary/)
- [Erreurs fréquentes](https://fr.wordpress.org/team/handbook/polyglots/le-glossaire-et-les-erreurs-de-traduction-les-plus-frequentes/)

## Licence

MIT
