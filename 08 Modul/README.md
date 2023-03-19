<div align="center">

<!-- title -->

# Modul 8 - Vježbe

<!-- description -->

Vježbe za Entity Framework (Code First) pristup s C# kodom koristeći .NET 6 u Web App ASP.NET MVC predlošcima projekta aplikacije.

</div>

<!-- TOC -->

## Content

- [Entity Framework](#entity-framework)
- [Entity Framework (Code First)](entity-framework-code-first)
- [Entity Framework migracije](#entity-framework-migrations)
- [Entity Framework seeding](#entity-framework-seeding)
- [Entity Framework (Database First)](entity-framework-database-first)

<!-- CONTENT -->
## Entity Framework

Entity Framework popularan je okvir **objektno-relacijskog mapiranja (ORM)** koji programerima omogućuje rad s bazama podataka koristeći objektno orijentirani kod.

Uz Entity Frameworku, programeri mogu definirati model za svoju bazu podataka, koja se sastoji od klasa i svojstava koja se mapiraju u tablice i stupce u bazi podataka. Oni također mogu definirati odnose između entiteta, koji predstavljaju odnose između tablica u bazi podataka.

Entity Framework olakšava interakciju s bazama podataka pomoću sintakse LINQ (Language Integrated Query), koja programerima omogućuje pisanje upita na intuitivniji i čitljiviji način. Također pruža alate za stvaranje, ažuriranje i brisanje podataka u bazi podataka.


## Entity Framework (Code First)

U Entity Frameworku pristup **code first** način je stvaranja baze podataka iz C# klasa. Umjesto da prvo dizajnirate bazu podataka, a zatim kreirate klase koje se mapiraju u tablice, prvo kreirate klase, a EF generira shemu baze podataka za vas.

Da biste koristili pristup **code first**, definirate svoje klase sa svojstvima koja predstavljaju polja u vašim tablicama.
Također možete definirati odnose između svojih klasa, koji će se preslikati na strane ključeve u vašoj bazi podataka. Zatim koristite EF za stvaranje ili ažuriranje baze podataka na temelju vaših klasa.


## Entity Framework migrations

Migracije Entity Frameworka način su upravljanja promjenama vaše sheme baze podataka tijekom određenog vremena. Kada napravite promjene u svojim klasama entiteta, možete koristiti migracije za ažuriranje sheme vaše baze podataka kako bi odgovarala tim promjenama. Migracije vam omogućuju da pratite promjene koje napravite na svojoj shemi tijekom vremena i jednostavno primijenite te promjene na druga okruženja.


## Entity Framework seeding

Entity Framework **seeding** je proces u kojem možete popuniti bazu podataka početnim podacima pomoću koda, umjesto ručnog unosa podataka u bazu podataka. Ovo može biti korisno ako želite osigurati da vaša aplikacija uvijek ima iste početne podatke kada se pokreće ili ako želite automatizirati proces dodavanja podataka u vašu bazu podataka.


## Entity Framework (Database first)

U Entity Frameworku pristup **database first** odnosi se na stvaranje podatkovnog modela temeljenog na postojećoj bazi podataka. Drugim riječima, shema baze podataka koristi se za generiranje modela Entity Framework.


<!-- END CONTENT -->