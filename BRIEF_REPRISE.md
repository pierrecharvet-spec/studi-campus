# BRIEF DE REPRISE — Studi Campus V5-b

> **À coller en première prompt de la prochaine session Claude**, accompagné des fichiers du bundle. Claude aura tout le contexte nécessaire pour reprendre sans te faire répéter.

---

Salut Claude. On reprend le projet **Studi Campus**, au point où on l'a laissé le 19 avril 2026.

Je suis Pierre Charvet, CEO de Studi (groupe Galileo Global Education). Tu peux me tutoyer.

## Ce qu'on fait

On construit la **landing page prototype de Studi Campus** — la formule Premium par défaut de Studi pour l'enseignement supérieur en ligne (Bac+2 à Bac+5). 3 facultés : Tech School, Business School, People & Finance School, avec nos écoles partenaires (Le Wagon, HETIC, Digital Campus, LISAA, ESG, PSB, Comptalia…).

## Où on en est

La **V5-b est finale côté structure, copy, layout et carte de France**. Il ne manque plus que les photos (que j'ai malheureusement perdues et dois régénérer via Ideogram).

## Fichiers joints à cette prompt

- `studi-campus-v5b.html` — la landing finale (237 KB, un seul fichier, inline SVG carte France 3 641 points)
- `studi-campus-v5a-copy.md` — la copy éditoriale complète itération #5 (référence de vérité)
- `studi-campus-ideogram-master.csv` — 23 prompts Ideogram consolidés, 66 images à générer
- `carte/carte_statique_dense.svg` — la carte France (déjà intégrée dans le HTML)
- `carte/carte_animation_optionnelle.gif` — GIF animé 1999-2026 (dispo, pas utilisé dans la landing)
- `previews/` — 7 screenshots de la V5-b telle qu'elle rend dans le navigateur

## Règles à respecter (décisions déjà actées — pas à re-challenger)

1. **Palette** : navy `#12161D` + paper `#F3ECDE` + terracotta `#C9542E` + jaune Studi `#FFCA4A` + bleu Studi `#255587`. On **garde** cette palette et **pas** celle de la charte officielle Studi v1.0.
2. **Typos** : Lora (display, italiques signatures, logo "studi.") + Roboto (body, UI, labels).
3. **Carte France** : statique uniquement dans la landing, pas le GIF.
4. **Pricing Premium** : 11 980 € par défaut (Graduate 5 590 € + Bachelor 6 390 €). Comparaison présentiel = 55 000 €, économie ≈ 43 000 €.
5. **Garanties** : "Diplômé ou Remboursé" + "Embauché ou Remboursé", wording NDS officiel.
6. **Phrase signature 10 ans d'accès** : *"Vous n'êtes jamais ancien élève. Vous êtes toujours étudiant·e. Pour 10 ans."*
7. **Siège Montpellier** : si photo utilisée, caption obligatoire "Siège Studi · Montpellier", **jamais en hero**.
8. **Hero principal** : photo Jardin du Luxembourg automne (fichier `assets/hero_jardin-lux.jpg`).

## Ce qu'il me reste à faire (par ordre)

1. Régénérer les 23 prompts du CSV dans Ideogram, sélectionner 1 image par prompt.
2. Renommer les photos avec les noms indiqués dans chaque prompt (`Intended file: xxx.jpg`).
3. Déposer le tout dans un dossier `assets/` à côté du HTML.

## Ce que je pourrais te demander à cette reprise

- **Itérer sur une section spécifique** du HTML (copy, layout, CTA, wording FAQ).
- **Déployer la landing** (Vercel / Netlify / GitHub Pages) — on peut aussi connecter le GitHub MCP.
- **Adapter en responsive mobile** avec plus de finesse (le HTML est déjà responsive, mais on peut pousser).
- **Variations A/B** du hero, du pricing ou du CTA final.
- **Traduire en anglais** pour le marché international (Le Wagon Europe).
- **Sortir un PDF** à partir du HTML pour le partager avec le COMEX.
- **Fabriquer des variations de la carte** (format square, format vertical, dark mode, etc).
- Travailler sur un **autre livrable Studi** (pitch deck, note stratégique, EGA, SOS, brief équipe).

## Ma priorité immédiate

[À remplir quand tu relances la session : "je veux d'abord…" / "mon problème c'est…" / "regarde la V5-b et donne-moi ton avis critique…"]

---

_Reprise au point exact où on s'est arrêté le 19 avril 2026, après la perte des photos Ideogram._
