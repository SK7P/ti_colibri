# Roadmap Ti'colibri

Feuille de route pour l'evolution du site Ti'colibri, organisee en phases et priorites.

## Legende

- **P1** : Critique / Bloquant
- **P2** : Important / Haute valeur
- **P3** : Souhaitable / Moyenne valeur
- **P4** : Nice to have / Basse valeur
- **P5** : Future / Backlog

## Phase 0 : Quick Wins (Site actuel - HTML/CSS/JS)

### Performance (P1)

- [ ] **Optimiser Tailwind CSS**
  - Remplacer CDN par fichier compile (~15KB au lieu de 3MB)
  - Gain: +40 points Lighthouse
  - Estimation: 2h

- [ ] **Optimiser les images**
  - Convertir en WebP avec fallback JPEG
  - Ajouter `loading="lazy"` sur images hors viewport
  - Dimensionner correctement (600x400 au lieu de full res)
  - Gain: +15 points Lighthouse
  - Estimation: 3h

- [ ] **Optimiser Google Fonts**
  - Ajouter `&display=swap` dans URL
  - Ou self-host avec `font-display: swap`
  - Gain: +5 points Lighthouse
  - Estimation: 1h

- [ ] **Minification HTML/JS**
  - Configurer Netlify pour minification auto
  - Estimation: 0.5h

### Contenu et completude (P1)

- [ ] **Ajouter vraies coordonnees**
  - Telephone cliquable
  - Email
  - Liens reseaux sociaux (Facebook, Instagram, LinkedIn)
  - Remplacer placeholders lignes 581 et 689
  - Estimation: 1h

- [ ] **Integrer le vrai logo**
  - Verifier que logo.png est accessible
  - Optimiser taille/format
  - Estimation: 0.5h

- [ ] **Remplacer images placeholder**
  - Hero section
  - Section "Qui se cache derriere Ti'colibri"
  - Temoignages (photos clientes)
  - Estimation: 2h

### Pages legales (P1 - RGPD)

- [ ] **Creer page Mentions legales**
  - Informations editeur
  - Hebergeur
  - Responsable publication
  - Estimation: 2h

- [ ] **Creer page Politique de confidentialite**
  - Donnees collectees
  - Utilisation des donnees
  - Droits RGPD
  - Estimation: 2h

- [ ] **Creer page CGV**
  - Conditions generales de vente
  - Modalites de paiement
  - Droit de retractation
  - Estimation: 3h

- [ ] **Ajouter banniere cookies**
  - Consentement cookies
  - Conformite RGPD/ePrivacy
  - Estimation: 2h

### SEO (P2)

- [ ] **Ajouter meta tags Open Graph**
  - og:title, og:description, og:image, og:url
  - Estimation: 1h

- [ ] **Ajouter meta tags Twitter Cards**
  - twitter:card, twitter:title, etc.
  - Estimation: 0.5h

- [ ] **Implementer Schema.org (JSON-LD)**
  - LocalBusiness schema
  - Service schema
  - Review/Rating schema
  - Estimation: 2h

- [ ] **Creer sitemap.xml**
  - Generation manuelle ou plugin Netlify
  - Estimation: 1h

- [ ] **Creer robots.txt**
  - Configuration crawl
  - Estimation: 0.5h

- [ ] **Optimiser meta descriptions**
  - Description plus engageante et keyword-rich
  - Estimation: 1h

### Accessibilite (P2)

- [ ] **Verifier contraste couleurs**
  - Ratio minimum 4.5:1 (WCAG AA)
  - Ajuster si necessaire
  - Estimation: 1h

- [ ] **Ajouter navigation clavier**
  - Menu mobile accessible au clavier
  - Carousel navigable (touches arrows)
  - Estimation: 2h

- [ ] **Ameliorer aria-labels**
  - Liens "En savoir plus" plus descriptifs
  - Formulaires avec aria-required
  - Estimation: 2h

- [ ] **Ajouter styles :focus-visible**
  - Indicateurs de focus visibles
  - Estimation: 1h

- [ ] **Ameliorer alt texts images**
  - Descriptions plus precises
  - Estimation: 1h

### Code quality (P3)

- [ ] **Externaliser JavaScript**
  - Creer script.js
  - Organiser en modules/fonctions
  - Estimation: 3h

- [ ] **Ajouter validation formulaires**
  - Validation cote client
  - Messages d'erreur clairs
  - Feedback visuel apres soumission
  - Estimation: 3h

- [ ] **Ajouter gestion d'erreurs**
  - Try/catch sur operations critiques
  - Fallbacks si Netlify Forms echoue
  - Estimation: 2h

### UX (P3)

- [ ] **Ajouter bouton CTA flottant**
  - Telephone/WhatsApp sticky
  - Visible en scroll
  - Estimation: 2h

- [ ] **Ameliorer feedback formulaires**
  - Confirmation visuelle apres envoi
  - Message d'erreur si echec
  - Loading state pendant soumission
  - Estimation: 2h

- [ ] **Ajouter animations subtiles**
  - Scroll reveal elements
  - Transitions plus fluides
  - Estimation: 3h

---

## Phase 1 : Migration Next.js (Preparation V2)

### Setup et infrastructure (P1)

- [ ] **Initialiser projet Next.js 14+**
  - App Router
  - TypeScript
  - Tailwind CSS (avec config)
  - Estimation: 2h

- [ ] **Configurer Supabase**
  - Creer projet Supabase
  - Setup authentification
  - Configurer storage
  - Estimation: 3h

- [ ] **Designer schema base de donnees**
  - Tables: clients, dossiers, documents, rendez_vous, devis
  - Relations et contraintes
  - Row Level Security (RLS)
  - Estimation: 4h

- [ ] **Configurer environnements**
  - Variables d'environnement (.env)
  - Dev / Staging / Production
  - Estimation: 2h

- [ ] **Setup Vercel deployment**
  - Connecter repo GitHub
  - Configurer domaines
  - Estimation: 1h

### Reproduction site actuel (P1)

- [ ] **Migrer landing page**
  - Composants React
  - Sections: Hero, Difficultes, Accompagnement
  - Estimation: 6h

- [ ] **Migrer section tarifs**
  - Cartes pricing
  - Hover effects
  - Estimation: 3h

- [ ] **Migrer carousel temoignages**
  - Component carousel React
  - Navigation
  - Estimation: 3h

- [ ] **Migrer formulaires**
  - Formulaire contact
  - Formulaire lead magnet
  - Integration email (Resend/SendGrid)
  - Estimation: 4h

- [ ] **Migrer header/footer**
  - Navigation responsive
  - Menu mobile
  - Estimation: 3h

- [ ] **Optimiser assets**
  - Images Next.js Image component
  - Fonts optimisees
  - Estimation: 2h

- [ ] **Tests responsive**
  - Mobile, tablet, desktop
  - Cross-browser
  - Estimation: 3h

---

## Phase 2 : Features V2 - Core Business

### 1. Generateur de devis dynamique (P1)

- [ ] **Creer formulaire multi-etapes**
  - Etape 1: Type de VAE
  - Etape 2: Formule
  - Etape 3: Options
  - Etape 4: Modalites paiement
  - Etape 5: Recapitulatif
  - Estimation: 8h

- [ ] **Implementer logique calcul prix**
  - Prix de base par formule
  - Options a la carte
  - Remises/promotions
  - Estimation: 4h

- [ ] **Generer PDF devis**
  - Template professionnel
  - Logo et branding
  - Conditions generales
  - Estimation: 6h

- [ ] **Workflow devis**
  - Sauvegarde en DB
  - Envoi email automatique
  - Tracking statut (envoye/accepte/refuse)
  - Estimation: 5h

- [ ] **Dashboard gestion devis**
  - Liste devis pour admin
  - Filtres et recherche
  - Actions (relancer, archiver)
  - Estimation: 5h

**Total estimation Devis:** 28h

### 2. Authentification et compte client (P1)

- [ ] **Setup Supabase Auth**
  - Email/password
  - Magic link (optionnel)
  - Verification email
  - Estimation: 4h

- [ ] **Pages authentification**
  - Login
  - Register
  - Forgot password
  - Reset password
  - Estimation: 6h

- [ ] **Middleware protection routes**
  - Routes privees espace client
  - Routes admin
  - Estimation: 2h

- [ ] **Gestion profil utilisateur**
  - Modifier informations
  - Changer mot de passe
  - Estimation: 3h

**Total estimation Auth:** 15h

### 3. Espace client (P2)

- [ ] **Dashboard client**
  - Vue d'ensemble progression
  - Prochains rendez-vous
  - Notifications
  - Estimation: 8h

- [ ] **Gestion documents**
  - Upload fichiers (Supabase Storage)
  - Liste documents avec filtres
  - Versioning
  - Telechargement
  - Estimation: 10h

- [ ] **Systeme commentaires**
  - Fanny commente documents
  - Notifications email
  - Estimation: 5h

- [ ] **Tracking progression dossier**
  - Barre de progression
  - Etapes completees/a venir
  - Timeline
  - Estimation: 6h

- [ ] **Messagerie integree**
  - Chat asynchrone avec Fanny
  - Pieces jointes
  - Notifications
  - Estimation: 8h

**Total estimation Espace client:** 37h

### 4. Systeme de paiement (P2)

- [ ] **Integration Stripe**
  - Setup compte Stripe
  - API keys et webhooks
  - Estimation: 3h

- [ ] **Checkout paiement**
  - Page paiement securisee
  - CB, Apple Pay, Google Pay
  - Estimation: 5h

- [ ] **Paiements recurrents**
  - Paiement 3x sans frais
  - Abonnement mensuel
  - Estimation: 4h

- [ ] **Gestion factures**
  - Generation factures auto
  - Telechargement PDF
  - Historique paiements
  - Estimation: 5h

- [ ] **Webhooks Stripe**
  - Confirmation paiement
  - Gestion echecs
  - Remboursements
  - Estimation: 4h

- [ ] **Integration CPF**
  - Instructions MonCompteFormation
  - Paiement mixte (CPF + CB)
  - Estimation: 3h

**Total estimation Paiement:** 24h

### 5. Calendrier et rendez-vous (P3)

- [ ] **Integration Cal.com ou Calendly**
  - Embed widget
  - Synchronisation Google Calendar
  - Estimation: 4h

- [ ] **Gestion rendez-vous**
  - Liste rendez-vous client
  - Annulation/report
  - Rappels email automatiques
  - Estimation: 6h

- [ ] **Types de rendez-vous**
  - Diagnostic initial
  - Suivi regulier
  - Preparation oral
  - Estimation: 3h

**Total estimation Calendrier:** 13h

---

## Phase 3 : Features Avancees

### 6. Blog et ressources (P3)

- [ ] **Setup CMS**
  - MDX local ou Contentful
  - Categories et tags
  - Estimation: 4h

- [ ] **Pages blog**
  - Liste articles
  - Article individuel
  - Filtres par categorie
  - Estimation: 6h

- [ ] **SEO blog**
  - Meta tags dynamiques
  - Schema.org Article
  - Sitemap auto
  - Estimation: 3h

- [ ] **Partage social**
  - Boutons partage
  - Open Graph par article
  - Estimation: 2h

- [ ] **Bibliotheque ressources**
  - Guides telechargeable (gated)
  - Videos privees
  - Templates documents
  - Estimation: 6h

**Total estimation Blog:** 21h

### 7. Dashboard administrateur (P3)

- [ ] **Vue d'ensemble admin**
  - KPIs (clients actifs, CA, conversions)
  - Graphiques
  - Estimation: 8h

- [ ] **Gestion clients**
  - Liste complete clients
  - Recherche et filtres avances
  - Fiche client detaillee
  - Notes privees
  - Estimation: 10h

- [ ] **Validation documents**
  - Interface validation/commentaires
  - Upload ressources pour clients
  - Estimation: 6h

- [ ] **Calendrier global**
  - Vue tous rendez-vous
  - Disponibilites
  - Estimation: 5h

- [ ] **Analytics integres**
  - Trafic et sources
  - Taux conversion
  - ROI pub
  - Estimation: 6h

**Total estimation Admin:** 35h

---

## Phase 4 : Optimisations et polish

### Performance (P2)

- [ ] **Optimisation images Next.js**
  - Lazy loading
  - Placeholder blur
  - WebP/AVIF
  - Estimation: 3h

- [ ] **Code splitting**
  - Dynamic imports
  - Route-based splitting
  - Estimation: 2h

- [ ] **Caching strategies**
  - ISR (Incremental Static Regeneration)
  - API routes caching
  - Estimation: 3h

- [ ] **Monitoring performance**
  - Web Vitals
  - Sentry error tracking
  - Estimation: 2h

### Tests (P2)

- [ ] **Tests unitaires**
  - Utilitaires critiques
  - Vitest ou Jest
  - Estimation: 8h

- [ ] **Tests integration**
  - Formulaires
  - Authentification
  - Estimation: 6h

- [ ] **Tests E2E**
  - Parcours utilisateur complets
  - Playwright ou Cypress
  - Estimation: 10h

### Documentation (P3)

- [ ] **Documentation technique**
  - Architecture
  - API endpoints
  - Schema DB
  - Estimation: 4h

- [ ] **Guide utilisateur**
  - Espace client
  - FAQ
  - Estimation: 3h

---

## Phase 5 : Features futures (Backlog)

### Communaute (P4)

- [ ] **Forum prive**
  - Echanges entre candidates
  - Moderation Fanny
  - Estimation: 20h

- [ ] **Webinaires**
  - Streaming live
  - Rediffusions
  - Estimation: 15h

### Marketing (P4)

- [ ] **Email marketing**
  - Newsletter automatique
  - Sequences drip
  - Integration Mailchimp/Brevo
  - Estimation: 8h

- [ ] **Programme parrainage**
  - Code parrain
  - Reductions
  - Tracking
  - Estimation: 10h

- [ ] **Temoignages video**
  - Upload videos
  - Player integre
  - Estimation: 5h

### Avance (P5)

- [ ] **IA assistant VAE**
  - Chatbot aide redaction
  - Suggestions ameliorations
  - Estimation: 40h

- [ ] **Application mobile**
  - React Native
  - Notifications push
  - Estimation: 80h

---

## Estimations globales

### Quick Wins (Site actuel)
**Total: ~40h** (8-12h pour les P1 critiques)

### Migration Next.js + Features V2 Core
**Total: ~117h**
- Migration: 28h
- Devis: 28h
- Auth: 15h
- Espace client: 37h
- Paiement: 24h
- Calendrier: 13h

### Features Avancees
**Total: ~56h**
- Blog: 21h
- Dashboard admin: 35h

### Total general (Phases 0-3)
**~213h de developpement**

**Repartition par priorite:**
- P1 (Critique): ~80h
- P2 (Important): ~90h
- P3 (Souhaitable): ~43h

---

## Prochaines etapes

1. **Valider les priorites** avec le client
2. **Definir le budget** et timeline
3. **Demarrer Phase 0** (Quick Wins) pour resultats immediats
4. **Planifier Phase 1** (Migration) une fois budget valide
5. **Iterer progressivement** sur les phases suivantes

---

**Derniere mise a jour:** 2025-01-XX
**Maintenu par:** Equipe Ti'colibri
