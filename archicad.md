Nulpunt in Archicad
===============================

**aanspreekpunt:**
Marc Dankers
marc@dankersslimmerbouwen.nl

**Samenvatting**
Tips voor nulpuntcoördinatie, het verplaatsen van het model en het instellen van RD coördinaten in Archicad

**Doelgroep**
Elke Archicad-modelleur.

Deze pagina is een weergave van de open source ontwikkelomgeving op [github](https://github.com/BIM-Handboek-NL/BIM-geboden). U kunt een bijdrage leveren door een 'pull request' te sturen op github, of het aanspreekpunt van deze pagina te benaderen via e-mail.
 
-----------

*Tip: Zorg dat je voor je begint met modelleren weet waar je nulpunt is, zodat je op een logische plek ten opzicht van het nulpunt kunt starten. Een logische positie voor 0,0,0 WCS is ook stramien A-1, dan blijf je ook altijd in + coordinaten. Het referentieobject staat dan -10,-10,Peil*

In Archicad wordt het project-nulpunt bij export ook het nulpunt van de IFC. Hieraan is verder niets in te stellen. Om dit nulpunt te indentificeren is het op de onderstaande plaatjes weergegeven in 2d op plattegrondweergave en in 3D.

![nulpunt in 3D](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/archicad_nulpunt_3D.PNG)

![nulpunt in 2D](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/archicad_nulpunt_2D.PNG)

Waar verder nog belangrijke zaken voor nulpuntcoordinatie kunnen worden ingesteld in Archicad:
Options/Project Preferences/Project Location is de plek waar de hoogte t.o.v. NAP kan worden ingesteld en de precieze locatie van het gebouw op de wereld (RD coordinaten), alsmede de noordrichting (bijvoorbeeld tbv. simulaties)

![nulpunt settings](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/archicad_nulpunt_settings.PNG)

![project location](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/archicad_project_location.PNG)
 
*Let op: om een of andere reden staat in de standaardtemplate die in Nederland met Archicad wordt meegeleverd de hoogte van peil op 20m +NAP. Stel dit bij in uw eigen template!*

**Later bijstellen van het nulpunt**

Het komt regelmatig voor dat er al met modelleren is begonnen voordat de BIM-uitwisseling wordt gestart. Vaak is het dan niet meer mogelijk of in ieder geval te veel werk om een model te verplaatsen zodat het nulpunt op de goede plek ligt, omdat er al veel 2D documentatie zoals maatvoering en tekst aan de plattegronden, gevels, doorsnedes  en details is toegevoegd.
Een goede workaround om toch het nulpunt op de juiste plek ten opzicht van het gebouw te krijgen  is om het gehele model als hotlink in een leeg Archicad-bestand in te laden en op de juiste locatie en rotatie te plaatsen. De IFC-export vindt dat telkens plaats vanuit dit bestand.

Een aantal belangrijke opmerkingen hierbij:

1. alle GUID's – de unieke ID's van de objecten in BIM – worden veranderd. Dat wil zeggen dat bijvoorbeeld de clashes in Solibri niet meer aan de objecten zijn gekoppeld.
2. Let op de verdiepingen in het lege bestand overeenkomen met de verdiepingen in het te hotlinken bestand.
3. Let op de attributes met dezelfde naam (Building Materials, surfaces, profiles) worden vervangen door de attributes in het lege bestand.

Een manier om problemen met punt 2 en 3 te voorkomen is om een kopie van het oorspronkelijke bestand te maken en alle 3D en 2D elementen weg te gooien. 
