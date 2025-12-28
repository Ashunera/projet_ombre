# 📊 Version Compacte - Overlay Stream

Version optimisée pour être incrustée en overlay dans un stream (OBS Studio / Streamlabs).

## 🎯 Différences avec la version complète

- **Design compact** : Barre horizontale avec éléments plus petits
- **Fond transparent** : Parfait pour l'overlay
- **Noms abrégés** : Eni, Eca, Enu, etc. pour économiser l'espace
- **Icônes réduites** : 32x32px au lieu de 80x80px
- **Taille minimale** : Optimisé pour prendre le moins de place possible

## 🚀 Utilisation dans OBS Studio

1. **Ajouter une source "Source navigateur"** (Browser Source)
2. **Paramètres** :
   - **URL** : Sélectionner `morts_par_classe_compact.html`
   - **Largeur** : 1920px (ou selon vos besoins)
   - **Hauteur** : 100px (ou ajuster selon le nombre de lignes)
   - **Fond transparent** : ✅ Cocher cette option
   - **Actualiser le navigateur quand la scène devient active** : ✅ Cocher
3. **Positionner** : Placer l'overlay en haut ou en bas de l'écran selon vos préférences

## ✏️ Modifier les statistiques

Même principe que la version complète :

1. Ouvrir `morts_par_classe_compact.html` avec un éditeur de texte
2. Chercher `deathsByClass` (vers la fin du fichier)
3. Modifier les valeurs :

```javascript
const deathsByClass = {
    'iop': 5,      // Changez ces valeurs
    'cra': 3,
    'sram': 8,
    ...
};
```

4. Sauvegarder
5. Dans OBS : Clic droit sur la source > Actualiser

## 🎨 Personnalisation

### Ajuster la taille

Modifiez dans le CSS :
- `.class-icon` : `width: 32px; height: 32px;` (icônes)
- `.class-name` : `font-size: 11px;` (texte)
- `.skull` : `font-size: 14px;` (têtes de mort)
- `.stats-bar` : `gap: 8px;` (espacement entre éléments)

### Changer la position

Dans OBS, vous pouvez :
- Redimensionner la source
- La positionner où vous voulez (haut, bas, coin, etc.)
- Ajouter des filtres (ombre, contour, etc.)

## 💡 Astuces

- **Pour un overlay en haut** : Positionnez la source en haut de l'écran
- **Pour un overlay en bas** : Positionnez la source en bas de l'écran
- **Pour économiser l'espace** : Réduisez encore la taille des icônes (24px)
- **Pour masquer les classes à 0 mort** : Ajoutez un filtre CSS pour cacher les éléments avec 0 mort

## 📐 Dimensions recommandées

- **Largeur** : 1920px (plein écran) ou 1280px (centré)
- **Hauteur** : 60-100px selon le nombre de lignes
- **Position** : Haut ou bas de l'écran

## 🎬 Exemple d'utilisation

Parfait pour afficher les statistiques en continu pendant un stream, sans prendre trop de place à l'écran !

