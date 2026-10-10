REFONTE DE « LA MAISON EN QUELQUES CHIFFRES », MÉLANGE DES PARFUMS ET PAGE PANIER (Dar Safia, Next.js App Router, TypeScript, dossier dar-safiyapromax)

RÔLE
Agis comme un UI/UX designer senior spécialisé luxe e-commerce et comme un développeur front-end senior en animation. Objectif : un site cohérent avec l'identité Dar Safia (maison de parfums de niche : fond brun très sombre, crème, or #C9A24B, titres en serif Cormorant Garamond, labels en capitales espacées, monogramme DP doré entrelacé). Chaque élément doit être élégant, animé avec retenue et réagir au survol.

RÈGLES GÉNÉRALES
- Ne supprime, n'écrase et ne renomme aucun fichier existant. Ne déplace rien dans public/img/ ni dans perfumes/. Crée uniquement de nouveaux fichiers.
- Ne modifie pas le quiz (/trouver), le carrousel « Les signatures », la vidéo du teaser, la fiche produit, le curseur, ni les prix existants.
- Langue : la page en /fr reste en français, la page en /en reste en anglais. Tout nouveau libellé (panier, boutons, états vides) doit exister en FR et EN, via le système de traduction du projet.
- Prix au format DZD (ex. DZD 25,500), jamais DA.
- Git non destructif : pas de reset --hard, git clean, git checkout ., git restore ., git stash drop, git push --force.
- Avant chaque tâche : git branch backup-avant-<nom-de-la-tâche>.
- Ne push pas pendant le travail. Un seul push, à la fin, après validation sur localhost.
- Animer uniquement transform et opacity. will-change seulement pendant l'animation. prefers-reduced-motion : réduire ou couper les animations, garder les états finaux visibles.
- Tout ce qui lit window, localStorage ou Math.random se fait dans un useEffect (pas d'erreur d'hydratation).

═══════════════════════════════════════════════
TÂCHE A : « LA MAISON EN QUELQUES CHIFFRES » (accueil /[locale] et /[locale]/la-maison)
═══════════════════════════════════════════════

CONSTAT
La section actuelle est sur fond crème clair, avec trois lignes fines et trois grands chiffres (45, 21, 58) et leurs libellés. Elle est plate et ne ressemble pas au reste du site, qui est sombre.

DIAGNOSTIC (lecture seule)
1) Trouve le composant de la section (ex. HouseStats.tsx ou équivalent) et ses styles. Indique fichier et lignes.
2) Vérifie d'où viennent les chiffres : en dur ou calculés depuis le catalogue (nombre de parfums, de maisons, de wilayas). Si ce sont des valeurs en dur, calcule-les depuis catalog-data.js lorsque c'est possible (ex. nombre de produits = 45), sans changer les libellés.

CONTENU (inchangé)
Titre « La maison en quelques chiffres », libellés « créations au catalogue », « maisons représentées », « wilayas livrées », note « Chiffres du catalogue actuel. ». Ne rien reformuler.

DESIGN ET ARRIÈRE-PLAN
1) Fond sombre de la marque, en harmonie avec le site : dégradé brun très sombre (de #1a100e vers #2a1612), halo radial doré très doux derrière le chiffre central (opacité 0,12 à 0,18), grain SVG feTurbulence très léger (opacité 0,03) pour éviter les bandes.
2) Monogramme DP doré entrelacé (public/img/logo/logo-dr/Monogramme DP doré entrelacé.png) en filigrane géant à droite, opacité 0,06 à 0,08, sans mask ni filter, qui dérive très lentement (translate3d, 30 s, alternate). Il ne doit jamais masquer le texte.
3) Texte crème pour les titres, or pour les libellés, chiffres en Cormorant Garamond très grands (clamp(72px, 9vw, 140px)).
4) Séparateurs : remplacer les lignes plates par un filet doré qui se dessine de gauche à droite (scaleX 0 → 1, 1,2 s) au défilement.

ANIMATIONS (IntersectionObserver, une seule fois)
1) Les trois colonnes apparaissent en décalage de 150 ms, fondu + translateY de 24 px, 800 ms, cubic-bezier(0.22, 1, 0.36, 1).
2) Les chiffres font un compteur ascendant de 0 à leur valeur en 1,6 s (easing sortie), déclenché à l'apparition.
3) Le titre se révèle mot par mot (masque overflow hidden, chaque mot monte de 100 %).

HOVER
1) Au survol d'une colonne : le chiffre passe en or, se soulève de 4 px, et un halo doré très doux apparaît derrière (box-shadow ou radial-gradient en pseudo-élément, sans filter animé).
2) Le filet doré au-dessus de la colonne s'élargit (scaleX 1 → 1,04) et prend une teinte plus vive.
3) Tactile : pas de translation au survol, seulement un état actif léger.

RESPONSIVE
- Desktop : trois colonnes égales. Tablette et mobile : colonnes empilées, centrées, espacement cohérent.

VÉRIFICATIONS A
- /fr et /fr/la-maison : section sombre, monogramme en filigrane, compteurs animés, survol fonctionnel.
- /en et /en/la-maison : libellés anglais inchangés.
- 375 px, 768 px, 1440 px, 1920 px. Aucun scroll horizontal, aucun texte coupé.

COMMIT A : "style: house stats section redesign with brand background and motion".

═══════════════════════════════════════════════
TÂCHE B : MÉLANGE DES PARFUMS SUR /[locale]/parfums
═══════════════════════════════════════════════

OBJECTIF
Les cartes de la liste des parfums (45 créations) doivent s'afficher dans un ordre mélangé à chaque visite. Le mélange doit être fait côté client, pour éviter une erreur d'hydratation.

DIAGNOSTIC (lecture seule)
1) Trouve la page /parfums, le composant de liste et l'ordre actuel (tri, filtres, pagination éventuelle).
2) Vérifie que les filtres (genre, famille olfactive, notes, intensité, saison) fonctionnent avec un tableau mélangé. Le mélange ne doit rien casser des filtres.

IMPLÉMENTATION
1) Ajoute une fonction de mélange (Fisher-Yates) appliquée à la liste filtrée, exécutée dans un useEffect au montage : le rendu serveur reste la liste d'origine, puis la liste mélangée s'affiche au montage. Pas de Math.random dans le rendu.
2) Lors d'un changement de filtre, la liste reste mélangée (pas de retour à l'ordre initial).
3) Bouton « Mélanger » (ou icône avec aria-label équivalent en FR et EN) : relance le mélange avec une animation de réorganisation (FLIP : les cartes glissent à leur nouvelle place en 500 ms). Libellé à valider avec moi si tu veux un libellé différent.
4) Le mélange ne modifie aucune donnée, uniquement l'ordre d'affichage.

ANIMATIONS ET HOVER DES CARTES
1) Apparition en cascade au montage et après mélange : fondu + translateY de 20 px, décalage de 40 ms entre cartes, 600 ms.
2) Survol d'une carte : soulèvement de 6 px, bordure dorée pleine, halo doré très léger, légère inclinaison 3D (max 3°) sur desktop uniquement.
3) Le monogramme ou la photo de la carte zoome légèrement (1,04) au survol, dans un cadre overflow hidden.
4) Tactile et reduced-motion : pas d'inclinaison, apparition simple.

VÉRIFICATIONS B
- /fr/parfums et /en/parfums : l'ordre change à chaque rechargement, les 45 cartes restent présentes, les filtres fonctionnent.
- Aucune erreur d'hydratation, badge « 1 Issue » absent.
- 375 px : grille propre, pas de scroll horizontal.

COMMIT B : "feat: shuffle perfume list with FLIP reorder and card motion".

═══════════════════════════════════════════════
TÂCHE C : PAGE PANIER MODERNE (/[locale]/panier)
═══════════════════════════════════════════════

OBJECTIF
Remplacer le panier actuel (icône en haut à droite de la navbar, badge « 2 ») par une page dédiée /[locale]/panier. Un clic sur l'icône ouvre cette page. Chaque ligne affiche la photo du parfum.

DIAGNOSTIC (lecture seule)
1) Trouve la logique du panier actuelle : contexte, store, localStorage, ou état. Indique où sont stockés les articles, la quantité et le total. Ne change pas cette logique de stockage.
2) Trouve le composant du bouton panier dans le header et ce qu'il fait aujourd'hui (drawer, lien, rien).
3) Trouve le formulaire de commande existant (« Vos informations », « Livraison ») pour que le bouton « Commander » du panier y mène.
4) Pour chaque produit du panier, vérifie le champ image (chemin dans public/img/perfumes/ ou équivalent). Si un produit n'a pas de photo, affiche le monogramme DP doré comme fallback.

STRUCTURE DE LA PAGE
1) Route : src/app/[locale]/panier/page.tsx. L'icône panier du header pointe vers /<locale>/panier (lien, pas de drawer).
2) En-tête : titre « Votre panier » (FR) / « Your cart » (EN), avec le compte d'articles, et un fil d'Ariane (Accueil › Parfums › Panier).
3) Layout en deux colonnes sur desktop : à gauche la liste des articles, à droite un récapitulatif sticky (sous-total, livraison si elle existe dans les données, total, bouton « Commander », lien « Continuer mes achats »). Sur mobile, le récapitulatif passe sous la liste.
4) Ligne d'article : photo du parfum dans un cadre arrondi (ratio 3:4, object-fit: contain sur fond sombre, aucune déformation), marque en or, nom, contenance, famille, prix unitaire en DZD, sélecteur de quantité (− / +), prix de la ligne, bouton de suppression (icône avec aria-label).
5) Quantité et suppression : mettre à jour la logique existante, sans changer la façon de stocker les articles.
6) Total : nombre d'articles et montant en DZD, recalculés automatiquement. Quand le total change, le nombre se met à jour avec une courte animation (translateY + fondu, 300 ms).
7) État vide : monogramme DP doré, message et bouton « Découvrir les parfums ». Libellés FR et EN.
8) Bouton « Commander » : doré plein, reflet qui balaie de gauche à droite au survol. Bouton secondaire « Continuer mes achats » en contour.

ANIMATIONS ET HOVER
1) Entrée de la page : titre révélé mot par mot, lignes d'article en cascade (80 ms entre lignes, fondu + translateY 16 px, 650 ms), récapitulatif qui glisse depuis la droite (24 px).
2) Ligne au survol : bordure dorée, fond très légèrement éclairci, photo qui zoome à 1,04, léger soulèvement de 3 px.
3) Boutons + et − : scale 0.92 au clic puis retour. Survol : bordure dorée.
4) Suppression : l'article sort en fondu et se referme vers le haut (hauteur qui se rétracte, 350 ms), avant de disparaître de la liste.
5) Badge du panier dans le header : petit rebond lors d'un ajout ou d'une suppression.

BRANDING
1) Fond : même fond sombre que la home, avec halo doré très doux et filigrane du monogramme DP en bas à droite (opacité 0,05).
2) Séparateurs dorés fins entre les lignes d'article.
3) Typographie : titres en Cormorant Garamond, prix et libellés dans la police du site.

VÉRIFICATIONS C
- Ajouter deux parfums depuis /parfums : la page panier affiche leurs photos, noms, contenances, prix DZD et quantités corrects.
- Modifier la quantité, supprimer un article, vider le panier : le total et le badge se mettent à jour.
- Panier vide : état vide correct.
- Icône panier du header : ouvre /panier, pas de drawer.
- Bouton « Commander » : mène au formulaire de commande existant.
- /fr/panier et /en/panier : libellés corrects dans chaque langue.
- 375 px, 768 px, 1440 px : pas de scroll horizontal, récapitulatif accessible sous la liste sur mobile.
- Aucune erreur console, npx tsc --noEmit passe.

COMMIT C : "feat: modern cart page with product images and motion".

═══════════════════════════════════════════════
FIN : VALIDATION ET PUSH
═══════════════════════════════════════════════
1) Vérifie les trois tâches sur localhost : /fr, /fr/la-maison, /fr/parfums, /fr/panier, /en/panier, mobile 375 px.
2) Vérifie qu'aucune erreur console ni badge « 1 Issue » ne reste (sinon lire le message exact et corriger sa cause).
3) Attends ma validation, puis git push origin <branche courante>.
4) Résumé : chemin du projet utilisé, fichiers créés et modifiés par tâche (chemins), hash des trois commits, liste des animations avec leurs durées, nouveaux libellés ajoutés (FR et EN), et confirmation qu'aucun prix, aucune donnée produit et aucun fichier n'ont été modifiés ou supprimés.
