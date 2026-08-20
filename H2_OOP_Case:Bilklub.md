# OOP Case: Bilklub

Der skal udarbejdes en **Bilklub-applikation**, der fx kan laves i Blazor, og som skal kunne følgende:

### 1. Oprette og slette en bruger

Brugeren skal kunne oprette en konto med:

* Navn
* Email
* Password

Brugeren skal også kunne slette sin konto.

**Krav:** Oprettelse af bruger skal ske ved hjælp af en Stored Procedure.

Ved sletning skal brugeren ikke nødvendigvis slettes fysisk fra databasen. Et felt som `IsDeleted` kan sættes til `1`.

---

### 2. Logge ind og logge ud

Brugeren skal kunne logge ind og logge ud.

Login skal udføres på en måde, så **SQL Injection ikke er mulig**.

Du skal kunne forklare, hvorfor følgende er problematisk:

```csharp
"SELECT * FROM Users WHERE Email = '" + email + "'"
```

og hvordan parameteriserede queries løser problemet.

---

### 3. Oprette en bil

En bruger skal kunne oprette en bil med:

* Bilmærke
* Model
* Årgang
* Farve
* Pris

Eksempel:

```text
BMW
320i
2020
Sort
275000
```

En bruger skal kunne have flere biler.

---

### 4. Slette en bil

Brugeren skal kunne slette en af sine biler.

Bilen skal ikke nødvendigvis slettes fysisk fra databasen.

Brug eksempelvis:

```text
IsDeleted = 1
```

---

### 5. Søge efter biler

Brugeren skal kunne søge efter biler ud fra forskellige kriterier.

Eksempelvis:

* Bilmærke
* Model
* Årgang
* Pris
* Farve

Brugeren skal kunne vælge et eller flere kriterier.

Eksempel:

> Find alle BMW'er fra 2020 eller nyere til under 300.000 kr.

---

### 6. Vise søgeresultater

Resultatet skal vises for brugeren.

Eksempel:

```text
BMW 320i
Årgang: 2020
Farve: Sort
Pris: 275.000 kr.

---------------------

BMW 330e
Årgang: 2022
Farve: Blå
Pris: 315.000 kr.
```

---

### 7. Like en bil

En bruger skal kunne like en anden brugers bil.

Systemet skal gemme liket i databasen.

Brugeren skal kunne se:

* Hvilke biler han/hun har liket
* Hvem der har liket ens egne biler

---

### 8. Match

Hvis to brugere liker hinandens biler, skal der oprettes et match.

Eksempel:

```text
Kim → liker Peters BMW
Peter → liker Kims Toyota

          ↓

        MATCH
```

---

### 9. Beskeder

En bruger må kun sende en besked til en anden bruger, hvis de har et match.

Eksempel:

```text
Peter:
"Er du interesseret i at bytte?"
```

Beskeden gemmes i databasen.

Det er ikke nødvendigt at lave realtime-chat.

Det er tilstrækkeligt at:

```text
INSERT → besked
SELECT → beskeder
```

---

# OOP-krav

Programmet skal udvikles med en **objektorienteret tankegang**.

Du skal som minimum overveje klasser som:

```text
User
Car
Like
Match
Message
```

Du bestemmer selv den endelige struktur.

---

# Interface

Du skal oprette mindst ét selvudviklet interface.

Eksempel:

```text
IEntity
ICar
IMessage
INotification
```

Du skal kunne forklare, hvorfor du har valgt at bruge et interface.

---

# Delegate / Event

Programmet skal indeholde mindst én **delegate/event**.

Eksempel:

Når en bruger får et like:

```text
Like
 ↓
Event
 ↓
"Du har fået et nyt like"
```

Du skal kunne forklare:

* Hvad en delegate er
* Hvad et event er
* Hvorfor du har anvendt det

---

# Override og overload

Du skal have mindst ét eksempel på **override** og ét eksempel på **overload**.

Eksempel:

```csharp
public override string ToString()
{
    ...
}
```

og:

```csharp
AddCar(Car car);

AddCar(string brand, string model);
```

Du skal kunne forklare forskellen på de to.

---

# Access modifiers

Du skal anvende forskellige access modifiers, eksempelvis:

```text
public
private
protected
```

Du skal kunne forklare, hvorfor du har valgt dem.

---

# Database

Der skal anvendes en **SQL Server-database**.

Du skal selv designe databasen.

En mulig løsning kunne være:

```text
Users
  │
  ├──── Cars
  │
  ├──── Likes
  │
  └──── Messages
          │
        Matches
```

Du skal selv lave tabeller, primary keys og foreign keys.

---

# Stored Procedure

Der skal mindst være én Stored Procedure.

Eksempel:

```text
CreateUser
```

Du kan selv vælge, om du også vil lave Stored Procedures til eksempelvis:

```text
LoginUser
CreateCar
SearchCars
DeleteCar
```

---

# SQL Injection

Login og andre databaseoperationer skal være beskyttet mod SQL Injection.

Du skal kunne forklare forskellen mellem:

```csharp
"SELECT ... WHERE Email = '" + email + "'"
```

og:

```csharp
"SELECT ... WHERE Email = @email"
```

med parameteren:

```csharp
command.Parameters.AddWithValue("@email", email);
```

---

# UML

Der skal udarbejdes et **UML klassediagram**.

Diagrammet skal vise de vigtigste klasser og deres relationer.

Eksempelvis:

```text
┌─────────────┐
│    User     │
├─────────────┤
│ Name        │
│ Email       │
│ Password    │
└──────┬──────┘
       │
       │ 1:N
       ↓
┌─────────────┐
│     Car     │
├─────────────┤
│ Brand       │
│ Model       │
│ Year        │
│ Price       │
└─────────────┘
```

---
