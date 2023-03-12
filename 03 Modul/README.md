<div align="center">

<!-- title -->

# Modul 3 - Vježbe

<!-- description -->

Vježbe za neke od naprednih pisanja C# koda i korištenje .NET 6 u predlošcima projekata konzolnih aplikacija.

</div>


<!-- TOC -->

## Contents

- [Try-Catch blokovi](#try-catch-statements)
- [Nullable tipovi](#nullable-value-types)
- [Anonimni tipovi i metode](#anonymous-types-methods)
- [Delegati](#delegates)
- [Eventi](#events)

<!-- CONTENT -->

## Try-Catch blokovi

Blokovi Try-catch koriste se za rukovanje iznimkama ili pogreškama koje se mogu pojaviti tijekom izvođenja programa.

Blok "try" sadrži kod koji bi mogao izazvati iznimku, dok se blok "catch" koristi za obradu iznimke i pružanje načina za oporavak od nje. Ako je iznimka bačena u bloku "try", program će odmah skočiti na odgovarajući blok "catch".

```csharp
try
{
    // Programski kod koji bi mogao izbaciti iznimku
}
catch(Exception e)
{
    // Ovdje obradite iznimku ako je uhvaćena
}
```


## Nullable vrijednosni tipovi

Vrijednosni tipovi su tipovi koji izravno drže vrijednosti, za razliku od referentnih tipova koji sadrže referencu na memorijsku lokaciju na kojoj je vrijednost pohranjena. Vrijednosni tipovi uključuju, između ostalog, cijele brojeve, brojeve s pomičnim zarezom i booleove vrijednosti.

Nullable vrijednosni tip omogućuje da varijabli tipa dodijelite null, što inače nije moguće.
Na primjer, vrijednost cijelog broja ne može biti null prema zadanim postavkama, ali cijeli broj koji može biti null može biti null. Ovo je korisno kada trebate predstaviti odsutnost vrijednosti, kao u slučajevima kada je vrijednost izborna ili nepoznata.

Da biste deklarirali tip nullable u C#, koristite simbol `?` nakon tipa podatka. 
Na primjer, `int? myNullableInt = null;` deklarira `nullable integer` varijablu koja se zove `myNullableInt` kojoj je dodijeljena null vrijednost.

Možete provjeriti je li tip vrijednosti null pomoću svojstva `HasValue`. Na primjer, `if(myNullableInt.HasValue)` provjerava ima li `myNullableInt` dodijeljenu vrijednost.

Da biste dohvatili vrijednost nullable tipa podatka, koristite svojstvo `Value`, ali morate prvo provjeriti ima li vrijednost, inače ćete dobiti `InvalidOperationException`. 
Na primjer, `int myInt = myNullableInt.Value;` dohvaća vrijednost `myNullableInt`, ali samo ako mu je dodijeljena vrijednost.


## Delegati

Delegat je tip koji predstavlja referencu na metodu s određenim popisom parametara i tipom povrata. Jednostavnije rečeno, delegat je poput pokazivača na metodu koja se može proslijediti kao parametar ili pohraniti kao varijabla.

Delegati su korisni kada želite proslijediti metodu kao argument drugoj metodi ili kada želite dodijeliti metodu varijabli. Obično se koriste za rukovanje događajima, gdje možete definirati vrstu delegata za događaj, a zatim registrirati metode koje će se pozvati kada se događaj dogodi.

Primjer deklaracije delegata:

```csharp
delegate int MyDelegate(int x, int y);
```

Primjer korištenja delegata:

```csharp
int Add(int x, int y) {
    return x + y;
}

int Multiply(int x, int y) {
    return x * y;
}

MyDelegate myDelegate = Add;
int result = myDelegate(3, 4); // result is 7

myDelegate = Multiply;
result = myDelegate(3, 4); // result is 12
```


## Anonimni tipovi i metode

Anonimni tipovi omogućuju definiranje novog tipa u hodu, bez potrebe za eksplicitnim definiranjem tipa. Umjesto toga, možete koristiti mehanizam za automatsko određivanje tipa. 
Možete stvoriti anonimni tip korištenjem ključne riječi `new` nakon koje slijedi inicijalizator objekta. Tip objekta određuje kompajler na temelju svojstava koja postavite.

```csharp
var person = new { Name = "John", Age = 25 };
```

Vrijednostima ovih svojstava možemo pristupiti pomoću notacije s točkama:

```csharp
Console.WriteLine(person.Name);
Console.WriteLine(person.Age);
```

Anonimne metode slične su lambda izrazima po tome što vam omogućuju definiranje bloka koda bez potrebe za stvaranjem zasebne metode. Korisni su kada trebate proslijediti delegat kao parametar, ali ne želite stvoriti zasebnu metodu za njega.

```csharp
delegate int MyDelegate(int x, int y);

MyDelegate del = delegate(int x, int y) {
    return x + y;
};
```

Delegata možemo pozvati ovako:

```csharp
int result = del(3, 5);
Console.WriteLine(result); // Output: 8
```


## Eventi

Događaj je obavijest koju šalje objekt kako bi signalizirao neke radnje. Događaji vam omogućuju da odgovorite na akcije koje poduzima korisnik ili sustav, poput klikova mišem ili dodavanja podataka u bazu podataka.

Da biste koristili događaje u C#, trebate definirati tip delegata koji specificira potpis rukovatelja događajima (eng.: event handler). Tip delegata definira potpis metode rukovatelja događajem, a to je metoda koja se poziva kada se događaj pokrene.

Da biste pokrenuli događaj, koristite ključnu riječ `event` da definirate događaj kao člana klase, a zatim pozivate metodu rukovatelja događajem kroz događaj. Kada se događaj pokrene, sve registrirane metode rukovatelja događajima izvršavaju se redom.

<!-- END CONTENT -->