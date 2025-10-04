# Funkcionális specifikáció

## 1. A rendszer céljai és nem céljai

### 1.1 A rendszer céljai

### 1.2 A rendszer ***NEM*** céljai

## 2. Jelenlegi helyzet

## 3. Vágyálom rendszer

## 4. Jelenlegi üzleti folyamatok

## 5. Igényelt üzleti folyamatok

### 5.1 Igényelt üzleti folyamatok leírása

### 5.2 Igényelt üzleti folyamatok diagram

## 6. Használati esetek

### 6.1 Aktorok (szereplők) meghatározása

### 6.2 Használati eset diagram

## 7. Követelménylista

| Modul        | ID  | Név                         | v.  | Kifejtés                                                                                                                                                                                     |
|--------------|-----|-----------------------------|-----|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Jogosultság  | K1  | Regisztrációs felület       | 1.0 | A felhasználó név, felhasználónév és jelszó megadásával regisztrálhat. Az adatok titkosított formában kerülnek az adatbázisba. Hiányos vagy hibás adat esetén a rendszer hibaüzenetet küld.  |
| Jogosultság  | K2  | Bejelentkezési felület      | 1.0 | A felhasználó a regisztrációkor megadott felhasználónév és jelszó megadásával tud bejelentkezni. Hibás adatok esetén a rendszer hibaüzenetet jelenít meg.                                    |
| Felület      | K3  | Landing page (Főoldal)      | 1.0 | A felhasználó bejelentkezés után a főoldalra kerül, ahol megjelennek az aktuális évszakhoz illő ruhadarabjai és legkedveltebb ruhadarabjai. A rendszer az aktuális időjárást is megjeleníti. |
| Felület      | K4  | Legkedveltebb ruhadarabok   | 1.0 | A főoldalon megjelennek a felhasználó által leggyakrabban használt ruhadarabok.                                                                                                              |
| Felület      | K5  | Évszak szerinti ruhadarabok | 1.0 | A főoldalon a rendszer az aktuális évszaknak megfelelő ruhadarabokat jeleníti meg.                                                                                                           |
| Felület      | K6  | Ruhadarabok oldal           | 1.0 | A felhasználó ezen az oldalon látja az összes feltöltött ruhadarabját Bootstrap kártyák formájában. A kártyákon módosítás és törlés gomb található.                                          |
| Felület      | K7  | Ruhadarab szűrés            | 1.0 | A ruhadarabok oldalon a felhasználó szűrhet évszak, típus és szín alapján.                                                                                                                   |
| Felület      | K8  | Outfitek oldal              | 1.0 | A felhasználó ezen az oldalon látja az összes általa létrehozott outfitet, kártyás elrendezésben.                                                                                            |
| Felület      | K9  | Outfit szűrés               | 1.0 | Az outfitek oldalon a felhasználó szűrhet évszak alapján.                                                                                                                                    |
| Feladattípus | K10 | Ruhadarab hozzáadása        | 1.0 | A felhasználó új ruhadarabokat tölthet fel a következő adatok megadásával: típus, évszak, márka, szín, anyag, kép (image_url).                                                               |
| Feladattípus | K11 | Ruhadarab módosítása        | 1.0 | A felhasználó módosíthatja a ruhadarabok adatait.                                                                                                                                            |
| Feladattípus | K12 | Ruhadarab törlése           | 1.0 | A felhasználó törölheti az általa feltöltött ruhadarabokat.                                                                                                                                  |
| Feladattípus | K13 | Outfit összeállítás         | 1.1 | A felhasználó korábban feltöltött ruhadarabokból új outfitet készíthet, valamint megadhatja az outfit nevét, illetve évszakját.                                                              |
| Feladattípus | K14 | Outfit módosítása           | 1.0 | A felhasználó módosíthatja az általa létrehozott outfiteket.                                                                                                                                 |
| Feladattípus | K15 | Outfit törlése              | 1.0 | A felhasználó törölheti az általa létrehozott outfiteket.                                                                                                                                    |
| Adatkezelés  | K16 | Tárolás                     | 1.0 | A rendszer az adatokat PostgreSQL adatbázisban fogja eltárolni.                                                                                                                              |
| Adatkezelés  | K17 | Időjárás adat lekérése      | 1.0 | A rendszer külső API segítségével lekéri az aktuális időjárást és megjeleníti az összes oldalon.                                                                                             |

## 8. Képernyőtervek

## 9. Forgatókönyvek