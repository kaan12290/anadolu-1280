# Anadolu 1280 — v0.4.0 geliştirmesi

**0.4.0-dev.1 / Aşama 1. Yayınlanmış v0.4.0 değildir.**

Canlı v0.3.2, `main` ve `backup/v0.3.2-before-v0.4.0` üzerinde korunur.
Bu dal kullanıcı yayın onayı vermeden main ile birleştirilmez; Pages/Site'a yayınlanmaz.

Tamamlananlar: şehir geliri dökümü ve ticaret merkezi/bağlantı/liman/istikrar
etkileri; piyade/süvari/okçu sayılarıyla ordu bölme, aynı şehirde birleştirme,
kısmi/tam terhis; 0,7 saniyelik arazi yardım kutuları; gerçek kale savunma bonusları;
AI'nin aynı ordu işlemlerini kaynak kısıtlarıyla kullanması.

Beyler, yeni şehir bağlılığı ve asimilasyon ayrımı, karma veraset, komutan
isyanları, yaralı/esir defteri ve ilişki/güven/tehdit diplomasisi sonraki aşamalardır.
Aşama 1 mevcut çalışan itibar sistemini korur; Aşama 5'te kayıt göçüyle kaldırılacaktır.

- Plan: `docs/V0.4.0-PLAN.md`
- Teslim ve devam raporu: `docs/V0.4.0-STAGE1-REPORT.md`
- Yapı: mevcut statik oyun; harita, şehir yerleri, görseller ve tasarım dili korundu.
- Kaynak: `anadolu-1280-source.zip` geliştirme kaynağını içerir. Altındaki eski
  sürüm notları kaynak oyunun tarihçesidir; v0.4.0 özelliklerinin tamamlandığı anlamına gelmez.
- Derleme: `npm install`, `npm test`, `npm run build`; oyun `dist/index.html`.
- Geliştirme kayıt anahtarı canlı sürümden ayrıdır. v0.3.2 JSON kayıtları içe alınabilir.

---

# Anadolu 1280 — Taht ve Toprak

Version 0.3.2 — Prestige and political influence.

Prestige is a saved strategic resource: levels 40/60/80/100 improve paid envoys
by +2/+4/+6/+8 relations and reduce alliance relation requirements by 2/4/6/8.
The larger of the two nations’ alliance discounts applies symmetrically.
A prestige embassy costs 15 points for up to +25 relations with a living nation
at peace, with a six-month global cooldown. Court support costs 20 points for
up to +8 stability, +5 legitimacy and +5 court faction support, once per year.
Neither decision costs gold or spends points when its conditions fail.
Victories grant +3 and defeats cost 2; captures grant +8 and lost cities cost 6.
Values stay within 0–100; battle previews do not change prestige.
The prestige number opens a compact decision window; Saray Defteri also links
to it. Existing schema-1 and schema-2 campaigns remain importable.


Version 0.3.1: cinematic palace opening menu with a separate campaign setup panel,
save summary, keyboard close and responsive layout. The background is original
AI-generated concept art inspired by late Seljuk Anatolia, not a documentary image.
Generation details and the exact prompt are in source-data/ui/README.md.
Menu QA covers 1363px desktop, a 1024×720 viewport and a 390×844 viewport,
country/ruler switching, Escape and button close, help, the existing-save
confirmation, resuming a campaign and returning to its dated save summary.
The visual update does not change the simulation or save schema.

Offline historical strategy campaign with combined-arms battles,
conditional peace and diplomacy, historical rulers, branching events and local
communities. The approved parchment map, fixed geographic frame, 69 stable city
regions and 20 playable starting countries are preserved. Six dormant Anatolian
beyliks can emerge through events; they do not start with independent territory.

The Windows portable app and standalone HTML contain every required asset and
run without an account, server or network. Save files transfer between versions;
schema-1 campaigns migrate to schema 2 without restarting their territorial game.

## Connected statecraft systems (0.3)

The new Devlet Yolu screen includes Dynasty, Supply and Command, Trade and a
state-specific Mission Tree. No fog of war or naval combat is added in this update.

- Legitimacy and court/nobility/army support govern procedural succession crises.
  Declaring a candidate changes faction support. Councils, alternate government,
  and territorial dynastic civil war are real saved outcomes. Marriages are abstract
  fictional house ties with diplomatic benefits, never undocumented real marriages.
- Armies carry supply and trace friendly land to capitals/depots. Overcapacity,
  winter mountains, summer desert heat and low stores cause actual attrition.
  Northern mountain crossings cost an additional winter month unless both ends
  have roads. Supply affects battle strength and a live map layer shows the route.
- Commanders have command/siege/cavalry skills, loyalty and experience. Assignments
  are exclusive. Flanking, holding, feigned retreat and controlled withdrawal affect
  battle rounds. Reserve formations commit on round four; controlled withdrawal
  ends combat on round three and reduces pursuit casualties.
- Persistent caravans physically advance between cities, pay on arrival, return,
  and buy replacement goods. War/rebellion blocks routes; escorts reduce raid risk.
  Existing sea transport links support island commerce without adding naval combat.
  Roads affect income, route speed, security and supply capacity; depots are supply hubs.
- All 20 starting nations have themed mission trees and specific territorial goals.
  Claiming the first branch selects trade, expedition or court. Rewards are one-time;
  the alternate branches lock and the final goal requires completing the chosen path.
- Existing schema-1 and schema-2 saves migrate in place. Depth fields and new records
  are validated rather than silently repaired on import.

## Game systems

- Infantry, cavalry and archers have individual recruitment prices and upkeep.
  Seeded battles resolve up to ten rounds with unit losses and morale. Replays
  display recorded outcomes; previews run on copies and do not alter campaign RNG.
- Plains favor cavalry; hills favor archers; mountains/forest favor infantry.
  Marshes and mountains penalize cavalry. Marked river crossings penalize the
  attacking force by 20%. These are coarse scenario attributes, not terrain GIS.
- White peace, compensated peace with return of wartime gains, and demands for
  reparations have separate acceptance rules using score, duration, army balance
  and war exhaustion. Rejection retains war and imposes a three-month cooldown.
- Relations and defensive alliances allow allied transit and defensive war entry.
  AI conducts diplomacy as well as recruitment, movement, sieges and war.
- Every month opens a report with war/alliance announcements and other important
  events. Routine reports can be disabled; important notices remain visible.
- Capital relocation moves the city's economic/manpower bonus and live map mark.
  Market, fort, development and barracks effects are shown with city contributions.
- Cultural-majority and loyalty map modes expose explicitly fictional percentage
  weights. Local rights, autonomy, voluntary integration, organization and garrison
  affect conditional revolts; rebellion suspends city tax/manpower until resolved.
- Historical rulers, known court figures, country histories before 1280 and source
  references are embedded. Unverified portraits are not fabricated. Available
  public-domain historical depictions retain provenance; later depictions are dated.
- Branching events cover selected succession and political developments in
  1280–1335. Player decisions can preserve a strong Seljuk center and loyal frontier
  beys, create tributary administrations, or release independent states. Historical
  campaign events initiate wars rather than transferring cities automatically.

Keys: 1/2/3/4 screens, N next month, Space pause/run, F11 desktop fullscreen.

## Build and verification

```sh
python scripts/prepare-campaign.py
python scripts/build-map.py
node tests/game-engine.test.cjs
node tests/game-depth.test.cjs
node tests/game-prestige.test.cjs
```

Use requirements.txt and installed Sharp. The primary runtime fallback is supported.
Portrait assets are checked in; scripts/fetch-ruler-art.py records verified source
and license metadata and skips files that do not meet its public-domain filter.
The build embeds source-data/campaign-1280.json and ruler art in dist/index.html.
Set ANADOLU_OUTPUT_DIR to also write Anadolu_1280.html into a deliverable directory.
The earlier atlas and UI concepts remain at dist/atlas.html and dist/arayuz.html.

src/game-engine.js and game-depth.js implement the browser-independent simulation; game-app.js and
game-expansion.js and game-depth-app.js implement the UI. Twenty-seven baseline simulation checks cover all starts,
unit costs, terrain/river modifiers, deterministic previews, peace rejection and
acceptance, defensive alliances, capital bonuses, city totals, revolts, integration,
branching beyliks, strong Seljuk survival, fragmentation, migration and corrupt saves.
Eighteen additional depth checks cover migration, dynastic crisis and civil war, marriages,
supply loss, winter delays, construction, commanders, tactics/reserves, withdrawals,
caravan ledgers, wartime closures, island commerce and exclusive mission branches.
Long AI campaigns validate finite state and bounded records. Chromium UI checks
cover the playable screens and interactive reports. Windows launch cannot be tested
on this Linux host; packaging checks the official runtime hash, archive CRC, PE
signature and exact equality of packaged HTML with the tested build.

## Desktop packaging

```sh
python scripts/package-desktop.py \
  --runtime /absolute/path/electron-v45.0.0-win32-x64.zip \
  --checksums /absolute/path/SHASUMS256.txt \
  --output /absolute/output/directory
```

Electron uses a sandboxed, isolated renderer, no Node integration, no external
navigation and no network calls. Official runtime and Chromium licenses ship in
the portable ZIP. Portrait credits are embedded; source-data/ruler-art/credits.json
retains the source record. Map geometry uses public-domain Natural Earth. Country
limits are approximate reconstructions and city regions are gameplay areas.
Cultural percentages, army strengths and economy are game parameters, not census
or historical statistics. The web distribution is published through GitHub Pages.
