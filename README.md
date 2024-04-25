# SocialMaps Data


Parität's Socialmaps project allows users to search for services they need in Berlin https://www.socialmap-berlin.de/

The data provided consists of several files:

```
socialmaps-items.json         # The services listed on the map 
socialmaps-translations.json  # The translations for the socialmaps ui
```

## Items

The items data can be described as follows:
```

 "items": [
    {
      "title": "Ausbildung zum Glas- und Gebäudereiniger/in", // Name of the service/location
      "image": null,
      "state": "public", // All items in this set are public
      "tags": [ // Items can be in multiple topics
        "young", 
        "disability_background",
        "reinickendorf",
        "educational_center",
        "wheelchair",
        "german",
        "o_ri_inggmh",
        "education",
        "labour",
        "service"
      ],
      "primaryTopic": "labour", // Items have 1 primary topic, for example used to colour-code the item
      "brief": { //prefixes indicate a machine translation e.g. [DeepL:] 
        "de": "von der Handwerkskammer anerkannter Handwerksberuf mit dualer Ausbildung",
        "en": "[DeepL:] Craft recognized by the Chamber of Crafts and Trades with dual training" 
      },
      "description": { // May contain markdown (text formatting markup)
        "de": "Die integra gGmbH bietet die Möglichkeit einer dualen Ausbildung zum Glas- und Gebäudereiniger/in.\nGlas- und Gebäudereiniger/innen sind für die Unterhaltsreinigung und zahlreiche weitere Bereiche zuständig. Sie säubern Schreibtische, Schränke und Böden, saugen die Teppiche, leeren Abfalleimer, reinigen die sanitären Anlagen und vieles mehr.\nGebäudereiniger/in ist ein von der Handwerkskammer anerkannter Handwerksberuf mit dualer Ausbildung, für den viele spezielle Fachkenntnisse von Nöten sind. Dabei geht es um weitaus mehr als um Sauberkeit, vielmehr geht es um Hygiene.\nFür die Ausbildung wird mindestens die erweiterte Berufsbildungsreife (eBBR) benötigt. Besser ist ein mittlerer Schulabschluss (MSA). Gerade aufgrund der häufig wechselnden Einsatzorte als Glas- und Gebäudereiniger/in ist ein Führerschein unbedingt sinnvoll. (Wir unterstützen Sie bei der Finanzierung der Fahrerlaubnis B). Mehr zu dem Berufsbild und der Ausbildung erfahren Sie direkt bei integra.",
        "en": "[DeepL:] integra gGmbH offers the possibility of dual training as a glass and building cleaner.\nGlass and building cleaners are responsible for maintenance cleaning and numerous other areas. They clean desks, cupboards and floors, vacuum carpets, empty waste garbage cans, clean sanitary facilities and much more.\nBuilding cleaners are a trade recognized by the Chamber of Crafts with dual training, for which many special skills are needed. It is about much more than cleanliness, it is about hygiene.\nFor the training, at least the extended vocational training maturity (eBBR) is required. An intermediate school leaving certificate (MSA) is better. A driver's license is absolutely essential, especially because of the frequently changing work locations as a glass and building cleaner. (We will support you in financing the B driving license). You can find out more about the job description and training directly from integra."
      },
      "location": null, // Name for the location different from the address e.g.name of the school, or "room 101"
      "address": "Lengeder Straße 48",
      "zip": "13407",
      "city": "Berlin",
      "latitude": 52.5826566,
      "longitude": 13.3581692,
      "responsible": "Integra gGmbH", // commercial entity?
      "website": "https://www.integra-berlin.de/ausbildung/glas-und-gebaeudereiniger-in/",
      "hours": {
        "de": ""
      },
      "creationDate": 1618255456582,
      "creator": null, // editor (stripped from the public link)
      "editingNote": null,
      "facebook": null,
      "lastEditDate": 1705050296324,
      "lastEditor": "4fdeeaa714c73959",  // id of the editor
      "mobile": null, // could be a phones
      "proposalFor": null,
      "resubmissionDate": null,
      "resubmissionNotification": null,
      "twitter": null,
      "whatsapp": null,
      "apiKeyUsed": false,
      "instagram": null,
      "location_ref": "8c75a2ba61aceb13", // Points to anothr item ID (and therefore they share the location data) e.g. Integra in this case
      "projectEndDate": null,
      "projectStartDate": null,
      "telegram": null,
      "vimeo": null,
      "youtube": null,
      "id": "9749276938bd792e"
    },
```

## Translations

Translation fields relevant to items are described below:
```
{
   ...
   // german translations:
   'DE' :{
     ...
     // User interface text for the item editor
     // Contains description of most item properties:
     'ITEMS': {

       ...

       // Label of the property 'brief' in the item editor:
       "BRIEF": "...",

       // Extra info about the property next to the label:
       "BRIEF_NOTE": "...",

       // Help text displayed after clicking a help button
       "BRIEF_HELP": "..."
     },

     "TYPES": {
       ...,
       "SERVICE" : "..."
     },

     "CATEGORIES": {
       ...,
       "SPORTS" : "..."
     },

     "UNSORTED_TAGS": {
       ...
       "SENIOR_CITIZENS" : "..."
     },

}
```

## Tags

The tags in the .tags property of items can include strings from types,
categories or unsorted_tags, e.g.:

```
{
   "title": "My Example Item",
   "tags": ["service", "sports", "senior_citizens"],
   ...
}
```

In this case the translation for the 'sports' tag can be found in
"DE.CATEGORIES.SPORTS"; and the translation for the 'senior_citizens'
can be found in "DE.UNSORTED_TAGS.SENIOR_CITIZENS".
