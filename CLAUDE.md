# OuPlacerMonArgent.fr — Contexte projet

## Présentation

Blog de finance personnelle française pour débutants.
Objectif : générer 500-1000€/mois de revenus passifs via des liens d'affiliation.
Auteur : Axel Lormeau, ingénieur data, 39 ans, basé à Rodez (France).

---

## Stack technique

- **Framework** : Astro (site statique)
- **Format articles** : MDX uniquement (plus de .md)
- **Hébergement** : Cloudflare Pages (gratuit)
- **Repo GitHub** : github.com/nazarlol/ouplacermonargent-
- **Domaine** : ouplacermonargent.fr
- **Articles** : `src/content/blog/`
- **Composants** : `src/components/`

---

## Composants disponibles

Tous les articles MDX doivent importer les composants en haut du fichier :

```mdx
import StatCard from '../../components/StatCard.astro';
import Callout from '../../components/Callout.astro';
import Schema from '../../components/Schema.astro';
import AffiliateCard from '../../components/AffiliateCard.astro';
```

### StatCard
Chiffre clé mis en valeur.
```mdx
<StatCard
  valeur="89 000€"
  label="Ce que j'aurais aujourd'hui"
  detail="200€/mois depuis 25 ans dans un ETF Monde à 8%/an"
  couleur="vert"
/>
```
Props : `valeur`, `label`, `detail?`, `couleur?` (vert | bleu | orange)

### Callout
Encadré texte mis en valeur.
```mdx
<Callout type="conseil" titre="À retenir">
  Votre contenu ici.
</Callout>
```
Props : `type?` (info | conseil | attention), `titre?`

### Schema
Schéma de progression visuelle.
```mdx
<Schema
  titre="Par où commencer ?"
  etapes={[
    { label: "Livret A", description: "3 mois de dépenses — votre filet de sécurité" },
    { label: "PEA + ETF", description: "Investir régulièrement sur le long terme" },
    { label: "Assurance Vie", description: "Ouvrir tôt, même avec 500€" },
  ]}
/>
```

### AffiliateCard
Carte d'affiliation — à utiliser uniquement quand le lien affilié est disponible.
```mdx
<AffiliateCard
  nom="Trade Republic"
  description="Le courtier que j'utilise pour mes ETF."
  avantages={[
    "0€ de frais de courtage sur les ETF",
    "Compte ouvert en 10 minutes",
  ]}
  lien="LIEN_AFFILIÉ"
  badge="Recommandé"
  couleur="vert"
/>
```

---

## Frontmatter standard

Chaque article doit avoir ce frontmatter :

```yaml
---
title: "Titre de l'article"
description: "Description SEO — 150-160 caractères"
pubDate: YYYY-MM-DD
author: "Axel"
tags: ["tag1", "tag2"]
slug: "slug-de-l-article"
---
```

---

## Persona — Axel, auteur du blog

Axel a 39 ans, ingénieur data, basé en France (pas à Paris).
Il n'est pas conseiller financier et ne prétend pas l'être.
Son angle : "je pars de zéro avec vous".

Ce qui le rend crédible : il a calculé ce qu'il aurait eu s'il avait investi 200€/mois depuis ses 25 ans. Le résultat l'a rendu malade. Ce blog c'est sa façon de ne pas répéter cette erreur — et d'aider ceux dans la même situation.

**Calcul de référence :**
- 200€/mois depuis 25 ans dans un ETF Monde à 8%/an = environ 89 000€ à 39 ans
- 100€/mois depuis 25 ans à 7%/an = environ 30 000€ à 39 ans

Axel parle à la première personne "je" pour ses anecdotes. Il vouvoie toujours le lecteur.

---

## WRITING RULES

### Ton
- Direct, honnête, légèrement cynique envers les banques traditionnelles
- Jamais comme un manuel scolaire — comme quelqu'un qui explique clairement
- Chaque article contient au moins un moment où Axel partage une opinion personnelle, une erreur, ou un calcul concret
- Contexte France entière — jamais centré sur Paris

### Voix et adresse au lecteur
- Toujours vouvoyer le lecteur — "vous", "votre", "vos"
- Axel parle à la première personne "je" pour ses anecdotes personnelles
- Ne jamais mélanger "tu" et "vous" dans le même article

### Style
- Phrases courtes. Maximum 2 lignes.
- Paragraphes courts — 3 lignes maximum
- Éviter les listes à rallonge — préférer des paragraphes rythmés
- Toujours utiliser des chiffres concrets et des exemples réels
- Le "si j'avais investi X€/mois depuis mes 25 ans" doit apparaître naturellement dans les articles pertinents

### Mots interdits
optimal, crucial, essentiel, incontournable, néanmoins, toutefois, il convient de, dans le cadre de, en outre, il est important de noter

### Format
- Toujours commencer par une accroche personnelle d'Axel (anecdote, calcul, réalisation)
- Jamais commencer par une définition générique
- Terminer par une recommandation claire et directe
- Disclaimer légal en italique à la fin

### Ancrage dans le vécu
Quand le sujet traite de situations universelles (revenus, dépenses, épargne, retraite, banque, abonnements...), formuler l'information de manière à ce que le lecteur fasse lui-même le lien avec sa situation.
- Pas une technique à placer à un endroit précis — une façon naturelle d'écrire
- Préférer "posez la question autour de vous" à "beaucoup de gens"
- Préférer "vous avez probablement déjà..." à "les Français ont tendance à..."
- L'information doit renvoyer le lecteur à sa propre réalité sans lui demander explicitement de le faire
- Si le sujet ne s'y prête pas naturellement, on ne force pas

### Disclaimer standard
À placer en italique à la fin de chaque article :

*Cet article est rédigé à titre informatif et pédagogique. Je ne suis pas conseiller financier. Les chiffres et exemples présentés sont des illustrations générales. Avant toute décision, prenez le temps d'analyser votre situation afin de ne pas compromettre votre situation financière.*

---

## Articles publiés

1. `ou-placer-son-argent-debutant.mdx` — Où placer son argent quand on débute ? Le guide complet 2026
2. `comment-gerer-son-budget.mdx` — Comment gérer son budget : l'audit que personne ne veut faire

---

## Articles à écrire

1. Meilleur courtier bourse débutant France 2026
2. PEA ou Assurance Vie — lequel choisir ?
3. Trade Republic avis 2026
4. Comment investir 100€ par mois en bourse

---

## Affiliation

### Programmes soumis
- **Linxea** (Awin) — en attente de validation
- **BoursoBank** (Awin) — en attente de validation
- **Trade Republic** (Impact.com) — en attente de validation

### Règle d'intégration
- Ne pas intégrer de lien affilié sans avoir le lien trackable réel
- Utiliser le composant `<AffiliateCard>` pour présenter les offres
- Mentionner "Lien affilié" de façon transparente

---

## SEO

- Google Search Console configuré et vérifié
- Sitemap soumis : `https://ouplacermonargent.fr/sitemap-index.xml`
- Balise `site` dans `astro.config.mjs` : `https://ouplacermonargent.fr`
- Robots.txt géré par Cloudflare — bots IA bloqués, Googlebot autorisé

---

## TODO

### Technique
- [ ] Composant `<Checklist>` avec localStorage — actions à cocher dans chaque article
- [ ] Redirect www en cours d'initialisation sur Cloudflare Pages
- [ ] Intégrer le logo OPMA sur le site

### Contenu
- [ ] Écrire les 4 prochains articles
- [ ] Intégrer les AffiliateCard une fois les liens validés

### Homepage
- À faire en dernier, juste avant l'indexation Google complète
- Doit raconter l'histoire d'Axel et mettre en avant les articles phares

---

## Contexte France

- Chiffres nationaux, pas parisiens
- Salaire médian français : ~2 000€ net
- Le lecteur type : 25-45 ans, en province, avec une capacité d'épargne mensuelle
- Éviter les références trop parisiennes (loyers, coût de la vie)
