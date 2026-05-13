# Leaving Limbo
### Syria's Displacement Crisis, 2024–2025

A scrollytelling data story mapping Syrian displacement and return in the year after the Assad government fell. Built for the web with no framework and no build step.

**[View the story →](https://dagmarroth.github.io/AlHol/syria_story.html)**

---

## About

When Bashar al-Assad's government collapsed on December 8, 2024, nearly two million Syrians began returning home. Six million remain internally displaced. This piece follows both populations across 8,325 monitored communities — and traces what happened when al-Hol, the ISIS-associated detention camp in northeastern Syria, began emptying in January 2026 without a coordinated plan.

Data is from the UNHCR/OCHA Displacement Tracking Matrix, December 2025. Quotes are drawn from contemporaneous reporting on the al-Hol exodus and reintegration efforts by Syrian civil society.

## Data & Analysis

The dataset covers 8,325 community-level locations across all 14 Syrian governorates, each with an IDP population count and a returnee count tracking movements since December 8, 2024. The core analytical finding — that aid declined far faster than the crisis — comes from comparing the 58% drop in US funding (USAID / UN Financial Tracking Service) against the 12% drop in the IDP population over the same period.

Community dots are encoded on two independent scales: IDP density (five tiers from 1–2K up to 200K+, rendered in blue) and returnee volume (five tiers from 1–500 up to 30K+, in amber). The scales are deliberately asymmetric — displacement concentrates in a handful of urban hubs like Jaramana (501K) and Ash-Sheikh Maqsoud (270K), while return is more geographically distributed. The 3:1 ratio of displaced to returned (5.96M vs. 1.91M) is the headline figure the map is built to make visceral rather than abstract.

Monthly return data shows a sharp spike in January 2025 (380K in one month) followed by a sustained but slowing trend — consistent with a self-selecting early-mover population giving way to harder cases of displacement where return is blocked by destroyed housing, land disputes, or community rejection. The full data pipeline and chart code are documented in `syria_story.ipynb`.

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
