# Živý Obraz pro Android

Živý Obraz pro Android je doprovodná aplikace ke službě Živý Obraz. Slouží pro rychlý přehled e-paper zařízení, jejich aktuálního stavu, senzorových hodnot a základní diagnostiky přímo v telefonu.

Aplikace se připojuje pomocí exportního klíče Živého Obrazu. Lze přidat jeden nebo více účtů, případně u každého účtu použít také ID skupiny pro omezení zobrazených zařízení.

## Co aplikace umí

- zobrazit přehled e-paper zařízení ze služby Živý Obraz,
- ukázat stav zařízení, poslední kontakt a upozornit na zpožděná nebo problémová zařízení,
- zobrazit dostupné hodnoty jako teplotu, vlhkost, tlak, stav baterie, Wi-Fi signál a technické informace zařízení,
- používat vlastní názvy zařízení a skrýt zařízení, která nechcete mít v hlavním přehledu,
- filtrovat zařízení podle problémů nebo nízké baterie,
- ukládat lokální historii měření a zobrazovat jednoduché grafy za 24 hodin, 7 dní, 30 dní nebo 1 rok,
- vytvářet vlastní karty s vybranými hodnotami, ikonami, barvami a různým rozložením,
- zobrazovat vybrané zařízení nebo vlastní kartu jako widget na domovské obrazovce,
- ručně i automaticky obnovovat data na pozadí,
- volitelně posílat stav baterie telefonu zpět do Živého Obrazu přes importní klíč,
- exportovat a mazat ladicí log pro jednodušší diagnostiku.

## Widgety

Aplikace obsahuje widget pro konkrétní e-paper, který zobrazuje název zařízení, teplotu, vlhkost, baterii a čas poslední aktualizace. Při přidání widgetu lze vybrat konkrétní zařízení nebo automatický výběr.

K dispozici jsou také widgety pro vlastní karty v několika velikostech. Díky nim lze na domovské obrazovce zobrazit například vybrané hodnoty z více zařízení nebo vlastní přehled podle potřeby.

## Soukromí

Konfigurace účtů, klíče, seznam zařízení, vlastní názvy, historie a diagnostické údaje se ukládají lokálně v zařízení. Aplikace komunikuje se službou Živý Obraz přes HTTPS endpointy pro export a volitelný import dat.

Podrobnosti jsou uvedené v [privacy.md](privacy.md).
