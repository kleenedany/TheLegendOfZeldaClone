# Abgabe für das WPM PRIMA
# TheLegendOfZeldaClone

 
[Spiel auf GitHub Pages](https://kleenedany.github.io/TheLegendOfZeldaClone/)

Designdokument

Gepacktes Archiv

[Quellcode](https://github.com/kleenedany/TheLegendOfZeldaClone)



| Nr | Bezeichnung           | Inhalt                                                                                                                                                                                                                                                                         |
|---:|-----------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|    | Titel                 | The Legend of Zelda Clone
|    | Name                  | Daniela Rotter
|    | Matrikelnummer        | 254 652
|  1 | Nutzerinteraktion     | Der Nutzer hat folgende Interaktionsmöglichkeiten mit der Applikation. Über die Tasten WASD kann die Spielfigur bewegt werden. Hierbei steht W für nach Norden laufen, A für nach Westen laufen, S für nach Süden laufen und D für nach Osten gehen. Mit der Leertaste können Pfeile abgeschossen werden. Weitere Interaktionsmöglichkeiten hat der Nutzer vor Spiel Start, auf dem Titelbildschirm. Dort stehen dem Nutzer drei Buttons zur Verfügung. Start Game, hier wird das Spiel gestartet. Controls, hier kann der Nutzer die Steuerung einsehen. Und Settings, hier kann der Nutzer die Lautstärke der Musik einstellen.
|  2 | Objektinteraktion     | Der Nutzer kann mit Objekten, diese sind Hecken, Häuser und Bäume, kollidieren. Dabei geschieht nichts. Des Weiteren kann der Nutzer mit den Gegnern kollidieren. Dabei verliert er, pro Kollision, ein Leben.
|  3 | Objektanzahl variabel | Zur Laufzeit werden Pfeile und die Munition des Gegners generiert. Die Pfeile werden generiert, wenn der Nutzer die Leertaste betätigt.Der Gegner schießt mit Munition, wenn der Nutzer einen Pfeil abschießt.
|  4 | Szenenhierarchie      | Die oberste Node ist die GameNode. Alle anderen Nodes sind dieser untergeordnet. Auf der zweiten Ebene befinden sich das Terrain, welches den Boden beinhaltet. Außerdem befindet sich die Map, welche alle Spielobjekte beinhaltet auf der zweiten Ebene. Auf der dritten Ebene befinden sich Leben, Pfeile und Munition der Gegner.
|  5 | Sound                 | Bei Start des Spiels setzt die Hintergrundmusik ein. Diese ist dauerhaft zu hören. Beifolgenden Aktionen wird die Hintergrundmusik durch Sound Effekte unterstützt. Abschießen eines Pfeils, treffen eines Gegners, wenn der Gegner schießt und wenn der Nutzer stirbt.
|  6 | GUI                   | Bei Start der Applikation, im Titelbildschirm, unter dem Punkt Settings hat der Nutzer die Möglichkeit, die Musiklautstärke anzupassen. 
|  7 | Externe Daten         | Objekte und Gegner sind in der GameInfo.json gespeichert. Diese wird bei Spielstart geladen und zeigt die Objekte und Gegner auf dem Spielfeld an.
|  8 | Subklassen            | Die Klassen Arrow, Endboss, Enemy, Floor, LifePoints, MapObjects, Player und Shoot erben von der Fudge Node Sprite.
|  9 | Maße & Positionen     | Die Spielfigur ist Größe 1. Alle anderen Objekte wurden der Spielfigur angepasst. So sind der Endboss, Häuser und Bäume größer wie die Spielfigur. Der Brunnen und die Hecken sind ungefähr so hoch wie der Spieler. Die schwachen Monster sind kleiner wie der Spieler. Der Mittelpunkt des Koordinatensystems ist das Zentrum des Spielfeldes. Das Spielfeld liegt auf der x-y-Ebene.
| 10 | Event-System          | Zu Beginn wird über window.load die hndLoad Funktion aufgerufen, welche alle Funktionen für den Spielstart beinhaltet.Für die Buttons, auf dem Titelbildschirm, Steuerung, Einstellungen, GameOver- und GameWonScreen, wurde das „click“ Event verwendet. Für die Bewegung der Spielfigur wurde das Fudge Keyboard Event verwendet.
