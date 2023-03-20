<div align="center">

<!-- title -->

# Osnovne vježbe za Entity Framework Core (code first) u web aplikaciji ASP.NET MVC

<!-- description -->

Skup vježbi pokriva najosnovnije načine pristupa **code first**. Definirajte svoje klase sa svojstvima koja predstavljaju stupce u vašim tablicama. Definirajte odnose između svojih klasa i koristite atribute za stvaranje primarnih/stranih ključeva u vašoj bazi podataka.

	* C# Data Annotations značajka je okvira .NET koja programerima omogućuje primjenu metapodataka na svojstva klase kako bi potvrdili ili opisali podatke.
	* To znači da svojstvu klase možete dodati posebne atribute kako biste odredili određena pravila koja podaci moraju slijediti, kao što su minimalna i maksimalna duljina, je li svojstvo potrebno ili kojeg je tipa podatak.
</div>

	* The examples below use MS SQL server databases.


## Exercise 1

1. Kreirajte novu ASP.NET Core MVC aplikaciju koristeći Visual Studio ili Visual Studio Code.
2. Instalirajte pakete Entity Framework Core:
	* Microsoft.EntityFrameworkCore
	* Microsoft.EntityFrameworkCore.Tools
	* Microsoft.EntityFrameworkCore.SqlServer
3. Dodajte novu klasu modela pod nazivom `Book` sa svojstvima kao što su:
	* Id (int)
	* Title (string),
	* Author (string),
	* PublicationDate (int),
	* Genre (string)
4. Uz pomoć `Data Annotations` unutar klase `Book` koristite atribute za definiranje primarnog ključa i potrebnih svojstava.
5. Dodajte novu klasu `DbContext` pod nazivom `BookDbContext` i upotrijebite svojstvo `DbSet` za definiranje tablice u bazi podataka.
6. U `Program.cs` ažurirajte servis `AddDbContext` da koristite opcije `UseSqlServer` s vašim `connection stringom`.
7. Upotrijebite naredbu `Add-Migration` u `Package Manager Console` da biste kreirali migraciju koja opisuje promjene koje ste napravili na svojim klasama entiteta.
	* naredba `dotnet ef migrations add` ako koristite CLI.
8. Upotrijebite naredbu `Update-Database` u `Package Manager Console` da primijenite migraciju na svoju bazu podataka.
	* naredba `dotnet ef database update` ako koristite CLI.
9. Provjerite je li tablica `Book` ispravno kreirana u vašoj bazi podataka.


## Exercise 2

1. Kreirajte novu ASP.NET Core MVC aplikaciju koristeći Visual Studio ili Visual Studio Code.
2. Instalirajte pakete Entity Framework Core:
	* Microsoft.EntityFrameworkCore
	* Microsoft.EntityFrameworkCore.Tools
	* Microsoft.EntityFrameworkCore.SqlServer
3. Dodajte novu klasu modela pod nazivom `Car` sa svojstvima kao što su:
	* Id (int)
    * Make (string),
    * Model (string),
    * Year (int),
    * Color (string),
    * Price (decimal)
4. Uz pomoć `Data Annotations` unutar klase `Car` koristite atribute za definiranje primarnog ključa i potrebnih svojstava.
5. Dodajte novu klasu `DbContext` pod nazivom `CarDbContext` i upotrijebite svojstvo `DbSet` za definiranje tablice u bazi podataka.
6. U `Program.cs` ažurirajte servis `AddDbContext` da koristite opcije `UseSqlServer` s vašim `connection stringom`.
7. Upotrijebite naredbu `Add-Migration` u `Package Manager Console` da biste kreirali migraciju koja opisuje promjene koje ste napravili na svojim klasama entiteta.
	* naredba `dotnet ef migrations add` ako koristite CLI.
8. Upotrijebite naredbu `Update-Database` u `Package Manager Console` da primijenite migraciju na svoju bazu podataka.
	* naredba `dotnet ef database update` ako koristite CLI.
9. Provjerite je li tablica `Car` ispravno kreirana u vašoj bazi podataka.


## Exercise 3

1. Kreirajte novu ASP.NET Core MVC aplikaciju koristeći Visual Studio ili Visual Studio Code.
2. Instalirajte pakete Entity Framework Core:
	* Microsoft.EntityFrameworkCore
	* Microsoft.EntityFrameworkCore.Tools
	* Microsoft.EntityFrameworkCore.SqlServer
3. Kreirajte klasu modela `BeerStyle`:
	* Id (int)
	* Name (string)
4. Kreirajte klasu modela `Beer`:
	Id (int)
	Name (string)
	Price (decimal)
	BeerStyleId (int)
	BeerStyle (BeerStyle)
5. Uz pomoć `Data Annotations` unutar klasa `Beer` i `BeerStyle` koristite atribute za definiranje primarnih ključeva, potrebnih svojstava i tipova podataka.
6. Dodajte novu klasu `DbContext` pod nazivom `BeerDbContext` i upotrijebite svojstvo `DbSet` za definiranje tablice u bazi podataka.
7. U `Program.cs` ažurirajte servis `AddDbContext` da koristite opcije `UseSqlServer` s vašim `connection stringom`.
8. Upotrijebite naredbu `Add-Migration` u `Package Manager Console` da biste kreirali migraciju koja opisuje promjene koje ste napravili na svojim klasama entiteta.
	* naredba `dotnet ef migrations add` ako koristite CLI.
9. Upotrijebite naredbu `Update-Database` u `Package Manager Console` da primijenite migraciju na svoju bazu podataka.
	* naredba `dotnet ef database update` ako koristite CLI.
10. Provjerite jesu li tablice `Beer` i `BeerStyle` ispravno kreirane u vašoj bazi podataka.

## Exercise 4

1. Kreirajte novu ASP.NET Core MVC aplikaciju koristeći Visual Studio ili Visual Studio Code.
2. Instalirajte pakete Entity Framework Core:
	* Microsoft.EntityFrameworkCore
	* Microsoft.EntityFrameworkCore.Tools
	* Microsoft.EntityFrameworkCore.SqlServer
3. Kreirajte klasu modela `Autor`:
	* Id (int)
	* Name (string) 
	* Books (List<Book>)
4. Napravite klasu modela `Book`:
	Id (int)
	Title (string)
	ISBN (string) // ISBN stands for "International Standard Book Number"
	Year (int)
	AuthorId (int)
	Author (Author)
5. Uz pomoć `Data Annotations` unutar klasa `Book` i `Author` koristite atribute za definiranje primarnih ključeva, potrebnih svojstava i tipova podataka.
6. Dodajte novu klasu `DbContext` pod nazivom `BookDbContext` i upotrijebite svojstvo `DbSet` za definiranje tablice u bazi podataka.
7. U `Program.cs` ažurirajte servis `AddDbContext` da koristite opcije `UseSqlServer` s vašim `connection stringom`.
8. Upotrijebite naredbu `Add-Migration` u `Package Manager Console` da biste kreirali migraciju koja opisuje promjene koje ste napravili na svojim klasama entiteta.
	* naredba `dotnet ef migrations add` ako koristite CLI.
9. Upotrijebite naredbu `Update-Database` u `Package Manager Console` da primijenite migraciju na svoju bazu podataka.
	* naredba `dotnet ef database update` ako koristite CLI.
10. Provjerite jesu li tablice `Book` i `Author` ispravno kreirane u vašoj bazi podataka.