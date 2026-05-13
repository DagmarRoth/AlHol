# Leaving Limbo
### Syria's Displacement Crisis, 2024–2025

A scrollytelling data story mapping Syrian displacement and return in the year after the Assad government fell. Built for the web with no framework and no build step.

**[View the story →](https://dagmarroth.github.io/AlHol/syria_story.html)**

---

## About

When Bashar al-Assad's government collapsed on December 8, 2024, nearly two million Syrians began returning home. Six million remain internally displaced. This piece follows both populations across 8,325 monitored communities — and traces what happened when al-Hol, the ISIS-associated detention camp in northeastern Syria, began emptying in January 2026 without a coordinated plan.

Data is from the UNHCR/OCHA Displacement Tracking Matrix, December 2025. Quotes are drawn from contemporaneous reporting on the al-Hol exodus and reintegration efforts by Syrian civil society.

## Stack

- **Leaflet 1.9.4** — dark tile map with flyTo transitions
- **Canvas dot layer** — 8,325 community dots rendered via `Float32Array` and batched rAF loop
- **D3 v7** — animated monthly returnee bar chart
- **IntersectionObserver** — scroll choreography, no scroll event listeners
- **4 full-bleed video sections** — Al Jazeera and WION footage, each with a distinct layout
- Single HTML file, no dependencies to install

## Files

| File | Description |
|------|-------------|
| `syria_story.html` | The story |
| `syria_story.ipynb` | Annotated notebook documenting the data pipeline and front-end code |
| `videoplayback (1).mp4` | Al Jazeera — al-Hol camp footage |
| `videoplayback.mp4` | WION — aerial footage |
