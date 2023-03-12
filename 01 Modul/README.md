<div align="center">

<!-- title -->

# Modul 1 - Vježbe

<!-- description -->

Vježbe za osnove pisanja C# koda i korištenja .NET 6 u predlošcima projekata konzolnih aplikacija.

</div>


<!-- TOC -->

## Contents

- [Varijable](#variables)
- [Uvjetne strukture](#conditional-statements)
- [Petlje](#loops)
- [Metode](#methods)
- [Klase i objekti](#classes-and-objects)
- [Nasljeđivanje](#inheritance)
- [Sučelja](#interfaces)

<!-- CONTENT -->

## Varijable

Varijable su spremnici za pohranjivanje vrijednosti podataka.
Svaka varijabla ima tip koji određuje koje se vrijednosti mogu pohraniti u varijablu.
C# je strogo tipiziran jezik i C# kompajler jamči da su vrijednosti pohranjene u varijablama uvijek odgovarajućeg tipa.


## Uvjetne strukture

Uvjetne strukture koriste se kada želimo izvršiti određenu radnju ovisno o dostupnom uvjetu.
Uvjetne strukture mogu se podijeliti na `if-else` i `switch-case`.


## Petlje

Petlje u C# se koriste za iteraciju stavki kolekcije ili za ponavljanje bloka koda dok se ne ispuni određeni uvjet.
Postoje četiri glavne vrste petlji u C#:


### `for` loop

Ova vrsta petlje se koristi kada znamo točan broj iteracija kojom želimo izvršiti blok koda. Ima tri dijela: inicijalizaciju, uvjet i inkrement.

```csharp
for (int i = 0; i < 10; i++)
{
    Console.WriteLine(i);
}
```


### `foreach`

Ova vrsta petlje omogućuje iteraciju preko kolekcije stavki kao što je niz (eng.: array), kolekcija (eng.: collection) ili drugi nabrojivi objekt (eng.: enumerable). Pojednostavljuje proces petlje kroz kolekciju automatskim rukovanjem iteracijom i omogućavanjem pristupa svakoj stavci u kolekciji.

```csharp
int[] numbers = { 1, 2, 3, 4, 5 };
foreach (int num in numbers)
{
    Console.WriteLine(num);
}
```


### `while` loop

Ova vrsta petlje se koristi kada želimo izvršiti blok koda dok je određeni uvjet istinit.

```csharp
int i = 0;

while (i < 10)
{
    Console.WriteLine(i);
    i++;
}
```


### `do-while` loop

Ova vrsta petlje slična je petlji `while`, osim što se blok koda izvršava barem jednom prije provjere uvjeta.

```csharp
int i = 0;

do
{
    Console.WriteLine(i);
    i++;
}
while (i < 10);
```


## Metode

Metoda je blok koda koji obavlja određeni zadatak.
Metode se koriste za izvođenje akcija ili izračuna i mogu se pozivati više puta iz različitih dijelova programa.

Metoda može imati naziv, parametre i vrstu podatka koju vraća. Naziv metode trebao bi odražavati ono što metoda radi. Parametri su vrijednosti koje se prosljeđuju metodi kada se pozove, a mogu se koristiti kao "input" u logiku metode. Tip metode specificira vrstu vrijednosti koju metoda vraća u kodu.

```csharp
public int Add(int num1, int num2)
{
    int sum = num1 + num2;
    return sum;
}

// How to call above method
int result = Add(2, 3);
```


## Klase i objekti

Klasa je poput nacrta ili predloška za stvaranje objekata.
Definira svojstva i ponašanja objekta.

Na primjer, klasa pod nazivom "Person" može imati svojstva kao što su "Name", "Age" i "Address" i metoda poput "Walk()" ili "Talk()".


Objekt je, s druge strane, instanca klase. To je poput objekta iz stvarnog svijeta stvorenog prema nacrtu.
Koristeći gornji primjer, ako stvorimo objekt iz klase "Person", mogli bismo stvoriti objekt pod nazivom "John" sa svojstvima kao što su "Name=John", "Age=30" i "Address=123 Main St", i uz pomoć objekta pozvati metode poput "Walk()" ili "Talk()".

```csharp
public class Person
{
    public string Name { get; set; }
    public int Age { get; set; }
    
    public void Walk()
    {
        Console.WriteLine("Walking...");
    }
    
    public void Talk()
    {
        Console.WriteLine("Talking...");
    }
}


// How you can create an object from the Person class
Person john = new Person();
john.Name = "John";
john.Age = 30;
john.Walk();
```


## Nasljeđivanje

Nasljeđivanje je mehanizam u C# koji omogućuje klasi da naslijedi svojstva, metode i polja od druge klase.
Klasa koja nasljeđuje naziva se izvedena klasa, dok se klasa od koje se nasljeđuje naziva bazna klasa.

Kada izvedena klasa naslijedi baznu klasu, ona automatski prima sva svojstva, metode i polja definirana u baznoj klasi. Izvedena klasa također može dodati dodatna svojstva, metode i polja koja su specifična za njezine potrebe.

Kod korištenja mehanizma nasljeđivanja obratite pozornost na modifikatore pristupa.


## Sučelja

Sučelje je nacrt za klasu.
Definira skup svojstava i metoda koje klasa mora implementirati.
Sučelje može sadržavati samo potpis metoda, svojstava, događaja ili indeksatora. Ne sadrži nikakvu implementaciju metoda ili svojstava.

Klasa koja implementira sučelje mora osigurati implementaciju za sve članove tog sučelja. Ovo osigurava da se klasa ponaša dosljedno s drugim klasama koje implementiraju isto sučelje.

<!-- END CONTENT -->