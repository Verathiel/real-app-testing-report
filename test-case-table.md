# Testovací scénáře – Login Form

| ID  | Název testu             | Vstupní data                        | Očekávaný výsledek                                   | Skutečný výsledek                                 | Status |
|-----|--------------------------|-------------------------------------|------------------------------------------------------|---------------------------------------------------|--------|
| TC1 | Platný login             | uživatel: standard_user<br>heslo: secret_sauce | Uživatel je přihlášen a přesměrován na produkty      | Přihlášení úspěšné – produkty zobrazeny           | ✅ PASS |
| TC2 | Uzamčený účet            | uživatel: locked_out_user<br>heslo: secret_sauce | Zobrazí se chybová hláška o uzamčeném účtu           | Hlásí chybu: „User has been locked out.“          | ✅ PASS |
| TC3 | Neplatný login           | uživatel: random<br>heslo: cokoliv | Chyba: „Username and password do not match“          | Hlásí chybu správně                                | ✅ PASS |
| TC4 | Prázdné pole username    | uživatel: *(prázdné)*<br>heslo: secret_sauce | Chyba: „Username is required“                        | Hlásí chybu správně                                | ✅ PASS |
| TC5 | Prázdné pole password    | uživatel: standard_user<br>heslo: *(prázdné)* | Chyba: „Password is required“                        | Hlásí chybu správně                                | ✅ PASS |
| TC6 | Zvláštní znaky v loginu  | uživatel: !@#$%^&*()<br>heslo: test | Chyba: „Username and password do not match“          | Hlásí chybu správně                                | ✅ PASS |
| TC7 | Problémový uživatel      | uživatel: problem_user<br>heslo: secret_sauce | Přihlášení proběhne, ale zobrazí se bugy v obrázcích | Bugy přítomné – obrázky se nenačítají             | ❗BUG |
| TC10 | Přidání více produktů do košíku |
