# Note de travail - Page d'accueil VoyageLibre

**Auteur :** Kaélé Bobée
**Technos :** HTML5, CSS3 (sans framework)

## Le projet

J'ai fait la page d'accueil d'un site de voyage. Le but n'était pas de faire des fonctions compliquées, mais de bien gérer le responsive : la page doit rester lisible et belle sur téléphone, tablette et ordinateur.

La page a plusieurs parties : un menu en haut, une grande image d'accueil (hero), une grille de destinations, une rangée qui défile sur le côté, une galerie de photos et un pied de page.

## Le responsive

J'ai travaillé en mobile-first : je fais d'abord le style pour les petits écrans, puis j'ajoute des règles pour les écrans plus grands avec les media queries.

J'ai utilisé 3 breakpoints :

- **480px** : mobile. Tout est sur une colonne, le menu se met à la verticale.
- **768px** : tablette. La grille passe à 2 colonnes, le menu et le footer se mettent en ligne.
- **1024px** : ordinateur. La grille passe à 3 colonnes avec un grand bloc principal.

## Grid et Flexbox

J'ai utilisé **Flexbox** pour aligner des éléments sur une ligne :

- le menu en haut
- les colonnes du footer
- la rangée qui défile horizontalement

J'ai utilisé **CSS Grid** pour les mises en page en 2 dimensions :

- la grille des destinations (6 blocs de tailles différentes)
- la galerie de photos

En gros : Flexbox pour aligner, Grid pour organiser en grille.

## Le scroll horizontal

La partie "Destinations populaires" est une rangée de cartes qu'on fait défiler vers la droite. J'ai utilisé `overflow-x: auto` pour le défilement et `scroll-snap` pour que ça s'arrête bien sur chaque carte.

## Les images

Les images viennent d'Unsplash (par lien direct). J'ai mis `max-width: 100%` et `object-fit: cover` pour qu'elles s'adaptent à leur cadre sans être déformées. Pour la grande image d'accueil j'ai utilisé `srcset` pour charger la bonne taille selon l'écran.

## Les tailles de texte

J'ai utilisé `clamp()` sur les titres pour que la taille s'adapte toute seule à la largeur de l'écran, sans devenir trop petite ou trop grande.

## Conclusion

La page coche toutes les cases demandées : une grille avec 6 blocs, du flexbox, plus de 10 images, des textes de longueurs variées, 3 breakpoints et un bloc qui défile à l'horizontale. Le tout en HTML et CSS, sans framework.
