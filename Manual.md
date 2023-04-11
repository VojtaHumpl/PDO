# K čemu aplikace slouží
Aplikace slouží k vizualizaci a analýze dat v chytrých budovách.
Umožňuje uživatelům importovat data z různých zdrojů, jako jsou databáze a soubory CSV, a následně je zobrazit v různých formátech, jako jsou schémata budov,
grafy, diagramy a tabulky. Aplikace je vhodná jak pro jednotlivé uživatele, kteří chtějí analyzovat a vizualizovat data ze svých chytrých zařízení v domácnosti,
tak pro firmy, které spravují více chytrých budov a potřebují monitorovat jejich stav a různé veličiny, jako například spotřebu energie.

Hlavní výhodou aplikace je, že umožňuje uživatelům snadno vizualizovat a porovnávat data v různých formátech,
což může pomoci s rozhodováním o úsporách energie a zlepšení efektivity v chytrých budovách. 
Díky využití vyhodnocování výrazů ve stylu Excel vzorců mohou uživatelé vytvářet vlastní výrazy pro zpracování dat a 
tvorbu pokročilých vizualizací.

Aplikace přináší uživatelům výhodu jednoduchého importování dat ze souborů CSV a propojení s databázemi,
což jim umožňuje snadno získávat data z různých zdrojů a pracovat s nimi v aplikaci.
Díky tomu uživatelé mohou efektivně zpracovávat velká množství dat.

Celkově tedy aplikace slouží k usnadnění vizualizace a analýzy dat v chytrých budovách a umožňuje uživatelům snadno monitorovat a
zlepšovat efektivitu a spotřebu energie.


# Základní kroky

## Import dat
Importovat data lze buď ze souboru formátu csv nebo z databáze PostgreSQL.
Pro import dat otevřeme menu *File* v levém horním rohu aplikace. Zde otevřeme podmenu import a zvolíme zdroj dat.

![image](https://user-images.githubusercontent.com/72192205/231018389-41026b02-de52-49f5-a2a1-dc81a3f73bdd.png)

Pro import ze souboru csv zvolíme *Import Dataset From File*.

![image](https://user-images.githubusercontent.com/72192205/231018573-ec9ec067-e665-444b-a152-ad2e6f011250.png)

Otevře se dialogové okno, pod nadpisem Path klikneme na ikonu složky a zvolíme náš csv soubor.

![image](https://user-images.githubusercontent.com/72192205/231018727-16b5e0ef-8f7b-41c3-8cfc-160edf73863e.png)

Potřebná nastavení importu se automaticky vyplní, pokud je soubor csv standardního formátu. Pokud ne, lze nastavení přepsat ručně. V okně *Preview* je náhled
na importovaný soubor. Zde si můžeme ověřit, jak se data načtou pomocí námi zadaných nastavení importu. Pkud chceme načít pouze určitý počet řádků souboru,
můžeme vyplnit pole *Number of lines to load* počtem řádků, které chceme načíst.

* Header Line Number - číslo řádku na kterém je hlavička dat
* Number of lines to load - počet řádků dat k načtení
* Delimiter - rozdělovač dat

## Import schématu
## Přidání zařízení
## Zobrazení dat

# Rozhraní
## Schéma
## Grafy
## Diagramy
## Data

# Zpracování výrazů

# Příklady použití
## Graf průměrné spotřeby domu
## Diagram chytrých zařízení v hale
## Schéma spotřebičů garáže
## Diagram obecných dat
## Propojení s databází
