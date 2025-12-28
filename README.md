# 📊 Statistiques de Morts - Dofus Serveur Ombre

Interface web pour afficher le nombre de morts par classe avec les icônes officielles de Dofus.

## 🚀 Installation

1. **Extraire tous les fichiers** du package dans un même dossier
2. **Vérifier la structure** :
   ```
   dossier/
   ├── morts_par_classe.html
   ├── images/
   │   ├── Iop.webp
   │   ├── cra.webp
   │   ├── Eniripsa_Logo.webp
   │   └── ... (autres icônes)
   ├── README.md
   └── GUIDE_RAPIDE.txt
   ```
3. **Ouvrir** le fichier `morts_par_classe.html` dans votre navigateur web
4. C'est tout ! L'interface est prête à être utilisée

## 📖 Utilisation

### Pour OBS Studio / Streamlabs

1. Ouvrez OBS Studio ou Streamlabs
2. Ajoutez une nouvelle source **"Source navigateur"** (Browser Source)
3. Dans les paramètres :
   - **URL** : Sélectionnez le fichier `morts_par_classe.html` (chemin local)
   - **Largeur** : 1920px (ou selon vos besoins)
   - **Hauteur** : 1080px (ou selon vos besoins)
   - Cochez **"Actualiser le navigateur quand la scène devient active"**
4. Cliquez sur **OK**

### Modifier les statistiques

Pour mettre à jour le nombre de morts par classe, modifiez le fichier `morts_par_classe.html` :

1. Ouvrez le fichier avec un éditeur de texte (Notepad++, VS Code, etc.)
2. Cherchez la section JavaScript (vers la fin du fichier)
3. Trouvez la variable `deathsByClass` et modifiez les valeurs :

```javascript
const deathsByClass = {
    'iop': 5,        // Changez ces nombres
    'cra': 3,
    'eniripsa': 0,
    'ecaflip': 2,
    // ... etc
};
```

4. Sauvegardez le fichier
5. Dans OBS, actualisez la source navigateur (clic droit > Actualiser)

### Ajouter une mort rapidement

Vous pouvez aussi cliquer directement sur une carte de classe dans le navigateur pour ajouter une mort (fonctionne uniquement en local, pas dans OBS).

## 🎨 Personnalisation

### Changer les couleurs

Les couleurs peuvent être modifiées dans la section `<style>` du fichier HTML :
- Fond : `background: linear-gradient(...)`
- Couleur des têtes de mort : `color: #ff6b6b`
- Couleur du texte : `color: #ffd700`

### Ajuster la taille

Modifiez les valeurs dans le CSS :
- `.class-icon` : taille des icônes de classe
- `.death-skull` : taille des têtes de mort
- `.stats-grid` : espacement entre les cartes

## 📁 Structure des fichiers

```
Statistiques_Morts_Dofus_Ombre/
├── morts_par_classe.html    # Fichier principal de l'interface
├── images/                  # Dossier contenant les icônes
│   ├── Iop.webp
│   ├── cra.webp
│   ├── Eniripsa_Logo.webp
│   ├── Ecaflip_Logo.webp
│   ├── Enutrof_Logo.webp
│   ├── Sram_Logo.webp
│   ├── Xelor_Logo.webp
│   ├── Osamodas_Logo.webp
│   ├── Sacrieur_Logo.webp
│   ├── Pandawa_Logo.webp
│   ├── Roublard.webp
│   ├── Zobal.webp
│   ├── Steamer.webp
│   ├── Eliotrope_Logo.webp
│   ├── Huppermage.webp
│   ├── Ouginak.webp
│   ├── Forgelance.webp
│   ├── Feca.webp
│   └── Sadida_Logo.webp
├── README.md                # Documentation complète
└── GUIDE_RAPIDE.txt         # Guide rapide
```

## ⚙️ Fonctionnalités

- ✅ Affichage des icônes de classe officielles
- ✅ Compteur de morts avec têtes de mort (💀)
- ✅ Design moderne et responsive
- ✅ Animations au survol
- ✅ Total des morts en bas de page
- ✅ Compatible OBS Studio / Streamlabs

## 🐛 Dépannage

**Les icônes ne s'affichent pas ?**
- Vérifiez que le dossier `images/` existe et contient tous les fichiers `.webp`
- Vérifiez que la structure des dossiers est correcte (images/ à côté du HTML)
- Les emojis de secours s'afficheront automatiquement si les images ne se chargent pas

**L'interface ne se met pas à jour dans OBS ?**
- Clic droit sur la source > Actualiser
- Vérifiez que le chemin du fichier est correct

**Les têtes de mort ne s'affichent pas ?**
- Vérifiez que vous avez bien modifié les valeurs dans `deathsByClass`
- Actualisez la page dans votre navigateur

## 📝 Notes

- Les données sont stockées uniquement dans le fichier HTML (pas de base de données)
- Pour sauvegarder les statistiques, modifiez directement le fichier HTML
- Compatible avec tous les navigateurs modernes

## 🎮 Pour le streameur

Cette interface est prête à être utilisée en direct ! Vous pouvez :
- L'afficher en overlay pendant vos streams
- La mettre à jour manuellement entre les sessions
- La personnaliser selon vos préférences visuelles

Bon stream ! 🎬

