<div align="center">

<!-- title -->

# Osnovne vježbe s klasama u konzolnim aplikacijama

<!-- description -->

Skup vježbi pokriva osnovne vježbe za učenje korištenja try-catch blokova, nullbilnih tipova, aninomnih tipova, metoda i delegata u C#.

</div>


## Vježba 1

* Napisati program koji omogućava korisniku unos dva broja i izračunava njihov kvocijent. 
* Program treba obraditi moguće iznimke koje se mogu dogoditi prilikom unosa brojeva i izračunavanja kvocijenta te ispisati odgovarajuću poruku za svaku iznimku.
* U slučaju kad se dogodi iznimka moguće je ispisati sljedeća upozorenja ovisno o greški koja se dogodi:
    * `Dijeljenje s nulom nije dozvoljeno` - ako korisnik unese nulu kao djelitelj
    * `Unijeli ste nevaljan format broja.` - ako korisnik nije unio dobar tip podatka za izračun
    * `Pojavila se nepoznata greška` - ako nismo sigurni gdje je problem nastao


## Vježba 2

* Napisati program koji omogućava unos podataka o studentu, predavaču i tečaju te ispisuje informacije o njima. 
* Program treba obraditi moguće iznimke koje se mogu dogoditi prilikom unosa podataka te ispisati odgovarajuću poruku za svaku iznimku.
* U nastavku se nalazi primjer klasa:

```csharp
    class Student
    {
        public string Ime { get; set; }
        public string Prezime { get; set; }

        public Student(string ime, string prezime)
        {
            Ime = ime;
            Prezime = prezime;
        }

        public override string ToString()
        {
            return $"Ime: {Ime}, Prezime: {prezime}";
        }
    }

    class Predavac
    {
        public string Ime { get; set; }

        public Predavac(string ime)
        {
            Ime = ime;
        }

        public override string ToString()
        {
            return $"Ime: {Ime}";
        }
    }

    class Tecaj
    {
        public string Naziv { get; set; }

        public Tečaj(string naziv)
        {
            Naziv = naziv;
        }

        public override string ToString()
        {
            return $"Naziv: {Naziv}";
        }
    }
```

## Vježba 3

* Napisati program koji će rekreirati kolekciju u nastavku tako da kreirate novu varijablu anonimnog tipa i u njoj kreirate svojstva anonimnih tipova.
* Na primjer: 

```csharp
    var anonimno = new { Svojstvo1 = new { podaci o prvom studentu }, Svojstvo2 = new { podaci o drugom studentu }, itd... }
```

* Sljedeći set podataka je moguće koristiti kao primjer za vježbu:

```csharp
// Kolekcija testnih podataka klase Student
List<Student> studenti = new List<Student>
{
    new Student { Ime = "Ana", Predmet = "Matematika" },
    new Student { Ime = "Marko", Predmet = "Fizika" },
    new Student { Ime = "Ivana", Predmet = "Informatika" },
    new Student { Ime = "Luka", Predmet = "Glazbena kultura" },
    new Student { Ime = "Petra", Predmet = "Biologija" },
    new Student { Ime = "Ivan", Predmet = "Fizika" },
    new Student { Ime = "Maja", Predmet = "Glazbena kultura" },
    new Student { Ime = "Tomislav", Predmet = "Matematika" },
    new Student { Ime = "Lara", Predmet = "Glazbena kultura" },
    new Student { Ime = "Leo", Predmet = "Psihologija" },
    new Student { Ime = "Ema", Predmet = "Psihologija" },
    new Student { Ime = "Filip", Predmet = "Matematika" },
    new Student { Ime = "Marta", Predmet = "Psihologija" },
    new Student { Ime = "Karlo", Predmet = "Biologija" }
};

// Klasa Student
class Student
{
    public string Ime { get; set; }
    public string Predmet { get; set; }
}
```

* Program mora proizvoljno ispisati podatke o studentu i predmetu iz novonastale kolekciju anonimnih tipova.


## Vježba 4

* Napisati program koji će biti konzolna aplikacija u kojoj su kreirane tri klase `Circle`, `Rectangle` i `Triangle` koje implementiraju sučelje `IShape`.
* Sučelje `IShape` u sebi sadrži samo jednu metodu:
    * CalculateArea() - double
* Svaka klasa u sadrži sljedeća svojstva:
    * Radius - double
    * Width - double
    * Height - double
    * Base - double
* U glavnoj klasi `Program`  i metodu `Main()` potrebno je kreirati objekt svake klase i pozvati metoda za izračun površine.



## Vježba 5

* Napisati program za jednostavnu konzolnu aplikaciju u C# programskom jeziku koja koristi četiri klase, sučelje, nasljeđivanje, delegate i try-catch blokove.
* Definirane su četiri klase `Employee`, `Manager`, `Developer` i `Program`.
* Klase `Manager` i `Developer` nasljeđuju klasu `Employee` te implementiraju metodu `CalculateSalary()`.
* Koristeći delegat `SalaryCalculationDelegate`, pozivaju se metode za izračun plaće svakog zaposlenika. 
    * U `try-catch` blokovima moguće je uhvatiti sve iznimke prilikom izračuna plaće.
* Ovo su primjeri klasa:

```csharp

interface IEmployee
{
    void CalculateSalary();
}

class Employee : IEmployee
{
    public string Name { get; }
    public double BaseSalary { get; } 
}

class Manager : Employee
{
    public double Bonus { get; }

}

class Developer : Employee
{
    public int HoursWorked { get; }

}

```

* U glavnoj klasi `Program`  i metodu `Main()` potrebno je kreirati objekte klasa i pozvati metoda za izračun plaće.
