# Opgave – Interface til produkter

Opret et nyt **C# Console-projekt** med navnet `MyProducts`, indeholdende klassen `Program` med metoden `Main()`.

## 1. Opret et interface

Opret et interface med navnet:

```text
IProduct
```

Interfacet skal indeholde følgende metoder:

* `GetName()`
* `GetPrice()`

Metoderne skal returnere relevante datatyper.

---

## 2. Opret klasser

Opret følgende tre klasser, som alle skal implementere `IProduct`:

### `Whisky`

Skal indeholde relevante data for en whisky, eksempelvis:

* Navn
* Destilleri
* Alder
* Pris

`GetName()` skal returnere whiskyens navn.

`GetPrice()` skal returnere whiskyens pris.

---

### `Book`

Skal indeholde relevante data for en bog, eksempelvis:

* Titel
* Forfatter
* Udgivelsesår
* Pris

`GetName()` skal returnere bogens titel.

`GetPrice()` skal returnere bogens pris.

---

### `Computer`

Skal indeholde relevante data for en computer, eksempelvis:

* Producent
* Model
* RAM
* Pris

`GetName()` skal returnere computerens navn/model.

`GetPrice()` skal returnere computerens pris.

---

# 3. Opret en liste

Opret en liste, der kan indeholde objekter af **alle tre klasser**.

Listen må **ikke** være af typen `object`.

Den skal i stedet bruge interfacet som type.

Tilføj flere objekter af hver type til listen.

Eksempelvis:

```text
Whisky
Whisky
Book
Book
Computer
Computer
```

---

# 4. Gennemløb listen

Løb listen igennem med en `foreach`.

For hvert objekt skal du udskrive:

* Typen
* Navnet
* Prisen

Eksempel på output:

```text
Type: Whisky
Navn: Glenfiddich 18
Pris: 899 kr.

Type: Book
Navn: Clean Code
Pris: 249 kr.

Type: Computer
Navn: ThinkPad T14
Pris: 8500 kr.
```

Du skal altså kunne kalde:

```csharp
item.GetName()
item.GetPrice()
```

uden at vide, om `item` er en `Whisky`, `Book` eller `Computer`.

---

# Ekstra 😈

Udvid interfacet med:

```text
GetDescription()
```

Alle tre klasser skal implementere metoden.

Den skal returnere en beskrivelse, der er specifik for typen.

Eksempel:

```text
Glenfiddich 18, 18 år gammel single malt fra Glenfiddich.
```

```text
Clean Code skrevet af Robert C. Martin.
```

```text
ThinkPad T14 med 32 GB RAM.
```

Udskriv derefter også beskrivelsen.

---

# Ekstra ekstra

Lav en metode:

```text
GetTotalPrice()
```

som modtager listen med `IProduct` og returnerer den samlede pris for alle produkterne.

Derefter skal programmet kunne udskrive:

```text
Samlet pris: 12345 kr.
```


Det er netop en af de ting, interfaces bruges rigtig meget til i større C#/.NET-programmer.
