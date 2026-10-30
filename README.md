# Lakaz Plan

*[English version](README.en.md)*

Relevé de bâtiments existants avant rénovation : plan coté, désordres avec photos, métrés et rapport PDF. Conçu pour des équipes non spécialistes qui travaillent sur le terrain aux Seychelles.

**Ouvrir l'application : https://myrdinevil.github.io/Lakaz-Plan/**

« Lakaz » veut dire « maison » en créole seychellois.

L'application existe en français et en anglais. Elle suit la langue du téléphone, et on peut en changer à tout moment (Menu › Langue).

## À quoi ça sert

Avant de rénover un immeuble en mauvais état, il faut savoir précisément ce qu'on a devant soi. Lakaz Plan produit :

- un plan de chaque niveau, à l'échelle, avec l'épaisseur des murs, les portes et les fenêtres ;
- la liste des désordres (fissures, béton éclaté, fers rouillés, humidité, termites, toiture…) placés sur le plan, avec photos, gravité et travaux préconisés ;
- les métrés pour chiffrer le chantier : surfaces de sol et de murs, plinthes, volumes ;
- un rapport PDF qu'on remet à l'architecte, à l'entreprise ou au propriétaire.

## Installer

Il n'y a rien à télécharger ni à installer.

### Sur iPhone

1. Ouvrir le lien ci-dessus dans **Safari**. Chrome et l'aperçu de WhatsApp ne permettent pas l'installation.
2. Toucher le bouton Partager (le carré avec une flèche vers le haut).
3. Choisir « Sur l'écran d'accueil », puis « Ajouter ».
4. Lancer l'application une première fois avec internet. Elle fonctionne ensuite sans réseau.

### Sur Android

Ouvrir le lien dans Chrome, menu ⋮, puis « Ajouter à l'écran d'accueil ».

### Sur ordinateur

Ouvrir le lien dans n'importe quel navigateur. On peut aussi télécharger ce dépôt (bouton vert « Code » › « Download ZIP ») et double-cliquer sur `index.html` : l'application fonctionne alors entièrement hors ligne.

## Utiliser

1. **Ébauche.** Ajouter les pièces une par une (bouton ➕), ou importer un croquis en fond (🖼️) et tracer dessus (✏️), ou faire lire le croquis par l'IA (✨).
2. **Mesures.** Pièce par pièce, mesurer les murs et les diagonales. Un schéma indique en rouge ce qu'il faut mesurer.
3. **Assemblage.** Faire glisser les pièces : elles s'aimantent les unes aux autres en laissant l'épaisseur du mur.
4. **Portes, fenêtres et désordres.** Outils 🚪, 🪟 et ⚠️. On ajoute les photos depuis le téléphone.
5. **Rapport.** Onglet « Rapport PDF », puis « Imprimer / Enregistrer en PDF ». Laisser l'échelle d'impression à 100 %.

Le mode d'emploi détaillé est dans l'application : Menu › Mode d'emploi.

## Précision des plans

Une photo ou un croquis ne donne pas de cotes exactes : on ne connaît pas l'échelle, et la perspective déforme. Ils servent seulement d'ébauche. La précision vient des mesures prises sur place.

- Avec un télémètre laser (environ 30 €) ou un mètre ruban, on obtient le centimètre.
- Sur iPhone Pro, l'application Mesures d'Apple, déjà installée, utilise le capteur LiDAR et peut remplacer le télémètre (1 à 2 cm d'écart).
- La diagonale est indispensable dans les bâtiments anciens, où les angles sont rarement droits : c'est elle qui donne la forme exacte de la pièce. La diagonale de contrôle permet de repérer une mesure fausse.
- Tant qu'une cote n'est pas mesurée, elle reste affichée en orange avec le signe ≈, sur le plan comme dans le rapport. Le rapport indique le pourcentage de cotes réellement mesurées.

## Données et sauvegarde

Il n'y a ni compte ni serveur. Les relevés sont enregistrés dans l'appareil qui les a créés et n'en sortent pas. Le lien de l'application ne donne accès à aucune donnée.

- Sauvegarder régulièrement le fichier projet : Menu › Sauvegarder le fichier projet. Ce fichier `.lakaz.json` contient tout, photos comprises. C'est la copie de sécurité.
- Pour transmettre un relevé à un collègue ou à l'architecte, on lui envoie ce fichier (WhatsApp, e-mail, clé USB). Il l'ouvre avec Menu › Ouvrir un fichier projet.
- Un relevé sur l'ordinateur et un autre sur le téléphone sont deux copies séparées : on passe de l'un à l'autre avec le fichier projet.
- Sur iPhone, Safari peut effacer les données d'une page qui n'a pas été ajoutée à l'écran d'accueil.

## Analyse IA (facultative)

L'outil ✨ envoie les images choisies à l'API Claude d'Anthropic, qui propose une ébauche : pièces, ouvertures, désordres visibles. Toutes les cotes qu'elle propose sont marquées ≈ et doivent être mesurées.

Il faut une connexion internet et une clé API personnelle (console.anthropic.com), facturée à l'usage : environ 0,05 à 0,20 $ par analyse. La clé reste enregistrée dans l'appareil. Le reste de l'application fonctionne sans internet et sans clé.

## Exports

| Format | Contenu |
|---|---|
| PDF | Synthèse, plans à l'échelle (1:50, 1:100…) avec cartouche, nord et barre d'échelle, métrés, désordres avec photos |
| CSV | Métrés et désordres, à ouvrir dans Excel |
| SVG | Plan du niveau à l'échelle 1:100, à reprendre dans un logiciel de dessin |
| `.lakaz.json` | Projet complet, pour la sauvegarde et l'échange |

## Contenu du dépôt

| Fichier | Rôle |
|---|---|
| `index.html` | L'application complète, en un seul fichier, sans dépendance |
| `sw.js` | Garde l'application dans le téléphone pour l'usage hors ligne |
| `manifest.webmanifest` | Nom et icône pour l'installation sur l'écran d'accueil |
| `icon.svg` | Icône de l'application |

## Mettre à jour l'application

Modifier `index.html`, puis publier avec GitHub Desktop (« Commit », puis « Push origin »). Le site est mis à jour en une à deux minutes. Les téléphones récupèrent la nouvelle version à la prochaine ouverture avec du réseau.
