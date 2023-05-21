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
Pro import dat otevřeme menu **File** v levém horním rohu aplikace. Zde otevřeme podmenu **Import** a zvolíme zdroj dat.

![image](https://user-images.githubusercontent.com/72192205/231018389-41026b02-de52-49f5-a2a1-dc81a3f73bdd.png)

### Import dat ze souboru CSV

Pro import ze souboru CSV zvolíme **Import Dataset From File**.

![image](https://user-images.githubusercontent.com/72192205/231018573-ec9ec067-e665-444b-a152-ad2e6f011250.png)

Otevře se dialogové okno, pod nadpisem **Path** klikneme na ikonu složky a zvolíme náš CSV soubor. Potřebná nastavení importu se automaticky vyplní, pokud je soubor CSV standardního formátu.

![image](https://user-images.githubusercontent.com/72192205/231018727-16b5e0ef-8f7b-41c3-8cfc-160edf73863e.png)

Pokud se nastavení nevyplnilo automaticky, lze nastavení přepsat ručně. V okně **Preview** je náhled
na importovaný soubor. Zde si můžeme ověřit, jak se data načtou pomocí námi zadaných nastavení importu. Pkud chceme načít pouze určitý počet řádků souboru,
můžeme vyplnit pole **Number of lines to load** počtem řádků, které chceme načíst.

* Header Line Number - číslo řádku na kterém je hlavička dat
* Number of lines to load - počet řádků dat k načtení
* Delimiter - rozdělovač dat

### Import dat z databáze PostgreSQL

Pro import z databáze zvolíme v nabídce **Filee** -> **Import** -> **Connect to database**.

![image](https://user-images.githubusercontent.com/72192205/235596008-ac938672-34f8-46b6-9802-b7daa621de83.png)

V dialogovém okně vyplníme potřební nastavení a vyzkoušíme připojení k databázi tlačítkem **Test Connection**.

![image](https://user-images.githubusercontent.com/72192205/235596168-893a5b2b-a44d-4db3-be88-d89db437aee8.png)

Pokud se zobrazí *Connection Established*, propojení bylo úspěšné a můžeme pokračovat kliknutím na *OK*.

![image](https://user-images.githubusercontent.com/72192205/235596203-06101768-55bb-4d40-a8dc-97805fadf4f3.png)

Poté se vytvoří záložka s načtenými daty.

![image](https://user-images.githubusercontent.com/72192205/235596239-2e040d37-8cfe-4623-a797-4f74c9cbda6c.png)

## Tvorba nového schématu

Pro vytvoření nového schématu zvolte v nabídce **File** (nebo po kliknutí na záložku **➕**) položku **Add New Schema**.

Otevře se dialogové okno, zde můžete zvolit název schématu, jeho výchozí dataset a zda chcete schéma propojit s diagramem. 
Pokud propjíte schéma s diagramem, vytvoří se spolu se záložkou schéma i záložka diagramu. Propojení záložek je indikováno stejnou barvou záložky.

### Import podkladu schématu

Pokud chcete do schématu přidat podklad, například půdorys budovy, lze tak učinit z nabídky **File** -> **Import** -> **Import plan**.

### Přidání zařízení

Pro přidání zařízení do schématu je třeba mít nejprve otevřenou záložku se schématem, poté v nabídce **Tools** zvolte položku **Add New Device**.

V dialogovém okně můžete zařízení pojmenovat, přidat k němu výraz a vybrat ikonu zařízení.

## Zobrazení dat

# Rozhraní
## Záložky

Záložky slouží pro kompaktní zobrazení možností aplikace. Existují čtyři typy záložek: Plan (Schéma), Graph, Diagram a Data.
Záložky můžeme tvořit z menu File (záložka data se tvoří automaticky s importem dat), dále je můžeme zavřít kliknutím na tlačítko X vedle jména záložky nebo je můžeme smazat kliknutím na ikonu popelnice vedle jména záložky.

### Schéma

#### Zařízení

### Grafy
### Diagramy
### Data

# Zpracování výrazů

Zpracování výrazů slouží k výpočtům a analýze dat, která chceme vizualizovat.
Podporované operace:
* závorky a záporná čísla
* sčítání a odčítání
* násobení a dělení
* mocnění
* druhá odmocnina
* exponenciála
* zaokrouhlování
* logaritmus
* modulo
* procenta
* absolutní hodnota
* signum

Podporované datové typy jsou **Integer** a **Double**, lze využít odkazů na buňky dat ve formátu **[data]!sloupecŘádek**. 
Pro práci s buňkami jsou podporovány tyto operace:
* suma
* průměr
* minimum
* maximum


# Příklady použití
## Graf průměrné spotřeby domu
## Diagram chytrých zařízení v hale
## Schéma spotřebičů garáže
## Diagram obecných dat
## Propojení s databází
