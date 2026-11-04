# SPEC — Tráiler « La Revolución Lufua: Siembra »

GOAL:    Faire qu'un abonné Instagram veuille lire le livre : il suit la prémisse et retient la graine, le titre et « link en bio ».
OUTPUT:  HyperFrames, 1080×1350 (post Instagram 4:5), 30 fps. (v1 était un Reel 1080×1920.)
TIME:    44,5 s × 30 = 1335 frames (v3, plus lent : chaque ligne tient ≥ 0,5 s + 0,3 s par mot, ×1,3). Pas de musique dans le fichier ; la musique s'ajoute dans Instagram.
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

SHOTS (secondes, temps absolu, v3) :
  relato 0–23,5   (le décor de veines pousse lentement de 6 % sur toute la scène ; grain animé ; vignettage 50 % aux bords)
   0,0–4,2   « En la fría nación de / Teneritas » à l'écran dès le frame 0, givre déjà présent aux bords.
   3,95–8,6  « Una joven / recibirá / una misión » : mots de l'ombre à l'ivoire (140 ms d'écart), « misión » en or à 4,85.
   8,35–13,6 « para la que, lo sepa o no, / se ha estado / preparando / toda su vida. » : une ligne toutes les 0,5 s.
  13,25–14,45 Inondation : sol froid → chaud, givre → veines d'or.
  14,2–19,4  « Junto a compañeros… / emprenderá / el viaje por / todo el Forte » ; la route d'or se trace (14,7–18,9) ; la caméra glisse de 320 px.
  19,15–23,5 « a fin de lograr / la revolución (lettre par lettre, or) / que salve a la humanidad. » ; fouet de sortie à 23,26.
  row 23,5–31,5
  23,5–25,35 Fouet d'entrée : « Deberá apurarse. » sur les veines d'or encore vivantes.
  25,35–28,5 « Row » claque (×1,25 → 1) ; les veines s'éteignent de droite à gauche en 2,6 s, la chaleur quitte le cadre.
  28,45–31,5 « Lo que pase en el este / podría condenar / el destino / de todos. » puis tout s'éteint.
  libro 31,5–44,5
  31,5–32,3  Noir, montée.
  32,3–34,4  La graine surgit en tournant légèrement (−5° → 0), la lumière la balaie ; impact.
  34,4–35,9  Elle prend sa place sur la couverture ; le titre se construit (« Siembra » lettre par lettre).
  36,5–38,5  Le cadre se trace, « Felipe Pollitzer » signe : la couverture entière tient ~1 s.
  38,5–39,45 La couverture glisse à gauche (×0,58).
  39,1–44,5  « Novela / Primer libro de la trilogía », la citation, « Comprar el libro », « Link en bio / @felipe.pollitzer ». Tenu ≥ 3,5 s.

SOUND:   whoosh-short au fouet (23,5) ; impact-bass-2 sur « Row » (25,35) ; riser vers impact-bass-1 sur la graine (32,3) ;
         whoosh-cinematic sur le déplacement de la couverture (38,95). Rien d'autre. La musique s'ajoute dans Instagram.

SAFE:    Post 4:5 : tout le texte dans la zone titre 80 % (x 108–972, y 135–1215).

BANNED:  vide sombre avec petits éléments flottants ; particules décoratives ; halos néon ; tout centré ; chaque ligne qui fond et glisse vers le haut ;
         titres qui dérivent après s'être posés ; trois cartes ; logo docké ; mots inventés hors du site
         (seuls « Link en bio » et « Lo que pase en el este » sont condensés du site / de la bio).

QA:      frames 0 ; 4,5 ; 8,5 ; 10,0 (inondation) ; 12,5 ; 15,5 ; 17,0 ; 18,5 ; 21,5 ; 23,3 ; 25,8 ; 27,0 ; 27,7 ; 30,5.
         Chaque frame : texte lisible ≥ 28 px, dans la zone sûre, un seul accent or.
