# Tesztelési jegyzőkönyv

## Manuális tesztek

### Összes felület

| ID | Név | Leírás | Megfelelés | QA |
|----|-----|--------|------------|----|
| GF-01 | Navigáció működése | Az alkalmazás menüpontjai közötti navigáció helyesen működik, minden link a megfelelő oldalra irányít. | OK         |     |
| GF-02 | Jogosultságkezelés | Be nem jelentkezett felhasználó nem érheti el az auth. oldalak mögötti funkciókat.                     | OK         |     |
| GF-03 | Hibakezelés        | Hibás URL megadása esetén a rendszer visszairányít a főoldalra vagy hibát jelez.                       | OK         |     |

### Regisztrációs / Bejelentkező felület

| ID | Név | Leírás | Megfelelés | QA |
|----|-----|--------|------------|----|
| LI-01 | Regisztráció valid adatokkal   | A felhasználó sikeresen regisztrál érvényes adatokkal.       | OK         |     |
| LI-02 | Regisztráció hiányos adatokkal | A rendszer hibát jelez, és nem hoz létre új felhasználót.    | OK         |     |
| LI-03 | Bejelentkezés helyes adatokkal | A felhasználó sikeresen bejelentkezik, a kezdőoldalra kerül. | OK         |     |
| LI-04 | Bejelentkezés hibás jelszóval  | A rendszer hibaüzenetet jelenít meg.                         | OK         |     |

### Landing page felület

| ID | Név | Leírás | Megfelelés | QA |
|----|-----|--------|------------|----|
| LP-01 | Időjárás widget megjelenése       | A főoldalon megjelenik az Open-Meteo alapú időjárás widget.       | OK         |     |
| LP-02 | Widget frissülése                 | A hőmérséklet automatikusan frissül az időzített kérés alapján.   | OK         |     |
| LP-03 | Évszakhoz illő ajánlások          | A widget megjeleníti az aktuális évszakhoz tartozó ruhadarabokat. | OK         |     |
| LP-04 | Kedvelt ruhadarabok megjelenítése | A widget megjeleníti a leggyakrabban viselt ruhadarabokat         | OK         |     |

### Ruhadarab feltöltő felület

| ID | Név | Leírás | Megfelelés | QA |
|----|-----|--------|------------|----|
| CLF-01 | Új ruhadarab feltöltése    | Új ruhadarab hozzáadása link, típus, évszak, szín, márka és anyag megadásával.     | OK         |     |
| CLF-02 | Hibás adatbevitel kezelése | Kötelező mező hiányában a rendszer validációs hibát jelez.                         | OK         |     |
| CLF-03 | Képmegjelenítés            | A ruhadarabról megadott link az adatbázisban tárolódik, és megjelenik a felületen. | OK         |     |

### Outfit összeállító felület

| ID | Név | Leírás | Megfelelés | QA |
|----|-----|--------|------------|----|
| OFF-01 | Új outfit mentése                 | A kiválasztott ruhadarabok kombinációja menthető különböző azonosítók kíséretében (pl.: név, évszak, kép, opcionálisan szabadon megválasztott címkék). | OK         |     |
| OFF-02 | Ruhadarab típus szerinti listázás | Az egyes kategóriák (felső, nadrág, cipő stb.) megfelelően szűrődnek.                                                                                  | OK         |     |
| OFF-03 | Outfit módosítása                 | Egy meglévő outfit szerkeszthető és újra elmenthető.                                                                                                   | OK         |     |

### Ruhadarabok felület

| ID | Név | Leírás | Megfelelés | QA |
|----|-----|--------|------------|----|
| CL-01 | Ruhadarab lista megjelenítése | A felhasználó saját ruhadarabjai listában megjelennek.       | OK         |     |
| CL-02 | Ruhadarab módosítása          | A kiválasztott ruhadarab adatai szerkeszthetők.              | OK         |     |
| CL-03 | Ruhadarab törlése             | Ruhadarab törlése után a lista frissül, a bejegyzés eltűnik. | OK         |     |

### Outfitek felület

| ID | Név | Leírás | Megfelelés | QA |
|----|-----|--------|------------|----|
| OF-01 | Összes outfit megjelenítése | A felhasználó korábban mentett outfitjei listázódnak. | OK         |     |
| OF-02 | Outfit törlése              | Egy outfit eltávolítható az adatbázisból.             | OK         |     |

## Unit teszt

| ID    | Név                 | Tesztelt metódus                       | Leírás                                                                   | Megfelelés | QA  |
| ----- | ------------------- | -------------------------------------- | ------------------------------------------------------------------------ | ---------- | --- |
| UT-01 | Ruhadarab mentés    | `WardrobeItemServiceImpl.save()`       | Ellenőrzi, hogy a mentés során a felhasználó helyesen kerül beállításra. | OK         |     |
| UT-02 | Ruhadarab frissítés | `WardrobeItemServiceImpl.update()`     | Ellenőrzi, hogy a módosított mezők mentés után frissülnek.               | OK         |     |
| UT-03 | Ruhadarab törlés    | `WardrobeItemServiceImpl.deleteById()` | Teszteli, hogy a kapcsolódó outfitek is törlődnek.                       | OK         |     |

## Böngésző kompatibilitás teszt

| ID | Funkció | Leírás | Megfelelés | QA |
|----|---------|--------|------------|----|
| BR-01 | Chrome  | Teljes funkcionalitás működik.               | OK         |     |
| BR-02 | Firefox | Megfelelő megjelenés és működés.             | OK         |     |
| BR-03 | Edge    | Időjárás-widget animáció és stílus hibátlan. | OK         |     |

## Tesztösszesítés

| Modul / Felület                           | Tesztek száma | OK    | Nem OK |
|-------------------------------------------|---------------|-------|--------|
| GF – Összes felület                       | 3             | 3      | 0      |
| LI – Regisztrációs / Bejelentkező felület | 4             | 4      | 0      |
| LP – Landing page felület                 | 4             | 4      | 0      |
| CLF – Ruhadarab feltöltő felület          | 3             | 3      | 0      |
| OFF – Outfit összeállító felület          | 3             | 3      | 0      |
| CL – Ruhadarabok felület                  | 3             | 3      | 0      |
| OF – Outfitek felület                     | 2             | 2      | 0      |
| UT – Unit teszt                           | 3             | 3      | 0      |
| BR – Böngésző teszt                       | 3             | 3      | 0      |
| **Összesen**                              | **28**        | **28** | **0**  |