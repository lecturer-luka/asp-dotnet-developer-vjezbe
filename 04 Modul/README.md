<div align="center">

<!-- title -->

# Modul 4 - Vježbe

<!-- description -->

Vježbe za pisanje integriranog upita (LINQ) za C# kod i korištenje .NET 6 u predlošcima projekta konzolne aplikacije.

</div>


<!-- TOC -->

## Content

- [LINQ](#linq)
- [LINQ i Entity Framework](#linq-and-ef)

<!-- CONTENT -->

## LINQ

LINQ (Language Integrated Query) značajka je jezika C# koja vam omogućuje izvođenje podatkovnih upita izravno u vašem kodu koristeći sintaksu sličnu SQL-u. Omogućuje vam rad sa zbirkama podataka, kao što su nizovi ili kolekcije, na način koji je učinkovitiji i izražajniji od tradicionalne petlje.

Pomoću LINQ-a možete filtrirati, sortirati, grupirati i transformirati podatke na razne načine. Možete koristiti LINQ za postavljanje upita podacima iz različitih izvora, kao što su baze podataka, XML datoteke ili drugi objekti. Rezultati LINQ upita vraćaju se kao nova zbirka objekata kojima možete manipulirati ili ih prikazati.

LINQ upiti imaju dva načina pisanja: `query syntax` ili `method syntax`.

Jednostavan primjer:

```csharp
int[] numbers = { 3, 7, 12, 15, 18, 21 };
var result = from num in numbers
             where num > 10 && num % 2 == 0
             select num;
```


## LINQ and Entity Framework

U Entity Frameworku programeri mogu koristiti LINQ za postavljanje upita bazi podataka i dohvaćanje podataka na intuitivniji način od pisanja SQL upita. LINQ upiti napisani su korištenjem C# sintakse i Entity Framework ih prevodi u SQL upite.

Jednostavan primjer:

```csharp
var context = new MyDbContext();
var students = from s in context.Students
               where s.Grade > 80
               orderby s.LastName
               select s;
```

<!-- END CONTENT -->