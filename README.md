# MMM-PrixCarburants

Ce module permet d'afficher les prix des carburants des stations selon votre code postal

## Screenshot
![](https://raw.githubusercontent.com/kelly97129/MMM-PrixCarburants/dev/data/screenshot.png)

## Installation

```sh
cd ~/MagicMirror/modules
git clone https://github.com/kelly97129/MMM-PrixCarburants
cd MMM-PrixCarburants
npm install
```

## Configuration

```
{
  module: "MMM-PrixCarburants",
  position: "top_center",
  config: {
    debug: false,
    CodePostaux: [ //
      "08320",
      "59610"
    ],
    Carburants: [
      1, // Gazole
      2, // SP95
      3, // E85
      4, // GPLc
      5, // E10
      6  // SP98
    ],
    Affiche: 5, // nombre de stations à afficher
    width: "450px" // largeur du module
  }
},
```

### CodePostaux : []
Permets de scanner les stations des codes postaux voulu
### Carburants : []
Permet d'afficher uniquement le type de carburant voulu.<br>
Commenter ou supprimer le type de carburant(s) ce que vous ne voulez pas voir
### Affiche
Nombre maximum de station à afficher
### width
Largeur du module, pour ajuster si besoin

## Mise à jour du module
Utilisez simplement cette commande
```
cd ~/MagicMirror/modules/MMM-PrixCarburants
npm run update
```

## Remerciements
 * kelly97129 pour son idée

## Sources
 * Ce module reprend plus ou moins le meme principe que le plugin [prixcarburants](https://github.com/floman321/prixcarburants) pour jeedom
 * Ce module utilise la meme base de donnée [nationale](https://www.prix-carburants.gouv.fr/)

## Notes:
 * Afin de ne pas perturber le chargement des autres modules, ce module va mettre environ 30 a 45 secondes pour s'afficher au premier démarrage (démarrage différé)
 * Une mise à jours automatique est faites toutes les heures
