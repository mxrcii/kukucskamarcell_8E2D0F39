> a weboldal a rocket league nevu jatekrol szol
---
> html, js, css van hasznalva
---
> ebbe a tombbe van az osszes region es pontszamuk 2025 rlcs-re
```javascript
const lcqPointsByRegion = {
      "Middle East & North Africa": 32,
      "Europe": 26.75,
      "North America": 19,
      "South America": 18,
      "Asia-Pacific": 10,
      "Oceania": 8,
      "Sub-Saharan Africa": 7
};
```
> ez a ciklus pedig megkeresi a legtobb pontot szerzett regiont es kiirja azt

```javascript
for (const region in lcqPointsByRegion) {
      const pts = lcqPointsByRegion[region];
      if (pts > maxPts) {
        maxPts = pts;
        topRegion = region;
      }
    }
    document.getElementById("top-region-output").textContent =
      `${topRegion} – ${maxPts} pont`;
```

