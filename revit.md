Nulpunt in Revit
===============================

**aanspreekpunt:**
Saul Henrion Verpoorten
SHenrionVerpoorten@jongen-venlo.nl

**Samenvatting**
Tips voor nulpuntcoördinatie in Revit

**Doelgroep**
Elke Revit-modelleur.

Deze pagina is een weergave van de open source ontwikkelomgeving op [github](https://github.com/BIM-Handboek-NL/BIM-geboden). U kunt een bijdrage leveren door een 'pull request' te sturen op github, of het aanspreekpunt van deze pagina te benaderen via e-mail.
 
-----------

In een BIM project moeten modelleer afspraken gemaakt worden, welke worden vastgelegd in een BIM plan. Een van die afspraken is het gemeenschappelijke 0 punt. Indien er geen afspraken gemaakt zijn is het verstandig om het 0 punt te positioneren op de kruising van as A en as 1 op peil=0. Indien er een niveau verschil aanwezig is tussen verschillende bouwdelen is het verstandig om een gemeenschappelijk vloerpeil aan te houden. 
Binnen Revit hebben we te maken met twee verschillende 0 punten te weten:

1. Project Base Point
2. Survey Point

Beide punten zijn nog aan te passen gedurende het modelleren, maar dit wordt bij voorkeur meteen goed ingesteld.

In beginsel zijn het Project Base Point en het Survey Point gelijk aan elkaar. Binnen Revit zijn deze zichtbaar te maken door op het lampje onder in je venster te klikken.

![lampje1](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/revit_01.PNG)
![lampje2](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/revit_01a.PNG)

Na het lampje aangeklikt te hebben ziet dit er als volgt uit:

![lampje3](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/revit_02.PNG)
![lampje4](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/revit_02a.PNG)

Het cirkelvormige symbool met het kruis erin is het Project Base Point en het driehoekige symbool is het Survey base point, zie onderstaande plaatjes:

![basepoint1](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/revit_03a.PNG)
![basepoint2](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/revit_03b.PNG)

Om een van de punten te kunnen selecteren ga je met de cursor over het symbool heen totdat deze blauw wordt vervolgens kun je die aanklikken. *TIP: door tab in te drukken is te switchen tussen objecten die over elkaar liggen.*
Wanneer weer op het lampje gedrukt wordt (lampje uit) zijn de 0 punten beide niet zichtbaar. Wanneer het wenselijk is deze zichtbaar te hebben moeten beide punten geselecteerd worden en vervolgens op de rechter muisknop geklit worden. Hiermee wordt een command screen geopend. Hier moet dan geselecteerd worden *unhide in view*. Ook kunnen de punten vastgezet worden middels het commando *PIN* hiermee komen de punten vast te staan en wordt er bij eventuele verplaatsing gevraagd of je dit wilt doen. Dit kan een extra veiligheidsmaatregel zijn binnen een werkomgeving.

- Binnen Revit wordt het Survey Point gebruikt voor het 0 punt van de ifc of ifczip. 
- Binnen Revit kunnen in het tabblad Manage diverse instellingen en aanpassingen gedaan worden aangaande de locatie, coördinaten en positie

![manage](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/revit_04.PNG)

Er zijn verschillende manieren om je project in te stellen qua coördinaten, positie en noorden. 
Zoals eerder al aangegeven heeft het de voorkeur de eerste keer de coördinaten goed in te stellen en hier verder niets meer aan te veranderen.

**Nulpunt indicator:**

In het Nationaal BIMhandboek wordt aangeraden een 0 punt indicator te plaatsen op het 0 punt om coördinatie tussen modellen te vereenvoudigen.
In de onderstaande voorbeelden wordt een indicator gebruikt die een noordpijl en een piramide bevat waarbij de punt van de piramide het 0 punt is. 

**Plaatsen nulpunt indicator:**

Er zijn verschillende type bestanden die gebruikt kunnen worden om in Revit te inserten of te linken:

1. Dwg bestanden  
2. Ifc bestanden
3. Revit bestanden

De voorkeur gaat in dit geval naar het linken van een dwg bestanden. Het dwg formaat heeft het kleinste bestandsformaat en zal hierdoor minder belasting geven van het computersysteem. Revit bestanden zijn van nature erg groot en wanneer een IFC wordt gelinkt converteert Revit deze op de achtergrond naar een .rvt bestand. Het linken biedt het voordeel dat het Survey point gebruikt kan worden de geel gemarkeerde optie te selecteren
- Auto - Center tot Center
- Auto - Origin to Origin (hierbij wordt het Project Base Point gebruikt)
- Auto - By Shared Coordinates (hierbij wordt het Survey Point gebruikt)

Wanneer nu tijdens het proces het gemeenschappelijk 0 punt (Survey Point ) niet overeen komt met het Project Base Point, en True North niet overeenkomstig het Project North gaat bij het wijzigen van het Survey Point en True North de 0 punt indicator automatisch mee.

**Stappen plaatsen nulpunt indicator**

1. Ga naar Insert tab en selecteer Link Cad

![linkCAD](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/revit_05.PNG)

2. Ga naar 0_punt.dwg en selecteer dit bestand en selecteer  Auto - By Shared Coordinates en de laag 00. Begane grond. Wanneer er vanuit de 3D view wordt geinsert wordt het laagste niveau geselecteerd dit is na plaatsing aan te passen in de properties tab.

![linkCAD](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/revit_06.PNG)

3. Wanneer nu weer op het lampje gedrukt wordt is te zien dat de 0 punt indicator correct geplaatst is.

![linkCAD](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/revit_07.PNG)

**TIP:**

>Het is verstandig het gelinkte dwg bestand daadwerkelijk te importeren in het model (via manage links  de link selecteren en dan op import klikken). Hiermee voorkom je dat bij het verwijderen van het gelinkte bestand er foutmeldingen optreden. Door het 0 punt te PINNEN wordt deze ook niet per ongeluk verplaatst.

**Wijzigen gemeenschappelijk nulpunt en True North**

Wanneer het gemeenschappelijk 0 punt (Survey Point) en True North niet correct zijn kunnen deze gemakkelijk aangepast worden. Voor het gemak is een vierkant getekend om het Survey Point en True North te wijzigen, dit gaat als volgt:

1. Ga naar de tab Manage
2. Selecteer Coordinates

![manage coordinates](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/revit_08.PNG)

3. Klik nu op specify coordinates at point
4. Klik op het punt dat als gemeenschappelijk 0 punt is aangewezen en stel de coördinaten (xyz) op dat punt in op 0,0,0 (indien de hoogte niet correct is kan dit in de Z waarde worden opgegeven)
5. Indien True North afwijkt is dit ook meteen in te stellen

![True North](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/revit_09.PNG)

6. Wanneer de coördinaten van de gemarkeerde hoek van het vierkant ingesteld worden op 0,0,0 en angle to True North op bijvoorbeeld 45° wordt ingesteld geeft dit het volgende resultaat. 

![45 graden](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/revit_10.PNG)

7. Om de 0 punt indicator tijdens de ifc export mee geëxporteerd te krijgen moet dit in de ifc mapping ingesteld worden. Dit doe je door in de mapping tabel de indicator in te stellen als bijvoorbeeld IfcObject

![IFCobject](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/revit_11PNG)

8. Via de open source ifc exporter wordt een goede ifc export gemaakt. De instellingen die hiervoor gebruikt moeten worden zijn te zien in de onderstaande plaatjes:

![IFC export](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/revit_12.PNG)
![IFC export](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/revit_13.PNG)
![IFC export](https://raw.githubusercontent.com/BIM-Handboek-NL/Werken-met-een-nulpunt-template/master/img/revit_14.PNG)

**TIP:**

>In de project browser kunnen 3D views aangemaakt worden waar middels filter een view gemaakt kan worden met bijvoorbeeld alleen bouwkundige of constructieve objecten (worksets kunnen hierbij erg makkelijk zijn).
Er zijn ook families beschikbaar waarmee het 0 punt te markeren is. Het nadeel hiervan is dat deze handmatig geplaatst moeten worden wat eventuele misplaatsing (minimale afwijkingen in x,y,z waarde) tot gevolg kan hebben. Door het op boven beschreven manier te doen ben je verzekerd van een exacte plaatsing en dat bij aanpassingen in 0 punt en eventueel het noorden de 0 punt indicator meegaat.
