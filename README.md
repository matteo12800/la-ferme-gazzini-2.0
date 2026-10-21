# La Ferme Gazzini

Quatre pages : `index.html`, `produits.html`, `galerie.html` et `contact.html`.
La présentation et l’histoire de la ferme se trouvent désormais sur l’accueil. Le bouton « Découvrir notre ferme » rejoint cette introduction. La page séparée `histoire.html` a été retirée.

## Voir le site

Ouvrir `index.html` ; conserver les quatre fichiers HTML dans le même dossier pour naviguer entre les rubriques. Les styles sont inclus dans chaque HTML pour permettre leur ouverture individuelle. `style.css` conserve une copie de référence : les pages ne le chargent pas.

Pour travailler avec un serveur local depuis ce dossier :

```sh
python3 -m http.server 3000 --bind 0.0.0.0
```

## Modifier l’accueil

Le texte provisoire est directement modifiable dans le paragraphe de `#notre-ferme` dans `index.html`.

Les quatre espaces photo sont intentionnellement vides : aucune image n’est fournie ou chargée. Pour ajouter plus tard vos photos, remplacer uniquement le contenu du bloc `.photo-slot` concerné par un élément `img` avec `src` et `alt`. Conserver le conteneur et ses classes : ils définissent la taille et les proportions. Le titre et le bouton sont dans un bloc indépendant sur fond uni et restent lisibles sans photo ou avec une photo.

Le site ne prend pas de commandes et n’envoie pas de messages. Les autres contenus restent à compléter.

## Présentation actuelle

L’accueil reprend la disposition de la capture de référence fournie : bandeau blanc, identité textuelle à gauche et navigation à droite, grande bannière pleine largeur avec titre en italique. Les photos restent absentes. Le menu est repliable sur mobile et reste affiché si JavaScript est désactivé. Le titre est foncé sur fond beige pour rester lisible sans photographie. Lors de l’ajout ultérieur d’une photo dans le bloc de bannière, un panneau uni est automatiquement placé derrière le texte pour préserver sa lisibilité.

## Introduction et rubriques d’accueil

Après la bannière, `#notre-ferme` contient l’introduction en trois paragraphes. Trois sections suivent : `#notre-histoire` (photo à gauche), Nos produits (photo à droite) et Galerie (photo à gauche). Les textes restent provisoires et sont modifiables directement dans `index.html`. L’histoire est présentée sur l’accueil ; son bouton mène au contact, sans recréer de page histoire. Les boutons produits et galerie ouvrent leurs pages respectives. Sur mobile, chaque emplacement photo précède son texte.

## Illustration de l’en-tête

`mouton_ferme_gazzini_optimise.jpg` provient du dépôt GitHub et est utilisé sans modification sur les quatre pages. Garder ce fichier à côté des HTML. Ses proportions d’origine (684 × 515) sont conservées par une largeur responsive et une hauteur automatique, sans recadrage. Le sous-titre est « Organic farming ». Cette illustration est distincte des zones photographiques, qui restent vides.

## Logo intégré aux pages

L’illustration originale est désormais encodée directement dans chaque fichier HTML pour être visible même si la page est téléchargée seule. Les octets JPEG sont identiques à ceux de l’original GitHub ; seul leur stockage dans le HTML change. Le fichier JPEG est conservé comme source. Les autres pages restent nécessaires pour les liens du menu.

## Nouveau logo PNG

Le logo actif est désormais `Crayon Sheep with Bees and Flowers.png`, récupéré depuis GitHub. Le PNG original (1446 × 1087, avec transparence) est intégré sans modification dans chaque HTML, en remplacement du JPEG précédent. Ses proportions et sa transparence sont préservées ; Organic farming reste sous le nom.

## Photo de la bannière

La photo authentique `ferme_gazzini_arc_en_ciel_optimise.jpg` récupérée sur GitHub est désormais intégrée directement dans l’accueil, derrière le titre. Son original est conservé. Un voile sombre assure la lisibilité du texte blanc. Les trois emplacements des sections restent vides.

## Page produits

La page produits comporte une bannière vide aux mêmes dimensions que l’accueil avec le titre « Les produits de la ferme », un espace de texte provisoire `.products-introduction`, puis six cartes Produit 1 à Produit 6. Trois colonnes sur ordinateur, deux sur tablette, une sur petit écran. La future photo de bannière se place dans `[data-photo="produits-banniere"]`. Aucun nouveau produit ni photo n’est inventé.

## Contact

La page reprend la capture fournie : coordonnées à gauche et formulaire sur fond beige à droite. Téléphones fournis : contact +41 76 718 85 08 ; commandes +41 76 75 74 129. Adresse confirmée : Route de Bossey 50, 1256 Troinex, Genève, Suisse. E-mail confirmé : la.ferme.gazzini@gmail.com. Le formulaire est connecté à FormSubmit (voir la procédure d’activation ci-dessous). Aucune newsletter ni fausse vérification anti-spam n’est ajoutée.

## Envoi du formulaire de contact

Le formulaire fait un POST HTTPS natif vers FormSubmit, à destination de `la.ferme.gazzini@gmail.com`. Aucun serveur ni mot de passe Gmail n’est nécessaire. FormSubmit traite les coordonnées et le message ; une indication figure sur le formulaire. Les champs sont obligatoires, l’e-mail est validé par le navigateur, un piège à robots est inclus et la protection anti-spam par défaut du service n’est pas désactivée.

**Activation indispensable :** au premier envoi réel, FormSubmit demande la confirmation de l’adresse destinataire par e-mail. Ouvrir le message de FormSubmit dans la boîte de la ferme (vérifier les indésirables) et confirmer. Après activation, effectuer un nouvel envoi réel pour vérifier la réception. L’ajout de l’action au HTML ne prouve pas l’activation ni la livraison des messages. Aucun envoi réel n’a été effectué pendant les tests.

Le formulaire nécessite Internet et fonctionne normalement depuis une page hébergée par HTTP(S). Pour tester, utiliser le serveur local ou le site publié, plutôt qu’un fichier ouvert en file://. Le service affiche sa propre confirmation et peut demander une vérification anti-spam. Si l’envoi échoue, les liens directs e-mail et téléphone restent accessibles.
