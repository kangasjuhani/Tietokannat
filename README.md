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
>SELECT Opiskelija.nimi, Kurssisuoritus.päivämäärä, Kurssisuoritus.arvosana FROM Opiskelija, Kurssisuoritus WHERE Opiskelija.opiskelijanumero = Kurssisuoritus.opiskelija 
#### Tehtävä 12
>SELECT Kurssi.nimi AS kurssi, Tehtävä.nimi AS tehtävä FROM Kurssi, Tehtävä, Kurssitehtävä WHERE Kurssi.kurssitunnus = Kurssitehtävä.kurssi AND Kurssitehtävä.tehtävä = Tehtävä.tunnus
#### Tehävä 13
>SELECT Kurssi.nimi AS kurssi, Tehtävä.nimi AS Tehtävä 
FROM Kurssi, Tehtävä, Kurssitehtävä, Opiskelija, Tehtäväsuoritus
WHERE Kurssi.kurssitunnus = Kurssitehtävä.kurssi 
AND Tehtävä.tunnus = Kurssitehtävä.tehtävä
AND Tehtäväsuoritus.tehtävä = Kurssitehtävä.tunnus
AND Tehtäväsuoritus.opiskelija = Opiskelija.opiskelijanumero
AND Opiskelija.nimi = 'Anna'
#### Tehtävä 14
>Toisessa etitään pelkät tehtävät ja toisessa oppilaat
#### Tehtävä 15
>SELECT nimi FROM kurssi k WHERE k.kurssitunnus NOT IN (SELECT kurssi FROM kurssitehtävä)

>SELECT nimi FROM kurssi k LEFT JOIN Kurssitehtävä t ON k.kurssitunnus=t.kurssi WHERE t.tunnus IS NULL
#### Tehtävä 16
>SELECT Kurssi.nimi AS kurssi, COUNT (Kurssisuoritus.arvosana) AS lukumäärä FROM Kurssisuoritus, Kurssi WHERE Kurssi.kurssitunnus = Kurssisuoritus.kurssi GROUP BY Kurssi.nimi
#### Tehtävä 17
>SELECT Kurssi.nimi AS kurssi, COUNT(Kurssisuoritus.kurssi) AS lukumäärä FROM Kurssi LEFT JOIN Kurssisuoritus
    ON Kurssi.kurssitunnus = Kurssisuoritus.kurssi GROUP BY Kurssi.nimi
#### Tehtävä 18
>CREATE TABLE Kurssi(kurssitunnus, nimi, kuvaus)
#### Tehtävä 19
>INSERT INTO Kurssi(kurssitunnus, nimi, kuvaus)
VALUES("SQL-kielen perusteet","12345","SELECT'Hei maailma';")
#### Tehtävä 20
>CREATE TABLE Infotest(opiskelijanumero integer, nimi varchar(40), syntymävuosi varchar(200), pääaine varchar(30))

>PRAGMA TABLE_INFO(Infotest)

#### Tehtävä 21
>CREATE TABLE Kurssi(kurssitunnus integer, nimi varchar(10000000), kuvaus varchar(100000000))


#### Tehtävä 22
>Se tekee kaikille opiskelijoille oman opiskelijanumeron

#### Tehtävä 23
>CREATE TABLE Kurssi(kurssitunnus integer PRIMARY KEY,nimi varchar(10000),kuvus varchar(1000000))

#### Tehtävä 24
>CREATE TABLE Tehtävä (tunnus integer PRIMARY KEY , nimi varchar(100) , kuvaus varchar(100));


CREATE TABLE Kurssitehtävä (tunnus integer PRIMARY KEY, tehtävä integer, nimi varchar(50), kuvaus varchar(200),
FOREIGN KEY(tehtävä) REFERENCES Tehtävä(tunnus)
);
#### Tehtävä 25
INSERT INTO Tehtävä(nimi, kuvaus) VALUES ('pablo esocbar','Myy huumeita')

#### Tehtävä 26
ALTER TABLELLA voi muakata tauluja esim jos haluat lisätä sarakkeen tauluun
>ALTER TABLE Oppilas
ADD Cringe Integer;








