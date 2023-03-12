<div align="center">

<!-- title -->

# Modul 2 - Vježbe

<!-- description -->

Vježbe za osnove korištenja SQL baze podataka.

</div>


<!-- TOC -->

## Content

- [Dijagram baze podataka](#database-diagram)
- [Normalizacija](#normalization)
- [SQL](#sql)

<!-- CONTENT -->

## Database diagram

Dijagram SQL baze podataka vizualni je prikaz tablica, odnosa i ograničenja u bazi podataka.

To je način dizajniranja i dokumentiranja baze podataka na jasan i organiziran način.
Dijagram uključuje okvire za tablice, linije koje povezuju okvire za predstavljanje odnosa između tablica i simbole za prikaz ključeva, indeksa i drugih objekata baze podataka.

Dijagram mogu koristiti dizajneri baza podataka, programeri i administratori kako bi razumjeli strukturu baze podataka i izvršili izmjene u njoj. Također se može koristiti za priopćavanje dizajna baze podataka drugima koji će možda morati koristiti ili modificirati bazu podataka.


## Normalization

SQL normalizacija je proces organiziranja podataka u bazi podataka kako bi se uklonila redundantnost i poboljšao integritet podataka. Jednostavno rečeno, to je skup pravila koja pomažu u dizajniranju baze podataka koja je učinkovita i organizirana. Svrha normalizacije je eliminirati svaku redundantnost podataka i osigurati da su podaci pohranjeni logično, učinkovito i dosljedno.

Postoje različite razine normalizacije:
* Prvi normalni oblik (1NF): osigurava da svaka tablica ima primarni ključ i da svaki stupac sadrži atomske vrijednosti (tj. ne viševrijedne).
* Drugi normalni oblik (2NF): Zahtijeva da je tablica u 1NF i da svaki stupac bez ključa ovisi o primarnom ključu.
* Treći normalni oblik (3NF): Zahtijeva da je tablica u 2NF i da nema tranzitivnih ovisnosti.


Proces normalizacije važan je jer pomaže u smanjenju redundantnosti podataka i nedosljednosti, što može dovesti do nedosljednosti podataka, problema s izvedbom i anomalija ažuriranja. Dobro normaliziranu bazu podataka lakše je održavati i ažurirati te pruža bolju osnovu za analizu podataka i izvješćivanje.

## SQL

SQL (Structured Query Language) je programski jezik koji se koristi za upravljanje i manipuliranje podacima u sustavu upravljanja relacijskom bazom podataka (RDBMS).

Jednostavno rečeno, SQL se koristi za stvaranje, modificiranje i izdvajanje podataka iz baze podataka. Korisnicima omogućuje interakciju s podacima pohranjenima u bazi podataka izvođenjem različitih operacija poput stvaranja tablica, umetanja podataka u tablice, ažuriranja postojećih podataka i brisanja podataka iz tablica.

SQL koristi skup naredbi ili upita za izvođenje ovih operacija. Ovi se upiti koriste za manipuliranje podacima u bazi podataka, dohvaćanje podataka iz baze podataka i izvođenje izračuna podataka. SQL također nudi različite značajke poput filtriranja podataka, sortiranja i grupiranja.

SQL se široko koristi u raznim aplikacijama i industrijama, uključujući web razvoj, analizu podataka i poslovnu inteligenciju. To je moćan i fleksibilan jezik koji korisnicima omogućuje učinkovito i djelotvorno upravljanje i manipuliranje podacima.

<!-- END CONTENT -->