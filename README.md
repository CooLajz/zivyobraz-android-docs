# Živý Obraz pro Android

[English version](README.en.md)

Android aplikace pro rychlý přehled zařízení ze služby [**Živý Obraz**](https://zivyobraz.eu/?page=o-sluzbe). V telefonu zobrazuje stav e-paperů, naměřené i vlastní hodnoty, baterie, historii grafů, lokální upozornění, zálohy a widgety přímo na domovské obrazovce.

## Instalace z Google Play

Aplikace **Živý Obraz** je veřejně dostupná v Google Play:

[Nainstalovat aplikaci z Google Play](https://play.google.com/store/apps/details?id=eu.coolajz.zivyobraz)

Pokud máte zájem podílet se na testování nových verzí před jejich vydáním, můžete se připojit k otevřenému beta testování:

[Připojit se k OpenBeta testování](https://play.google.com/apps/testing/eu.coolajz.zivyobraz)

## Hlavní funkce

- **Přehled všech zařízení** - teplota, vlhkost, tlak nebo CO2, baterie, online stav, souhrn dashboardu a rychlé filtrování problémů.
- **Přehled baterií e-paperů** - samostatný seznam zařízení řazený podle baterie, včetně zařízení bez dostupného procenta.
- **Lokální upozornění na e-papery** - Android notifikace pro nově zpožděná zařízení, návrat online a baterii na 20 % nebo méně.
- **Widgety na domovskou obrazovku** - jeden widget pro konkrétní e-paper a tři velikosti widgetů pro vlastní karty.
- **Vlastní karty pro libovolné hodnoty** - sestavení karty z hodnot dostupných v exportu `my_values`, včetně rozložení, ikon, barev, prefixů, suffixů, formátu čísel a podmíněných barev.
- **Automatická aktualizace dat** - ruční refresh, obnova při návratu do aplikace, widget refresh a plánovaná obnova na pozadí přes Android WorkManager.
- **Detail zařízení a grafy** - informace o signálu, baterii, firmwaru, posledním kontaktu, diagnostice a historii měření s možností fullscreen grafu.
- **Více účtů a skupin** - více exportních klíčů, volitelný Group ID filtr, skenování klíčů z QR kódu a zobrazení informací o předplatném.
- **Úprava dashboardu** - vlastní aliasy, změna pořadí zařízení a vlastních karet, skrytí nepoužívaných e-paperů.
- **Volitelné odesílání baterie telefonu** - stav baterie Android telefonu lze posílat zpět do Živého Obrazu přes importní API.
- **Šifrované zálohy** - ruční a volitelné automatické zálohy nastavení, uložených klíčů a volitelně také historie měření.
- **Diagnostika provozu** - ladicí log, stav posledního background refresh běhu, diagnostika odesílání baterie telefonu, informace o buildu a přehled lokální databáze grafů.

## Ukázky aplikace

### Přehled zařízení

Dashboard ukazuje e-papery v kartách, souhrn zařízení, vlastních karet, problémů a baterií. Klepnutím na souhrn lze rychle filtrovat zobrazení.

<p>
  <img src="pics/hlavni_obrazovka_zarizeni.png" alt="Hlavní obrazovka se seznamem zařízení" width="280">
  <img src="pics/hlavni_obrazovka_vlastni_karty.png" alt="Hlavní obrazovka s vlastními kartami" width="280">
</p>

### Detail zařízení a historie

Detail e-paperu zobrazuje aktuální hodnoty, stav kontaktu, baterii, grafy historie a technické diagnostické informace zařízení.

<p>
  <img src="pics/detail_zarizeni_historie.png" alt="Detail zařízení s historií měření" width="280">
  <img src="pics/detail_zarizeni_diagnostika.png" alt="Detail zařízení s technickou diagnostikou" width="280">
</p>

### Přehled baterií

Samostatný přehled baterií pomáhá rychle najít e-papery s nejnižší baterií a zobrazit také napětí baterie.

<p>
  <img src="pics/prehled_baterii.png" alt="Přehled baterií e-paperů" width="280">
</p>

### Vlastní karty a widgety

Vlastní karty mohou kombinovat hodnoty z exportu `my_values`, používat vlastní ikony, barvy, rozložení a podmíněné barvy. Stejné karty lze přidat také jako widgety na domovskou obrazovku Androidu.

<p>
  <img src="pics/detail_vlastni_karty_historie.png" alt="Detail vlastní karty s grafy" width="280">
  <img src="pics/editor_vlastni_karty.png" alt="Editor vlastní karty" width="280">
</p>

<p>
  <img src="pics/widgety_na_plose.png" alt="Widgety Živý Obraz na domovské obrazovce Androidu" width="560">
</p>

### Nastavení, zálohy a databáze grafů

Nastavení obsahuje správu účtů, upozornění na e-papery, šifrované zálohy a přehled lokální databáze grafů.

<p>
  <img src="pics/nastaveni_zalohy.png" alt="Nastavení účtů, upozornění a záloh" width="280">
  <img src="pics/databaze_grafu.png" alt="Přehled databáze grafů" width="420">
</p>

## Jak aplikaci nastavit

### 1. Připravte exportní klíč

Ve službě Živý Obraz si připravte **exportní klíč**. Aplikace ho používá pro načítání e-paperů, informací o účtu a vlastních hodnot.

Pokud chcete v aplikaci zobrazit jen vybranou skupinu zařízení, připravte si také **Group ID**. Tento krok je volitelný.

### 2. Přidejte účet v aplikaci

1. Otevřete aplikaci Živý Obraz.
2. Otevřete **Nastavení**.
3. Vyberte existující účet nebo klepněte na **Přidat další účet**.
4. Vyplňte název účtu.
5. Vložte exportní klíč nebo ho naskenujte z QR kódu.
6. Volitelně vložte Group ID.
7. Pokud chcete odesílat baterii telefonu do Živého Obrazu, zapněte tuto volbu a doplňte importní klíč a název zařízení.
8. Uložte změny tlačítkem **Hotovo**.

Po uložení aplikace zkontroluje nastavení účtů, načte e-papery, uloží data pro widgety a může zobrazit také informace o předplatném účtu.

Uložené exportní a importní klíče se v editoru znovu nezobrazují celé. Pro jejich nahrazení použijte **Zadat znovu** nebo účet odeberte a přidejte znovu.

### 3. Přidejte widget na domovskou obrazovku

1. Na domovské obrazovce Androidu podržte volné místo.
2. Vyberte **Widgety** a najděte **Živý Obraz**.
3. Přidejte widget pro e-paper.
4. Při konfiguraci vyberte konkrétní zařízení nebo ponechte možnost **Automaticky**.

Widget používá poslední načtená data a průběžně si plánuje aktualizace přes Android WorkManager. Pokud při přidávání widgetu nejsou dostupná žádná data, otevřete aplikaci a proveďte ruční obnovu.

### 4. Vytvořte vlastní kartu a widget

1. Na dashboardu otevřete část **Vlastní** nebo klepněte na přidání vlastní karty.
2. Zvolte název, ikonu, barvu a rozložení karty.
3. Přidejte hodnoty z exportu `my_values`.
4. U každé hodnoty nastavte název, ikonu, barvu názvu, barvu hodnoty, prefix, suffix a případně formát čísla.
5. Pro číselné hodnoty můžete nastavit podmíněné barvy a plynulý přechod barev.
6. Přidejte na domovskou obrazovku malý, střední nebo velký widget vlastní karty a vyberte vytvořenou kartu.

Vlastní karta je vhodná například pro venkovní teplotu, vlhkost, tlak, CO2, kvalitu vzduchu, spotřebu energie, stav baterie nebo jakoukoli další hodnotu dostupnou ve vašem exportu.

## Dashboard, baterie a historie grafů

Dashboard zobrazuje e-papery a vlastní karty v jednom přehledu. Nahoře je souhrn pro zařízení, vlastní karty, problémy a slabé baterie. Klepnutím lze přepnout filtr na všechna zařízení, vlastní karty, problémová zařízení nebo zařízení s nízkou baterií.

Zařízení je v aplikaci považované za **po termínu**, pokud je více než 15 minut za očekávaným dalším kontaktem. Slabá baterie v dashboardu znamená přibližně 30 % a méně.

Přehled baterií zobrazuje e-papery podle stavu baterie od nejnižší po vyšší. Zařízení bez dostupného procenta baterie jsou oddělená, aby bylo jasné, že je aplikace nemůže přesně seřadit.

Detail e-paperu obsahuje:

- aktuální hodnoty teploty, vlhkosti, tlaku nebo CO2,
- stav kontaktu, poslední kontakt a další očekávaný kontakt,
- Wi-Fi SSID a RSSI,
- účet, skupinu, model, rozlišení, barvy, desku a firmware,
- napětí baterie, důvod restartu, čas stažení obrázku a čas obnovení displeje,
- historii baterie, napětí, teploty, vlhkosti a tlaku nebo CO2.

Grafy podporují rozsahy **24 h**, **7 dní**, **30 dní** a **1 rok**. Graf lze otevřít na celou obrazovku a tažením nebo podržením v grafu zobrazit hodnotu v konkrétním čase. Poslední zvolená metrika a rozsah se ukládají pro dané zařízení.

Historii grafů lze smazat pro konkrétní e-paper nebo pro konkrétní vlastní kartu. V nastavení je také přehled lokální databáze grafů s velikostí, počtem záznamů, počtem sledovaných zařízení a počtem sledovaných vlastních hodnot.

## Vlastní karty a widgety

Vlastní karty se plní z hodnot dostupných v exportu `my_values`. Jedna karta může používat hodnoty z různých účtů. Hodnoty mohou být textové, číselné, desetinné, logické nebo prázdné; historie se ukládá jen pro číselné hodnoty.

Dostupná rozložení:

- **1 dominantní** - jedna velká hodnota.
- **2 rozdělené** - dvě vyvážené hodnoty.
- **3 smíšené** - jedna hlavní hodnota a dvě menší hodnoty.
- **4 mřížka** - čtyři kompaktní hodnoty.
- **Seznam** - až šest řádků.

Editor podporuje duplikování karet, změnu pořadí karet, výběr ikon podle kategorií, paletu barev, vlastní prefixy a suffixy, poloviční velikost suffixu pro jednotky, formátování čísel na celé číslo nebo 1 až 3 desetinná místa a podmíněné barvy podle prahů.

Widgety vlastních karet existují ve třech velikostech:

- **Malý widget** podporuje rozložení 1 dominantní, 2 rozdělené, 3 smíšené a seznam.
- **Střední widget** podporuje rozložení 1 dominantní, 2 rozdělené, 3 smíšené a 4 mřížka.
- **Velký widget** podporuje všechna rozložení.

Pokud karta obsahuje číselné hodnoty, aplikace pro ni ukládá samostatnou historii. Detail vlastní karty pak nabídne grafy se stejnými rozsahy jako u e-paperů.

## Lokální upozornění na e-papery

Aplikace umí posílat Android notifikace při změně stavu e-paperů. Funkce je zapnutá v nastavení aplikace, ale na Androidu 13 a novějším je zároveň potřeba povolit systémové oprávnění pro notifikace.

Aplikace upozorní na:

- nově zpožděný e-paper,
- návrat zařízení zpět online,
- pokles baterie e-paperu na 20 % nebo méně.

Notifikace se vyhodnocují při refreshi na pozadí. Aplikace si ukládá poslední známý stav zařízení, aby stejné upozornění neposílala opakovaně. U nízké baterie používá jednodenní ochranu proti příliš častému opakování.

## Obnova dat na pozadí

Aplikace používá Android WorkManager:

- hlavní background refresh se plánuje v intervalu 30 minut a vyžaduje připojení k síti,
- widget refresh se plánuje v intervalu 15 minut a také vyžaduje připojení k síti,
- při návratu aplikace do popředí se data obnoví, pokud jsou starší než přibližně 5 minut.

Android může práci na pozadí odložit v režimu Doze, při šetření baterie nebo podle nastavení výrobce telefonu. Pokud se data neaktualizují tak často, jak čekáte, může pomoci nastavit baterii aplikace v systému na režim **Bez omezení**.

V nastavení je vidět diagnostika posledního naplánování, spuštění a dokončení background refresh běhu.

## Odesílání baterie telefonu do Živého Obrazu

U každého účtu lze zapnout odesílání baterie telefonu do Živého Obrazu. Je potřeba:

- zapnout volbu **Odesílat baterii zařízení do ŽO**,
- zadat importní klíč,
- zadat název zařízení, pod kterým se má baterie v Živém Obrazu zapisovat.

Aplikace odesílá procenta baterie a stav nabíjení na importní endpoint Živého Obrazu. V nastavení je k dispozici ruční test odeslání a diagnostika posledního pokusu.

## Zálohy a obnova

Android verze používá lokální šifrované zálohy do složky vybrané uživatelem. Záloha není cloudová synchronizace; je to soubor, který si uložíte do vybrané složky v zařízení nebo do úložiště dostupného přes systémový výběr souborů.

Záloha vždy obsahuje:

- nastavení aplikace,
- účty,
- aliasy,
- pořadí a skrytí zařízení,
- vlastní karty,
- uložené exportní a importní klíče.

Volitelně může obsahovat také lokální databázi historie měření pro grafy.

Záloha je chráněná heslem o délce alespoň 8 znaků. Soubor používá formát `.zivybackup` a je šifrovaný pomocí AES-256-GCM; klíč se odvozuje z hesla pomocí PBKDF2WithHmacSHA256.

V nastavení lze:

- vybrat složku pro zálohy,
- nastavit nebo změnit heslo,
- zvolit, zda zahrnout historii měření,
- zapnout automatické denní zálohy,
- spustit ruční zálohu,
- obnovit data ze zálohy.

Automatické zálohy běží jednou denně, pokud Android povolí práci na pozadí a baterie není nízká.

## Nastavení, diagnostika a soukromí

V nastavení najdete správu účtů, upozornění, zálohy, databázi grafů, background refresh, odesílání baterie telefonu, ladicí log a informace o buildu aplikace.

Exportní a importní klíče se ukládají do šifrovaných Android SharedPreferences. Běžná konfigurace, cache zařízení, vlastní karty a stav dashboardu se ukládají lokálně v zařízení. Historie měření je uložená v lokální SQLite databázi.

Aplikace komunikuje se službou Živý Obraz přes:

- exportní API: `https://out.zivyobraz.eu/`
- importní API pro baterii telefonu: `https://in.zivyobraz.eu/`

Podrobnosti o zpracování dat jsou uvedené v [privacy.md](privacy.md).

## Technické informace

- Platforma: Android
- Balíček aplikace: `eu.coolajz.zivyobraz`
- Minimální Android SDK: 26
- Cílové Android SDK: 35
- Jazyk: Kotlin
- UI: Jetpack Compose a Material 3
- Background sync: WorkManager
- Lokální úložiště: SharedPreferences, EncryptedSharedPreferences a SQLite
- Widgety: AppWidgetProvider a RemoteViews
- QR skenování: CameraX a ML Kit Barcode Scanning
