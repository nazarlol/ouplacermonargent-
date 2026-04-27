# OuPlacerMonArgent.fr — Contexte projet

## Présentation

Blog de finance personnelle française pour débutants.
Objectif : générer 500-1000€/mois de revenus passifs via des liens d'affiliation.
Auteur : Axel Lormeau, ingénieur data, 39 ans, basé dans une petite bourgade du sud de la France.

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
  Ton contenu ici.
</Callout>
```
Props : `type?` (info | conseil | attention), `titre?`

### Schema
Schéma de progression visuelle.
```mdx
<Schema
  titre="Par où commencer ?"
  etapes={[
    { label: "Livret A", description: "3 mois de dépenses — ton filet de sécurité" },
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

Chaque article doit avoir ce frontmatter. Le slug est dérivé automatiquement du nom de fichier par Astro — ne pas le dupliquer ici.

```yaml
---
title: "Titre de l'article"
description: "Description SEO — 150-160 caractères"
pubDate: YYYY-MM-DD
author: "Axel"
tags: ["tag1", "tag2"]
---
```

---

## Persona — Axel, auteur du blog

Axel a 39 ans, ingénieur data, basé dans une petite bourgade du sud de la France.
Il n'est pas conseiller financier et ne prétend pas l'être.
Son angle : "je pars de zéro avec toi".

Ce qui le rend crédible : il a calculé ce qu'il aurait eu s'il avait investi 200€/mois depuis ses 25 ans. Le résultat l'a rendu malade. Ce blog c'est sa façon de ne pas répéter cette erreur — et d'aider ceux dans la même situation.

**Calcul de référence :**
- 200€/mois depuis 25 ans dans un ETF Monde à 8%/an = environ 89 000€ à 39 ans
- 100€/mois depuis 25 ans à 7%/an = environ 30 000€ à 39 ans

Axel parle à la première personne "je" pour ses anecdotes. Il tutoie le lecteur, sans jamais tomber dans le familier.

---

## WRITING RULES

### Ton
- Direct, honnête, légèrement cynique envers les banques traditionnelles
- Jamais comme un manuel scolaire — comme quelqu'un qui explique clairement
- Chaque article contient au moins un moment où Axel partage une opinion personnelle, une erreur, ou un calcul concret
- Contexte France entière — jamais centré sur Paris

### Voix et adresse au lecteur
- Toujours tutoyer le lecteur — "tu", "ton", "tes", "toi"
- Axel parle à la première personne "je" pour ses anecdotes personnelles
- Ne jamais mélanger "tu" et "vous" dans le même article
- Le tutoiement reste sérieux et précis — jamais familier, jamais racoleur. "Tu as probablement déjà..." oui. "Ouais mec laisse tomber..." non.
- Pas d'argot, pas d'expressions très orales ("genre", "du coup", "en mode"), pas d'interpellations agressives
- Le tutoiement crée la proximité, le contenu apporte le sérieux

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

### Calibrage longueur (SEO)

La longueur cible dépend du type d'article. Ne pas remplir avec du vide pour atteindre la fourchette — mais ne pas finir nettement en-dessous non plus, Google récompense la profondeur sur les requêtes commerciales.

- **Articles transactionnels** (avis produit, comparatifs "meilleur X", "X vs Y") : **2 500 à 3 500 mots**
  Exemples : "Trade Republic avis 2026", "Meilleur courtier bourse débutant France 2026"
- **Articles informationnels approfondis** (guides complets, comparaisons de dispositifs) : **2 000 à 2 800 mots**
  Exemples : "PEA ou Assurance Vie", "Où placer son argent quand on débute"
- **Articles informationnels pratiques** (tutoriels, méthodes, calculs) : **1 500 à 2 200 mots**
  Exemples : "Comment investir 100€ par mois", "Comment gérer son budget"

Au-delà de 3 500 mots, mieux vaut découper en deux articles et les lier entre eux.

### Maillage interne

Chaque article doit pointer vers d'autres articles du blog. C'est un des leviers SEO les plus rentables — Google s'en sert pour comprendre la structure du site, et ça fait circuler le lecteur sur les pages qui convertissent.

- **Minimum 3 liens internes** vers d'autres articles, intégrés dans le corps du texte (pas en bloc à la fin)
- Les articles informationnels doivent toujours lier vers les articles transactionnels quand le sujet s'y prête (pousser le trafic vers ce qui rapporte)
- Format : `[texte d'ancrage descriptif](/blog/slug-article/)` — l'ancre doit décrire le contenu cible, jamais "cliquez ici" ou "voir cet article"
- Lier dès qu'un sujet d'article existant est mentionné naturellement dans le texte
- Si un lien serait pertinent mais que l'article cible n'existe pas encore, noter dans un commentaire MDX `{/* TODO: lier vers article-X quand publié */}`
- Ne jamais forcer un lien artificiellement — si le contexte ne s'y prête pas, on s'abstient

### Ancrage dans le vécu
Quand le sujet traite de situations universelles (revenus, dépenses, épargne, retraite, banque, abonnements...), formuler l'information de manière à ce que le lecteur fasse lui-même le lien avec sa situation.
- Pas une technique à placer à un endroit précis — une façon naturelle d'écrire
- Préférer "pose la question autour de toi" à "beaucoup de gens"
- Préférer "tu as probablement déjà..." à "les Français ont tendance à..."
- L'information doit renvoyer le lecteur à sa propre réalité sans lui demander explicitement de le faire
- Si le sujet ne s'y prête pas naturellement, on ne force pas

### Disclaimer standard
À placer en italique à la fin de chaque article :

*Cet article est rédigé à titre informatif et pédagogique. Je ne suis pas conseiller financier. Les chiffres et exemples présentés sont des illustrations générales. Avant toute décision, prends le temps d'analyser ta situation afin de ne pas compromettre ta situation financière.*

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
- ✅ Première version en place
- La home ne doit pas être centrée sur l'histoire personnelle d'Axel — c'est le rôle de la page À propos
- Message général et universel : épargner/investir se fait dans le temps, le plus tôt le mieux
- Structure actuelle : accroche générale → derniers articles → lien vers tous les articles
- Pas de section "par où commencer" avec ancres — les IDs générés par Astro sur les titres avec accents sont imprévisibles

---

## Contexte France

- Chiffres nationaux, pas parisiens
- Salaire médian français : ~2 000€ net
- Le lecteur type : 25-45 ans, en province, avec une capacité d'épargne mensuelle
- Éviter les références trop parisiennes (loyers, coût de la vie)