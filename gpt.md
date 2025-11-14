# gpt promptok 
----
## elfelejtettem bejelentkezni es bezartam az ablakot de nagyreszt ezek voltak a promptok
----
>a 3. weboldal pedig legyen a 2025 rlcs-rol, amiben eloszor is kigyujtod az osszes resztvevo csapatot es kiirod oket, majd kigyujtod a last chance qualifier osszes regioit es pontszamaikat es ezek kozul kiirod hogy melyiknek lett tobb. ez utan kigyujtod az eddigi rlcs wolrd championship prize pooljat es mind ezt eltarolod aztan osszegezve kiirod.
----
## gpt valasza 
---
## 3. weboldal
----
```html
<!DOCTYPE html>
<html lang="hu">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>RLCS 2025 World Championship – Adatok és Elemzés</title>
  <style>
    body {
      background-color: #121212;
      color: #e0e0e0;
      font-family: Arial, sans-serif;
      padding: 20px;
    }
    h1, h2 {
      color: #00aaff;
    }
    section {
      margin-bottom: 40px;
    }
    pre {
      background-color: #1f1f1f;
      padding: 10px;
      overflow: auto;
    }
  </style>
</head>
<body>
<nav style="
  background-color: #004080;
  padding: 10px 20px;
  display: flex;
  gap: 20px;
  justify-content: center;
  font-weight: bold;
">
  <a href="oldal.html" style="color: #ffffff; text-decoration: none;">🎮 Játék bemutatása</a>
  <a href="esport.html" style="color: #ffffff; text-decoration: none;">🏆 E-sport történelem</a>
  <a href="25.html" style="color: #ffffff; text-decoration: none;">📊 RLCS 2025 statisztikák</a>
</nav>
  <header>
    <h1>RLCS 2025 World Championship – Adatok</h1>
  </header>

  <section id="teams-section">
    <h2>Résztvevő csapatok (2025)</h2>
    <ul id="teams-list">
    </ul>
  </section>

  <section id="lcq-section">
    <h2>Last Chance Qualifier pontszámok régiónként</h2>
    <pre id="lcq-json"></pre>
    <p>A régió, amelyik a legtöbb pontot kapta: <strong id="top-region-output"></strong></p>
  </section>

  <section id="prize-section">
    <h2>Díjalap történet és összegzés</h2>
    <p id="prize-sum-text"></p>
    <pre id="prize-list"></pre>
  </section>

  <script>
    const teams2025 = [
      "Karmine Corp", "Dignitas", "Team Vitality", "Geekay Esports",
      "NRG", "The Ultimates", "Spacestation Gaming", "Wildcard",
      "FURIA Esports", "Team Secret", "Team Falcons", "Twisted Minds",
      "Gen.G Mobil1 Racing", "TSM", "Virtus.pro", "FUT Esports",
      "ROC Esports", "MIBR", "Shopify Rebellion", "Ninjas in Pyjamas"
    ];

    const lcqPointsByRegion = {
      "Middle East & North Africa": 32,
      "Europe": 26.75,
      "North America": 19,
      "South America": 18,
      "Asia-Pacific": 10,
      "Oceania": 8,
      "Sub-Saharan Africa": 7
    };

    const prizePoolsHistory = [
      { year: 2016, prizePool: 150000 },
      { year: 2017, prizePool: 250000 },
      { year: 2018, prizePool: 500000 },
      { year: 2019, prizePool: 1000000 },
      { year: 2020, prizePool: 1100000 },
      { year: 2021, prizePool: 1200000 },
      { year: 2022, prizePool: 2085000 },
      { year: 2023, prizePool: 1500000 },
      { year: 2024, prizePool: 1000000 },
      { year: 2025, prizePool: 1200000 }  // 2025-ös adat: $1,200,000 USD :contentReference[oaicite:3]{index=3}
    ];


    const teamsListElem = document.getElementById("teams-list");
    teams2025.forEach(team => {
      const li = document.createElement("li");
      li.textContent = team;
      teamsListElem.appendChild(li);
    });

    document.getElementById("lcq-json").textContent =
      JSON.stringify(lcqPointsByRegion, null, 2);

    let topRegion = null;
    let maxPts = -Infinity;
    for (const region in lcqPointsByRegion) {
      const pts = lcqPointsByRegion[region];
      if (pts > maxPts) {
        maxPts = pts;
        topRegion = region;
      }
    }
    document.getElementById("top-region-output").textContent =
      `${topRegion} – ${maxPts} pont`;

    let totalPrize = 0;
    prizePoolsHistory.forEach(item => {
      totalPrize += item.prizePool;
    });
    document.getElementById("prize-sum-text").textContent =
      `Az összes eddigi Rocket League World Championship díjalap összege: $${totalPrize.toLocaleString()} USD`;

    document.getElementById("prize-list").textContent =
      prizePoolsHistory
        .map(item => `${item.year}: $${item.prizePool.toLocaleString()}`)
        .join("\n");
  </script>
</body>
</html>
```
---
## masodik weboldal
> csinalj egy weboldalt a rocket league esportjarol. a weboldal ugy epuljon fel, hogy eloszor leirod az elso esport eventet majd az rlcs season 1 es annak gyozteseit. ezek utan irj a rocket league esportjarol magyarorszagon: mikor kezdodott, elso verseny, annak gyoztesei(magyar esportrol nem birt irni annak egy reszet en kellett irjam.)
```html
<!DOCTYPE html>
<html lang="hu">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Rocket League eSport Bemutató</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #1a1a1a;
      color: #e0e0e0;
      margin: 0;
      padding: 0;
    }
    header {
      background-color: #004080;
      padding: 20px;
      text-align: center;
    }
    header h1 {
      color: #ffffff;
      margin: 0;
    }
    .container {
      max-width: 800px;
      margin: auto;
      padding: 20px;
    }
    h2 {
      color: #00ccff;
      margin-top: 40px;
    }
    p {
      line-height: 1.6;
    }
  </style>
</head>
<body>
<nav style="
  background-color: #004080;
  padding: 10px 20px;
  display: flex;
  gap: 20px;
  justify-content: center;
  font-weight: bold;
">
  <a href="oldal.html" style="color: #ffffff; text-decoration: none;">🎮 Játék bemutatása</a>
  <a href="esport.html" style="color: #ffffff; text-decoration: none;">🏆 E-sport történelem</a>
  <a href="25.html" style="color: #ffffff; text-decoration: none;">📊 RLCS 2025 statisztikák</a>
</nav>
  <header>
    <h1>Rocket League eSport – Történet és Jelentős Helyi Események</h1>
  </header>

  <div class="container">
    <h2>Mikor indult az eSport Rocket League-ben?</h2>
    <p>
      A Rocket League hivatalosan 2016 márciusában jelentette be az első Rocket League Championship Series‑t (RLCS), mint versenyrendszert, amely azóta is a játék egyik legfontosabb eSport eseményévé vált.
    </p>

    <h2>Az első világbajnokság</h2>
    <p>
      Dátum: <strong>2016. augusztus 7.</strong>
    </p>
    <p>
      Győztes csapat: <a href="https://liquipedia.net/rocketleague/IBUYPOWER" style="font-weight: bold; color: #00ccff;">iBuyPower Cosmic</a>
      Tagok: Cameron “Kronovi” Bills, Brandon “Lachinio” Lachin, Ted “0ver Zer0” Keil.
      Ők domináltak az egész verseny során és a finals best of 7-ben egy kénylemes 4-2-es győzlmet értek el a FlipSid3 Tactics ellen, ezzel megnyerve a legelső rlcs-t
    </p>

    <h2>Magyarországi eSport események és Rocket League helyzet</h2>
    <p>
      Magyarországon a <strong>Magyar Nemzeti E‑sport Bajnokság (MNEB)</strong> 2018‑tól működik, és Rocket League is része a bajnokságnak.
    </p>
    <p>
      A legelso magyar verseny ami fel van jegyezve liquipedian az a <a href="https://liquipedia.net/rocketleague/Dribble_Hungary/3v3/Season_1/Elite_Division" style="font-weight: bold; color: #00ccff;">Dribble Hungary 3v3 Season 1: Elite Division</a>
    </p>
    <p>
     A Dribble Hungary 3v3 Season 1: Elite Division bajnokai az <a href="https://liquipedia.net/rocketleague/MTK_Budapest/Results"style="font-weight: bold; color: #00ccff;">MTK Budapest</a> Tagjai: Zoltán "CokeHUN" Bartha, Gergely "ProFessorvF" Gellén, Richárd "richmond" Yem
    </p>
  </div>

  
</body>
</html>
```
---

## 2. weboldal

> csinalj egy weboldalt a rocket league nevu jatekrol. a weboldal ugy epuljon fel, hogy eloszor beszelsz a jatek tortenelmerol: peldaul mikor jelent meg, milyen enginen fut, aztan leirod a jatek menetet, mechanikait.

```html

<!DOCTYPE html>
<html lang="hu">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>1.</title>
  <style>
    body {
      font-family: Arial, sans-serif;
      background-color: #0f0f0f;
      color: #ffffff;
      line-height: 1.6;
      margin: 0;
      padding: 0;
    }

    header {
      background-color: #ff6600;
      padding: 20px 0;
      text-align: center;
    }

    header h1 {
      margin: 0;
      font-size: 2.5em;
    }

    .container {
      padding: 20px;
      max-width: 900px;
      margin: auto;
    }

    h2 {
      color: #00aaff;
    }

    p {
      margin-bottom: 15px;
    }
    #nav{
        
        border: 2px solid orange;
        width: 200px;
        text-align: center;
        }
       a{color: #00aaff;
    font-weight: bold;}
  </style>
</head>
<body>
<nav style="
  background-color: #004080;
  padding: 10px 20px;
  display: flex;
  gap: 20px;
  justify-content: center;
  font-weight: bold;
">
  <a href="oldal.html" style="color: #ffffff; text-decoration: none;">🎮 Játék bemutatása</a>
  <a href="esport.html" style="color: #ffffff; text-decoration: none;">🏆 E-sport történelem</a>
  <a href="25.html" style="color: #ffffff; text-decoration: none;">📊 RLCS 2025 statisztikák</a>
</nav>
  <header>
    <h1>Rocket League – A Játék Bemutatása</h1>
  </header>
  
  <div class="container">
    <h2>A játék története</h2>
    <p>A Rocket League egy autós foci videojáték, amelyet a Psyonix fejlesztett és 2015. július 7-én adtak ki.</p>
    <p>A játék elődje a <strong>Supersonic Acrobatic Rocket-Powered Battle-Cars</strong> volt, amely 2008-ban jelent meg, de csak korlátozott sikert ért el.</p>
    <p>A Rocket League Unreal Engine 3-on fut, és több platformra is elérhető: PC, PlayStation, Xbox, Nintendo Switch.</p>
    <p>2019-ben az Epic Games felvásárolta a Psyonixot, és 2020-ban a játék ingyenessé vált az Epic Games Store-ban.</p>

    <h2>A játékmenet</h2>
    <p>A Rocket League lényege, hogy autókkal játszol focit. A célod az, hogy az óriási labdát az ellenfél kapujába juttasd, miközben a saját kapudat véded.</p>
    <p>A meccsek 5 percesek, és jellemzően 1v1, 2v2 vagy 3v3 felállásban zajlanak. Léteznek különleges játékmódok is, mint a „Rumble”, „Dropshot” vagy a „Hoops”.</p>
    <p>Az autók képesek gyorsítani („boost”-ot használni), ugrani, falon mászni, sőt levegőben is irányíthatók, így a játék tele van látványos trükkökkel és akciókkal.</p>
    <p>A játék egyszerre könnyen tanulható és nehezen mesteri szinten elsajátítható, ami miatt nagy közösségi és e-sport jelenléttel is rendelkezik.</p>
  </div>

</body>
</html>


```