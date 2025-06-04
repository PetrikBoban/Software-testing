# Tesztautomatizálási kérdések

## Tesztelési alapok (ISTQB-hez kapcsolódó)
<img src="https://www.mindsmapped.com/wp-content/uploads/2016/06/ISTQB.jpg" alt="image" width="300" height="220">

#### ✅ Mi a tesztelés célja? Mi nem az?

Tesztelés célja:

Hibák azonosítása a szoftverben.

Bizonyosság növelése a rendszer működéséről.

Minőségbiztosítás támogatása.

Követelményeknek való megfelelés ellenőrzése.

Tesztelés nem célja:

Nem garantálja a hibamentességet.

Nem a fejlesztés helyettesítése.

Nem csak hibakeresés: dokumentáció, kommunikáció, kockázatkezelés is része.


#### ✅ Mik a tesztelési alapelvek?
Tesztelés kimutatja a hibákat, de nem igazolja a hibamentességet.

A kimerítő tesztelés lehetetlen.

A korai tesztelés megelőzi a költséges hibákat.

A hibák csoportosulnak – Pareto-elv (80/20 szabály).

A tesztelés függ a kontextustól.

Az ismételt tesztelés elavult lehet (regresszió ellen tesztelni kell).

Nincs hibaillúzió – ha nem találunk hibát, attól még lehet benne.


#### ✅ Mi az egységtesztelés (unit testing)? Ki felelős az egységtesztek írásáért?
Definíció: A legkisebb szoftveregységek (pl. függvények, metódusok) viselkedésének tesztelése izoláltan.

Cél: Ellenőrizni, hogy egy adott egység helyesen működik.

Felelős: Általában a fejlesztők írják (TDD - Test Driven Development során különösen).


#### ✅ Mik a tesztszintek, és mi a különbség köztük?
Tesztszint	Ki végzi?	Mit tesztel?
Egységteszt	Fejlesztők	Függvények, metódusok
Integrációs teszt	Fejlesztők vagy tesztelők	Modulok együttműködése
Rendszerteszt	Tesztelők	Teljes rendszer, funkcionális és nem funkcionális
Elfogadási teszt (UAT)	Üzleti felhasználók	Rendszer megfelel-e az üzleti igényeknek
#### ✅ Mi a különbség a verifikáció és a validáció között?
Fogalom	Kérdés	Fókusz	Mikor történik?
Verifikáció	"Jól építjük?"	Tervezés, specifikáció betartása	Fejlesztés közben
Validáció	"A jót építjük?"	Üzleti igények kielégítése	Rendszer kész állapotában

#### ✅ Mik a tesztelési típusok, és mi a különbség köztük?
Típus	Leírás
Funkcionális teszt	A rendszer "mit csinál" – követelmények ellenőrzése
Nem-funkcionális teszt	Hogyan működik – pl. teljesítmény, skálázhatóság
Regressziós teszt	Korábban működő funkciók nem romlottak-e el új módosítások miatt
Biztonsági teszt	Jogosultságok, hozzáférések ellenőrzése
Teljesítményteszt	Válaszidő, terhelhetőség, stabilitás
#### ✅ Mi a különbség a fehér doboz, szürke doboz és fekete doboz tesztelés között?
Típus	Ismerjük a belső működést?	Ki használja?	Példa
Fehér doboz	Igen	Fejlesztő	Kódszintű tesztelés
Fekete doboz	Nem	Tesztelő, végfelhasználó	Funkciók tesztelése
Szürke doboz	Részben	Tesztelő + fejlesztő	API tesztelés

#### ✅ Mi a különbség a felhasználói elfogadási teszt (UAT) és a rendszerteszt között?
Cél	Üzleti igények kielégítése	Teljes rendszer működése
Készíti	Üzleti felhasználók	Tesztelők
Mikor?	Végső fázisban	Fejlesztés utolsó szakasza
Fókusz	Valódi felhasználási esetek	Technikai és funkcionáli
#### ✅ Sorolj fel különbségeket a regressziós tesztelés, a füsttesztelés és az újratesztelés között!
Regresszió	Új hibák keresése a korábban jó funkciókban	Frissítés, módosítás után
Füstteszt	Alapfunkciók gyors ellenőrzése	Build után, telepítés után
Újratesztelés	Egy adott hiba javításának ellenőrzése	Konkrét bugfix után
#### ✅ Mi a különbség a statikus és dinamikus tesztelés között?
Statikus	Nem	Kódszemle, lintelés
Dinamikus	Igen	Unit teszt, UAT
### ✅ Hasonlítsd össze a V-modellt, a vízesés modellt és az Agile megközelítést a tesztelés szempontjából!
Vízesés	Tesztelés a végén	Fejlesztés után	Lineáris
V-modell	Párhuzamos a fejlesztéssel	A specifikációval együtt	Strukturált, formális
Agile	Folyamatos, iteratív	Már az első sprintben	Iteratív, rugalmas

<img src="https://t4.ftcdn.net/jpg/03/90/15/65/360_F_390156585_8w1lsOyICIAOvDCU8tExXW2QwLCOFwXD.jpg" alt="image" width="550" height="400">


<img src="https://i.imgur.com/S38EBJw.png" alt="image" width="550" height="400">   <img src="https://segedletek.level14.hu/assets/img/modszertan-vizeses.svg" alt="image" width="550" height="400">


<img src="https://promanconsulting.hu/wp-content/uploads/2022/03/agilis-modszertanok-optimized.jpg" width="550" height="400">





## Reporting, Bugs
<img src="https://moolya.com/blog/wp-content/uploads/2023/05/Bug-Report.png" alt="image" width="300" height="220">

#### ✅ Milyen lépéseket követnél egy hiba megtalálásakor?
A hiba reprodukálása

Ismételd meg a lépéseket, hogy biztos legyél abban, hogy tényleg hiba történt.

Részletek rögzítése

Rendszerinformációk, környezet, verzió, képernyőképek, logok összegyűjtése.

Hibabejelentés készítése

Tiszta, részletes és strukturált hibajelentés létrehozása (lásd lejjebb).

Prioritás és súlyosság meghatározása

Megítélni, mennyire kritikus a hiba (üzletileg, technikailag).

Kommunikáció a fejlesztőkkel / csapattal

Tisztázás, kérdések megválaszolása, ha szükséges.

Hiba követése

Figyelemmel kísérni a javítást és végül újratesztelni, hogy biztosan megszűnt
#### ✅ Beszélj a gyakori tesztjelentésekről és részleteikről!
Hibajelentés (Bug Report)

Egy adott hiba leírása és státusza (lásd lentebb részletesen).

Tesztelési összefoglaló jelentés (Test Summary Report)

Átfogó kép a tesztelési tevékenységről. Tartalmazhatja:

Mikor történt a tesztelés

Mely modulokat tesztelték

Összes tesztelt esetek száma

Sikeres / sikertelen / kihagyott esetek

Összes hibák, státuszuk

Teszt eset jelentés (Test Case Report)

Egyéni tesztesetek eredményei, részletekkel.

Regressziós teszt jelentés

Az új verzió után újratesztelt funkciók állapota.


#### ✅ Mit tartalmaz egy hibajelentés?
Mező	Példa vagy magyarázat
Cím / Összefoglaló	Pl. "A bejelentkezés gomb nem működik Firefox alatt"
Leírás	A probléma részletes ismertetése
Lépések a reprodukáláshoz	1. Nyisd meg az oldalt → 2. Kattints...
Elvárt eredmény	A felhasználó belép a rendszerbe
Valós eredmény	A gomb nem csinál semmit
Környezet	OS, böngésző, verzió, szerver, stb.
Súlyosság	Kritikus / Magas / Közepes / Alacsony
Prioritás	Magas / Közepes / Alacsony (üzleti szempontból)
Csatolmányok	Képernyőkép, logfájl, videó
Hivatkozott modul / komponens	Melyik részhez kapcsolódik
Státusz	Új / Megerősítve / Javítás alatt / Lezárva
Felelős / hozzárendelt személy	Ki dolgozik rajta
#### ✅ Hogyan rangsorolnál egy hibát?
A hibák rangsorolása két dimenzió alapján történik:

🔹 1. Súlyosság (Severity) – technikai hatás:
Kritikus: Teljes rendszerleállás, adatvesztés.

Magas: Fontos funkció nem működik, de rendszer működik.

Közepes: Kevésbé fontos funkció hibás.

Alacsony: Esztétikai vagy kisebb használhatósági hiba.

🔹 2. Prioritás (Priority) – üzleti fontosság:
Magas: Azonnali javítást igényel, pl. élő rendszerben hiba.

Közepes: Következő fejlesztési ciklusban javítandó.

Alacsony: Később is ráér javítani, nem kritikus.

Példa kombinációkra:

Kritikus súlyosság + Magas prioritás: Rendszer nem indul el – azonnali javítás.

Alacsony súlyosság + Magas prioritás: Elgépelés a főoldalon – presztízskérdés.

Magas súlyosság + Alacsony prioritás: Tesztkörnyezetben crash, de élesben nem fordul elő.

## Test Automation, Selenium
<img src="https://media.licdn.com/dms/image/C4D12AQE3GOyVsZazOw/article-cover_image-shrink_600_2000/0/1583830696602?e=2147483647&v=beta&t=bYHbKyhMoWsMgtEug6eSf3m0db5ZtGEl437TeS1qkfI" alt="image" width="320" height="220">

#### ✅ Melyik teszteseteket érdemes automatizálni és melyiket nem?
Érdemes automatizálni:

Gyakran ismételt tesztek (regressziós tesztelés).

Stabil és kiszámítható funkciók (pl. bejelentkezés).

Nagy adathalmazokat igénylő tesztek (adatvezérelt tesztek).

Teljesítménytesztek, ahol manuális tesztelés lehetetlen.

Éjszaka futtatható CI/CD pipeline-ba integrálható tesztek.

Nem érdemes automatizálni:

Egyszeri tesztek vagy gyorsan elavuló funkciók.

Vizuális tesztek, ahol az esztétika számít.

Komplex üzleti logikát igénylő UAT vagy UX alapú tesztek.

Kreatív, exploratory tesztelés, ahol a tesztelő szabadon navigál.
#### ✅ Írj le egy jó automatizált tesztet!
from selenium import webdriver
from selenium.webdriver.common.by import By
from selenium.webdriver.support.ui import WebDriverWait
from selenium.webdriver.support import expected_conditions as EC

driver = webdriver.Chrome()
driver.get("https://example.com/login")

# Wait until the username field is visible
WebDriverWait(driver, 10).until(EC.visibility_of_element_located((By.ID, "username")))

driver.find_element(By.ID, "username").send_keys("testuser")
driver.find_element(By.ID, "password").send_keys("securepassword")
driver.find_element(By.ID, "loginBtn").click()

# Assert login was successful
WebDriverWait(driver, 10).until(EC.url_contains("/dashboard"))
assert "/dashboard" in driver.current_url

driver.quit()
#### ✅ Mi a Selenium, Selenium IDE és Selenium WebDriver?
Eszköz	Leírás
Selenium	Automatizált tesztelési keretrendszer webalkalmazásokhoz, több nyelven használható (Java, Python, C#, stb.)
Selenium IDE	Böngésző plugin, amely rögzíti és lejátssza a teszteket (low-code, tanuláshoz jó).
Selenium WebDriver	A Selenium motorja, programozási nyelven keresztül vezérli a böngészőt (pl. ChromeDriver, GeckoDriver).
#### ✅ Hogyan lehet azonosítani a webes elemeket?
Főbb módszerek:

By.ID("elemId")

By.NAME("username")

By.CLASS_NAME("form-control")

By.TAG_NAME("input")

By.XPATH("//input[@id='email']")

By.CSS_SELECTOR("input#email")

Eszközök:

Böngésző fejlesztői eszközei (pl. Chrome DevTools, Inspect).

XPath Helper, ChroPath, SelectorsHub (pluginok).
#### ✅ Hogyan lehet várni az elemekre, és mi lehet a probléma? Gyűjtsd össze a lehetséges hibákat és okokat!
Megoldások:

time.sleep() – kerülendő (lassú, nem dinamikus).

WebDriverWait + ExpectedConditions – helyes módszer.

Példa:

python
Másolás
Szerkesztés
WebDriverWait(driver, 10).until(EC.visibility_of_element_located((By.ID, "submit")))
Lehetséges hibák és okok:

Hiba	Ok
ElementNotVisibleException	Az elem nem látszik a DOM-ban.
NoSuchElementException	Az elem nem létezik vagy hibás lokátor.
StaleElementReferenceException	Az oldal frissült, és az elem referenciája elavult.
TimeoutException	Az elvárt feltétel nem teljesült időben.


#### ✅ Hasonlítsd össze a POM és a Keyword Driven Testing megközelítéseket!
Fókusz	Weboldal struktúráján	Tesztműveleteken (kulcsszavakon)
Megvalósítás	Programozói szinten, OOP	Konfiguráció fájlokon (pl. Excel)
Kód újrafelhasználás	Magas	Magas
Karbantartás	Jó, ha jól szervezett	Jó, nem fejlesztők által is használható
Alkalmazás	Nagy tesztcsomagok	Tesztautomatizáló keretrendszerek
#### ✅ Mi a különbség a TDD és BDD között?
Fókusz	Fejlesztők írják előbb a teszteket	Viselkedés-alapú, üzleti nyelven
Tesztformátum	Unit tesztek, kód alapján	Szenáriók Gherkin nyelven (Given-When-Then)
Kommunikáció	Fejlesztők között	Fejlesztők + üzlet együttműködnek
Eszközök	JUnit, PyTest, NUnit	Cucumber, Behave, SpecFlow
#### ✅ Mi az API tesztelés és miért hasznos?
Mi ez? Az alkalmazás programozási felületeinek (API) működését teszteljük.

Miért hasznos?

Gyorsabb, mint UI tesztelés.

Független a frontendtől.

Hibák hamarabb kiszűrhetők.

Eszközök: Postman, REST Assured, SoapUI, Swagger, cURL.
#### ✅ Mi az adatvezérelt tesztelés és miért hasznos?
ényege: Ugyanazt a tesztet több különböző bemenettel futtatjuk.

Haszna:

Tesztek újrafelhasználása.

Több variáció lefedése kevesebb kóddal.

Adatforrás lehet: CSV, Excel, JSON, adatbázis.

Példa (Python):

python
Másolás
Szerkesztés
import pytest

@pytest.mark.parametrize("username,password", [("admin", "123"), ("user", "abc")])
def test_login(username, password):
    assert login(username, password) == "success"