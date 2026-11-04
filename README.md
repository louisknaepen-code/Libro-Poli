# Libro-Poli

Vidéo de présentation Instagram du roman *La Revolución Lufua: Siembra* de Felipe Pollitzer, réalisée avec [HyperFrames](https://github.com/heygen-com/hyperframes) (HTML rendu en vidéo).

- Format : post Instagram 4:5, 1080×1350, 30 i/s, 31,5 s, textes en espagnol.
- Style : celui du site du livre, avec un fond noir, un serif doré et la graine marbrée aux veines d'or.
- Scénarios proposés : [`STORYLINES.md`](STORYLINES.md).

## Contenu

- `index.html` : composition racine (31,5 s) et placement des bruitages.
- `compositions/relato.html` : de Teneritas jusqu'à « la revolución » (givre → veines d'or → route).
- `compositions/row.html` : la menace (Row).
- `compositions/libro.html` : la graine, la couverture, la citation et l'appel à l'achat.
- `SPEC.md` : cahier des charges plan par plan. `REVIEW.md` : relecture et limites connues.
- `out/trailer-siembra-post-4x5.mp4` : la vidéo à publier (post 4:5).
- `out/trailer-siembra-reel.mp4` : la première version au format Reel 9:16 (ancienne version du code, voir l'historique git).

## Retravailler

```bash
npx hyperframes preview      # aperçu et édition dans le navigateur
npx hyperframes check        # vérification
npx hyperframes render --output out/trailer-siembra-post-4x5.mp4
```

Les textes de la carte de fin (citation, bouton, compte) sont des variables modifiables dans l'aperçu.
