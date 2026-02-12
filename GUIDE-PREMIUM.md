# 🚀 Meuz'MUN PREMIUM - Guide des fonctionnalités

## ✨ Nouveautés ULTRA-MODERNES

### 🎨 Design Premium
- ✅ Hero avec gradient animé fluide (15s de boucle)
- ✅ Particules interactives (50 particules qui réagissent à la souris)
- ✅ Curseur personnalisé avec traînée
- ✅ Glassmorphism (effet verre dépoli) sur toutes les cartes
- ✅ Cards 3D qui se retournent au hover (flip effect)
- ✅ Timeline interactive avec effet glassmorphism
- ✅ Animations au scroll (révélation progressive)
- ✅ Orbes flottantes animées en arrière-plan

### 🎯 Effets interactifs

#### Curseur custom
- Le curseur principal suit la souris avec un léger délai
- Un deuxième curseur suit avec plus de retard (effet de traînée)
- S'agrandit au hover des éléments interactifs

#### Particules
- 50 particules dorées qui flottent
- S'éloignent de votre curseur quand vous approchez
- Se connectent entre elles avec des lignes bleues

#### Cards flip 3D
- Passez la souris sur une carte → elle se retourne en 3D
- Face avant : Titre + icône
- Face arrière : Description détaillée

### 📱 Sur mobile
- Curseur custom désactivé (pas pratique sur tactile)
- Cards flip par tap
- Timeline verticale adaptée
- Navigation hamburger fluide

## 🎨 Personnalisation

### Changer les couleurs du gradient animé
Dans `style.css`, ligne ~100 :
```css
background: linear-gradient(-45deg, #0066cc, #0a1628, #4169e1, #00a8ff);
```
Remplacez les couleurs par les vôtres !

### Modifier la vitesse d'animation du gradient
Ligne ~102 :
```css
animation: gradientShift 15s ease infinite;
```
Changez `15s` (15 secondes) par la durée voulue.

### Ajuster le nombre de particules
Dans `script.js`, ligne ~42 :
```javascript
const particleCount = 50;
```
Plus = plus beau mais plus lourd. 30-80 recommandé.

### Ajouter une vraie vidéo
Remplacez la section hero dans index.html :
```html
<section class="hero">
    <video autoplay muted loop playsinline style="position: absolute; width: 100%; height: 100%; object-fit: cover; z-index: 0;">
        <source src="votre-video.mp4" type="video/mp4">
    </video>
    <div class="hero-content">
        <!-- contenu -->
    </div>
</section>
```

## 🚀 Performance

### Le site est optimisé mais...
- Les particules utilisent requestAnimationFrame (60 FPS fluide)
- Le curseur custom aussi
- Glassmorphism nécessite backdrop-filter (supporté sur navigateurs modernes)
- Les animations CSS sont hardware-accelerated

### Pour un site encore plus rapide
1. Réduisez le nombre de particules (ligne 42 du script.js)
2. Désactivez le curseur custom sur mobile (déjà fait)
3. Utilisez des images optimisées (WebP recommended)

## 📸 Où ajouter vos photos

### Hero avec photo de fond
```html
<section class="hero" style="background-image: linear-gradient(rgba(0, 0, 0, 0.4), rgba(0, 0, 0, 0.4)), url('votre-photo.jpg'); background-size: cover;">
```

### Cards avec photo
```css
.event-card-front {
    background-image: linear-gradient(rgba(0, 102, 204, 0.9), rgba(0, 102, 204, 0.9)), url('photo.jpg');
    background-size: cover;
}
```

### Timeline avec photos
Ajoutez dans chaque `.timeline-content` :
```css
background-image: url('photo.jpg');
background-size: cover;
background-position: center;
```

## 🎯 Prochaines améliorations possibles

1. **Smooth scroll custom** (pas juste CSS)
2. **Loader animé** au chargement
3. **Page transitions** entre les pages
4. **Audio ambiance** (musique de fond désactivable)
5. **Mode sombre/clair** toggle
6. **Animations GSAP** pour encore plus de fluidité

## 💡 Astuces

### Tester en local
Ouvrez `index.html` dans votre navigateur. Pour les particules, vous devez être sur un serveur (Live Server dans VS Code).

### Désactiver temporairement le curseur custom
Dans `script.js`, commentez les lignes 1-30.

### Changer la police
Remplacez `Montserrat` et `Inter` par vos polices dans :
1. L'import Google Fonts (ligne 1 du CSS)
2. Les font-family dans le CSS

---

## 🔥 Résultat attendu

Votre site devrait maintenant ressembler à :
- Stripe (gradients fluides)
- Apple (minimalisme et glassmorphism)  
- Awwwards (créativité et interactions)

Un site **PREMIUM** digne des plus grandes marques ! 🚀