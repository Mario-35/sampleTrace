# Presentation

Application web (accessible par browser) windows, linux, telephonne, tablette :

BDD PostgresSql mais en fait cela n'a pas réélement d'importance....

l'impression des etiquettes ne se fera pas en ouvrant un fichier excel mais un appel a l'appli qui envera un json imprimera l'etiquette
car les infos sont dans la base en passan par le formulaire

## Modéle de données du formulaire de saisie
```JSON
{
    "Uuid" : "Code auo generé",
    "status": "ACTIF | ERREUR | PERDU | DETRUIT",
    "printed": "Bool",
    "Programme / Projet" : "Text => Liste",
    "Responsable" : "Text => Liste",
    "N° Interne" :"Text",	
    "conditionnement" : {
        "Localisation" : "Text => Liste",
        "Type conditionnement" : "Text => Liste",
        "Nbre conditionnement": "Number",
        "Etagère" : "Text"
    },
    "Infos" : "Json",	
    "Date de péremption" : "date",    
    "prelevement" : {
        "parcelle" : {
            "nom" : "Text",
            "Préleveur" : "Text",
            "Code Postal" : "Text",
            "Coordonée GPS" : "Text",
            "SI hors bretagne" : {
                "n-1": {
                    "culture" : {
                        "especes" :"Text",
                        "Rendement" :"Text",
                        "Destination Résidu" :"Text"
                    },
                    "travail du sol" : {
                        "type" :"Text",
                        "profondeur" :"Text"
                    },
                    "couvert interculture" : {
                        "especes" :"Text",
                        "Rendement" :"Text",
                        "Destination Résidu" :"Text"
                    }
                },
                "n-5": {
                    "culture" : {
                        "especes" :"Text",
                        "Rendement" :"Text",
                        "Destination Résidu" :"Text"
                    },
                    "travail du sol" : {
                        "type" :"Text",
                        "profondeur" :"Text"
                    },
                    "couvert interculture" : {
                        "especes" :"Text",
                        "Rendement" :"Text",
                        "Destination Résidu" :"Text"
                    }
                }
            }
        },
        "Nature"	: "Text => Liste",
        "Methode"	: "Text => Liste",
        "Probleme(s)"	: "Text",
        "Date" : "DateTime",
        "Localisation": "{geo} : GeoJson",
        "Pays" : "Text => Liste",
        "Région" : "Text => Liste"
    }
}

```