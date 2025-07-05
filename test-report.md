# 🧪 Testování aplikace SauceDemo

## ℹ️ O testované aplikaci
- **Název**: SauceDemo
- **URL**: [https://www.saucedemo.com](https://www.saucedemo.com)
- **Typ aplikace**: Demo e-shop pro testování
- **Přihlašovací údaje**:  
  - Uživatel: `standard_user`  
  - Heslo: `secret_sauce`

## 🎯 Cíl testování
Ověřit funkčnost základních prvků aplikace, zejména:
- Přihlášení
- Přidávání zboží do košíku
- Objednávkový proces
- Uživatelská použitelnost a validace

## 🧭 Použitý přístup
- Manuální testování (černá skříňka)
- Testování v prohlížeči Chrome
- Testovací scénáře sepsány v tabulce `test-cases.xlsx`

## 🐞 Seznam nalezených chyb
### ❗ Bug #1 – Přihlášení zablokovaného uživatele
- **Uživatel**: `locked_out_user`
- **Kroky**:
  1. Otevři https://www.saucedemo.com
  2. Zadej `locked_out_user` / `secret_sauce`
  3. Klikni na Login
- **Očekávané chování**: Aplikace by měla zobrazit jasnou informaci, že účet je zablokován.
- **Skutečné chování**: Zobrazí se hláška „Sorry, this user has been locked out.“  
- **Závažnost**: nízká (funkčně správné, ale nepřehledná UX hláška)
- **Screenshot**: `screenshots/locked_user_error.png`

---

### ❗ Bug #2 – Nesprávné obrázky u problem_user
- **Uživatel**: `problem_user`
- **Kroky**:
  1. Přihlas se jako `problem_user`
  2. Prohlédni zboží na hlavní stránce
- **Očekávané chování**: Obrázky produktů odpovídají popisu
- **Skutečné chování**: Některé produkty mají špatné obrázky nebo se nenačítají
- **Závažnost**: střední
- **Screenshot**: `screenshots/problem_user_bug.png`

---

### ⚠️ Poznámka – performance_glitch_user
- **Uživatel**: `performance_glitch_user`
- **Chování**: Aplikace je výrazně pomalejší při načítání
- **Závažnost**: nízká až střední (simuluje zátěž, ale je to záměr)

## ✅ Závěr
Testování je v průběhu. Bude doplněn přehled chyb a doporučení.
