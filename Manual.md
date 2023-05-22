# K čemu aplikace slouží
Aplikace slouží k vizualizaci a analýze dat v chytrých budovách. Umožňuje uživatelům importovat data z různých zdrojů, jako jsou databáze a soubory CSV, a následně je zobrazit v různých formátech, jako jsou schémata budov, grafy, diagramy a tabulky. Aplikace je vhodná jak pro jednotlivé uživatele, kteří chtějí analyzovat a vizualizovat data ze svých chytrých zařízení v domácnosti, tak pro firmy, které spravují více chytrých budov a potřebují monitorovat jejich stav a různé veličiny, jako například spotřebu energie.

Hlavní výhodou aplikace je, že umožňuje uživatelům snadno vizualizovat a porovnávat data v různých formátech,
což může pomoci s rozhodováním o úsporách energie a zlepšení efektivity v chytrých budovách. Díky využití vyhodnocování výrazů ve stylu Excel vzorců mohou uživatelé vytvářet vlastní výrazy pro zpracování dat a tvorbu pokročilých vizualizací.

Aplikace přináší uživatelům výhodu jednoduchého importování dat ze souborů CSV a propojení s databázemi,
což jim umožňuje snadno získávat data z různých zdrojů a pracovat s nimi v aplikaci. Díky tomu uživatelé mohou efektivně zpracovávat velká množství dat.

Celkově tedy aplikace slouží k usnadnění vizualizace a analýzy dat v chytrých budovách a umožňuje uživatelům snadno monitorovat a zlepšovat efektivitu a spotřebu energie.


# Základní kroky

## Import dat
Importovat data lze buď ze souboru formátu csv nebo z databáze PostgreSQL. Pro import dat otevřeme menu **File** v levém horním rohu aplikace. Zde otevřeme podmenu **Import** a zvolíme zdroj dat. Načítaná data se musí držet formátu, který je popsán v kapitole [Formát dat](#formát-dat).

![import-dat](https://github.com/VojtaHumpl/PDO/assets/72192205/91f6640e-00d5-482b-bab8-558f7c9efe14)

Poté úspěšném načtení dat se vytvoří záložka s datasetem.

![data-tab](https://github.com/VojtaHumpl/PDO/assets/72192205/de24712c-cdf0-4eb1-8586-80a775493fad)

### Import dat ze souboru CSV

Pro import ze souboru CSV zvolíme **Import Dataset From File**.

![import-csv1](https://github.com/VojtaHumpl/PDO/assets/72192205/287472db-3231-462b-974e-b68fb547ae07)

Otevře se dialogové okno, pod nadpisem **Path** klikneme na ikonu složky a zvolíme náš CSV soubor. Potřebná nastavení importu se automaticky vyplní, pokud je soubor CSV standardního formátu.

![import-csv2](https://github.com/VojtaHumpl/PDO/assets/72192205/5f137107-4111-4eae-8801-334834375a80)

Pokud se nastavení nevyplnilo automaticky, lze nastavení přepsat ručně. V okně **Preview** je náhled na importovaný soubor. Zde si můžeme ověřit, jak se data načtou pomocí námi zadaných nastavení importu. Pkud chceme načít pouze určitý počet řádků souboru, můžeme vyplnit pole **Number of lines to load** počtem řádků, které chceme načíst.

* Header Line Number - číslo řádku na kterém je hlavička dat
* Number of lines to load - počet řádků dat k načtení
* Delimiter - rozdělovač dat

### Import dat z databáze PostgreSQL

Pro import z databáze zvolíme v nabídce **File** -> **Import** -> **Connect to Database**.


V dialogovém okně vyplníme potřební nastavení a vyzkoušíme připojení k databázi tlačítkem **Test Connection**.

![import-postgres1](https://github.com/VojtaHumpl/PDO/assets/72192205/7a98f263-023d-4344-9e19-936bbe9ac24e)

Pokud se zobrazí *Connection Established*, propojení bylo úspěšné a můžeme pokračovat kliknutím na *OK*.

![import-postgres2](https://github.com/VojtaHumpl/PDO/assets/72192205/594bb93d-8891-41c4-a082-94c2c9903350)

## Tvorba nového schématu

Pro vytvoření nového schématu zvolte v nabídce **File** (nebo po kliknutí na záložku **➕**) položku **New Schema**.

![new-schema1](https://github.com/VojtaHumpl/PDO/assets/72192205/9d7d7019-0665-4d79-a062-6fac65d8cc88)
![new-schema2](https://github.com/VojtaHumpl/PDO/assets/72192205/8243d751-aa80-40c4-9060-ce0681d08697)

Otevře se dialogové okno, zde můžete zvolit název schématu, jeho výchozí dataset a zda chcete schéma propojit s diagramem. Pokud propojíte schéma s diagramem, vytvoří se spolu se záložkou schéma i záložka diagramu. Propojení záložek je indikováno stejnou barvou záložky.

![schema-dialog](https://github.com/VojtaHumpl/PDO/assets/72192205/5811d9a5-fea7-4e61-83e5-1d339f78522d)

### Import podkladu schématu

Pokud chcete do schématu přidat podklad, například půdorys budovy, lze tak učinit z nabídky **File** -> **Import** -> **Import Schema Background**.

![schema-background](https://github.com/VojtaHumpl/PDO/assets/72192205/751e179c-92f6-4bf9-a8b7-728aa276d38e)

### Přidání zařízení

Pro přidání zařízení do schématu je třeba mít nejprve otevřenou záložku se schématem, poté v nabídce **Tools** zvolte položku **Add New Device**.

V dialogovém okně můžete zařízení pojmenovat, přidat k němu výraz a vybrat ikonu zařízení.

![schema-device](https://github.com/VojtaHumpl/PDO/assets/72192205/b6eb97a2-de9c-46f9-b97b-b186a1354c77)

Zařízení pak ve schímatu vypadá takto.

![schema-device2](https://github.com/VojtaHumpl/PDO/assets/72192205/f0203015-8fa4-42f6-b178-b3687e2f8d1a)


# Rozhraní
## Záložky

Záložky slouží pro kompaktní zobrazení možností aplikace. Existují čtyři typy záložek: Schéma, Graphs, Diagram a Data. Záložky můžeme tvořit z menu File (záložka data se tvoří automaticky s importem dat), dále je můžeme zavřít kliknutím na tlačítko X vedle jména záložky nebo je můžeme smazat kliknutím na ikonu popelnice vedle jména záložky. Propojené záložky schématu a diagramu jsou indikovány stejnou barvou záložky. Záložka **➕** slouží jako alternativní metoda vytváření záložek.

![zalozky](https://github.com/VojtaHumpl/PDO/assets/72192205/3472188c-de67-4431-ae96-8bde49742166)

Pokud byly některé záložky schovány, je možné je zobrazit kliknutím skrze nabídku **View**, kde zvolíme příslušný typ záložek.

![new-schema1](https://github.com/VojtaHumpl/PDO/assets/72192205/7294f29b-9c5a-46f8-bd55-eb961047fb74)

### Schéma

Záložka schéma slouží k tvorbě a editaci schématu. V rámci této záložky je možné přidávat zařízení, importovat podklad schématu a editovat vlastnosti zařízení. Schéma může být propojeno s diagramem. Pokud je schéma propojeno s diagramem, zařízení přidané do schématu se automaticky přidají i do diagramu.

K navigaci po schématu se využívá střední tlačítko myši, které se drží pro pohyb. Kolečko myši pak také umožňuje přiblížení nebo oddálení schématu. Pracovní plocha schématu je nekonečná, takže není problém přidat velké množství zařízení a volně se pohybovat.

#### Zařízení

Zařízení je základní stavební prvek schématu. Zařízení může mít název, ikonu a výraz. Výraz slouží k výpočtům a analýze dat, která chceme vizualizovat. Výraz může být například výpočet spotřeby zařízení, výpočet výkonu, výpočet teploty, atd. Výraz může být libovolně složitý, ale je třeba dbát na jeho správnou syntaxi. Spodní text zařízení je jeho jméno a vrchní text je jeho výraz. Zařízením lze pohybovat podržením levého tlačítka myši na ikoně zařízení. Pokud je zařízení propojeno s diagramem, změny zařízení se projevují i v diagramu.

Zařízení je možné přidat do schématu z menu **Tools** -> **Add New Device**. V dialogovém okně můžeme zařízení pojmenovat, přidat k němu výraz a vybrat ikonu zařízení. Pokud je schéma propojeno s diagramem, zařízení se automaticky přidá i do diagramu.

![schema-device](https://github.com/VojtaHumpl/PDO/assets/72192205/bfe89e81-5922-4574-96de-4db008b15ee3)

Výraz je možné editovat při kliknutí na jeho vrchní text (editace se dokončí stisknutím klávesy **Enter**) nebo otevřít editační dialogové okno po dvojkliku levým tlačítkem myši nebo při pravém kliku na zařízení a zvolení volby **Edit**.

![device-data](https://github.com/VojtaHumpl/PDO/assets/72192205/94dd5fdc-13b5-482a-a4d6-c856251b0370)
![device-data2](https://github.com/VojtaHumpl/PDO/assets/72192205/258b2ee0-cbbe-4108-8948-c7b3f4bc71d4)

Zařízení lze odstranit při pravém kliku na zařízení a zvolení volby **Delete**.

![device-right-click](https://github.com/VojtaHumpl/PDO/assets/72192205/426167c4-efda-4947-8273-824b8ef2db2c)

### Grafy

Záložka grafy slouží k tvorbě grafů. V rámci této záložky je možné přidávat grafy s různými datasety. Zatím je možné vytvořit pouze čárový typ grafu. Graf může zobrazovat i více křivek najednou pro různá data v datasetu.

Záložka grafů je vytvářena z nabídky **File** -> **New Graphs**. V této záložce po kliknutí na tlačítko **➕** můžeme přidat jednotlivé grafy. V nabídce je možné zvolit tři velikosti grafu podle toho, kolik plochy záložky bude graf zabírat - čtvrtinový, poloviční nebo celý graf. V dialogovém okně můžeme graf pojmenovat, vybrat dataset a nastavit jeho vlastnosti.

![graphs1](https://github.com/VojtaHumpl/PDO/assets/72192205/36ad8340-9e73-45cb-bf86-b9e42e6b76cd)

Poté se otevře dialogové okno. Pro data na ose X je možné zvolit pouze jednu datovou řadu ve formátu **[počáteční buňka]:[koncová buňka]**, například **A1:A200**. Dat na ose Y může být více. S pomocí oddělovače **;** může možný výraz vypadat takto **[počáteční buňka]:[koncová buňka];[počáteční buňka]:[koncová buňka]**, konkrétně například **A1:A200;B1:B200**.

![graphs2](https://github.com/VojtaHumpl/PDO/assets/72192205/15b88996-7414-4420-9213-faa2ceb3faf5)

A výsledný graf.

![graphs3](https://github.com/VojtaHumpl/PDO/assets/72192205/31e025d7-a0c9-4900-80ae-08157ffc3e18)

### Diagramy

Záložka diagramy slouží k vizualizaci dat pomocí uzlů diagramu. V rámci této záložky je možné přidávat uzly diagramu, tyto uzly propojovat konektory a editovat výrazy uzlů diagramu. Diagram může být propojen se schématem. Pokud je diagram propojen se schématem, změny propojených uzly se projevují i na konkrétních zařízeních ve schématu.

Do diagramu lze přidávat dva typy uzlů - **zdrojový** a **agregační**. Zdrojový uzel diagramu je vstupní bod diagramu, který většinou představuje konkrétní zařízení ve schématu. Agregační uzel diagramu je prázdný uzel, který propojuje různé další uzly.

Diagram obsahuje lištu nástrojů.

![diagram-menu](https://github.com/VojtaHumpl/PDO/assets/72192205/6b6143d7-7f39-4d2e-b191-df90fe06be4c)

Mezi uzly je možné vytvářet konektory pomocí nástroje **Connector** v liště nástrojů. Konektor je vytvořen mezi dvěma uzly a představuje proměnnou, kterou může spojený uzel využít pro další výpočty. Konektor je vytvořen mezi dvěma uzly tak, že se zvolí nástroj **Connector**, poté se klikne na spojovací bod jednoho uzlu a táhne se na spojovací bod jiného uzlu. Konektor je možné smazat při kliknutí na konektor a stisknutím klávesy **Delete**.

K navigaci po diagramu slouží nástroj **Hand** v liště nástrojů. Pomocí tohoto nástroje je možné posouvat diagram. Diagram je možné přibližovat a oddalovat pomocí držení klávesy **Control** a pohybu kolečka myši.

Nástroj **Text** slouží k přidání textového pole do diagramu. Textové pole je možné editovat při dvojkliku levým tlačítkem myši. Textové pole je možné smazat při kliknutí na textové pole a stisknutím klávesy **Delete**.

Nástroj **Ukazatel** slouží k přepnutí ukazatele z režimu **Connector** nebo **Hand**.

Tlačítka **Undo** a **Redo** slouží k vrácení nebo opětovnému provedení poslední akce.

Diagram v liště nástrojů má také kontextové menu, které slouží k tisku nebo exportu diagramu v různých formátech.

### Data

Záložka data slouží pouze pro zobrazení načtených dat ve formě tabulky. Kolečkem myši lze posunovat zobrazená data. Tato záložka se tvoří automaticky při importu dat.

### Časová osa

Ovládací prvek časové osy slouží k dynamickému posunu v čase při prohlížení dat ve vybraných schématech a diagramech. Díky němu můžete sledovat vývoj a změny dat v závislosti na čase.

# Zpracování výrazů

Pro vstup výrazů je třeba, aby všechny začínaly znakem "=", po kterém následuje výraz k vyhodnocení. Tím aplikace pozná, že má poslaný výraz interpretovat a vyhodnotit. Například **=SQRT(16)** nebo **=data1!A1 + data1!B1**.

### Podporované operace

* **Závorky a záporná čísla -** Používají se pro seskupení výrazů a změně priority operací. Například, **=(-5 + 3) * 2** vrací výsledek -4.

* **Sčítání a odčítání -** Provádějí se pomocí znaků "+" a "-". Například, **=5 + 3** a **=5 - 3**.

* **Násobení a dělení -** Provádějí se pomocí znaků "*" a "/". Například, **=5 * 3** a **=6 / 3**.

* **Mocnění -** Provádí se pomocí znaku "^". Například, **=2 ^ 3** vrací 8.

* **Druhá odmocnina -** Výraz vypadá takto **=SQRT(x)**, kde x je číslo nebo odkaz na buňku. Vypočítá druhou odmocninu z x.

* **Exponenciála -** Výraz vypadá takto **=EXP(x)**, kde x je číslo nebo odkaz na buňku. Vypočítá e umocněné na x, kde e je Eulerovo číslo (přibližně rovno 2.71828).

* **Zaokrouhlování -** Výraz vypadá takto **=ROUND(x, n)**, kde x je číslo nebo odkaz na buňku a n je počet desetinných míst. Zaokrouhlí x na n desetinných míst. Například **=ROUND(3.14159, 2)** vrátí 3.14.

* **Logaritmus -** Výraz vypadá takto **=LOG(x, base)**, kde x je číslo nebo odkaz na buňku a base je základ logaritmu. Vypočítá logaritmus x s daným základem base. 

* **Modulo -** Výraz vypadá takto **=MOD(x, y)**, kde x je číslo nebo odkaz na buňku a y je dělitel. Vypočítá zbytek po dělení x dělitelem y. Například **=MOD(5, 2)** vrátí 1.

* **Procenta -** Použijte operátor procenta "%". Výraz **=x%** dělí x číslem 100, čímž vrátí procentní hodnotu. Například **=50%** vrátí 0.5.

* **Absolutní hodnota -** Výraz vypadá takto **=ABS(x)**, kde x je číslo nebo odkaz na buňku. Vrátí absolutní hodnotu x. Například **=ABS(-5)** vrátí 5.

* **Signum -** Výraz vypadá takto **=SIGN(x)**, kde x je číslo nebo odkaz na buňku. Vrátí signum x, tedy 1 pro kladná čísla, -1 pro záporná čísla a 0 pro nulu. Například **=SIGN(-7)** vrátí -1.


### Podporované operace s buňkami

Při práci s buňkami je důležité dodržet, že rozsah dat musí být buď data v jednom řádku, nebo data v jednom sloupci. Výraz **=data1!A1:data1!A20** je tedy validní, ale **=data1!A1:data1!B3** už ne, protože buňka B3 nemá společný řádek ani sloupec s buňkou A1.

Podporované datové typy jsou **Integer** a **Double**, lze využít odkazů na buňky dat ve formátu **[název datasetu]![buňka]**. 

* **Suma -** Výraz vypadá takto **=SUM(data1!A1:data1!A5)**, kde data1!A1:data1!B2 je rozsah buněk. Sečte hodnoty v buňkách od A1 do A5 včetně. Například, pokud buňky A1 až A5 obsahují hodnoty 1, 2, 3, 4 a 5, pak výraz **=SUM(A1:A5)** vrátí 15.

* **Průměr -** Výraz vypadá takto **=AVG(data1!A1:data1!A5)**, kde data1!A1:data1!B2 je rozsah buněk. Vypočítá průměr hodnot v buňkách od A1 do A5 včetně. Například, pokud buňky A1 až A5 obsahují hodnoty 1, 2, 3, 4 a 5, pak výraz **=AVG(A1:A5)** vrátí 3.

* **Minimum -** Výraz vypadá takto **=MIN(data1!A1:data1!A5)**, kde data1!A1:data1!B2 je rozsah buněk. Vrátí nejnižší hodnotu z buňek od A1 do A5 včetně. Například, pokud buňky A1 až A5 obsahují hodnoty 1, 2, 3, 4 a 5, pak výraz **=MIN(A1:A5)** vrátí 1.

* **Maximum -** Výraz vypadá takto **=MAX(data1!A1:data1!A5)**, kde data1!A1:data1!B2 je rozsah buněk. Vrátí nejvyšší hodnotu z buňek od A1 do A5 včetně. Například, pokud buňky A1 až A5 obsahují hodnoty 1, 2, 3, 4 a 5, pak výraz **=MAX(A1:A5)** vrátí 5.


# Formát dat

Aplikace předpokládá určitý formát importovaných dat. První sloupec musí obsahvat časové razítko ve formátu ISO 8601, například **yyyy-MM-dd'T'HH:mm:ss**. Každý řádek tedy představuje hodnoty v určitém časovém okamžiku. Další sloupce obsahují data. Data jsou ukládána vždy jako čísla, pokud je potřeba ukládat text, je třeba jej převést na číslo.

# Příklady použití
## Graf spotřeby domu
## Schéma spotřebičů garáže
## Diagram obecných dat
## Propojení s databází
