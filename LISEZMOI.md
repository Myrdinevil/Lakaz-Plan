# Lakaz Plan : relevé de bâtiments avant rénovation

Application pour dresser le plan coté d'une maison ou d'un appartement existant, relever les désordres (fissures, béton éclaté, humidité, termites…) avec photos et sortir les métrés pour chiffrer les travaux. Pensée pour des utilisateurs non spécialistes, sur le terrain aux Seychelles.

## Installer

Il n'y a rien à installer. Le dossier contient une seule page : `index.html`.

- **Sur ordinateur (Windows, Mac)** : double-cliquez sur `index.html`. Elle s'ouvre dans Chrome, Edge, Firefox ou Safari et fonctionne sans internet.
- **Sur iPhone ou Android** : un téléphone ne sait pas ouvrir une page enregistrée dans ses fichiers. Il faut la mettre en ligne une fois (voir plus bas), l'ouvrir dans Safari puis faire *Partager › Sur l'écran d'accueil*. Elle se lance ensuite comme une application et fonctionne hors ligne.

### Mettre l'application en ligne (pour les téléphones)

Déposez le dossier `Lakaz-Plan` complet (`index.html`, `sw.js`, `manifest.webmanifest`, `icon.svg`) sur n'importe quel hébergement de pages statiques en HTTPS : GitHub Pages, Netlify ou le serveur de votre organisation. Les fichiers `sw.js` et `manifest.webmanifest` ne servent qu'à ça : garder l'application dans le téléphone pour l'utiliser hors ligne.

Seule la page est hébergée. Les relevés restent dans chaque téléphone et ne passent jamais par ce serveur.

## Utiliser

1. **Ébauche** : ajoutez les pièces (bouton ➕), ou importez un croquis en fond (🖼️) et tracez dessus (✏️), ou faites lire le croquis par l'IA (✨).
2. **Mesures** : pour chaque pièce, mesurez les murs et les diagonales au télémètre laser ou au mètre. Les cotes non mesurées restent en orange avec le signe ≈.
3. **Assemblage** : faites glisser les pièces. Elles s'aimantent contre les pièces voisines en laissant l'épaisseur du mur.
4. **Portes, fenêtres, désordres** : outils 🚪 🪟 ⚠️, avec photos.
5. **Rapport** : onglet *Rapport PDF*, puis *Imprimer / Enregistrer en PDF*. Laissez l'échelle d'impression à 100 %.

Le mode d'emploi complet est dans l'application : *Menu › Mode d'emploi*.

## Précision : ce qu'il faut savoir

- Une photo ou un croquis ne donne pas de cotes exactes : il manque l'échelle et la perspective déforme. Ils servent d'ébauche.
- La précision vient des mesures sur place. Avec un télémètre laser et la méthode des diagonales, on obtient le centimètre.
- La diagonale est indispensable dans les bâtiments anciens, où les angles sont rarement droits. La diagonale de contrôle permet de repérer une mesure fausse.
- Sur iPhone Pro, l'application *Mesures* d'Apple (déjà installée) utilise le capteur LiDAR et peut remplacer le télémètre (1 à 2 cm d'écart).

## Données et sauvegarde

- Tout est enregistré dans le navigateur de l'appareil. Il n'y a ni compte ni serveur.
- **Sauvegardez régulièrement le fichier projet** (*Menu › Sauvegarder le fichier projet*). Ce fichier `.lakaz.json` contient tout, photos comprises. C'est votre copie de sécurité, et c'est lui qu'on transmet à un collègue ou à l'architecte (WhatsApp, e-mail, clé USB). Le destinataire l'ouvre avec *Menu › Ouvrir un fichier projet*.
- Un relevé ouvert sur l'ordinateur et un autre sur le téléphone sont deux copies séparées. On passe de l'un à l'autre avec le fichier projet.
- Sur iPhone, Safari peut effacer les données d'une page qui n'est pas ajoutée à l'écran d'accueil.

## Analyse IA (facultative)

L'analyse IA envoie les images choisies à l'API Claude d'Anthropic. Il faut :
- une connexion internet ;
- une clé API personnelle (console.anthropic.com), facturée à l'usage : environ 0,05 à 0,20 $ par analyse.

La clé reste enregistrée sur l'appareil. Tout le reste de l'application fonctionne sans internet et sans clé.

## Exports

- **PDF** : synthèse, plans à l'échelle avec cartouche, nord et barre d'échelle, tableau des métrés, relevé des désordres avec photos.
- **CSV** : métrés et désordres, à ouvrir dans Excel.
- **SVG** : plan du niveau à l'échelle 1:100, à importer dans un logiciel de dessin.
