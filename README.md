# POTA-France
Parks of the Air (POTA) - French database

## ToDo List

1. Import POTA list in local database
  * [POTA API : List of french parks](https://api.pota.us/locations/F-FR)
2. Import french parks with good names and coordinates
  * Parcs Naturels Nationaux :
    * [ParcsNationaux.fr](http://www.parcsnationaux.fr/fr)
    * [Wikipedia : Liste des parcs naturels de France](https://fr.wikipedia.org/wiki/Liste_des_parcs_naturels_de_France)
    * [Wikipedia : List of national parks of France](https://en.wikipedia.org/wiki/List_of_national_parks_of_France)
  * Parcs Naturels Régionaux
    * [Wikipedia : Parcs naturels français](https://commons.wikimedia.org/wiki/File:Parcs_naturels_fran%C3%A7ais.svg?uselang=fr)
  * Natura 2000
    * [Natura2000.fr](https://www.natura2000.fr/)
    * [inpn.mnhn.fr](https://inpn.mnhn.fr/site/natura2000/listeSites)

## Notes

[Diplômes France Flora Fauna](https://www.france-flora-fauna.fr/diplomes-fff/)
  * [Parcs Naturels Nationaux](https://www.france-flora-fauna.fr/programme-fff/les-parcs-nationaux/)
  * [Parcs Naturels Régionaux](https://www.france-flora-fauna.fr/programme-fff/les-parcs-regionaux/)
  * [Les réserves naturelles](https://www.france-flora-fauna.fr/programme-fff/les-reserves-naturelles/)
  * [Natura 2000](https://www.france-flora-fauna.fr/programme-fff/natura-2000/)

```
$ curl -s https://api.pota.us/park/K-2548 | jq '.'
[
  {
    "parkId": 2548,
    "reference": "K-2548",
    "name": "Paul B. Johnson",
    "latitude": 31.1409,
    "longitude": -89.2464,
    "parktypeId": 101,
    "active": 1,
    "parkComments": null,
    "accessibility": null,
    "sensitivity": null,
    "accessMethods": null,
    "activationMethods": null,
    "agencies": null,
    "agencyURLs": null,
    "parkURLs": null,
    "createdByAdmin": null,
    "parktypeDesc": "State Park",
    "locationDesc": "US-MS",
    "locationName": "Mississippi",
    "entityId": 291,
    "entityName": "United States Of America",
    "referencePrefix": "K",
    "entityDeleted": 0
  }
]
```

```
$ curl -s https://api.pota.us/locations/US-CA | jq '.'
{
  "parks": [
    {
      "reference": "K-4575",
      "name": "Old Spanish National Historic Trail",
      "locationDesc": "US-AZ,US-CA,US-CO,US-NV,US-NM,US-UT",
      "locationName": "Arizona,California,Colorado,Nevada,New Mexico,Utah",
      "entityName": "United States Of America"
    }
  ],
  "partition_key": "Park#Location#US-CA",
  "item_type": "Location"
}
```
