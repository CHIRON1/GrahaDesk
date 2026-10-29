# GrahaDesk

**The real-time cosmic HUD for your workspace.**

A desktop widget + full app that puts a live Vedic kundli, today's panchang,
and the Hindu calendar on your Windows desktop — behind your windows, always
visible after Win+D, drag it anywhere.

## What it does

- **Live kundli widget** on your desktop: North or South Indian chart with
  real-time planet positions and current panchang (tithi, nakshatra, yoga,
  karana, hora, sunrise/sunset, Vikram Samvat), updated every second.
- **Hindu calendar** with 30 tithi cells per month, festival dates
  (Diwali, Holi, Navratri, Ekadashi and 30+ more), moon phases on every day,
  and PDF export.
- **Birth charts** with D1, D9 Navamsa, D10 Dashamsa, Bhava Chalit, Vimshottari
  dasha, Ashtakavarga, Shadbala, yogas, Sade Sati periods — exportable as PDF.
- **Matching (Guna Milan)** with full Ashtakoota breakdown.
- **Muhurat tools:** Rahu Kaal, Choghadiya, Hora, Brahma Muhurat, Abhijit,
  plus a muhurat finder for travel, marriage, grihapravesh and more.
- **Transits & gochar** on your natal chart, with Saturn's Sade Sati periods.
- **Date search:** type any birthday or event date to see its chart and
  panchang in one click.
- **Hindi + English** throughout, with separate UI and chart-language settings.

## Design choices

- **Accurate.** Positions come from NASA JPL DE440s via Skyfield; Lahiri
  ayanamsa with IAU 2006 precession matches the standard values to ~0.001″.
- **Light.** The widget uses about 0.1 ms of CPU per second while live.
  Panchang values are only recomputed when they change; the whole widget is
  drawn once and cached, each second only the clock is redrawn.
- **Private.** Everything stays on your device. The only network calls are
  the daily GitHub update check. No analytics, no accounts, no ads.
- **Dates 1850 – 2148** supported.

## Install (Windows)

Download `GrahaDesk-Setup-x.y.z.exe` from the latest release and run it.
Per-user install, no admin rights or Python needed. Updates check in once a
day and install with one click (Settings → Updates).

## Tech

PySide6 (LGPL) · Skyfield + jplephem (MIT) · NASA JPL DE440s (public domain) ·
NumPy · GeoNames city data (CC BY 4.0).

## Credits

Built by **Technoshree Technologies Pvt Ltd**. Festival rules follow common
North-Indian conventions and can differ by tradition and region — see
`tools/accuracy_report.md`.
