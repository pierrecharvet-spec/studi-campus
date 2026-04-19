# CLAUDE.md — Instructions pour Claude Code

> Fichier lu automatiquement par Claude Code à chaque session ouverte dans ce repo.
> Ne pas supprimer. Mettre à jour quand les règles de collaboration évoluent.

---

## 0. Lecture préalable obligatoire

Avant toute action dans ce repo, lis dans cet ordre :

1. **`CONTEXT.md`** — doctrine projet (positionnement, voix, design system, non-négociables)
2. **`BRIEF_REPRISE.md`** — état du projet au 19 avril 2026
3. **`README.md`** — structure et vue d'ensemble
4. **`studi-campus-v5a-copy.md`** — référence de vérité copy éditorial (à consulter à chaque modif de texte)

Si tu modifies du copy sans avoir lu v5a-copy.md, tu vas casser la voix. Ne saute pas cette étape.

---

## 1. À qui tu parles

**Pierre Charvet**, CEO de Studi (groupe Galileo Global Education).

- **Tutoiement**, toujours
- Préfère **concis, concret, assertif** — pas de préambules, pas de "bien sûr, je vais…"
- Il sait coder. Ne pas sur-expliquer la syntaxe.
- Projet stratégique — ce n'est pas un proto jetable, c'est le vrai prototype de présentation du service

---

## 2. Règles de collaboration

### Une itération à la fois

- **Maximum 2 changements par prompt**. C'est la règle fixée sur Trajectoire, elle tient ici aussi.
- Si Pierre demande 5 choses, tu en fais 2, tu testes, tu commites, et tu annonces les 3 suivantes.

### Annonce avant d'agir

- Pour toute modif **structurelle** (changer une section, refondre un layout, toucher la carte, changer la palette) : **explique ce que tu vas faire en 2-3 lignes avant d'agir**, attends validation.
- Pour les modifs **cosmétiques** (ajuster un padding, corriger une faute, renommer un fichier) : fais, dis-le après.

### Test visuel systématique

- Après **chaque** modification du HTML ou du CSS : `open index.html` pour que Pierre vérifie visuellement.
- Ne commit **jamais** sans que Pierre ait validé le rendu visuel.

### Commits atomiques

- Un sujet = un commit.
- Messages en **français**, format : `type: description courte`
- Types utilisés : `copy:`, `design:`, `fix:`, `chore:`, `assets:`, `feat:`, `docs:`
- Exemples :
  - `copy: retouche tagline hero — angle temps/avenir`
  - `design: ajuste contraste cartouches DOM-TOM sur carte France`
  - `assets: ajoute les 6 photos Ideogram validées`
  - `docs: mets à jour CONTEXT.md avec décision pricing`

### Pas de bulk

- Jamais de commit fourre-tout type `update` ou `changes`.
- Si tu as touché 10 choses sans commit intermédiaire, split le commit avant de pousser.

---

## 3. Ce qu'on ne touche pas sans validation explicite Pierre

Zone rouge — pas de modif sans demande directe :

- **Palette couleurs** (les 7 hex de `CONTEXT.md` §4)
- **Typos** (Lora + Roboto)
- **Pricing** (11 980 € Premium)
- **Garanties** (wording NDS exact)
- **Phrase signature 10 ans**
- **Carte France SVG** (3 641 points, inline)
- **Architecture 18 sections** du HTML
- **Contenu de `studi-campus-v5a-copy.md`** (référence figée)

Si Pierre demande de toucher à une de ces zones, reconfirme l'intention avant d'exécuter.

---

## 4. Règles techniques

### Stack

- **HTML / CSS / JS vanilla**, single-file preference
- **Pas de framework** (pas de React, pas de Vue, pas de Tailwind build)
- **Pas de npm**, pas de `package.json`
- **Pas de build step** — on ouvre `index.html` direct, c'est la règle
- **SVG inline** pour tout graphique (la carte est inline dans le HTML)

### Si un nouveau besoin impose une dépendance

- Justifie le besoin en 2 lignes
- Propose l'alternative vanilla d'abord
- Attends validation Pierre avant d'introduire la dépendance

### Fichiers

- `index.html` à la racine (anciennement `studi-campus-v5b.html`)
- `assets/` pour les photos
- `carte/` pour les fichiers source carte (SVG, GIF) — référence, pas servi en prod
- `previews/` pour screenshots — référence, pas servi en prod
- Les `.md` de doctrine restent à la racine

---

## 5. Git workflow

### Branches

- `main` = production. Ce qui est sur `main` est déployable.
- Pour les expérimentations larges, branche `iter/nom-court` puis merge.
- Pour modif standard, direct sur `main` (projet solo, on ne se complique pas).

### Avant chaque push

1. `open index.html` — test visuel
2. `git status` — confirmer le scope
3. `git log --oneline -5` — voir le contexte des derniers commits
4. Validation Pierre
5. `git push`

### Remote

- `origin` → `https://github.com/pierrecharvet-spec/studi-campus.git`

---

## 6. Commandes utiles

```bash
# Preview local
open index.html

# Serveur local (si besoin de tester en conditions réelles)
python3 -m http.server 8000
# puis http://localhost:8000

# Historique propre
git log --oneline --graph -20

# Voir ce qui a bougé depuis le dernier push
git diff origin/main

# Déploiement Vercel (quand scopé)
# vercel --prod
```

---

## 7. Patterns d'itération récurrents

Ce que Pierre demande souvent, et comment y répondre :

### "Itère sur le hero"

- Ouvre `studi-campus-v5a-copy.md` section 02
- Propose **2-3 variations courtes** (pas 10)
- Chaque variation : H1 + baseline + 1 ligne de rationale
- Attends le choix avant d'intégrer

### "Variation A/B sur X"

- Crée une branche `iter/ab-X`
- Livre 2 versions complètes (pas partielles)
- Screenshot compare si possible

### "Responsive mobile"

- Teste à 375px (iPhone SE) et 390px (iPhone 14)
- La carte France doit rester lisible — si nécessaire, version simplifiée en mobile
- Touch targets : minimum 44×44px

### "Version EN"

- Ne traduis **pas** littéralement
- Adapte la voix au marché — la voix française éditoriale ne marche pas en anglais international
- Valide les équivalents RNCP / garanties juridiques avant de traduire (certaines formulations ne sont pas exportables telles quelles)

### "Export PDF pour COMEX"

- `wkhtmltopdf` ou équivalent, format A4 paysage
- Proposer aussi version diapo (10-15 slides) extraite du HTML si le cas d'usage est présentation live

---

## 8. Anti-patterns — à ne jamais faire

- ❌ Modifier le copy sans avoir consulté `v5a-copy.md`
- ❌ Changer la palette "pour améliorer le contraste"
- ❌ Introduire Tailwind, Bootstrap, ou tout framework CSS
- ❌ Minifier le HTML en commit (il doit rester lisible)
- ❌ Commit avec message `update` ou `wip`
- ❌ Push sans test visuel
- ❌ Remplacer la carte inline par une image — la carte est un asset éditorial, pas décoratif
- ❌ Utiliser "100 %", "révolutionnaire", "unique", "leader" dans le copy
- ❌ Ajouter un compte à rebours ou du urgency manipulatif
- ❌ Écrire "statut étudiant" — Studi Campus ne l'attribue pas

---

## 9. Quand tu n'es pas sûr

**Demande.** Pierre préfère une question claire à 3 itérations correctives.

Format de question recommandé :
> *« Avant de toucher à X, je veux être sûr : tu veux [option A] ou [option B] ? Mon intuition est A parce que [raison], mais je te laisse trancher. »*

---

*Ce fichier évolue avec le projet. Quand une règle est ajoutée, la commit en `docs: ajoute règle X à CLAUDE.md`.*
