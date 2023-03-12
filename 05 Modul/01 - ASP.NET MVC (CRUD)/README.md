<div align="center">

<!-- title -->

# Osnovne vježbe za Web App ASP.NET MVC

<!-- description -->

Popis vježbi za manipulaciju podacima u MVC arhitekturi. Vježbe vas uče kako izraditi osnovne CRUD web aplikacije.

</div>

## Vježba 1

1. Stvorite novu ASP.NET Core MVC aplikaciju koristeći Visual Studio ili Visual Studio Code.
2. Dodajte novu klasu modela pod nazivom "Book" sa svojstvima kao što su:
	* Id (int)
	* Title (string),
	* Author (string),
	* PublicationDate (int),
	* Genre (string)
3. Stvorite novi kontroler pod nazivom "BookController" s akcijama kao što su "Index", "Create", "Edit" i "Delete".
4. U akciji "Index" dohvatite popis knjiga iz izvora podataka (npr. JSON datoteka ili hard-kodirana kolekcija) i proslijedite ga odgovarajućem pogledu za prikaz.
5. U akciji "Create" prikažite HTML obrazac kako biste korisnicima omogućili unos pojedinosti o novoj knjizi, zatim je spremite u izvor podataka i preusmjerite na akciju "Index" za prikaz ažuriranog popisa.
6. U akciji "Edit", dohvatite pojedinosti knjige prema ID-u, prikažite HTML obrazac s unaprijed popunjenim trenutnim vrijednostima, dopustite korisnicima da ih uređuju i spremite ažuriranu knjigu u izvor podataka, zatim preusmjerite na akciju "Index" za prikaz ažuriranog popisa.
7. U akciju "Delete", dohvatite pojedinosti knjige prema njezinom ID-u, prikažite poruku potvrde za brisanje, zatim je izbrišite iz izvora podataka i preusmjerite na akciju "Index" za prikaz ažuriranog popisa.


## Vježba 2

1. Stvorite novu ASP.NET Core MVC aplikaciju koristeći Visual Studio ili Visual Studio Code.
2. Dodajte novu klasu modela pod nazivom "Car" sa svojstvima kao što su:
	* Id (int)
    * Make (string),
    * Model (string),
    * Year (int),
    * Color (string),
    * Price (decimal)
3. Stvorite novi kontroler pod nazivom "CarController" s akcijama kao što su "Index", "Create", "Edit" i "Delete".
4. Koristite sljedeće demo podatke za svoje akcije kontrolera:
	```csharp
	List<Car> demoCarData = new List<Car> {
		new Car {Id = 11, Make = Toyota, Model = Corolla, Year = 2020, Color = Gray, Price = 25000},
		new Car {Id = 12, Make = Honda, Model = Civic, Year = 2021, Color = Red, Price = 28000},
		new Car {Id = 15, Make = Ford, Model = F-150, Year = 2018, Color = Blue, Price = 35000},
		new Car {Id = 16, Make = BMW, Model = X5, Year = 2019, Color = Black, Price = 50000},
		new Car {Id = 20, Make = Chevrolet, Model = Camaro, Year = 2016, Color = Yellow, Price = 42000}
	};
	```
5. U akciji "Index", dohvatite popis automobila iz izvora podataka i proslijedite ga odgovarajućem pogledu za prikaz.
6. U akciji "Create" prikažite HTML obrazac kako biste korisnicima omogućili unos pojedinosti o novom automobilu, zatim ga spremite u izvor podataka i preusmjerite na akciju "Index" za prikaz ažuriranog popisa.
7. U akciji "Edit", dohvatite pojedinosti o automobilu prema njegovom ID-u, prikažite HTML obrazac s unaprijed popunjenim trenutačnim vrijednostima, dopustite korisnicima da ih uređuju i spremite ažurirani automobil u izvor podataka, zatim preusmjerite na "Index" akciju za prikaz ažuriranog popisa.
8. U akciji "Delete", dohvatite pojedinosti o automobilu prema ID-u, prikažite poruku potvrde o brisanju, zatim ga izbrišite iz izvora podataka i preusmjerite na akciju "Index" za prikaz ažuriranog popisa.


## Vježba 3

1. Stvorite novu ASP.NET Core MVC aplikaciju koristeći Visual Studio ili Visual Studio Code.
2. Dodajte novu klasu modela "Football" u mapu "Models" sa sljedećim svojstvima:
	* Id (int)
	* TeamName (string)
	* Country (string)
	* Stadium (string)
	* Founded (int)
3. Stvorite novu klasu kontrolera "FootballController" s akcijskom metodom "Index".
4. U akciji "Index" stvorite objekt `List<Football>` i popunite ga nekim lažnim podacima (npr. 5 objekata klase Football).
5. Proslijedite objekt `List<Football>` u odgovarajući pogled "Index".
6. Stvorite novi pogled "Index.cshtml" u mapi Views/Football i prikažite podatke o nogometu u obliku tablice.
7. Dodajte novu akciju "Details" u "FootballController" i odgovarajući prikaz "Details.cshtml" u mapi Views/Football.
8. U akciji "Details" dohvatite objekt klase Football s navedenim ID-om (proslijeđenim kao parametar).
9. Proslijedite Football objekt u pogled "Details".
10. U pogledu "Details" prikažite detalje podataka objekta na jednostavan način.


## Vježba 4

1. Stvorite novu ASP.NET Core MVC aplikaciju koristeći Visual Studio ili Visual Studio Code.
2. Dodajte novu klasu modela "Beer" u mapu "Models" sa sljedećim svojstvima:
	* Id (int)
	* Name (string)
	* Type (string)
	* AlcoholPercentage (double)
	* Brewery (string)
	* Country (string)
3. Koristite sljedeće demo podatke za akcije kontrolera:
	```csharp
	IEnumerable<Beer> beers = new List<Beer>
	{
		new Beer { Id = 1001, Name = "Heineken", Type = "Lager", AlcoholPercentage = 5, Brewery = "Heineken International", Country = "Netherlands" },
		new Beer { Id = 1002, Name = "Guinness", Type = "Stout", AlcoholPercentage = 4.2, Brewery = "Guinness & Co.", Country = "Ireland" },
		new Beer { Id = 1003, Name = "Corona", Type = "Lager", AlcoholPercentage = 4.5, Brewery = "Grupo Modelo", Country = "Mexico" },
		new Beer { Id = 1004, Name = "Budweiser", Type = "Lager", AlcoholPercentage = 5, Brewery = "Anheuser-Busch InBev", Country = "United States" },
		new Beer { Id = 1005, Name = "Stella Artois", Type = "Pilsner", AlcoholPercentage = 5, Brewery = "Anheuser-Busch InBev", Country = "Belgium" },
		new Beer { Id = 1006, Name = "Sapporo", Type = "Lager", AlcoholPercentage = 5, Brewery = "Sapporo Breweries Ltd.", Country = "Japan" },
		new Beer { Id = 1007, Name = "Peroni", Type = "Lager", AlcoholPercentage = 5.1, Brewery = "Peroni Brewery", Country = "Italy" },
		new Beer { Id = 1008, Name = "Asahi", Type = "Lager", AlcoholPercentage = 5, Brewery = "Asahi Breweries Ltd.", Country = "Japan" },
		new Beer { Id = 1009, Name = "Hoegaarden", Type = "Witbier", AlcoholPercentage = 4.9, Brewery = "InBev Belgium", Country = "Belgium" },
		new Beer { Id = 1020, Name = "Tsingtao", Type = "Lager", AlcoholPercentage = 4.7, Brewery = "Tsingtao Brewery Co. Ltd.", Country = "China" }
	};
	```
4. Dodajte pogled "List" koji prikazuje popis svih piva iz izvora podataka.
5. Dodajte pogled "Details" koji prikazuje pojedinosti o jednom pivu.
6. Dodajte pogled "Create" koji korisnicima omogućuje dodavanje novog piva na popis.
7. Dodajte potvrdu u polged "Create" kako biste bili sigurni da su sva potrebna polja ispunjena.
8. Dodajte mogućnost uređivanja i brisanja piva iz izvora podataka.
9. Dodajte mogućnosti pretraživanja i filtriranja u prikaz "Details", tako da korisnici mogu tražiti piva prema nazivu, vrsti, pivovari ili zemlji.