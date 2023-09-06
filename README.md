# lab1

**Øvelse 2: Opret en mappe**
Endpoint: https://api.dropboxapi.com/2/files/create_folder
HTTP-verb: POST

Body request: {
      "path": "/TestMappe"
  }

Body response: {
     "name": "TestMappe",
     "path_lower": "/testmappe",
     "path_display": "/TestMappe",
     "id": "id:cDODuX3Ank0AAAAAAAAXhQ"
  }

Er flowet i overenstemmelse med princippet om "uniform interface" i REST principperne?
- Jeg mener at flowet er i overensstemmelse med princippet om "uniform interface" i REST principperne, da vi bruger det korrekte HTTP-verb (POST), jeg fik også et body response i JSON-  format. 


**Øvelse 3: Hent mappe detaljer**
Endpoint: https://api.dropboxapi.com/2/files/get_metadata

HTTP-verb: POST (fik ikke JSON-format i response, da jeg bruger GET, med forskellige endpoints.. dette var den eneste måde jeg fik json tilbage. Jeg spurgte chatGPT, og fik af vide, at nogle API'er, som Dropbox, bruger POST i stedet for GET, pga. sikkerhedsmæssige årsager, så jeg har valgt at gå videre med det :) )

Body request: {
    "path": "/TestMappe"
}

Body response: {
    ".tag": "folder",
    "name": "TestMappe",
    "path_lower": "/testmappe",
    "path_display": "/TestMappe",
    "id": "id:cDODuX3Ank0AAAAAAAAXhQ"
}

Status code: 200 ok

Er flowet i overenstemmelse med princippet om "uniform interface" i REST principperne?
- Jeg mener at flowet er i overensstemmelse med princippet om "uniform interface" i REST principperne, selvom jeg ikke bruger det "korrekte" HTTP-verb, da jeg læste at nogle API'er       vælger at bruge POST af sikkerhedsmæssige årsager, og det ikke er noget man kan gøre noget ved. Jeg er dog lidt usikker på, om det er fordi jeg har brugt forkert endpoint, og det       måske virkede med et specifikt endpoint, men jeg fik prøvede lidt forskelligt, og blev ved med at få HTML-format når jeg bruger GET. Kunne det være noget du kunne forklare, da jeg er   lidt forvirret :) 


**Øvelse 4: Upload en fil**
Endpoint: https://content.dropboxapi.com/2/files/upload
HTTP-verb: POST

Hvordan uploades filen? -->
Body request: {
    "autorename": false,
    "mode": "add",
    "mute": false,
    "path": "/TestMappe,
    "strict_conflict": false
}

Body response:  {
    "name": "Skærmbilledetest.png",
    "path_lower": "/testmappe/skærmbilledetest.png",
    "path_display": "/TestMappe/Skærmbilledetest.png",
    "id": "id:cDODuX3Ank0AAAAAAAAXiw",
    "client_modified": "2023-09-06T09:15:44Z",
    "server_modified": "2023-09-06T09:15:45Z",
    "rev": "604ad303d71271340a69d",
    "size": 120,
    "is_downloadable": true,
    "content_hash": "349c8297a94ca9213532e810faa63db39bf733f3087f5e966d5217eee5b2ba69"
}

Jeg har ændret værdien i key fra -->  "Content-Type: application/JSON" til "application/octet-stream"

Jeg har dernæst tilføjet en fil i binary under body

Jeg har i header tilføjet følgende key --> Dropbox-API-Arg:  og værdien --> {\"autorename\":false,\"mode\":\"add\",\"mute\":false,\"path\":\"/Homework/math/Matrices.txt\",\"strict_conflict\":false}"




    








