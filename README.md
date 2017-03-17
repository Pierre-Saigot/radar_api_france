
# **AUTO_RADAR-FR (API)**

## Introduction

Cette API permet à l’utilisateur de récupérer les radars ville par ville. Vitesse, emplacement exact (textuel), descriptif, sens et remarque sont au rendez-vous pour chaque cas.

## REST (JSON)

    Serveur API : http://radar-de-france.xyz/api/v1

L’API est principalement RESTful. Les données sont exposées sous la forme d’URI qui représentent des ressources et peuvent être récupérées via des clients HTTP (comme les navigateurs web).

## Code source

**Aucun code source** ne sera **distribué** pour des **raisons légales**.

## Documentation

La liste des ressources est disponible ici :

    http://radar-de-france.xyz/api/v1/documentation/

## Exemples

Quelques exemples sont disponibles ici :

*   [Départements](#départements)
*   [Communes](#communes)
*   [Radar](#radar)

# Format

Les données renvoyées sont disponibles au format **JSON**.

# Exemples de requêtes

## Départements

Exemple de requête pour récupérer tous les départements :

    //Requête 
    http://radar-de-france.xyz/api/v1/departements/

* * * 
    // Réponse 

        {
                  "france_radar": {
                    "departements": {
                      "ain": {
                        "nom": "Ain",
                        "lien": "/communes/?r=/ain/"
                      },
                      "aisne": {
                        "nom": "Aisne",
                        "lien": "/communes/?r=/aisne/"
                      },
                      "allier": {
                        "nom": "Allier",
                        "lien": "/communes/?r=/allier/"
                      },
                      "alpes de haute provence": {
                        "nom": "Alpes de Haute Provence",
                        "lien": "/communes/?r=/alpes-de-haute-provence/"
                      },
                      "hautes-alpes": {
                        "nom": "Hautes-Alpes",
                        "lien": "/communes/?r=/hautes-alpes/"
                      },
                      "alpes maritimes": {
                        "nom": "Alpes Maritimes",
                        "lien": "/communes/?r=/alpes-maritimes/"
                      },
                      "ardèche": {
                        "nom": "Ardèche",
                        "lien": "/communes/?r=/ardeche/"
                      },
                      "ardennes": {
                        "nom": "Ardennes",
                        "lien": "/communes/?r=/ardennes/"
                      },
                      "ariège": {
                        "nom": "Ariège",
                        "lien": "/communes/?r=/ariege/"
                      },
                      "aube": {
                        "nom": "Aube",
                        "lien": "/communes/?r=/aube/"
                      },
                      "aude": {
                        "nom": "Aude",
                        "lien": "/communes/?r=/aude/"
                      },
                      "aveyron": {
                        "nom": "Aveyron",
                        "lien": "/communes/?r=/aveyron/"
                      },
                      "bouches du rhône": {
                        "nom": "Bouches du Rhône",
                        "lien": "/communes/?r=/bouches-du-rhone/"
                      },
                      "calvados": {
                        "nom": "Calvados",
                        "lien": "/communes/?r=/calvados/"
                      },
                      "cantal": {
                        "nom": "Cantal",
                        "lien": "/communes/?r=/cantal/"
                      },
                      "charente": {
                        "nom": "Charente",
                        "lien": "/communes/?r=/charente/"
                      },
                      "charente maritime": {
                        "nom": "Charente Maritime",
                        "lien": "/communes/?r=/charente-maritime/"
                      },
                      "cher": {
                        "nom": "Cher",
                        "lien": "/communes/?r=/cher/"
                      },
                      "corrèze": {
                        "nom": "Corrèze",
                        "lien": "/communes/?r=/correze/"
                      }
                }
            }
         }

## Communes

Exemple de requête pour récupérer tous les communes dans un département :

    //Requête 
    http://radar-de-france.xyz/api/v1/communes/?r=/yvelines/

* * *

    // Réponse 
        {
                  "france_radar": {
                    "communes": {
                      "ablis": {
                        "nom": "Ablis",
                        "lien": "/radar/?r=/yvelines/ablis/"
                      },
                      "acheres": {
                        "nom": "Acheres",
                        "lien": "/radar/?r=/yvelines/acheres/"
                      },
                      "adainville": {
                        "nom": "Adainville",
                        "lien": "/radar/?r=/yvelines/adainville/"
                      },
                      "aigremont": {
                        "nom": "Aigremont",
                        "lien": "/radar/?r=/yvelines/aigremont/"
                      },
                      "allainville": {
                        "nom": "Allainville",
                        "lien": "/radar/?r=/yvelines/allainville/"
                      },
                      "les alluets le roi": {
                        "nom": "Les Alluets Le Roi",
                        "lien": "/radar/?r=/yvelines/les-alluets-le-roi/"
                      },
                      "andelu": {
                        "nom": "Andelu",
                        "lien": "/radar/?r=/yvelines/andelu/"
                      },
                      "andresy": {
                        "nom": "Andresy",
                        "lien": "/radar/?r=/yvelines/andresy/"
                      },
                    "news": [
                      {
                        "new": "Le radar du Pecq détruit dans un accident",
                        "date": "[30-05-2011]"
                      }
                    ]
                  }
                }

## Radar

Exemple de requête pour récupérer les radars et les informations qui s’ensuivent dans une ville.

    //Requête 
    http://radar-de-france.xyz/api/v1/radar/?r=/yvelines/trappes/

* * *

    // Réponse 
        {
              "france_radar": {
                "ville": {
                  "radar": [
                    {
                      "emplacement": "N10 - Trappes",
                      "etat": "En service",
                      "sens": "Paris - Province",
                      "description": "Au niveau du quartier de la Boissière, 500 metres aprés le feu tricolore de la station BP (c'est le deuxième feu de Trappes) Signalisation : Panneau d'avertissement environ 200 mètres avant le radar",
                      "pk": "16+0",
                      "flash": "Flash Arrière",
                      "type_radar": "Radar fixe (3ème génération 2007)",
                      "vitesse": "70 km/h",
                      "remarques": "2015: Le radar de première génération est remplacé par un radar de troisième génération Cabine installée le 27 aout 2004 Mise en service le 30 septembre 2004"
                    },
                    {
                      "emplacement": "N10 - Trappes",
                      "etat": "En service",
                      "sens": "Paris vers Province",
                      "description": "La vitesse maximum autorisée sera abaissée de 110 à 90 km/h à partir du 4 juillet 2016\. Juste après la station Total à l'entrée de Trappes. Le radar est au pied d'un pylone d'éclairage urbain, 200m après la jonction N10/A12\. Signalisation : 300 mètres avant environ",
                      "pk": "12+1150",
                      "flash": "Flash Arrière",
                      "type_radar": "Radar fixe (3ème génération 2007)",
                      "vitesse": "90 km/h",
                      "remarques": "Juillet 2016: La vitesse maximum autorisée est abaissée de 110 à 90 km/h Cabine installée le 1er juillet 2008"
                    }
                  ]
                }
              }
            }

# License

Toutes  **les données sont libre** mais appartiennent à “http://www.radars-auto.com/”  
et sont **à utilisées** dans un **but strictement personnel** ou de **recherche** et non dans un but commercial.
