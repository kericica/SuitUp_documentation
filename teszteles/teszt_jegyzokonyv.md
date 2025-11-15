# Tesztelési jegyzőkönyv

## Manuális tesztek

### Összes felület

| ID    | Név                | Leírás                                                                                                 | Megfelelés | QA                                                     |
|-------|--------------------|--------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------|
| GF-01 | Navigáció működése | Az alkalmazás menüpontjai közötti navigáció helyesen működik, minden link a megfelelő oldalra irányít. | OK         |                                                        |
| GF-02 | Jogosultságkezelés | Be nem jelentkezett felhasználó nem érheti el az auth. oldalak mögötti funkciókat.                     | OK         |                                                        |
| GF-03 | Hibakezelés        | Hibás URL megadása esetén a rendszer visszairányít a főoldalra vagy hibát jelez.                       | OK         |                                                        |
| GF-04 | Responsive design  | Mobil- és tablet-nézetben is jó az oldalak elrendezése.                                                | OK         | [Szőllős Boglárka](https://github.com/SzollosBoglarka) | 	

### Regisztrációs / Bejelentkező felület

| ID    | Név                            | Leírás                                                       | Megfelelés | QA                                       |
|-------|--------------------------------|--------------------------------------------------------------|------------|------------------------------------------|
| LI-01 | Regisztráció valid adatokkal   | A felhasználó sikeresen regisztrál érvényes adatokkal.       | OK         | [Varga Tímea](https://github.com/timi15) |
| LI-02 | Regisztráció hiányos adatokkal | A rendszer hibát jelez, és nem hoz létre új felhasználót.    | OK         |                                          |
| LI-03 | Bejelentkezés helyes adatokkal | A felhasználó sikeresen bejelentkezik, a kezdőoldalra kerül. | OK         | [Varga Tímea](https://github.com/timi15) |
| LI-04 | Bejelentkezés hibás jelszóval  | A rendszer hibaüzenetet jelenít meg.                         | OK         |                                          |

### Landing page felület

| ID    | Név                                         | Leírás                                                                                                                                                | Megfelelés | QA                                                     |
|-------|---------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------|
| LP-01 | Időjárás widget megjelenése                 | A főoldalon megjelenik az Open-Meteo alapú időjárás widget.                                                                                           | OK         | [Kántor Kamilla](https://github.com/kericica)          |
| LP-02 | Widget frissülése                           | A hőmérséklet automatikusan frissül az időzített kérés alapján.                                                                                       | OK         | [Kántor Kamilla](https://github.com/kericica)          |
| LP-03 | Évszakhoz illő ajánlások                    | A widget megjeleníti az aktuális évszakhoz tartozó ruhadarabokat.                                                                                     | OK         | [Kántor Kamilla](https://github.com/kericica)          |
| LP-04 | Kedvelt ruhadarabok megjelenítése           | Az oldalon megjelennek a leggyakrabban viselt ruhadarabokat                                                                                           | OK         |                                                        |
| LP-05 | Átirányítás az outfit összeállító felületre | A carousel-ben megjelenő képre kattintva a felhasználó átkerül az outfit összeállító oldalra, ahol az adott ruhadarab automatikusan betöltésre kerül. | OK         | [Szőllős Boglárka](https://github.com/SzollosBoglarka) |

### Ruhadarab feltöltő felület

| ID     | Név                        | Leírás                                                                                                | Megfelelés | QA                                                     |
|--------|----------------------------|-------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------|
| CLF-01 | Új ruhadarab feltöltése    | Új ruhadarab hozzáadása link, típus, évszak, szín, márka és anyag megadásával.                        | OK         | [Varga Tímea](https://github.com/timi15)               |
| CLF-02 | Hibás adatbevitel kezelése | Kötelező mező hiányában a rendszer validációs hibát jelez.                                            | OK         |                                                        |
| CLF-03 | Képmegjelenítés            | A ruhadarabról megadott link az adatbázisban tárolódik, és megjelenik a felületen.                    | OK         |                                                        |
| CLF-04 | Egyedi címke megadása      | A felhasználó egyedi címkéket adhat hozzá az egyes ruhadarabokhoz, ezek eltárolódnak az adatbázisban. | OK         | [Szőllős Boglárka](https://github.com/SzollosBoglarka) |

### Outfit összeállító felület

| ID     | Név                               | Leírás                                                                                                                                                 | Megfelelés | QA                                                     |
|--------|-----------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------|
| OFF-01 | Új outfit mentése                 | A kiválasztott ruhadarabok kombinációja menthető különböző azonosítók kíséretében (pl.: név, évszak, kép, opcionálisan szabadon megválasztott címkék). | OK         | [Varga Tímea](https://github.com/timi15)               |
| OFF-02 | Ruhadarab típus szerinti listázás | Az egyes kategóriák (felső, nadrág, cipő stb.) megfelelően szűrődnek.                                                                                  | OK         | [Kántor Kamilla](https://github.com/kericica)          |
| OFF-03 | Egyedi címke megadása             | A felhasználó egyedi címkéket adhat hozzá az egyes outfitekhez, ezek eltárolódnak az adatbázisban.                                                     | OK         | [Szőllős Boglárka](https://github.com/SzollosBoglarka) |
| OFF-04 | Hibás adatbevitel kezelése        | Kötelező mező hiányában a rendszer validációs hibát jelez.                                                                                             | OK         | [Szőllős Boglárka](https://github.com/SzollosBoglarka) |

### Ruhadarabok felület

| ID    | Név                                         | Leírás                                                                                                                                | Megfelelés | QA                                                     |
|-------|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------|
| CL-01 | Ruhadarab lista megjelenítése               | A felhasználó saját ruhadarabjai listában megjelennek.                                                                                | OK         |                                                        |
| CL-02 | Ruhadarab módosítása                        | A kiválasztott ruhadarab adatai szerkeszthetők.                                                                                       | OK         | [Kántor Kamilla](https://github.com/kericica)          |
| CL-03 | Ruhadarab törlése                           | Ruhadarab törlése után a lista frissül, a bejegyzés eltűnik.                                                                          | OK         | [Varga Tímea](https://github.com/timi15)               |
| CL-04 | Címkék megjelenítése                        | Minden ruhadarabhoz a megfelelő címkék jelennek meg.                                                                                  | OK         | [Szőllős Boglárka](https://github.com/SzollosBoglarka) |
| CL-05 | Ruhadarabok szűrése                         | A ruhadarabokat lehet szűrni típus, évszak, szín, márka, anyag, és egyedi címke alapján.                                              | OK         | [Szőllős Boglárka](https://github.com/SzollosBoglarka) |
| CL-06 | Átirányítás az outfit összeállító felületre | A plusz ikonra kattintva a felhasználó átkerül az outfit összeállító oldalra, ahol az adott ruhadarab automatikusan betöltésre kerül. | OK         | [Szőllős Boglárka](https://github.com/SzollosBoglarka) |

### Outfitek felület

| ID    | Név                                   | Leírás                                                                                                      | Megfelelés | QA                                                     |
|-------|---------------------------------------|-------------------------------------------------------------------------------------------------------------|------------|--------------------------------------------------------|
| OF-01 | Összes outfit megjelenítése           | A felhasználó korábban mentett outfitjei listázódnak.                                                       | OK         |                                                        |
| OF-02 | Outfit törlése                        | Egy outfit eltávolítható az adatbázisból.                                                                   | OK         | [Kántor Kamilla](https://github.com/kericica)          |
| OF-03 | Outfitek szűrése                      | Az outfiteket lehet szűrni évszak, név, és az egyedi címkék alapján.                                        | OK         | [Szőllős Boglárka](https://github.com/SzollosBoglarka) |
| OF-04 | Címkék megjelenítése                  | Minden outfithez a megfelelő címkék jelennek meg.                                                           | OK         | [Szőllős Boglárka](https://github.com/SzollosBoglarka) |
| OF-05 | Outfitben szereplő képek megtekintése | A felhasználó egy modal ablakban megnézheti egyben, hogy melyik ruhadarabokból állította össze az outfitet. | OK         | [Szőllős Boglárka](https://github.com/SzollosBoglarka) |
| OF-06 | Outfit létrehozásának dátuma          | Minden outfithez helyesen megjelenik, hogy melyik napon hozta létre a felhasználó.                          | OK         | [Szőllős Boglárka](https://github.com/SzollosBoglarka) |

## Unit teszt

| ID    | Név                 | Tesztelt metódus                       | Leírás                                                                   | Megfelelés | QA                                            |
|-------|---------------------|----------------------------------------|--------------------------------------------------------------------------|------------|-----------------------------------------------|
| UT-01 | Ruhadarab mentés    | `WardrobeItemServiceImpl.save()`       | Ellenőrzi, hogy a mentés során a felhasználó helyesen kerül beállításra. | OK         | [Kántor Kamilla](https://github.com/kericica) |
| UT-02 | Ruhadarab frissítés | `WardrobeItemServiceImpl.update()`     | Ellenőrzi, hogy a módosított mezők mentés után frissülnek.               | OK         | [Kántor Kamilla](https://github.com/kericica) |
| UT-03 | Ruhadarab törlés    | `WardrobeItemServiceImpl.deleteById()` | Teszteli, hogy a kapcsolódó outfitek is törlődnek.                       | OK         | [Kántor Kamilla](https://github.com/kericica) |

## Behavior-Driven Development teszt

| ID     | Név                             | Tesztelt metódus / endpoint     | Leírás                                                                                         | Megfelelés | QA                                       |
|--------|---------------------------------|---------------------------------|------------------------------------------------------------------------------------------------|------------|------------------------------------------|
| BDD-01 | Sikeres regisztráció            | `POST /auth/register`           | A felhasználó megadja a regisztrációhoz szükséges adatokat, majd sikeresen létrejön a fiókja.  | OK         | [Varga Tímea](https://github.com/timi15) |
| BDD-02 | Regisztráció utáni visszajelzés | `POST /auth/register redirect ` | Regisztráció után a rendszer átirányítja a felhasználót a bejelentkezési oldalra.              | OK         | [Varga Tímea](https://github.com/timi15) |
| BDD-03 | Sikeres bejelentkezés           | `POST /auth/login`              | A már regisztrált felhasználó helyes adatokkal be tud jelentkezni.                             | OK         | [Varga Tímea](https://github.com/timi15) |
| BDD-04 | Bejelentkezés utáni átirányítás | `POST /auth/login redirect`     | A rendszer bejelentkezés után átirányítja a felhasználót a /home személyes tartalmak oldalára. | OK         | [Varga Tímea](https://github.com/timi15) |

## Böngésző kompatibilitás teszt

| ID    | Funkció | Leírás                                       | Megfelelés | QA                                            |
|-------|---------|----------------------------------------------|------------|-----------------------------------------------|
| BR-01 | Chrome  | Teljes funkcionalitás működik.               | OK         | [Kántor Kamilla](https://github.com/kericica) |
| BR-02 | Firefox | Megfelelő megjelenés és működés.             | OK         | [Kántor Kamilla](https://github.com/kericica) |
| BR-03 | Edge    | Időjárás-widget animáció és stílus hibátlan. | OK         | [Kántor Kamilla](https://github.com/kericica) |

## Tesztösszesítés

| Modul / Felület                           | Tesztek száma | OK     | Nem OK |
|-------------------------------------------|---------------|--------|--------|
| GF – Összes felület                       | 4             | 4      | 0      |
| LI – Regisztrációs / Bejelentkező felület | 4             | 4      | 0      |
| LP – Landing page felület                 | 5             | 5      | 0      |
| CLF – Ruhadarab feltöltő felület          | 4             | 4      | 0      |
| OFF – Outfit összeállító felület          | 4             | 4      | 0      |
| CL – Ruhadarabok felület                  | 6             | 6      | 0      |
| OF – Outfitek felület                     | 6             | 6      | 0      |
| UT – Unit teszt                           | 3             | 3      | 0      |
| BDD – Behavior-Driven Development teszt   | 4             | 4      | 0      |
| BR – Böngésző teszt                       | 3             | 3      | 0      |
| **Összesen**                              | **43**        | **43** | **0**  |