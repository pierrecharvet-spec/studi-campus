# CONTEXT — Studi Campus

> Doctrine du projet. À lire avant toute itération.
> Ce document capte le **quoi** et le **pourquoi actuel** — pas l'historique des versions.
> Il est vivant : on l'enrichit au fil des décisions prises.

---

## 1. Positionnement produit

**Studi Campus** est la formule **Premium par défaut** de Studi pour l'enseignement supérieur en ligne (Bac+2 à Bac+5). Ce n'est **pas** une sous-marque ou une école satellite. C'est la manière dont Studi propose son supérieur, point.

Trois facultés, construites chacune avec des écoles partenaires de référence :

- **Tech School** — en partenariat avec Le Wagon, HETIC, Digital Campus, LISAA
- **Business School** — en partenariat avec ESG, PSB
- **People & Finance School** — en partenariat avec ESG RH, ESG Finance, ESG Immobilier, ESG Tourisme, Comptalia

Diplômes **reconnus par l'État (RNCP)** : Bachelor, Graduate, Mastère, MBA.

**Ligne de base :** *Une grande école. Trois facultés. Chez vous.*

**Métaphore de marque :** *Le plus grand campus de France. Sans campus.*

---

## 2. Proposition de valeur non-négociable

Ces éléments ne se re-challengent plus. Ils sont actés.

### Pricing

- Formule Premium à **11 980 €** (Graduate 5 590 € + Bachelor 6 390 €)
- Comparaison présentiel publique : **~55 000 €** (scolarité 24 000 € + logement 22 500 € + vie courante 9 000 €)
- Économie affichée : **~43 000 €** — crédible, non-attaquable

### Garanties (wording NDS officiel)

- **Diplômé ou Remboursé**
- **Embauché ou Remboursé**
- Double garantie contractuelle, pas une promesse marketing

### 10 ans d'accès

- **120 mois** d'accès à la plateforme, contenus, formateurs, mises à jour
- Phrase signature, intouchable :
  > *« Vous n'êtes jamais ancien élève. Vous êtes toujours étudiant·e. Pour 10 ans. »*

### Rentrées

- **12 rentrées par an** — une par mois
- Baseline : *« Inscrivez-vous maintenant, démarrez quand vous voulez — tout de suite, cet été, ou à la rentrée. »*

### Chiffres clés affichés

- **59 000** apprenants en formation
- **25 ans** d'existence (depuis 1999)
- **400+** métiers couverts
- **700+** formateurs
- **15** filières métiers
- **Siège Montpellier** (pas Paris — c'est volontaire)

---

## 3. Voix de marque

### Piliers

**Accessible · Concret · Légitime**

### Principes d'écriture

**Concis · Concret · Concentré · Ancré dans le quotidien**

### Règles dures

- **Pas** de clichés EdTech (transformation, révolution, disrupter, accélérer, booster, unlock)
- **Pas** d'énumération de features — on parle usages, bénéfices, vie réelle
- **Pas** de "100 %" — son creux, banni
- **Pas** d'urgency manipulative (compte à rebours bidon, "plus que X places")
- **Pas** de "statut étudiant" — Studi Campus **n'attribue pas** ce statut. Les programmes sont RNCP, c'est la ligne légale.
- **Pas** de ton pushy — direct, rassurant, commercialement assertif **sans manipulation**

### Distinctions lexicales

- **Formateur** et **professionnel du secteur** sont deux rôles distincts, pas des synonymes. On les emploie de façon contextuelle, jamais interchangeable.
- **Faculté** = les 3 blocs pédagogiques. **École partenaire** = Le Wagon, HETIC, ESG, etc. Ne pas confondre.

### Ton recommandé

Direct. Court. Éditorial. Un peu sec parfois, jamais sirupeux. Les italiques Lora pour les phrases-signature. Des taglines courtes, pas des slogans.

### Pilier parents

Levier de confiance central. On parle **aux parents** autant qu'aux apprenants. Section dédiée, tableau comparatif, garanties mises en avant, kit PDF à télécharger.

---

## 4. Design system

### Palette (verrouillée — ne pas remplacer par la charte officielle v1.0)

| Rôle | Hex | Usage |
|---|---|---|
| Paper | `#F3ECDE` | Fond principal |
| Paper warm | `#EDE4D0` | Fond sections alternées |
| Navy | `#12161D` | Texte principal, bandeaux forts |
| Slate | `#2F3A4B` | Texte secondaire |
| Terracotta | `#C9542E` | Accent éditorial, CTA secondaires |
| Jaune Studi | `#FFCA4A` | CTA primaires, highlights |
| Bleu Studi | `#255587` | Accents marque, liens |

**Décision Pierre actée :** on garde cette palette, **pas** la palette officielle de la charte Studi v1.0 (navy/gris/jaune). La palette Claude a été validée explicitement comme palette de référence Studi Campus.

### Typographies (Google Fonts, déjà câblées)

- **Lora** — display, titres, italiques signature, logo *studi.*
- **Roboto** — body, UI, labels, meta

### Photographie

- Style **documentaire 35mm Kodak Portra 400**
- Authentique, pas stock, pas de sourires forcés
- Pas de HDR, pas de plastique, pas de pose
- Diversité réelle des profils et géographies (métropole + DOM-TOM + France rurale)
- Les prompts Ideogram sont dans `studi-campus-ideogram-master.csv`

### Siège Montpellier — règle photo

Si la photo du siège est utilisée :
- **Caption obligatoire** : *"Siège Studi · Montpellier"*
- **Jamais en hero** (risque de confusion présentiel)

---

## 5. Architecture technique

- **Single-file HTML** — `index.html` à la racine
- **SVG inline** pour la carte France (144 KB, 3 641 points, Corse + 5 DOM-TOMs en cartouches)
- **Google Fonts** pour Lora + Roboto
- **Zéro dépendance externe** — pas de framework, pas de build, pas de npm
- **Assets locaux** dans `/assets/` (photos JPG)
- **Responsive mobile-first**
- **Carte statique uniquement** dans la landing — le GIF animé existe (`carte/carte_animation_optionnelle.gif`) mais n'est **pas** utilisé ici

---

## 6. Structure V5-b — 18 sections

1. Nav sticky (logo *studi.* + 5 liens + CTA primary)
2. Hero — *Une grande école. Trois facultés. Chez vous.*
3. Portes d'entrée (Métier / Compétences / Faculté / Orientation)
4. 6 Profils transverses (Pressé·e, Fan digital, Budget malin, Loin des villes, Double projet, Mobilité)
5. **Carte France densifiée** + 4 stats (59 000 · 25 ans · 400+ · 700+)
6. Les 3 facultés avec partenaires académiques
7. Compétences 360 (6 accélérateurs : IA, Cours Florent, logiciels, langues, entrepreneuriat, coaching)
8. L'école qui reste (IA + maj hebdo + 10 ans + double garantie)
9. Plateforme de profs (50 séances × 30 min + 10 000+ classes virtuelles + 700+ formateurs)
10. Tempo (Maintenant / Été / Rentrée / J'explore)
11. **Pricing Premium 11 980 €** (vs 55 000 € présentiel)
12. Ce qu'inclut Studi Campus Premium (Pédagogie / Accompagnement / Projection pro)
13. Financement (individuel / alternance / France Travail)
14. Pour les parents (tableau comparatif + 5 garanties + kit PDF)
15. Témoignages (Andréa · Martine · Marion)
16. Stats band navy (4 chiffres clés)
17. FAQ (8 questions dont valeur MBA en ligne + rétractation 14j)
18. CTA final + Footer

---

## 7. Assets — état et minimum viable

### Le HTML V5-b ne référence que 6 photos

Ce sont les **seules** strictement nécessaires pour que la landing s'affiche sans placeholders :

| Fichier | Contenu |
|---|---|
| `assets/hero_jardin-lux.jpg` | Femme 26 ans, Jardin du Luxembourg automne, manteau camel |
| `assets/prof_ring-light.jpg` | Formatrice 42 ans, home office, ring light |
| `assets/prof_learner.jpg` | Femme 30 ans, pull crème, laptop, salon cosy |
| `assets/temoignage_andrea.jpg` | Portrait 28 ans, pull jaune moutarde |
| `assets/temoignage_martine.jpg` | Portrait 44 ans, col roulé crème, mèches grises |
| `assets/temoignage_marion.jpg` | Portrait 30 ans, origine créole, top lin blanc |

### Photos persona (bonus, non référencées dans V5-b actuel)

17 photos persona décrites dans le CSV Ideogram. Utilisables pour V6+, variations A/B, ou sections enrichies.

---

## 8. Sources de vérité — ordre de priorité

En cas de contradiction entre deux documents, on tranche dans cet ordre :

1. **Décisions Pierre explicites** (dans les conversations ou dans `BRIEF_REPRISE.md`)
2. **`studi-campus-v5a-copy.md`** — référence de vérité pour le copy éditorial (637 lignes, itération #5 figée)
3. **`studi-campus-v5b.html`** — matérialisation design et structure
4. **`README.md`** — vue d'ensemble
5. **Ce `CONTEXT.md`** — doctrine consolidée

---

## 9. Chantiers ouverts

Tout ce qui reste à itérer. Cette section se met à jour au fil de l'eau.

### Court terme

- Intégration des 6 photos + test visuel complet
- Déploiement GitHub Pages ou Vercel
- Responsive mobile — passe de finition
- Vérification accessibilité (contrastes, alt text, navigation clavier)

### Moyen terme

- Variations A/B sur hero, pricing, CTA final
- Version **EN** pour Le Wagon Europe / marché international
- PDF export pour partage COMEX / parents
- Intégration analytics (Plausible ou équivalent)
- Variations de la carte (format square pour social, vertical pour mobile, dark mode)

### Long terme

- Enrichissement des 17 personas Ideogram si V6 en tire parti
- Intégration formulaire admission (lien Salesforce à scoper)
- Page détail par faculté
- Page parents dédiée (actuellement section)

---

## 10. Décisions Pierre — à ne pas re-challenger

La liste courte, pour fixer le cadre :

- **Palette** : celle définie en §4, pas celle de la charte v1.0
- **Tutoiement** : Pierre tutoie, tu le tutoies
- **Siège Montpellier** : caption obligatoire, jamais en hero
- **Carte** : statique uniquement dans la landing
- **Pricing** : 11 980 € Premium par défaut
- **Garanties** : wording NDS officiel exact
- **10 ans** : phrase signature intouchable
- **Pas de "statut étudiant"** — RNCP uniquement
- **Single-file HTML**, pas de framework, pas de build step

---

*Dernière mise à jour : 19 avril 2026 — reprise post V5-b final.*
