# Studi Campus V5-b — Export complet

Bundle auto-suffisant pour reprendre le projet **sans rien perdre**, dans une autre session, sur un autre ordinateur, à un autre moment.

---

## 📦 Contenu du bundle

```
studi-campus-v5b/
├── README.md                          ← ce fichier
├── BRIEF_REPRISE.md                   ← à coller en première prompt de la prochaine session Claude
├── studi-campus-v5b.html              ← la landing finale (237 KB, un seul fichier)
├── studi-campus-v5a-copy.md           ← toute la copy éditoriale (637 lignes, itération #5)
├── studi-campus-ideogram-master.csv   ← les 23 prompts Ideogram à rejouer
├── carte/
│   ├── carte_statique_dense.svg       ← carte France intégrée dans la V5-b (144 KB, 3 641 points)
│   ├── carte_statique_dense.png       ← preview de la carte
│   └── carte_animation_optionnelle.gif ← GIF animé 1999-2026 (459 KB, non utilisé dans la landing)
└── previews/
    ├── 01_hero.png                    ← aperçus rendus navigateur de la V5-b
    ├── 02_profils.png
    ├── 03_profils_suite.png
    ├── 04_carte_france.png
    ├── 05_ecole_reste.png
    ├── 06_garanties.png
    └── 07_profs.png
```

---

## 🚀 Comment repartir proprement

### 1. Régénérer les 23 photos Ideogram
Ouvre `studi-campus-ideogram-master.csv` dans Ideogram. Lance le batch. Chaque prompt a un nom de fichier intégré dans le texte (`Intended file: xxx.jpg`) qui **correspond exactement** au nom attendu par le HTML.

**Budget estimé** : 66 images générées au total (23 prompts × 2-3 images chacun). Sélectionne la meilleure de chaque série.

### 2. Construire le dossier final à déployer
Crée cette arborescence :
```
ma-landing/
├── studi-campus-v5b.html
└── assets/
    ├── hero_jardin-lux.jpg
    ├── persona_chambre.jpg
    ├── persona_outre-mer.jpg
    ├── persona_cafe-hipster.jpg
    ├── persona_athlete-gym.jpg
    ├── persona_mere-canape.jpg
    ├── persona_auvergne.jpg
    ├── persona_lisbonne.jpg
    ├── prof_ring-light.jpg
    ├── prof_learner.jpg
    ├── persona_tgv.jpg
    ├── persona_athlete-rentre.jpg
    ├── persona_pere-fils.jpg
    ├── persona_biblio.jpg
    ├── persona_coworking.jpg
    ├── persona_metro.jpg
    ├── persona_duo-cafe.jpg
    ├── temoignage_andrea.jpg
    ├── temoignage_martine.jpg
    └── temoignage_marion.jpg
```

Photos bonus (facultatives) : `hero_canape-paris.jpg`, `parents_conversation.jpg`, `cta_admission.jpg`.

### 3. Vérifier
Ouvre `studi-campus-v5b.html` dans un navigateur. Les placeholders stylés disparaissent automatiquement dès que les images sont bien nommées et placées. S'il reste un placeholder, le nom du fichier attendu est affiché dedans.

---

## 🎨 Rappels palette & typo (au cas où)

**Palette** (gardée de la V4/V5, pas la palette officielle Pierre d'accord) :
- Paper : `#F3ECDE`
- Paper warm : `#EDE4D0`
- Navy : `#12161D`
- Slate : `#2F3A4B`
- Terracotta : `#C9542E`
- Jaune Studi : `#FFCA4A`
- Bleu Studi : `#255587`

**Typographies** (Google Fonts, déjà câblées dans le HTML) :
- Display : **Lora** (titres, italiques signature, logo "studi.")
- Body : **Roboto** (corps, UI, labels)

---

## 📋 Structure de la V5-b — 18 sections

1. Nav sticky (logo studi. + 5 liens + CTA primary)
2. Hero — *Une grande école. Trois facultés. Chez vous.*
3. Portes d'entrée (4 portes : Métier / Compétences / Faculté / Orientation)
4. 6 Profils transverses (Pressé·e, Fan digital, Budget malin, Loin des villes, Double projet, Mobilité)
5. **Carte France densifiée** (SVG inline, 3 641 points, Corse + 5 DOM-TOMs en cartouches) + 4 stats (59 000 · 25 ans · 400+ · 700+)
6. Les 3 facultés (Tech / Business / People & Finance) avec partenaires académiques
7. Compétences 360 (6 accélérateurs : IA, Cours Florent, logiciels, langues, entrepreneuriat, coaching)
8. L'école qui reste (IA au cœur + mises à jour hebdo + 10 ans d'accès + double garantie)
9. Plateforme de profs (50 séances × 30 min + 10 000+ classes virtuelles + 700+ formateurs)
10. Tempo (Maintenant / Été / Rentrée / J'explore + 3 cartes réassurance)
11. **Pricing Premium : 11 980 €** (vs 55 000 € présentiel, économie ≈ 43 000 €)
12. Ce qu'inclut Studi Campus Premium (3 colonnes : Pédagogie / Accompagnement / Projection pro)
13. Financement (individuel / alternance / France Travail)
14. Pour les parents (tableau comparatif + 5 garanties + kit PDF)
15. Témoignages (Andréa · Martine · Marion)
16. Stats band navy (4 chiffres clés)
17. FAQ (8 questions dont valeur MBA en ligne + rétractation 14j)
18. CTA final + Footer

---

## 🗺️ À propos de la carte

La carte **statique** (`carte_statique_dense.svg`) est déjà intégrée inline dans `studi-campus-v5b.html`. Tu n'as rien à faire pour qu'elle s'affiche.

Le GIF animé 1999→2026 (`carte_animation_optionnelle.gif`) a été conçu mais **n'est pas utilisé** dans la landing (décision Pierre : "trop raconter notre vie"). Il reste dispo pour d'autres usages : rapport annuel, pitch deck investisseurs, slide COMEX, page "À propos".

Caractéristiques de la carte statique :
- 2 190 points métropole + 80 Corse + 126 DOM-TOMs (Guadeloupe · Martinique · Guyane · Réunion · Mayotte en cartouches à droite)
- Clusters renforcés sur Paris / Lyon / Marseille / Toulouse / Bordeaux / Lille / Nantes / Strasbourg / Montpellier / Rennes / Nice / Reims
- Navy `#12161D` sur paper `#F3ECDE`
- 144 KB en SVG, scale parfait, zéro requête externe

---

## ⚠️ Décisions Pierre à respecter

- **Palette** : on garde la palette Claude (paper/terracotta/navy/jaune), **pas** la palette officielle de la charte Studi v1.0 (qui est navy/gris/jaune uniquement). Pierre a validé explicitement.
- **Siège Montpellier** : si tu insères cette photo, caption obligatoire "Siège Studi · Montpellier", **jamais en hero** (risque de confusion présentiel).
- **Tutoiement** : Pierre tutoie Claude.
- **Carte** : **pas** de GIF animé dans la landing — statique uniquement.
- **Pricing** : Premium par défaut à **11 980 €** (Graduate 5 590 € + Bachelor 6 390 €).
- **Garanties** : wording NDS officiel ("Diplômé ou Remboursé" + "Embauché ou Remboursé").
- **10 ans d'accès** : phrase signature = *"Vous n'êtes jamais ancien élève. Vous êtes toujours étudiant·e. Pour 10 ans."*

---

## 📊 Statut projet au moment de cet export

| Item | État |
|---|---|
| Copy éditorial itération #5 | ✅ Figée |
| Carte France statique | ✅ Finale, intégrée inline |
| Carte France GIF | ✅ Dispo (non utilisée) |
| HTML V5-b (18 sections) | ✅ Finale |
| Prompts Ideogram consolidés | ✅ 23 prompts, 66 images |
| Photos Ideogram générées | ⚠️ À régénérer (perdues) |
| Intégration photos dans landing | ⚠️ À faire quand photos prêtes |

---

_Export généré le 19 avril 2026 · Studi Campus V5-b final build_
