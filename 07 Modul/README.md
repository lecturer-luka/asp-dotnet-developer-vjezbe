<div align="center">

<!-- title -->

# Modul 7 - Vježbe

<!-- description -->

Vježbe za uzorak repozitorija (eng.: Repository pattern) s C# kodom pomoću .NET 6 u web aplikaciji ASP.NET MVC predloška projekta aplikacije.

</div>


<!-- TOC -->

## Content

- [Repository obrazac](#repository-pattern)
- [Pogled & djelomični Pogled](view-partial-view)
- [HTML forma and Razor sintaksa](html-and-razor)
- [Domain Driven Design](#ddd)

<!-- CONTENT -->

## Repository obrazac

Uzorak repozitorija u C# je obrazac dizajna koji odvaja logiku koja pristupa podacima od poslovne logike u aplikaciji.

Osnovna ideja koja stoji iza uzorka Repository je osigurati sloj apstrakcije između pohrane podataka (kao što je baza podataka) i ostatka aplikacije. Umjesto izravnog pristupa pohrani podataka, aplikacija komunicira s repozitorijem, koji obrađuje detalje pohrane i dohvaćanja podataka.


## Pogled & djelomični Pogled

U C# web razvoju, `View` je predložak koji definira HTML i logiku prezentacije za renderiranje web stranice.

Pogled se može zamisliti kao način za odvajanje logike prezentacije web stranice od ostatka koda aplikacije. Obično sadrži HTML oznake i rezervirana mjesta za podatke koje će osigurati aplikacija.

S druge strane, djelomični pogled je višekratni dio pogleda koji se može uključiti u druge prikaze. To je u biti manji, samostalni `View` koji se može koristiti za prikaz određenog dijela web stranice.


## View Component

Komponenta prikaza (eng.: View Component) je način za odvajanje funkcionalnosti i logike prezentacije u samostalnu komponentu koja se može jednostavno ponovno upotrijebiti u više prikaza u web aplikaciji. To je u biti kombinacija radnje kontrolera i djelomičnog prikaza, koji se može koristiti za prikaz određenog dijela web stranice.

Komponente prikaza također se mogu koristiti za složenije funkcije, kao što je dohvaćanje podataka iz baze podataka ili upućivanje API poziva. Enkapsulacijom ove funkcionalnosti u samostalnu komponentu, svoj kod možete učiniti modularnijim i lakšim za održavanje.


## HTML forma and Razor sintaksa

HTML obrazac je način na koji korisnik može unijeti podatke i poslati ih web poslužitelju na obradu.

HTML obrasci se stvaraju pomoću oznake `<form>` u HTML-u i mogu sadržavati različita polja za unos kao što su tekstualni okviri, potvrdni okviri, radio gumbi i padajući izbornici. Kada korisnik pošalje obrazac, podaci koje je unio šalju se web poslužitelju kao HTTP zahtjev, koji se zatim može obraditi kodom na strani poslužitelja.

U C# web razvoju, Razor sintaksa je način za ugradnju koda na strani poslužitelja (kao što je C# kod) u HTML dokument. Razor sintaksa koristi se za generiranje dinamičkog sadržaja na web stranici, kao što je dohvaćanje podataka iz baze podataka i njihovo prikazivanje na stranici ili obrada podataka dostavljenih putem HTML obrasca.

Općenito, HTML obrasci i C# Razor sintaksa važni su alati za izgradnju dinamičnih, interaktivnih web aplikacija u C#. Omogućuju vam stvaranje web stranica koje mogu prihvatiti korisnički unos, obraditi podatke na poslužitelju i generirati dinamički sadržaj za prikaz na stranici.


## Domain Driven Design

Domain Driven Design (DDD) pristup je razvoju softvera koji se usredotočuje na izradu softvera koji blisko modelira problematičnu domenu stvarnog svijeta koju treba riješiti.

To znači da programeri moraju dobro razumjeti domenu za koju izrađuju softver i da bi softver koji izrađuju trebao biti u skladu s konceptima i terminologijom koja se koristi u toj domeni.

Sveukupno, Domain Driven Design je moćan pristup razvoju softvera koji naglašava važnost izrade softvera koji blisko odražava problematičnu domenu stvarnog svijeta koju treba riješiti. Izgradnjom softvera koji točno modelira domenu, programeri mogu stvoriti softver koji je lakši za razumijevanje, održavanje i razvoj tijekom vremena.


<!-- END CONTENT -->