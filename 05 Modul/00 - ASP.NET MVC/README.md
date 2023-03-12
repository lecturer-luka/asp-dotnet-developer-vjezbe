<div align="center">

<!-- title -->

# Uvodne vježbe za Web App ASP.NET MVC

<!-- description -->

Popis vježbi za uvodnu razinu manipulacije podacima u MVC arhitekturi. Vježbe vas uče kako proslijediti podatke iz kontrolera u pogled.

</div>

Osnovni načini prosljeđivanja podataka:
	* Objekt modela - odnosi se na podatke modela koji se prosljeđuju iz kontrolera u pogled. Ovi podaci mogu biti bilo kojeg tipa, ali obično je to instanca klase koja predstavlja podatke koje pogled treba prikazati.
	* ViewBag - dinamički objekt u C# koji se koristi za prijenos podataka između kontrolera i pogleda u ASP.NET aplikacijama. To je svojstvo osnovne klase "Controller" koje vam omogućuje pohranjivanje podataka i pristup njima iz pogleda.
	* ViewData - objekt koji se koristi za prijenos podataka iz akcije kontrolera u pogled. To je kolekcija koji pohranjuje parove ključ-vrijednost, gdje je ključ naziv tipa "string", a vrijednost može biti bilo koji objekt.


## Exercise 1

1. Stvorite novu ASP.NET Core MVC aplikaciju koristeći Visual Studio ili Visual Studio Code.
2. Dodajte novu klasu modela pod nazivom "Book" sa svojstvima kao što su:
	* Title (string), 
	* Author (string), 
	* PublicationDate (int), 
	* Genre (string)
3. Napravite novi kontroler pod nazivom "BookController" s radnjom "Index"
4. Unutar "BookController" kreirajte privatnu metodu "DemoBookCollection" koja će vratiti kolekciju knjiga koja će sadržavati 4 objekta klase "Book" ispunjenih proizvoljnim podacima.
5. U radnji "Index" dohvatite popis svih knjiga iz izvora podataka i proslijedite ga odgovarajućem pogledu za prikaz.

## Exercise 2

1. Stvorite novu ASP.NET Core MVC aplikaciju koristeći Visual Studio ili Visual Studio Code.
2. Dodajte novu klasu modela pod nazivom "Car" sa svojstvima kao što su:
	* Make (string), 
	* Model (string), 
	* Year (int), 
	* Color (string), 
	* Price (decimal)
3. Napravite novi kontroler pod nazivom "CarController" s radnjama "Index", "FilterByYear" i "FilterByColor".
4. Koristite sljedeće demo podatke za svoje akcije kontrolera:
	 ```csharp
	List<Car> demoCarData = new List<Car> {
		new Car {Make = Toyota, Model = Corolla, Year = 2020, Color = Gray, Price = 25000},
		new Car {Make = Honda, Model = Civic, Year = 2021, Color = Red, Price = 28000},
		new Car {Make = Ford, Model = F-150, Year = 2018, Color = Blue, Price = 35000},
		new Car {Make = BMW, Model = X5, Year = 2019, Color = Black, Price = 50000},
		new Car {Make = Chevrolet, Model = Camaro, Year = 2016, Color = Yellow, Price = 42000}
	};
	```
5. U akciji "Index", dohvatite popis svih automobila iz izvora podataka i proslijedite ga odgovarajućem pogledu za prikaz.
6. U akciji "FilterByYear" dohvatite popis automobila starijih od 2020 godine i proslijedite ga odgovarajućem pogledu za prikaz.
6. U akciji "FilterByColor" dohvatite popis automobila čija boja sadrži slovo "L" i proslijedite ga odgovarajućem pogledu za prikaz.

## Exercise 3

1. Stvorite novu ASP.NET Core MVC aplikaciju koristeći Visual Studio ili Visual Studio Code.
2. Dodajte novu klasu modela "Football" u mapu "Models" sa sljedećim svojstvima:
	* TeamName (string)
	* Country (string)
	* Stadium (string)
	* Founded (int)
3. Stvorite novu klasu kontrolera "FootballController" s akcijskom metodom "Index".
4. U akciji "Index" stvorite objekt `List<Football>` i popunite ga nekim lažnim podacima (npr. 5 objekata klase "Football").
5. Proslijedite objekt `List<Football>` u odgovarajući pogled akcije "Index".
6. Stvorite novi prikaz "Index.cshtml" u mapi "Views/Football" i prikažite podatke o nogometu u obliku tablice.

## Exercise 4

1. Stvorite novu ASP.NET Core MVC aplikaciju koristeći Visual Studio ili Visual Studio Code.
2. Dodajte novu klasu modela "Beer" u mapu "Models" sa sljedećim svojstvima:
	* Name (string)
	* Type (string)
	* AlcoholPercentage (double)
	* Brewery (string)
	* Country (string)
3. Koristite sljedeće demo podatke za akcije kontrolera:
	```csharp
	IEnumerable<Beer> beers = new List<Beer>
	{
		new Beer { Name = "Heineken", Type = "Lager", AlcoholPercentage = 5, Brewery = "Heineken International", Country = "Netherlands" },
		new Beer { Name = "Guinness", Type = "Stout", AlcoholPercentage = 4.2, Brewery = "Guinness & Co.", Country = "Ireland" },
		new Beer { Name = "Corona", Type = "Lager", AlcoholPercentage = 4.5, Brewery = "Grupo Modelo", Country = "Mexico" },
		new Beer { Name = "Budweiser", Type = "Lager", AlcoholPercentage = 5, Brewery = "Anheuser-Busch InBev", Country = "United States" },
		new Beer { Name = "Stella Artois", Type = "Pilsner", AlcoholPercentage = 5, Brewery = "Anheuser-Busch InBev", Country = "Belgium" },
		new Beer { Name = "Sapporo", Type = "Lager", AlcoholPercentage = 5, Brewery = "Sapporo Breweries Ltd.", Country = "Japan" },
		new Beer { Name = "Peroni", Type = "Lager", AlcoholPercentage = 5.1, Brewery = "Peroni Brewery", Country = "Italy" },
		new Beer { Name = "Asahi", Type = "Lager", AlcoholPercentage = 5, Brewery = "Asahi Breweries Ltd.", Country = "Japan" },
		new Beer { Name = "Hoegaarden", Type = "Witbier", AlcoholPercentage = 4.9, Brewery = "InBev Belgium", Country = "Belgium" },
		new Beer { Name = "Tsingtao", Type = "Lager", AlcoholPercentage = 4.7, Brewery = "Tsingtao Brewery Co. Ltd.", Country = "China" }
	};
	```
4. Stvorite novu klasu kontrolera "BeerController" s akcijama "Index", "FilterByPercentage", "GroupByCountry", "FilterByName" i "GroupByType".
5. U akciji "Index" dohvatite popis svih piva iz izvora podataka i proslijedite ga odgovarajućem pogledu za prikaz.
6. U akciji "FilterByPercentage" dohvatite popis svih piva s višim postotkom alkohola od 5% iz izvora podataka i proslijedite ga u odgovarajući pogledu za prikaz.
7. U akciji "GroupByCountry", dohvatite popis svih piva iz izvora podataka, grupirajte ih po državi i proslijedite ga u odgovarajući pogled za prikaz.
8. U akciji "FilterByName" dohvatite popis svih piva iz izvora podataka, filtrirajte nazive prema slovu "S" i proslijedite ga odgovarajućem pogledu za prikaz.
9. U akciji "GroupByType", dohvatite popis svih piva iz izvora podataka, grupirajte ih prema vrsti i proslijedite ga u odgovarajući pogled za prikaz.