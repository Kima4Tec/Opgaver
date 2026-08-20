# Opgave: Struct til temperatur

I denne opgave skal du arbejde med en **`struct`** og bruge den til at repræsentere en lille datastruktur.

En temperatur kan beskrives med en værdi og en måleenhed. Du skal derfor oprette en struct, der kan indeholde disse oplysninger.

### 1. Opret en struct

Opret en struct med navnet:

```text
Temperature
```

Struct'en skal indeholde:

* `Value` – en `double`, der indeholder temperaturen
* `Unit` – en `string`, der indeholder måleenheden, f.eks. `"C"` eller `"F"`

### 2. Opret en constructor

Lav en constructor, som modtager:

* temperaturens værdi
* temperaturens enhed

Eksempel på ønsket brug:

```csharp
Temperature temperature = new Temperature(20.5, "C");
```

### 3. Ændr en værdi

Efter du har oprettet temperaturen, skal du ændre dens værdi til `25`.

Udskriv derefter temperaturen til konsollen.

Resultatet skal eksempelvis være:

```text
Temperaturen er: 25 C
```

### 4. Opret en ny temperatur

Opret endnu en `Temperature`:

```text
100 F
```

Udskriv også denne til konsollen.

### 5. Undersøg struct som value type

Lav følgende:

```csharp
Temperature temperature1 = new Temperature(20, "C");
Temperature temperature2 = temperature1;

temperature2.Value = 30;
```

Udskriv derefter både `temperature1` og `temperature2`.

Overvej:

> Hvorfor er `temperature1` stadig 20, mens `temperature2` er 30?

---

# Ekstra

Udvid din `Temperature` struct med en metode:

### `ToFahrenheit()`

Hvis temperaturen er angivet i Celsius, skal metoden returnere temperaturen omregnet til Fahrenheit.

Formlen er:

```text
F = C × 9 / 5 + 32
```

Eksempel:

```text
20 C → 68 F
```

### Ekstra ekstra

Tilføj en metode:

### `ToCelsius()`

Der omregner Fahrenheit til Celsius.

Formlen er:

```text
C = (F - 32) × 5 / 9
```

---
