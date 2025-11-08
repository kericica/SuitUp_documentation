```gherkin
Feature: Főoldali megjelenítés és inspiráció

  Mint Stílusos Stella
  Azért, hogy mindig ötletet kapjak a napi stílusomhoz
  Szeretném, ha a főoldalon láthatnám a legkedveltebb
  valamint az aktuális évszakhoz illő ruhadarabjaim.

  Scenario: A felhasználó megnyitja a főoldalt
    Given a felhasználó be van jelentkezve az alkalmazásba
    When megnyitja a főoldalt
    Then megjelennek a felhasználó által legkedveltebb ruhadarabok
    And az aktuális évszakhoz illő ruhadarabok

```
