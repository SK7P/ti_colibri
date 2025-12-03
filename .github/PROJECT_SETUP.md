# Configuration du projet GitHub

Guide pour creer et configurer le projet GitHub avec kanban.

## Etape 1 : Creer le projet GitHub

1. Aller sur votre repo GitHub : https://github.com/SK7P/ti_colibri
2. Cliquer sur l'onglet **Projects**
3. Cliquer sur **New project**
4. Choisir **Board** (vue kanban)
5. Nommer le projet : **Ti'colibri - Roadmap**
6. Cliquer sur **Create**

## Etape 2 : Configurer les colonnes

Le projet GitHub cree automatiquement 3 colonnes. Modifiez-les ainsi :

### Colonnes suggerees :

1. **Backlog** - Issues en attente de priorisation
2. **Quick Wins** - Ameliorations immediates (site actuel)
3. **A faire** - Issues priorisees, pret a demarrer
4. **En cours** - Travail en cours
5. **A tester** - Termine, en attente de test
6. **Termine** - Complete et valide

### Pour ajouter/modifier les colonnes :

1. Cliquer sur **...** en haut de chaque colonne
2. **Rename** pour renommer
3. Cliquer sur **+ Add column** pour ajouter

## Etape 3 : Creer les labels

Les labels sont dans le fichier `.github/labels.json`. Pour les creer :

### Option A : Manuellement
1. Aller sur **Issues** > **Labels**
2. Cliquer sur **New label**
3. Creer chaque label du fichier labels.json

### Option B : Avec CLI GitHub (si compte connecte)
```bash
gh label create quick-win --color 10B981 --description "Amelioration immediate"
gh label create v2 --color 8B5CF6 --description "Feature pour Next.js"
# ... etc pour tous les labels
```

## Etape 4 : Creer les issues depuis ROADMAP.md

Pour chaque tache du fichier `ROADMAP.md` :

1. Aller sur **Issues** > **New issue**
2. Choisir le template approprie :
   - **Quick Win** pour Phase 0
   - **Feature V2** pour Phases 1-5
   - **Bug Report** pour les bugs
3. Remplir les informations
4. Ajouter les labels appropries (priorite, type, etc.)
5. Assigner a vous-meme si vous travaillez dessus
6. Creer l'issue

### Exemple : Issue "Optimiser Tailwind CSS"

**Template:** Quick Win
**Titre:** [QUICK WIN] Optimiser Tailwind CSS
**Labels:** `quick-win`, `performance`, `p1-critical`
**Description:**
```
Remplacer le CDN Tailwind (3MB) par un fichier compile (~15KB).

**Impact attendu:**
- Gain de 2.9MB sur le poids de la page
- +40 points sur score Lighthouse
- Temps de chargement reduit

**Estimation:**
- Temps: 2 heures
- Priorite: Haute (P1)

**Checklist:**
- [ ] Installer Tailwind CLI
- [ ] Extraire classes utilisees
- [ ] Compiler fichier CSS
- [ ] Remplacer CDN par fichier local
- [ ] Tester en local
- [ ] Deployer sur Netlify
- [ ] Verifier score Lighthouse
```

## Etape 5 : Lier les issues au projet

1. Ouvrir chaque issue creee
2. Dans la barre laterale droite, chercher **Projects**
3. Selectionner **Ti'colibri - Roadmap**
4. Choisir la colonne appropriee :
   - **Backlog** pour P4-P5
   - **Quick Wins** pour Phase 0
   - **A faire** pour les taches priorisees

## Etape 6 : Utiliser le kanban

### Workflow suggere :

1. **Backlog** : Toutes les nouvelles issues arrivent ici
2. **Quick Wins** : Issues Phase 0 (ameliorations site actuel)
3. **A faire** : Issues priorisees pour le sprint en cours
4. **En cours** : Issues sur lesquelles vous travaillez actuellement (max 2-3)
5. **A tester** : Issues completees, en attente de validation
6. **Termine** : Issues validees et deployees

### Deplacer les cartes :

- Drag & drop entre colonnes
- Ou cliquer sur la carte > **Move to** > choisir colonne

### Automatisations GitHub :

GitHub peut automatiquement deplacer les cartes :
- Issue assignee → passe en "A faire"
- Pull request creee → passe en "En cours"
- Pull request mergee → passe en "A tester"
- Issue fermee → passe en "Termine"

Pour activer : **Project Settings** > **Workflows** > activer les automatisations

## Etape 7 : Organisation par milestones (optionnel)

Pour mieux organiser les phases :

1. Aller sur **Issues** > **Milestones**
2. Creer des milestones :
   - **Phase 0 - Quick Wins** (date: dans 2 semaines)
   - **Phase 1 - Migration Next.js** (date: dans 2 mois)
   - **Phase 2 - Features V2** (date: dans 4 mois)
   - etc.

3. Assigner chaque issue a un milestone

Cela permet de :
- Voir progression par phase
- Estimer date de completion
- Prioriser les phases

## Etape 8 : Vues personnalisees (optionnel)

GitHub Projects permet de creer des vues personnalisees :

### Vue par priorite :
1. Dans le projet, cliquer sur **+ New view**
2. Choisir **Table**
3. Nommer : **Par priorite**
4. Grouper par : **Labels** > `p1-critical`, `p2-high`, etc.

### Vue par phase :
1. Creer une nouvelle vue **Table**
2. Nommer : **Par phase**
3. Grouper par : **Milestone**

### Vue timeline :
1. Creer une nouvelle vue **Roadmap**
2. Permet de voir les issues sur une timeline

## Commandes utiles (si gh CLI configuree)

```bash
# Lister les projets
gh project list --owner SK7P

# Creer une issue
gh issue create --title "Titre" --body "Description" --label "quick-win,p1-critical"

# Lister les issues
gh issue list

# Voir une issue
gh issue view 123

# Fermer une issue
gh issue close 123

# Lier une issue au projet
gh project item-add <PROJECT_NUMBER> --owner SK7P --url https://github.com/SK7P/ti_colibri/issues/123
```

## Ressources

- [Documentation GitHub Projects](https://docs.github.com/en/issues/planning-and-tracking-with-projects)
- [Guide Kanban sur GitHub](https://docs.github.com/en/issues/planning-and-tracking-with-projects/customizing-views-in-your-project/changing-the-layout-of-a-view#about-the-board-layout)

---

**Astuce :** Commencez par creer quelques issues de la Phase 0 (Quick Wins) pour tester le workflow avant de tout creer.
