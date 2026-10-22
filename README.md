# Chatuchot I-Girder Erection 4D BIM

4D BIM method statement – precast I-girder erection by two-crane tandem lift, Chalong Rat Expressway Extension – static web app (three.js), opens in any modern browser, installable as a PWA.

| Feature | |
|---|---|
| 4D timeline | play / scrub dates, Gantt, S-curve, method statement steps |
| BIM | click an element for ID, drawing ref, quantity, dates · GLB export |
| Themes | Day · Sunset · Night · BIM 4D · Blueprint · TH / EN |
| Drone | automatic drone tour + free-fly (W/A/S/D, R/F, mouse) · ambient sound |
| Update programme | upload PDF (MS Project print) / MS Project XML / CSV / JSON – stored per browser |

## Run locally
```bash
python -m http.server 8080
```
open http://localhost:8080

## Deploy (GitHub Pages)
Push to `main`, then Settings ▸ Pages ▸ Source = **GitHub Actions**. The workflow publishes index.html, manifest, sw.js, icons and sample/.

> A public repository / Pages site exposes the model geometry and programme to anyone with the link. Use a private repo with
> access-controlled hosting if the project data is confidential. Source drawings are never committed (.gitignore).

## Update the programme
PDF printed from MS Project (ID / Task Name / Duration / Start / Finish), MS Project XML (Save As ▸ XML), CSV, or JSON.
.mpp → `python tools/mpp2json.py file.mpp` (Java + `pip install mpxj`) or Save As XML.
