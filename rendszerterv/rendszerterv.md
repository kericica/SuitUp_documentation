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

* **Felhasználó:**
  A rendszer végfelhasználója, aki regisztrál, bejelentkezik, ruhadarabokat és outfiteket kezel, valamint megtekinti az ajánlásokat és statisztikákat.

* **Rendszer:**
  A háttérben futó alkalmazás, amely kezeli a felhasználói műveleteket, tárolja és megjeleníti az adatokat, valamint kommunikál a külső időjárás-API-val.

* **Megrendelő:**
  A rendszer funkcionális és üzleti igényeit meghatározó fél, aki a fejlesztési követelményeket definiálja.

### 3.2 Üzleti folyamatok

#### Regisztráció

* A felhasználó regisztrál a rendszerben, megadva nevét, felhasználónevét és jelszavát.
* A rendszer eltárolja az adatokat, és létrehozza a felhasználói fiókot.

#### Bejelentkezés

* A felhasználó megadja a felhasználónevét és a jelszavát, amelyet a rendszer hitelesít.
* Bejelentkezés után a felhasználó a főoldalra kerül, ahol személyre szabott információkat lát.

#### Kijelentkezés

* A felhasználó a profil ikonra kattintva megnyitja a lenyíló menüt, ahol a "Kijelentkezés" opciót választja.
* A rendszer bontja a munkamenetet és visszairányítja a felhasználót a Bejelentkezési oldalra.

#### Ruhadarabok kezelése

* **Új ruhadarab létrehozása:** a felhasználó feltölti a ruhadarab képének URL-jét, emellett különböző jellemzőket rendelhet hozzá: típus, szín, évszak, anyag, márka.
* **Módosítás és törlés:** a felhasználó szerkesztheti vagy eltávolíthatja a már feltöltött ruhadarabokat.
* **Szűrés:** a rendszer lehetővé teszi a ruhadarabok listázásának szűrését típus, szín és évszak alapján.
* **Megjelenítés:** a felhasználó megtekintheti az összes feltöltött ruhadarabot címkékkel és előnézeti képpel.

#### Outfitek kezelése

* **Új outfit létrehozása:** a felhasználó a feltöltött ruhadarabokból állíthat össze szetteket, amelyekhez nevet és évszakot rendelhet.
* **Módosítása és törlése:** a rendszer támogatja a korábban mentett kombinációk szerkesztését és eltávolítását.
* **Szűrés:** a rendszer lehetővé teszi az outfitek listázásának szűrését évszak alapján.
* **Megjelenítés:** a felhasználó megtekintheti az összes mentett outfitet címkékkel és előnézeti képekkel.

#### Integrációk 

* **Időjárás-integráció:** a rendszer külső API segítségével megjeleníti az aktuális időjárást.

#### Statisztikák és ajánlások

* **Statisztikák:** a rendszer megjeleníti a leggyakrabban viselt ruhadarabokat.
* **Ajánlások:** a rendszer az aktuális évszakhoz illeszkedő ruhadarabokat javasol.

### 3.3 Üzleti entitások

* **Felhasználó:**
  A rendszer regisztrált használója.
  *  *Attribútumai:* név, felhasználónév, jelszó.

* **Ruhadarab:**
  A rendszer egyik alapvető entitása.
  * *Attribútumai:* id, kép-URL, típus, szín, évszak, márka, anyag.

* **Outfit:**
  Ruhadarabok kombinációja, amelyet a felhasználó hoz létre.
  * *Attribútumai:* id, cím, évszak, létrehozás dátuma, tartalmazott ruhadarabok.

* **Időjárás-adat:**
  Külső API-ból származó információ, amely segíti a felhasználót a megfelelő ruhadarabok kiválasztásában.

## 4. Követelmények

### 4.1 Funkcionális követelmények

### 4.2 Nemfunkcionális követelmények

## 5. Funkcionális terv

### 5.1 Rendszerszereplők

Esetünkben az egyetlen rendszerszereplő maga a **felhasználó**, aki regisztrál, bejelentkezik,
ruhadarabokat és outfiteket kezel, valamint megtekinti az ajánlásokat és statisztikákat.

### 5.2 Rendszerhasználati esetek és lefutásaik

#### Regisztráció
* *Lefutás:* Regisztrációs oldal → név, felhasználónév, jelszó megadása → "Regisztráció" gomb → sikeres regisztráció után automatikus átirányítás a Bejelentkezési oldalra.

#### Bejelentkezés
* *Lefutás:* Bejelentkezési oldal → felhasználónév és jelszó megadása → "Bejelentkezés" gomb → sikeres hitelesítés után automatikus átirányítás a Főoldalra → aktuális időjárás, ajánlások és statisztikák megjelenítése.

#### Új ruhadarab feltöltése
* *Lefutás:* Navigációs sáv → "Új" → "Ruhadarab feltöltése" → űrlap kitöltése (kép URL, típus, szín, évszak, márka, anyag) → "Mentés" gomb → sikeres mentés után megjelenik a Ruhadarabok oldalon.

#### Ruhadarab módosítása
* *Lefutás:* "Gardróbom" → "Ruhadarabok" oldal → kiválasztott ruhadarab alatti "Módosítás" gomb → mezők szerkesztése → "Mentés" → frissített adatok megjelennek az oldalon.

#### Ruhadarab törlése
* *Lefutás:* "Gardróbom" → "Ruhadarabok" oldal → kiválasztott ruhadarab alatti "Törlés" gomb → törlés megerősítése → ruhadarab eltűnik a listából.

#### Ruhadarabok szűrése
* *Lefutás:* Ruhadarabok oldal → szűrési feltételek megadása (típus, szín, évszak) → a lista frissül a szűrési feltételek alapján.

#### Új outfit létrehozása
* *Lefutás:* Navigációs sáv → "Új" → "Outfit létrehozása" → korábban feltöltött ruhadarabok kiválasztása → az outfit nevének és évszakának megadása → "Mentés" → outfit megjelenik az Outfitek oldalon.

#### Outfit módosítása
* *Lefutás:* "Gardróbom" → "Outfitek" oldal → kiválasztott outfit alatti "Módosítás" gomb → ruhadarabok vagy adatok módosítása → "Mentés" → frissített adatok megjelennek az oldalon.

#### Outfit törlése
* *Lefutás:* "Gardróbom" → "Outfitek" oldal → kiválasztott outfit alatti "Törlés" gomb → törlés megerősítése → outfit eltűnik a listából.

#### Outfitek szűrése
* *Lefutás:* Outfitek oldal → évszak kiválasztása → a lista frissül a megadott szűrési feltételek alapján.

#### Kijelentkezés
* *Lefutás:* Profil ikon → lenyíló menü → "Kijelentkezés" → visszairányítás a Bejelentkezési oldalra.

### 5.3 Határosztályok

#### Bejelentkezési oldal
* Üdvözlő üzenet
* Aktuális időjárás megjelenítése
* Felhasználónév input mező
* Jelszó input mező
* "Bejelentkezés" gomb
* "Regisztráció" gomb (link a Regisztrációs oldalra)

#### Regisztrációs oldal
* Név input mező
* Felhasználónév input mező 
* Jelszó input mező
* "Regisztráció" gomb (link a Bejelentkezési oldalra)

#### Főoldal
* Aktuális időjárás megjelenítése
* Évszaknak megfelelő ruhadarab ajánlás
* Statisztikák blokk (leggyakrabban viselt ruhadarabok)
* Navigációs sáv: "Új", "Gardróbom", profil ikon

#### Ruhadarabok oldal
* Ruhadarabok listája (kártyás elrendezésben, címkékkel)
* Szűrőmezők: típus, szín, évszak
* "Módosítás" és "Törlés" gomb ruhadarabonként
* Navigációs sáv: "Új", "Gardróbom", profil ikon

#### Outfitek oldal
* Outfitek listája (előnézeti képekkel, címkékkel)
* Szűrés évszak alapján
* "Módosítás" és "Törlés" gomb outfitenként
* Navigációs sáv: "Új", "Gardróbom", profil ikon

#### Új ruhadarab feltöltése oldal
* Kép URL input mező
* Típus, szín, évszak, márka, anyag input mezők
* "Mentés" gomb
* Navigációs sáv: "Új", "Gardróbom", profil ikon

#### Új outfit létrehozása oldal
* Ruhadarabok listája (carousel-ben)
* Outfit név input mező
* Évszak input mező
* "Mentés" gomb
* Navigációs sáv: "Új", "Gardróbom", profil ikon

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