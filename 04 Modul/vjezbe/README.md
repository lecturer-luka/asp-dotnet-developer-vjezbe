<div align="center">

<!-- title -->

# Osnovne vježbe za LINQ u konzolnim aplikacijama

<!-- description -->

Skup vježbi pokriva osnovne vježbe za učenje LINQ upita.

</div>

## Vježba 1:

* Kreirati konzolnu aplikaciju.
* Kreirati klase modela na temelju kolekcija u nastavku:

```chasrp
List<Odjel> odjeli = new List<Odjel>
{
    new Odjel { Id = 1, Naziv = "Informatika" },
    new Odjel { Id = 2, Naziv = "Dizajn" },
    new Odjel { Id = 3, Naziv = "Marketing" },
    new Odjel { Id = 4, Naziv = "Serveri" }
};

List<Zaposlenik> zaposlenici = new List<Zaposlenik>
{
    new Zaposlenik { ImePrezime = "Mićo Programerić", Email = "mico@email.com", Telefon = "0981234567", Adresa = "Stara Cesta bb", OdjelId = 1, Dob = 34, Placa = 4658.11 },
    new Zaposlenik { ImePrezime = "Martina Programerić", Email = "martina@email.com", Telefon = "091234567", Adresa = "Mala plaža 11", OdjelId = 3, Dob = 28, Placa = 90456.00 },
    new Zaposlenik { ImePrezime = "Ana Dizajnerić", Email = "ana@email.com", Telefon = "099123456", Adresa = "Vukovarska 33", OdjelId = 2, Dob = 34, Placa = 11549.00 },
    new Zaposlenik { ImePrezime = "Ivo Sistemovski", Email = "ivo@email.com", Telefon = "098716363", Adresa = "Pavlov put 5c", OdjelId = 4, Dob = 18, Placa = 6430.77 },
    new Zaposlenik { ImePrezime = "Mirna Kodić", Email = "mirna@email.com", Telefon = "091273621", Adresa = "Mala plaža 4c", OdjelId = 1, Dob = 28, Placa = 876.00 },
    new Zaposlenik { ImePrezime = "Ana Marija Vitar", Email = "ana.marija@email.com", Telefon = "0962616623", Adresa = "Mala plaža 9", OdjelId = 1, Dob = 19, Placa = 1468.77 },
    new Zaposlenik { ImePrezime = "Ivona Mreža", Email = "ivona@email.com", Telefon = null, Adresa = "Planina 4c", OdjelId = 2, Dob = 19, Placa = 650.00 },
    new Zaposlenik { ImePrezime = "Patrik Mrežić", Email = "patrik@email.com", Telefon = null, Adresa = "Visoki most bb", OdjelId = 2, Dob = 35, Placa = 24765.88 },
    new Zaposlenik { ImePrezime = "Ivan Marko Prodajić", Email = "ivan.marko@email.com", Telefon = null, Adresa = "Stara Cesta bb", OdjelId = 3, Dob = 18, Placa = 5973.22 },
    new Zaposlenik { ImePrezime = "Pero Validovski", Email = "pero@email.com", Telefon = "097552413", Adresa = "Osnovna cesta 3", OdjelId = 3, Dob = 34, Placa = 45965.09 },
    new Zaposlenik { ImePrezime = "Marko Programerić", Email = "marko@email.com", Telefon = null, Adresa = "Otočni put 2", OdjelId = 1, Dob = 20, Placa = 1300.00 },
};
```

## Vježba 2

* Dohvati prvi element iz kolekcije odjela koji počinje sa slovom "t", ako element ne postoji ispiši tekst da ne postoji.

## Vježba 3

* Dohvati posljednji element iz kolekcije odjela koji počinje sa slovom "m", ako element ne postoji ispiši tekst da ne postoji.

## Vježba 4

* Dohvati prvi element iz kolekcije zaposlenika koji u sebi ima slovo "r". Kao rezultat vrati rezultat tipa `string` i u varijablu spremi ime i prezime zaposlenika.

## Vježba 5

* Dohvati posljednji element iz kolekcije zaposlenika koji u sebi ima slovo "o".

## Vježba 6

* Pronađi sve zaposlenike koji su u odjelu s ID-em `2`. Kao rezultat vrati tip generičke kolekcije `List<Zaposlenik>` s listom zaposlenika tog odjela. Ako rezultat ne postoji ispiši tekst da ne postoji.

## Vježba 7

* Pronađi odjel s šifrom `11`, ako postoji ispiši naziv odjela, ako ne postoji ispiši tekst da ne postoji.

## Vježba 8

* Pronađi sve zaposlenike čija adresa počinje slovom "s" ili "p", grupiraj ih po godinama i ispiši na ekran.

## Vježba 9

* Pronađi sve zaposlenike s manjom plaćom od `1000` eura, grupiraj ih po adresi i ispiši na ekran. Ako rezultati ne postoje, ispiši da ne postoji niti jedan zaposlenik s tim kriterijem.

## Vježba 10

* Pronađi sve zaposlenike u odijelima informatike i marketinga, grupiraj ih po godinama.

## Vježba 11

* Pronađi sve zaposlenike starije od `30` godina, grupiraj ih po odjelu i kao rezultat vrati kolekciju anonimnih objekata sa svojstvom "Ime" u koje će biti pohranjeno ime zaposlenika.

## Vježba 12

* Pronađi sve zaposlenike mlađe od `30` godina, grupiraj ih po godinama i kao rezutat vrati kolekciju anonimnih objekata sa svojstvom "Zaposlenik" u koje će biti pohranjen objekt klase zaposlenik s podacima o zaposleniku.









