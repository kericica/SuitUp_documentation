```gherkin
Feature: Időjárás megjelenítése

  Mint Stílusos Stella
  Azért, hogy az öltözködésemet az aktuális időjáráshoz igazíthassam
  Szeretném, ha a bejelentkező, fő, ruhadarabjaim, outfitjeim és outfit összeállítás oldalon megjelennének az aktuális időjárási adatok,
  hogy mindig az alkalomhoz illően öltözhessek fel.

  Scenario: Aktuális időjárás megjelenítése az alkalmazás főoldalán
    Given a felhasználó megnyitja az alkalmazást
    When az alkalmazás lekéri az aktuális időjárási adatokat az API-ból
    Then megjeleníti a hőmérsékletet, időjárási ikont és várost a főoldalon

  Scenario: Időjárási adatok megjelenítése a ruhadarabjaim oldalon
    Given a felhasználó a "Ruhadarabjaim" oldalon van
    When az alkalmazás rendelkezik aktuális időjárási adatokkal
    Then megjeleníti az aktuális hőmérsékletet és időjárást az oldal tetején

  Scenario: Időjárási adatok megjelenítése az outfitjeim és outfit összeállítás oldalon
    Given a felhasználó az "Outfitjeim" vagy "Outfit összeállítás" oldalon van
    When az alkalmazás betölti az időjárási információkat
    Then megjeleníti az aktuális időjárást és javaslatot ad az öltözködéshez

  Scenario: Időjárási adatok betöltésének hibája
    Given az alkalmazás nem tudja elérni az időjárási API-t
    When a lekérés sikertelen
    Then a rendszer hibaüzenetet jelenít meg
    And alapértelmezett ikonokat és szöveget mutat

```