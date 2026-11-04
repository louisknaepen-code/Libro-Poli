# SPEC — Tráiler « La Revolución Lufua: Siembra »

GOAL:    Faire qu'un abonné Instagram veuille lire le livre : il suit la prémisse et retient la graine, le titre et « link en bio ».
OUTPUT:  HyperFrames, 1080×1920 (Reel 9:16), 30 fps.
TIME:    31,5 s × 30 = 945 frames. Pas de musique dans le fichier (aucune source accessible) : la musique s'ajoute dans Instagram, et le fichier porte les bruitages.

LOOK:    Le site du livre, en matière et non en vide.
         - Sol : noir chaud #0b0906, avec un halo radial #2a1d0c à 35 % au centre (comme le site) et 3 % de grain fixe.
         - Monde de Teneritas : sol #070b10, encre givre #dfe9f0.
         - Encre de lecture : ivoire #efe6d4. Phrase discrète : ivoire à 72 %.
         - Accent or : dégradé #f3d58a → #c8923a → #9a6a24. Un seul mot ou objet en or par plan.
         - Police d'affichage : Cormorant Garamond 600. Lignes fortes en 132 px (interligne 1,0, approche -0,01em) ; mot héros de 200 à 260 px.
           Phrase discrète : Cormorant Garamond 500 italique, 58 px.
         - Matière : des veines. Le givre de Teneritas pousse en branches de 1 à 2,5 px. Au moment de la « misión », il devient or :
           ce sont les veines de la graine, puis la route du voyage. La graine (asset réel) porte les mêmes veines.
         - Lumière : le seul éclat est le filet doré du cadre de couverture, avec 4 points scintillants, comme sur le vrai livre.

OBJECTS: - La graine : `assets/img/semilla.png`, détourée depuis le site. Elle occupe 70 % de la largeur à son apparition.
         - La couverture : reconstruite à l'identique (double filet or, titre, séparateur à point, graine, nom de l'auteur).
           À remplacer par le fichier original dès qu'on l'a (variable `cover`).
         - Le bouton « Comprar el libro » : or #e2a84b, texte #1a1208, rayon 10 px, comme sur le site.

MOTION:  - Arrivée : expo.out ou power4.out, 0,5–0,9 s. Sortie : flou 8 px + opacité, 0,2 s, mot par mot, avec 40 ms de décalage.
         - Caméra et inondation de couleur : power2.inOut. Fouet : 0,2 s, flou horizontal 24 → 0.
         - Mots : 70–100 ms de décalage ; lettres : 1 frame (33 ms).
         - Un titre posé ne bouge plus.

SHOTS (secondes, temps absolu) :
  relato 0–16,5
   0,0–3,0   Le frame 0 montre déjà « En la fría nación de / Teneritas ». Le givre pousse depuis les bords.
             « Teneritas » 250 px en givre. Lecture en bas à gauche (y 1000–1300).
   3,0–6,3   « Una joven / recibirá / una misión » : chaque mot passe du gris à l'ivoire, 90 ms d'écart. « misión » en or : premier objet chaud.
   6,3–9,9   « Para la que, lo sepa o no, / se ha estado / preparando / toda su vida. » : lignes floutées puis nettes, centrées verticalement.
   9,6–10,4  Inondation : le sol passe du froid au chaud et le givre vire à l'or (les veines).
  10,2–13,8  « Junto a compañeros de tierras vecinas, / emprenderá / el viaje por / todo el Forte » :
             une veine-route dorée se dessine de gauche à droite, la caméra glisse de 320 px.
  13,9–16,5  « A fin de lograr / la revolución / que salve a la humanidad. » : « revolución » lettre par lettre, en or.
  row 16,5–22,3
  16,5–17,7  Fouet d'entrée : « Deberá apurarse. »
  17,7–20,2  « Row » à 420 px qui claque (échelle 1,25 → 1, 0,22 s expo.out), sous-ligne « tiene intereses distintos de los suyos. »
  20,2–22,3  « Lo que pase en el este / podría condenar / el destino de todos. » puis flou vers le noir.
  libro 22,3–31,5
  22,3–23,0  Noir et montée (riser).
  23,0–24,4  La graine surgit, la lumière la balaie, impact. 760 px de large.
  24,2–26,2  Le titre se construit au-dessus : « La Revolución / Lufua: » + séparateur + « Siembra » lettre par lettre.
  26,0–27,2  Le double filet se trace autour et « Felipe Pollitzer » apparaît : c'est la couverture.
  27,2–28,2  La couverture glisse et rapetisse (×0,62) vers le haut. « Novela · Primer libro de la trilogía » au-dessus.
  28,0–31,5  « Aquí soy semilla, árbol y fruto. », puis le bouton « Comprar el libro », puis « Link en bio · @felipe.pollitzer ».
             Tenu au moins 2,5 s.

SOUND:   whoosh-short au fouet (16,5) ; impact-bass-2 sur « Row » (17,7) ; riser de 22,3 vers impact-bass-1 sur la graine (23,0) ;
         whoosh-cinematic sur le déplacement de la couverture (27,2). Rien d'autre. La musique s'ajoute dans Instagram.

SAFE:    Rien sous y 168 ; tout le texte entre y 168 et 1330 ; x entre 108 et 940 (rail d'actions à droite).

BANNED:  vide sombre avec petits éléments flottants ; particules décoratives ; halos néon ; tout centré ; chaque ligne qui fond et glisse vers le haut ;
         titres qui dérivent après s'être posés ; trois cartes ; logo docké ; mots inventés hors du site
         (seuls « Link en bio » et « Lo que pase en el este » sont condensés du site / de la bio).

QA:      frames 0 ; 4,5 ; 8,5 ; 10,0 (inondation) ; 12,5 ; 15,5 ; 17,0 ; 18,5 ; 21,5 ; 23,3 ; 25,8 ; 27,0 ; 27,7 ; 30,5.
         Chaque frame : texte lisible ≥ 28 px, dans la zone sûre, un seul accent or.
