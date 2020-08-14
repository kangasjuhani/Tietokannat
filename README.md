SQL TEHTÄVÄT

#### Tehtävä 4
>SELECT * FROM Kurssisuoritus 
#### Tehtävä 5
>SELECT kurssi FROM Kurssisuoritus
#### Tehtävä 6
>SELECT DISTINCT kurssi FROM Kurssisuoritus
#### Tehtävä 7
>SELECT * FROM Opiskelija Where nimi = 'Anna'
#### Tehtävä 8
>SELECT * FROM Kurssisuoritus WHERE opiskelija = 999999
#### Tehtävö 9
>SELECT  DISTINCT pääaine FROM Opiskelija WHERE pääaine LIKE '%tiede%'
#### Tehtävä 10
>SELECT Kurssi.nimi, Kurssisuoritus.päivämäärä, Kurssisuoritus.arvosana FROM Kurssi, Kurssisuoritus WHERE Kurssi.kurssitunnus = Kurssisuoritus.kurssi
#### Tehtävä 11
>SELECT nimi, päivämäärä, arvosana FROM Opiskelija, Kurssisuoritus
#### Tehtävä 12
>SELECT Kurssi.nimi AS kurssi, Tehtävä.nimi AS tehtävä FROM Kurssi, Tehtävä, Kurssitehtävä WHERE Kurssi.kurssitunnus = Kurssitehtävä.kurssi AND Kurssitehtävä.tehtävä = Tehtävä.tunnus
#### Tehävä 13
SELECT Kurssi.nimi AS kurssi, Tehtävä.nimi AS Tehtävä 
FROM Kurssi, Tehtävä, Kurssitehtävä, Opiskelija, Tehtäväsuoritus
WHERE Kurssi.kurssitunnus = Kurssitehtävä.kurssi 
AND Tehtävä.tunnus = Kurssitehtävä.tehtävä
AND Tehtäväsuoritus.tehtävä = Kurssitehtävä.tunnus
AND Tehtäväsuoritus.opiskelija = Opiskelija.opiskelijanumero
AND Opiskelija.nimi = 'Anna'
#### Tehtävä 14






