---
name: wp-fr-typo
description: >
  Traduit des textes anglais en français en respectant a 100% les regles typographiques
  officielles ET le glossaire officiel de l'equipe de traduction WordPress Francophone
  (translate.wordpress.org). Declencher ce skill des que l'utilisateur demande de
  traduire un texte, une chaine, une interface, une extension ou un theme WordPress
  de l'anglais vers le francais, ou qu'il mentionne : "traduis", "traduire",
  "traduction WordPress", "translate WP", "chaine a traduire", "po/pot/mo",
  "GlotPress", ou "wordpress.org/translate".
  Ce skill est aussi utile pour verifier ou corriger une traduction francaise existante.
---

> **Version du glossaire** : 30/03/2026 — Source : export officiel `translate.wordpress.org/locale/fr/default/glossary/` (602 termes).

# Skill : Traduction WordPress FR -- Typographie + Glossaire officiel

Traduction conforme a 100% aux regles Polyglots WordPress FR :
- Regles typo : https://fr.wordpress.org/team/handbook/polyglots/les-regles-typographiques-utilisees-pour-la-traduction-de-wp-en-francais/
- Glossaire : https://translate.wordpress.org/locale/fr/default/glossary/

---

## 1. PROCESSUS DE TRADUCTION

Ordre imperatif :

1. Identifier et remplacer tous les termes du glossaire (section 3) dans le texte source.
2. Traduire le reste en francais courant, voix active, phrases courtes.
3. Appliquer toutes les regles typographiques (section 2).
4. Passer la checklist (section 4) point par point.
5. Livrer le texte final pret a copier-coller dans GlotPress.
6. Signaler tout choix non evident (terme conserve, epicene retenu, etc.).

---

## 2. REGLES TYPOGRAPHIQUES OBLIGATOIRES

### 2.1 Espaces et ponctuation

#### Pas d'espace avant -- une espace apres
| Signe | Remarque |
|-------|----------|
| Point . | |
| Virgule , | |
| Points de suspension ... | Caractere U+2026 unique -- jamais trois points |
| Parenthese fermante ) | |
| Crochet fermant ] | |

#### Une espace avant -- pas d'espace apres
| Signe |
|-------|
| Parenthese ouvrante ( |
| Crochet ouvrant [ |

#### Espace insecable (U+00A0) avant -- espace ordinaire apres
OBLIGATOIRE. Voir section 6 pour les contraintes d'encodage specifiques aux fichiers .po.

| Signe |
|-------|
| Deux-points : |
| Point-virgule ; |
| Point d'interrogation ? |
| Point d'exclamation ! |
| Guillemet francais fermant >> (U+00BB) |
| Pourcentage % |
| Unites de mesure (km, Mo, px, etc.) |
| Symboles monetaires (euro, $, etc.) |
| Signes mathematiques (=, <, >, ~, +) |

#### Espace ordinaire avant -- espace insecable (U+00A0) apres
| Signe |
|-------|
| Guillemet francais ouvrant << (U+00AB) |

Resultat attendu : << espace-insecable texte espace-insecable >>

#### Pas d'espace avant ni apres
| Signe | Remarque |
|-------|----------|
| Barre oblique / | Exception : espace de chaque cote si l'un des membres contient un tiret ou expression longue. |

---

### 2.2 Apostrophe -- courbe obligatoire

Utiliser ' (U+2019) -- JAMAIS ' (U+0027, ASCII droit).

Correct : l'extension, c'est, j'ai
Incorrect : l'extension (apostrophe droite)

---

### 2.3 Points de suspension -- caractere unique

Utiliser le caractere unique U+2026 -- jamais trois points separes.

Correct : Chargement...
Incorrect : Chargement... (trois points ASCII)

---

### 2.4 Guillemets -- francais obligatoires

<< et >> avec espaces insecables interieures -- jamais guillemets anglais droits.

Correct : Un traducteur intervient : << Ou se trouve le glossaire ? >>.
Incorrect : Un traducteur intervient: "Ou se trouve le glossaire?".

---

### 2.5 Majuscules

Regle de base : beaucoup moins de majuscules qu'en anglais.
Majuscule UNIQUEMENT pour : debut de phrase, noms propres, sigles.

Exemples de declassement (anglais -> francais) :
- Settings (milieu de phrase) -> reglages
- Add New Post -> Ajouter un article
- Media Library -> mediatheque
- Monday, March 30 -> lundi 30 mars

Majuscules accentuees obligatoires : E accent aigu, A accent grave, E accent circonflexe, etc.
Correct : Etant donne, Editeur, A noter
Incorrect : Etant donne (sans accent), Editeur (sans accent)

---

### 2.6 Nombres

| Regle | Correct | Incorrect |
|-------|---------|-----------|
| Separateur decimal | virgule , | point . |
| Separateur de milliers | espace insecable | point ou virgule |
| Ordinaux | 1er, 1re, 2e, 3e | 1eme, 2eme, 1st, 2nd |
| Siecles | XXIe siecle | 21eme siecle |

Exemples : 1 234,56 euros -- 100 % -- 2e version

---

### 2.7 Abreviations

- Terminee par la DERNIERE LETTRE du mot -> pas de point : Mme, Dr, Pr, Me, bd
- NON terminee par la derniere lettre -> point : M., art., cat.
- Sigles : pas de point entre les lettres : ONU, CSS, API
- Mr est un ANGLICISME -> REFUSE, ecrire M.

---

### 2.8 Accents sur les majuscules

Toujours accentuer les majuscules (sauf sigles).
Correct : Etiquette avec accent, Editeur avec accent
Incorrect : Etiquette sans accent, Editeur sans accent

---

### 2.9 Ponctuation -- cas particuliers

- Fin de phrase : toujours ., ?, ! ou points de suspension
- Fin de titre / chapitre : PAS de ponctuation.
- Liste en une seule phrase : ; apres chaque item, . apres le dernier.
- Apres etc. : pas de points de suspension.
- Entre les lettres d'un sigle : pas de point.

---

### 2.10 Redaction epicene (ecriture inclusive)

Ordre de preference :

1. Formulation neutre -> les personnes chargees de l'administration
2. Formulation combinee -> les administrateurs et administratrices
3. Point median (en dernier recours) -> les administrateur.ice.s
   - Point median : U+00B7 (pas un point ordinaire, pas un tiret)

---

## 3. GLOSSAIRE OFFICIEL WORDPRESS FR

Source : https://translate.wordpress.org/locale/fr/default/glossary/
ATTENTION : Ces termes sont OBLIGATOIRES. Toute deviation est un motif de rejet.

### 3.1 Regles generales

- Vouvoiement : toujours "vous", jamais "tu".
- Infinitif pour les boutons d'action : Save -> Enregistrer.
- Imperatif pour conseils/aides : Click here -> Cliquez ici.
- WordPress : toujours W et P majuscules, sans exception.
- Ne pas traduire : noms de themes, noms d'extensions, URL, chemins de fichiers.
- Ne pas modifier : variables gettext (%s, %1$s, etc.) et balises HTML dans les chaines.
- URL est FEMININ : une URL (pas un URL).

---

### 3.2 Termes critiques — erreurs de rejet les plus fréquentes

| Anglais | ✅ Officiel | ❌ À rejeter / Notes |
|---------|------------|----------------------|
| `plugin` / `plug-in` | **extension** | plugin, plug-in, greffon |
| `post` (générique) | **publication** | post, billet ; « article » si contexte blog précis |
| `save` | **enregistrer** | sauvegarder (réservé backups) |
| `settings` | **réglages** | paramètres, configurations |
| `edit` (action) | **modifier** | éditer |
| `upload` | **téléverser** | uploader |
| `download` | **télécharger** | downloader |
| `dashboard` | **Tableau de bord** | dashboard (majuscule à Tableau) |
| `media library` | **médiathèque** | bibliothèque de médias |
| `featured image` | **image mise en avant** | image à la une |
| `template` | **gabarit** (FSE/site editor) — **modèle de page** (classique) | template, gabarit seul hors FSE |
| `template part` | **partie de gabarit** | élément de modèle |
| `pattern` / `block pattern` | **composition** | motif toléré si non-UI |
| `block theme` | **thème basé sur des blocs** | thème de blocs si manque de place |
| `full site editing` / `FSE` | **éditeur de site** / **édition de site** | |
| `global styles` | **styles globaux** | |
| `query loop` | **boucle de requête** | |
| `customize` | **personnaliser** | customiser |
| `Customizer` | **Outil de personnalisation** | |
| `sidebar` | **barre latérale** | colonne latérale |
| `tag` (taxonomie) | **étiquette** | tag |
| `tag` (HTML) | **balise** | |
| `slug` | **slug** | identifiant normalisé (nicename) |
| `permalink` | **permalien** | lien permanent |
| `trash` (nom) | **corbeille** | |
| `trash` (verbe) | **mettre à la corbeille** | |
| `remove` | **retirer** | supprimer (sauf users/extensions/thèmes) |
| `update` (nom) | **mise à jour** | |
| `update` (verbe) | **mettre à jour** | updater |
| `username` | **identifiant** | nom d'utilisateur |
| `widget` | **widget** | non traduit |
| `back-end` / `backend` | **interface d'administration** | |
| `front-end` / `frontend` | **interface publique** | |
| `hook` (action) | **crochet d'action** | |
| `hook` (filter) | **crochet de filtre** | |
| `add-on` / `addon` | **module** | module complémentaire si possible |
| `capabilities` | **permissions** | droits selon contexte |
| `shortcode` | **code court** | |
| `tooltip` | **infobulle** | |
| `breadcrumb` | **fil d'ariane** | |
| `changelog` | **journal des modifications** | |
| `thumbnail` | **miniature** | |
| `header` | **en-tête** | masculin |
| `footer` | **pied de page** | |
| `AI` | **IA** | Intelligence artificielle |
| `mu-plugin` | **extension indispensable** | must-use |
| `deprecated` | **obsolète** | |
| `popup` | **fenêtre surgissante** | fenêtre contextuelle selon type |
| `Mr` | **M.** | Mr = anglicisme refusé |
| `Are you sure` | **Confirmez-vous** | Êtes-vous sûr·e ? |
| `successfully` | **bien** | P. ex. : La mise à jour a bien été effectuée |

---

### 3.3 Interface -- navigation et structure

| Anglais | Francais officiel |
|---------|-------------------|
| Dashboard | tableau de bord |
| Admin bar / Toolbar | barre d'outils |
| Screen | ecran |
| Screen Options | options de l'ecran |
| Panel | panneau |
| Settings | reglages |
| General Settings | reglages generaux |
| Sidebar | barre laterale |
| Widget area | zone de widgets |
| Block | bloc |
| Block editor | editeur de blocs |
| Classic editor | editeur classique |
| Block inserter | outil d'insertion de blocs |
| Inspector panel / Settings sidebar | panneau de reglages (colonne laterale des reglages) |
| Reusable block | bloc reutilisable |
| Preview | previsualisation |
| Fullscreen mode | mode plein ecran |
| Spotlight mode | mode focus |
| Top toolbar | barre d'outils superieure |
| Document overview | vue d'ensemble du document |
| Publish | publier |
| Update (bouton) | Mettre a jour |
| Save draft | Enregistrer le brouillon |
| Discard | Ignorer les modifications |
| Duplicate | Dupliquer |

---

### 3.4 Contenus

| Anglais | Francais officiel |
|---------|-------------------|
| Post (type blog) | article |
| Post (generique) | publication |
| Page | page |
| Custom post type | type de publication personnalise |
| Attachment | fichier joint |
| Media | medias |
| Featured image | image mise en avant |
| Thumbnail | miniature |
| Gallery | galerie |
| Category | categorie |
| Tag | etiquette |
| Taxonomy | taxonomie |
| Term | terme |
| Comment | commentaire |
| Excerpt | extrait |
| Revision | revision |
| Draft | brouillon |
| Pending review | en attente de relecture |
| Sticky post | article epingle |
| Slug | identifiant |
| Permalink | permalien |
| Archive | archives |
| Feed | flux |
| Homepage / Front page | page d'accueil |
| Blog page | page des articles |

---

### 3.5 Editeur de blocs / FSE / Gutenberg

| Anglais | Francais officiel |
|---------|-------------------|
| Block | bloc |
| Pattern | composition |
| Template | gabarit |
| Template part | partie de gabarit |
| Global styles | styles globaux |
| Style variation | variation de style |
| Site editor | editeur de site |
| Full site editing | edition de site |
| Navigation block | bloc Navigation |
| Query loop | Boucle de requete |
| Block locking | verrouillage de bloc |
| Cover block | bloc Couverture |
| Group block | bloc Groupe |
| Columns block | bloc Colonnes |
| Spacer | Espacement |
| Separator | Separateur |
| Embed | Incorporation |
| Shortcode | shortcode (invariable) |
| Custom HTML | HTML personnalise |
| theme.json | theme.json (ne pas traduire) |

---

### 3.6 Utilisateurs et roles

| Anglais | Francais officiel |
|---------|-------------------|
| User | utilisateur.rice |
| Profile | profil |
| Role | role |
| Administrator | administrateur.rice |
| Editor | editeur.rice |
| Author | auteur.rice |
| Contributor | contributeur.rice |
| Subscriber | abonne.e |
| Super Admin | super administrateur.rice |
| Username | identifiant |
| Password | mot de passe |
| Log in | se connecter |
| Log out | se deconnecter |
| Register | s'inscrire |
| Account | compte |
| Avatar | avatar |

---

### 3.7 Extensions et themes

| Anglais | Francais officiel |
|---------|-------------------|
| Plugin | extension |
| Theme | theme |
| Child theme | theme enfant |
| Block theme | theme de blocs |
| Classic theme | theme classique |
| Activate | activer |
| Deactivate | desactiver |
| Install | installer |
| Uninstall | desinstaller |
| Update (nom) | mise a jour |
| Update (verbe) | mettre a jour |
| Upgrade | mettre a niveau |
| Delete | supprimer |
| Customize | personnaliser |
| Customizer | Outil de personnalisation |
| Theme options | options du theme |
| Header | en-tete |
| Footer | pied de page |
| Logo | logo |
| Background | arriere-plan |

---

### 3.8 Reglages systeme

| Anglais | Francais officiel |
|---------|-------------------|
| General | general |
| Writing | ecriture |
| Reading | lecture |
| Discussion | commentaires |
| Permalinks | permaliens |
| Privacy | confidentialite |
| Site title | titre du site |
| Tagline | slogan |
| Timezone | fuseau horaire |
| Date format | format de date |
| Time format | format d'heure |
| Language | langue |
| Search engine visibility | visibilite pour les moteurs de recherche |
| Homepage display | page d'accueil |

---

### 3.9 Termes a NE PAS traduire

Conserver tels quels dans tous les contextes :
widget -- nonce -- transient -- cron -- Gutenberg -- WordPress --
noms d'extensions -- noms de themes -- URL -- chemins PHP --
fonctions/hooks (wp_head, the_content, etc.)

Variables gettext dans une chaine (%s, %1$s, %2$d) : NE JAMAIS modifier ni deplacer.
Balises HTML dans une chaine (<strong>, <a href="...">) : NE JAMAIS modifier.

---

## 4. CHECKLIST DE VALIDATION (avant livraison)

### Typographie
- [ ] Apostrophes courbes (U+2019) -- pas de droites (U+0027)
- [ ] Points de suspension U+2026 -- pas trois points ASCII
- [ ] Guillemets francais << >> -- pas guillemets anglais
- [ ] Espace insecable avant : ; ? ! >> % et unites
- [ ] Espace insecable apres <<
- [ ] Pas d'espace avant . , ... ) ]
- [ ] Pas de majuscules inutiles (calque de l'anglais)
- [ ] Majuscules accentuees (E accent aigu, A accent grave, etc.)
- [ ] Separateur decimal = virgule
- [ ] Separateur de milliers = espace insecable
- [ ] Redaction epicene si le texte designe des personnes
- [ ] Abreviations correctes (point ou non selon la regle)
- [ ] Pas de point dans les sigles

### Glossaire
- [ ] Pas de "plugin" -> "extension"
- [ ] "post" generique -> "publication"
- [ ] "settings" -> "reglages"
- [ ] "save" -> "enregistrer"
- [ ] "upload" -> "televerser"
- [ ] "featured image" -> "image mise en avant"
- [ ] "pattern" -> "composition"
- [ ] "template" -> "gabarit"
- [ ] "tag" -> "etiquette"
- [ ] "dashboard" -> "tableau de bord"
- [ ] "media library" -> "mediatheque"
- [ ] "Mr" -> "M."
- [ ] "WordPress" avec W et P majuscules
- [ ] Variables gettext (%s, etc.) non modifiees
- [ ] Balises HTML non modifiees
- [ ] Vouvoiement (vous) respecte
- [ ] Noms d'extensions/themes non traduits

---

## 5. EXEMPLES COMPLETS

| Anglais | Francais conforme |
|---------|-------------------|
| Save Changes | Enregistrer les modifications |
| Add New Plugin | Ajouter une extension |
| Settings | Reglages |
| Media Library | Mediatheque |
| Are you sure? | Confirmez-vous ? |
| Error: invalid value. | Erreur : valeur non valide. |
| Loading... | Chargement... (U+2026) |
| 1 item found | 1 element trouve |
| 100% | 100 % |
| 2nd version | 2e version |
| Mr. Smith | M. Smith |
| "quoted text" | << texte entre guillemets >> |
| it's done | c'est termine |
| Upload your file | Televersez votre fichier |
| Edit post | Modifier la publication |
| Add new tag | Ajouter une etiquette |
| Block pattern | Composition |
| Site Editor | Editeur de site |
| The plugin was deleted. | L'extension a ete supprimee. |
| Featured image | Image mise en avant |
| Dashboard | Tableau de bord |
| Publish | Publier |
| Update (bouton) | Mettre a jour |
| Trash | Corbeille |
| Child theme | theme enfant |
| Full site editing | edition de site |

---

## 6. NOTES POUR LES FICHIERS .PO / GETTEXT

Les regles typographiques de la section 2 (quels caracteres utiliser, ou placer les espaces)
s'appliquent integralement aux fichiers .po. Cette section couvre uniquement les contraintes
**specifiques au format .po** qui s'ajoutent aux regles generales.

### 6.1 REGLE CRITIQUE -- encodage des caracteres dans les fichiers .po

Les fichiers .po sont du **texte brut UTF-8**. GlotPress et gettext ne font aucune
interpretation des sequences d'echappement Unicode ni des entites HTML.

**INTERDICTION ABSOLUE** d'ecrire des sequences d'echappement dans les chaines msgstr :
- Pas de \uXXXX (ex: \u2019, \u00a0, \u2026, \u00ab, \u00bb, \u2014, \u00b7, \u0153, etc.)
- Pas de &#xXXXX; ni &#NNN;
- Pas de &nbsp; ni &laquo; ni aucune entite HTML (sauf celles deja presentes dans le msgid source)

**Toujours inserer le caractere reel UTF-8 directement dans la chaine.**

Cela concerne TOUS les caracteres typographiques decrits en section 2 :
apostrophe courbe, espace insecable, points de suspension, guillemets francais,
tirets, point median, ligatures oe/OE, majuscules accentuees, symbole multiplication, etc.

**Pourquoi** : les sequences non interpretees s'affichent telles quelles a l'ecran.
Exemple : "Lu2019extension" au lieu de "L'extension".

**Methode** : lors de l'ecriture du fichier avec l'outil Write, inserer directement
le caractere Unicode dans la chaine. Si l'outil serialise des \uXXXX malgre tout,
appliquer un post-traitement Python pour remplacer les sequences par les vrais caracteres.

### 6.2 Regles specifiques au format .po

- Conserver la casse des variables gettext : %s, %1$s, %2$d.
- Ne jamais modifier, supprimer ni reordonner les variables gettext.
- Ne jamais modifier les balises HTML presentes dans une chaine.
- Les seuls echappements autorises dans un .po sont ceux du format gettext : \n (saut de ligne), \t (tabulation), \" (guillemet double litteral).

---

## 7. SOURCES DE REFERENCE

- Regles typographiques : https://fr.wordpress.org/team/handbook/polyglots/les-regles-typographiques-utilisees-pour-la-traduction-de-wp-en-francais/
- Glossaire officiel : https://translate.wordpress.org/locale/fr/default/glossary/
- Erreurs frequentes : https://fr.wordpress.org/team/handbook/polyglots/le-glossaire-et-les-erreurs-de-traduction-les-plus-frequentes/
- Recommandations : https://fr.wordpress.org/team/handbook/traduire-wordpress-en-francais/recommandations/

---

## 8. GARDE-FOUS EN CAS DE DOUTE

Ne jamais silencieusement choisir une traduction incertaine. Appliquer cette procedure :

### 8.1 Cas declencheurs d'un signal de doute

Signaler explicitement (notation `[DOUTE]`) quand :
- Le terme n'est pas dans le glossaire officiel (section 3) ni dans la memoire (section 9)
- Le contexte change la traduction : `post` blog vs `post` generique, `template` FSE vs classique
- Le terme est peut-etre un nom propre (nom d'extension, nom de theme, nom de marque)
- La chaine contient du jargon technique ambigu (API, CLI, UI/UX, slug de taxonomie)
- La ponctuation source est inhabituelle et pourrait etre intentionnelle (ex : ellipse vs ...)
- Le genre grammatical n'est pas evident (acronyme, neologisme, emprunt)
- Le vouvoiement / l'epicene creerait une formulation tres lourde

### 8.2 Format du signal

Apres la traduction proposee, ajouter un bloc de ce type :

```
[DOUTE] "terme source"
- Traduction retenue : "ma proposition"
- Alternatives : "option B" (raison) / "option C" (raison)
- Question : precisez le contexte si [X] ou [Y]
```

Ne jamais bloquer la livraison pour un doute : proposer la traduction la plus probable ET signaler.

### 8.3 Termes a ne JAMAIS traduire sans confirmation

Si le terme ressemble a un nom propre (extension, theme, service tiers, marque) :
- Le conserver tel quel dans la traduction
- Ajouter `[DOUTE - nom propre ?]` en fin de chaine

---

## 9. MEMOIRE D'APPRENTISSAGE

Le skill maintient une memoire des corrections et termes valides par projet.
Fichiers dans `<repertoire-du-skill>/memory/` :

- `corrections.md` — corrections apportees par l'utilisateur sur des traductions proposees
- `project-glossary.md` — termes specifiques au projet courant (non couverts par le glossaire officiel)

### 9.1 Lecture au demarrage

AVANT de traduire, lire ces deux fichiers s'ils existent.
Les termes de `project-glossary.md` ont PRIORITE sur les valeurs par defaut du skill
(sauf sur le glossaire officiel §3 qui reste non negociable).

### 9.2 Ecriture apres correction

Quand l'utilisateur corrige une traduction proposee :
1. Ajouter une ligne dans `corrections.md` avec le format :
   `| EN | FR propose | FR corrige | Raison | Date |`
2. Si la correction etablit une regle generale pour ce projet, l'ajouter dans `project-glossary.md`.

### 9.3 Structure des fichiers memoire

**corrections.md** :
```
# Corrections de traduction

| Anglais | Propose | Corrige | Raison | Date |
|---------|---------|---------|--------|------|
```

**project-glossary.md** :
```
# Glossaire projet

Termes specifiques a ce projet, prioritaires sur les valeurs par defaut.

| Anglais | Francais retenu | Contexte / Note |
|---------|-----------------|-----------------|
```
