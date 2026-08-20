# Klasse med liste af biler

Opgaven handler om at oprette en klasse, der kan indeholde en liste af biler og lave forskellige beregninger, søgninger og ændringer på listen.

Opret et nyt **Console-projekt** indeholdende klassen `Program` med metoden `Main()`.

Tilføj en klasse `Car` med følgende properties:

* `Brand` – bilmærket
* `Model` – bilmodellen
* `Year` – bilens årgang
* `Price` – bilens pris

Tilføj derefter en klasse `CarCollection` med følgende indhold:

## Fields

* En liste med navnet `Cars`, som kan indeholde `Car`-objekter.

## Metoder

Implementér følgende metoder:

* **AddCar**
  Modtager en `Car` som parameter og indsætter bilen i listen.

* **GetCount**
  Returnerer antallet af biler i listen.

* **GetTotalValue**
  Returnerer den samlede værdi af alle biler i listen.

* **GetAveragePrice**
  Returnerer gennemsnitsprisen på alle biler i listen.

* **GetOldestCar**
  Returnerer den ældste bil i listen.

* **GetNewestCar**
  Returnerer den nyeste bil i listen.

* **ToString**
  Returnerer en `string` med information om alle biler i listen.

## Constructors

`CarCollection` skal have:

* En constructor uden parametre, som opretter en tom liste.

* En constructor med en `Car` som parameter, hvor bilen indsættes som det første element i listen.

---

# Ekstra

Udvid `CarCollection` med:

* En constructor, som modtager en `List<Car>` som parameter, og indsætter bilerne i listen.

* En metode `AddCars`, som modtager en `List<Car>` som parameter og indsætter alle bilerne i listen.

* En metode `DeleteByIndex`, som har et heltal som parameter, der angiver index på den bil, der skal slettes.

* En metode `DeleteFirstByBrand`, som har et bilmærke som parameter og sletter den første bil, der har dette mærke.

* En metode `DeleteAllByBrand`, som har et bilmærke som parameter og sletter alle biler, der har dette mærke.

---

# Ekstra ekstra

Når ovenstående fungerer, udvid klassen med:

* **GetByBrand**
  Returnerer alle biler af et bestemt bilmærke.

* **GetByYear**
  Returnerer alle biler fra et bestemt år.

* **GetMoreExpensiveThan**
  Returnerer alle biler, der er dyrere end en angivet pris.

* **GetCheaperThan**
  Returnerer alle biler, der er billigere end en angivet pris.

* **GetAveragePriceByBrand**
  Returnerer gennemsnitsprisen for et bestemt bilmærke.

* **SortByPrice**
  Sorterer bilerne efter pris.

* **SortByYear**
  Sorterer bilerne efter årgang.

* **SortByBrand**
  Sorterer bilerne alfabetisk efter bilmærke.

---

## Eksempeldata

Du kan selv vælge bilerne, men du kan bruge disse til at teste:

| Brand      | Model   | Year |  Price |
| ---------- | ------- | ---: | -----: |
| Toyota     | Corolla | 2020 | 180000 |
| BMW        | 320i    | 2019 | 275000 |
| Ford       | Mustang | 2021 | 450000 |
| Volkswagen | Golf    | 2018 | 160000 |
| Toyota     | Yaris   | 2022 | 195000 |
| BMW        | X5      | 2020 | 650000 |

Især `GetOldestCar`, `GetAveragePriceByBrand`, sletning og sortering er gode øvelser i `List<T>` og LINQ.
