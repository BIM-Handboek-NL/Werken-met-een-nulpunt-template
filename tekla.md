Nulpunt in Tekla
===============================

**aanspreekpunt:**
Sander Kouwenberg
Sander.Kouwenberg@bekendam.com

**Samenvatting**
Tips voor nulpuntcoördinatie in Tekla

**Doelgroep**
Elke Tekla-modelleur.

Deze pagina is een weergave van de open source ontwikkelomgeving op [github](https://github.com/BIM-Handboek-NL/BIM-geboden). U kunt een bijdrage leveren door een 'pull request' te sturen op github, of het aanspreekpunt van deze pagina te benaderen via e-mail.
 
-----------

**Coördinatensysteem.**

Het symbool met drie assen (x, y en z) staat voor het lokale coördinatensysteem en geeft de richting van het model. Het is gelegen in de rechter benedenhoek van het model view . Het coördinatiesymbool volgt het werkvlak.

![xyz](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/tekla01.png)

**Oorsprong.**

Het groene kubus symbool staat voor het globale assenstelsel en ligt op het globale punt van oorsprong (0,0,0).

![nulpunt](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/tekla02.png)

**basispunt model.**

Kies voor het basispunt van het model een gemakkelijk herkenbare locatie. Bijvoorbeeld; het snijpunt van het raster as-1 en as-A en op een hoogte Peil. Dit punt is niet het referentiepunt. 

![basispunt](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/tekla03.png)

**Referentiepunt model.**

Het geniet de voorkeur om het referentiepunt van het model niet te laten samenvallen met het basispunt. Gebouwmodellen met veel elementen kunnen er voor zorgen dat het referentiepunt niet direct zichtbaar is.
Kies voor het referentiepunt van het model een punt buiten het model. Bij voorkeur is dit punt het globale punt van oorsprong. (0,0,0) Het model met raster kan iets verderop gemodelleerd worden. Bijvoorbeeld; met basispunt de locatie 3000,3000,0. Door het referentiepunt buiten het gebouw te kiezen voorkom je de visuele vertroebeling van het globale punt van oorsprong. (0,0,0) 

![referentiepunt](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/tekla04.png)

**Referentiemodellen.**

Sommige modellering systemen werken op mondiale of nationale coördinatensystemen, terwijl anderen werken op een lokaal assenstelsel. De modellen gemaakt in systemen die niet voldoen aan de afgesproken assenstelsel dienen de waarden voor de translatievector mee te geven voor een juiste positionering in het integrale model. 
Het afgesproken referentiepunt zou vastgelegd kunnen worden in een DWG-bestand, dat verstrekt wordt aan de betrokken partijen.

![referentiemodellen](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/tekla05.png)

**Referentieblok.**

Bij het samenstellen van een integraal model of het toevoegen van referentiemodellen aan uw eigen model wordt vaak een referentieblokje gebruikt. Dit referentieblokje is 1,0x1,0x1,0 m³ groot. Bij samenstellen van het integraal model is direct duidelijk of alle modellen geometrisch juist zijn gepositioneerd. Immers; positie afwijkingen worden direct gesignaleerd doordat de referentieblokjes niet overeen komen.
Door uw logo in of op uw eigen referentieblokje te plaatsen is direct zichtbaar van welke modellerende partij een referentieblokje is. 

![blokje](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/tekla06.jpg)




