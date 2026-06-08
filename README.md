# Raamatukogu

Raamatukogu on veebirakendus, mis võimaldab hallata raamatuid, kasutajaid ja laenutusi.
Kasutaja saab otsida raamatuid, vaadata nende infot, laenutada ja tagastada raamatuid ning vaadata statistikat.

## Tehnoloogiad

* Node.js
* Express.js
* JWT autentimine

## Käivitamine

```bash
npm install
```
```bash
node src/app.js
```

Server töötab aadressil:
```bash
http://localhost:3000
```

## Testikasutajad

username: admin
password: admin

## API endpointid

### Kasutajad

| Meetod | URL | Kirjeldus |
|--------|-----|-----------|
| POST | /api/users/signup | kasutaja registreerimine |
| POST | /api/users/login | sisselogimine |
| POST | /api/users/logout | väljalogimine |
| GET | /api/users/me | praegune kasutaja |

### Raamatud

| Meetod | URL | Kirjeldus |
|--------|-----|-----------|
| GET | /api/books | kõik raamatud |
| GET | /api/books/:id | üks raamat |
| GET | /api/books/search | otsing autori või pealkirja järgi |
| GET | /api/books/genres | žanrid |
| GET | /api/books/genre/:genre | raamatud žanri järgi |

### Laenud

| Meetod | URL | Kirjeldus |
|--------|-----|-----------|
| POST | /api/loans | raamatu laenutamine |
| POST | /api/loans/:id/return | raamatu tagastamine |
| GET | /api/loans | kõik laenud |
| GET | /api/loans/me | kasutaja laenud |

## Testid
``` bash
node src/test.js
```

Kõik testid peavad läbima edukalt.

## GitHub Actions

Projekt kasutab GitHub Actions automaattestide käivitamiseks.
Testid käivitatakse iga pushi ja pull requesti korral.
