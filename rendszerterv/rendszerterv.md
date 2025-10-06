# Rendszerterv

## 1. A rendszer célja

A rendszer célja egy olyan **webalkalmazás** fejlesztése, amely segíti a felhasználókat ruhadarabjaik rendszerezésében,
nyilvántartásában és outfitjeik megtervezésében.  
A felhasználók regisztráció után saját ruhatárat hozhatnak létre, ahol a ruhadarabokat különféle jellemzők alapján
kezelhetik.

A rendszer biztosítja:

- új ruhadarabok és outfitek **feltöltését, módosítását és törlését**,
- a **legkedveltebb és aktuális évszakhoz illő ruhadarabok** megjelenítését a főoldalon,
- **szűrési lehetőséget** a ruhadarabok és outfitek között,
- valamint az **aktuális időjárás megjelenítését** egy külső API segítségével.

A cél egy **modern, felhasználóbarát és személyre szabható** rendszer, amely támogatja a felhasználókat a mindennapi
öltözködés megtervezésében.

## 2. Projektterv

### 2.1  Projektszerepkörök, felelősségek

* **PM** (Project Manager): Az a személy, aki a projekt vezeti. Ez a személy végzi a projekt felülvizsgálatát, mind
  részfeladatok meghatározása, mind változtatások bekerülése terén.
* **UI/UX Designer**: Felhasználóbarát és átlátható felület tervezése. Színek, ikonok, tipográfia, reszponzív elrendezés
  meghatározása
* **PA** (Program Analyst): Tervezésért, fejlesztésért felelős személy. Optimális megoldások kifejlesztésére is
  hivatott. Programkódok írása.
* **QA** (Quality Assurance): Teszteket biztosít a projekthez, amik a kód helyes működést támasztják alá.

### 2.2 Projektmunkások és felelősségeik

* **Varga Tímea**: *PM, PA*
* **Szőllős Boglárka**: *UI/UX Designer, PA*
* **Kántor Kamilla**: *QA, PA*

### 2.3 Ütemterv

**Ütemterv:**

| Funkció / Story               | Feladat / Task                                                                                                              | Prioritás | Becsült szükséges idő (óra) | Ráfordított idő (óra) |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------|-----------|-----------------------------|-----------------------|
| Követelmény specifikáció      | Követelmények összegyűjtése                                                                                                 | 1         | 6                           | -                     |
| Funkcionális specifikáció     | Funkciók meghatározása, use-case-ek meghatározása , user story-k kidolgozása                                                | 1         | 6                           | -                     |
| Rendszerterv                  | Adatbázisterv, architektúrális modell, menü-hierarchia, képernyőtervek készítése, technológiák kiválasztása                 | 1         | 6                           | -                     |
| Szerveroldal létrehozása      | Adatbáziskapcsolat megvalósítása, regisztárció/bejelentkezés, CRUD műveletek implementálása                                 | 2         | 24                          | -                     |
| Kinézet létrehozása           | Szerveroldali megjelenítés kialakítása sablonok segítségével, reszponzív elrendezéssel és újrahasznosítható oldalelemekkel. | 2         | 18                          | -                     |
| Tesztek megírása és futtatása | Funkcionális teszt, reszponzív teszt, hibajavítás                                                                           | 3         | 8                           | -                     |

## 3. Üzleti folyamatok modellje

### 3.1 Üzleti szereplők

### 3.2 Üzleti folyamatok

### 3.3 Üzleti entitások

## 4. Követelmények

### 4.1 Funkcionális követelmények

### 4.2 Nemfunkcionális követelmények

## 5. Funkcionális terv

### 5.1 Rendszerszereplők

### 5.2 Rendszerhasználati esetek és lefutásaik

### 5.3 Határosztályok

### 5.4  Menü-hierarchiák

![SuitUp! - Menü-hierarchiák](src/menu_hierarchia.png)

### 5.5 Képernyőtervek

**Bejelentkezési oldal**

![SuitUp! - Bejelentkezesi_oldal](src/bejelentkezes.png)

**Regisztrációs oldal**

![SuitUp! - Regisztracios_oldal](src/regisztracio.png)

**Főoldal**

![SuitUp! - Fo_oldal](src/fo_oldal.png)

**Ruhadarabok oldal**

![SuitUp! - Ruhadarabok_oldal](src/ruhadarabok.png)

**Outfitek oldal**

![SuitUp! - Outfitek_oldal](src/outfitek.png)

**Új ruhadarab feltöltése oldal**

![SuitUp! - Uj_ruhadarab_feltoltese_oldal](src/uj_ruhadarab.png)

**Új outfit készítése oldal**

![SuitUp! - Uj_outfit_keszitese_oldal](src/uj_outfit.png)

## 6. Fizikai környezet

### 6.1 Fejlesztő eszközök

| Eszköz / Szoftver               | Rendeltetés                                                   | Megjegyzés                                                                                                                        |
|---------------------------------|---------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| JetBrains Intellij Ultimate     | Fejlesztői környezet (IDE)                                    | Spring Boot projektek fejlesztésére, hibakeresésre és integrált verziókezelésre használható.                                      |
| Spring Boot                     | Backend keretrendszer, szerveroldali logika kezelése          | REST API-k, adatbáziskapcsolat, autentikáció és üzleti logika megvalósítása Java nyelven.                                         |
| Thymeleaf                       | Szerveroldali sablonmotor, dinamikus HTML-oldalak létrehozása | A szerverről kapott adatok megjelenítése sablonokon keresztül, reszponzív és újrahasznosítható nézetekkel.                        |
| HTML5                           | Weboldalak struktúrájának kialakítása                         | Az oldal vázát adja, minden frontend fejlesztés alapja                                                                            |
| CSS3                            | Stílusok kezelése                                             | A weboldal kinézetének, színeknek, betűtípusoknak és elrendezésnek meghatározása.                                                 |
| Bootstrap                       | Frontend-fejlesztési keretrendszer                            | Előre elkészített komponensek és rácsrendszer a reszponzív designhoz                                                              |
| JavaScript                      | Kliensoldali logika, interaktív elemek, dinamikus viselkedés  |                                                                                                                                   |
| PostgreSQL                      | Relációs adatbázis-kezelő rendszer                            |                                                                                                                                   |
| Chrome / Firefox / Edge / Opera | Funkcionális tesztelés, reszponzív teszt, hibakeresés         | Fejlesztői eszközök (DevTools) használatával kódprofilozás, hibakeresés és performance teszt                                      |
| Git/GitHub                      | Verziókezelés, kódmegosztás, csapatmunka                      | Commit-ok, branch-ek és pull request-ek kezelése, projektek nyomon követése                                                       |
| Trello                          | Projekt- és feladatmenedzsment                                | Kanban tábla a sprintek és taskok vizuális követéséhez, prioritások kezelése, agile tool-ok használata (story points, wip number) |

## 7. Architekturális terv

### 7.1 Komponensek

| **Komponens**                          | **Leírás**                                                                                                                                                                                          |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Prezentációs réteg (View)**          | A felhasználói felület, amely szerveroldali sablonok segítségével jeleníti meg az adatokat. HTML, CSS, Bootstrap és JavaScript biztosítja a megjelenést és az interaktivitást.                      |
| **Vezérlő réteg (Controller)**         | A kliens oldali kérések fogadása és a válaszok előkészítése. A vezérlők továbbítják az adatokat a szolgáltatásréteg felé, és a megjelenítéshez szükséges modelleket adják át a sablonmotor számára. |
| **Szolgáltatás réteg (Service)**       | Az üzleti logika megvalósítása. Feldolgozza az adatokat, kezeli a tranzakciókat, és meghívja az adattárolási réteg metódusait.                                                                      |
| **Adatkezelő réteg (Repository)**      | A **Spring Data JPA** segítségével kezeli az adatbázis-műveleteket. A Repository interfészek biztosítják a CRUD műveleteket a **PostgreSQL** adatbázis felé.                                        |
| **Adatbázis (PostgreSQL)**             | A relációs adatbázis, amely tárolja a felhasználók, könyvek és egyéb entitások adatait.                                                                                                             |
| **Biztonsági réteg (Spring Security)** | Hitelesítést (authentication) és jogosultságkezelést (authorization) valósít meg. Ellenőrzi a bejelentkezést, védi az URL-eket és szerepkörök alapján korlátozza a hozzáféréseket.                  |
| **Segédkomponensek**                   | Statikus erőforrások (CSS, JS, képek), konfigurációs fájlok (`application.properties`)                                                                                                              |

## 7.2 Call Chain

Az alkalmazás MVC architektúrát követ, ahol az egyes komponensek meghatározott sorrendben hívják egymást a kérések
feldolgozása során:

1. **Felhasználó** – böngészőből HTTP kérést küld (pl. bejelentkezés, adatlekérés).
2. **Biztonsági réteg** – ellenőrzi a felhasználó hitelesítését és jogosultságát.
3. **Controller** – fogadja a kérést, és meghívja a szolgáltatásréteget.
4. **Service** – végrehajtja az üzleti logikát és adatkezelést.
5. **Repository** – kommunikál az adatbázissal (CRUD műveletek).
6. **Adatbázis (PostgreSQL)** – tárolja és visszaadja az adatokat.
7. **View (Thymeleaf)** – a visszaadott adatokból szerveroldalon HTML-oldalt generál, amely visszajut a böngészőbe.

### 7.3 Architekturális ábra

![SuitUp! - Architekturális ábra](src/springboot_thymeleaf.png)

## 8. Adatbázisterv

![SuitUp! - Adatbázisterv](src/suit_up_database_uml.png)

## 9. Osztálydiagram

![SuitUp! - Osztálydiagram](src/suit_up_class_diagram.png)

## 10. Implementációs terv

## 11. Tesztterv

### 11.1 Tesztelés célja

### 11.2 Tesztelési típusok

### 11.3 Tesztesetek

## 12. Telepítési / Indítási terv

## 13. Karbantartási terv

Az alkalmazás folyamatos és megbízható működésének biztosítása érdekében szükséges a rendszer rendszeres és megfelelő
karbantartása. Mivel az adatok egy relációs adatbázisban (PostgreSQL) kerülnek tárolásra, elengedhetetlen az adatbázis 
szerver folyamatos felügyelete, biztonsági mentések készítése és az adatbázis optimalizálása. Emellett továbbra is figyelmet 
kell fordítani a hibák kijavítására, a felhasználói élmény javítására és a webes technológiák fejlődéséből adódó lehetőségek 
integrálására. Továbbá az új felhasználói igények megjelenésével szükségessé válhat új funkciók beépítése is.

| Karbantartás típusa                       | Karbantartási tevékenység a rendszerben                                                                                                                         |
|-------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Corrective Maintenance** (Hibajavító)   | A felhasználók által jelzett hibák kijavítása.                                                                                                                  |
| **Adaptive Maintenance** (Alkalmazkodó)   | Az alkalmazás kompatibilitásának fenntartása különböző böngészők és verziók között. A felület naprakészen tartása a webes szabványok változásainak megfelelően. |
| **Perfective Maintenance** (Tökéletesítő) | Új funkciók bevezetése. Felhasználói élmény javítása.                                                                                                           |
| **Preventive Maintenance** (Megelőző)     | Kódellenőrzés és refaktorálás. Biztonsági szempontok ellenőrzése.                                                                                               |