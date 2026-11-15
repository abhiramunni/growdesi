# GrowDesi — Your Balcony Kitchen Garden

A single-file web app that helps anyone with an Indian balcony grow their own
vegetables and herbs: what to sow this month, a visual garden-bed planner,
daily watering care and harvest countdowns. No backend, no signup — everything
is saved in the browser's localStorage.

**Live:** https://abhiramunni.github.io/growdesi/

## What it does

- **Sow in November** — a seed-packet rail showing the 17 plants that sow well
  right now (winter is the best sowing season for most of India), each with
  sprouting time, harvest time, pot size, sun needs and a growing tip.
- **My Garden** — three beds (sunny railing, partial shade, pots & grow bags)
  with 12 plots. Tap an empty plot to plant, and each planted plot shows a
  growth ring, sowing date, expected harvest date and a daily water button.
- **Care & Harvest** — today's jobs auto-generated from your garden (water
  what's thirsty, harvest what's ready, check leaves, finger-test the soil)
  plus a soonest-first harvest countdown.
- **Plant Library** — 20 kitchen-garden favourites (tomato, methi, palak,
  dhania, pudina, radish, beans, peas, cauliflower and more) with honest
  numbers: germination days, days to harvest, pot size, spacing, sun and
  water. Search, filter by category, or show easy plants only.
- **Guides** — six plain-language answers: soil mix, watering, balcony sun,
  neem spray for pests, bucket compost, and when to harvest.
- **Tools** — copy a garden summary, remove sample plants, or erase
  everything (two-tap confirm).

## Details

- **Design:** warm editorial palette (ivory paper, espresso ink, bronze /
  terracotta / gold), Fraunces + Inter, cinematic sprout intro with
  tap-to-skip (quick version on return visits), 3-step onboarding coach,
  Ken Burns drift on the two AI-generated garden photos.
- **Data:** sowing months and harvest windows are typical for the Indian
  plains; the app notes that hills sow winter crops a month earlier and the
  far south sows through December. Your balcony's sun and soil will shift
  timings a little.
- **Privacy:** all data stays on the device (localStorage key `growdesi_v1`).
  No accounts, no tracking, no network calls except Google Fonts.

## Files

- `index.html` — the whole app (single self-contained file, ~490 KB
  including two embedded photos)
- `qa-test.js` — jsdom functional test (66 assertions)

## QA

- `node --check` on the extracted script: OK
- jsdom functional test: **66/66 assertions pass**, zero uncaught JS errors
  (November sowing list, seeded garden maths, harvest ordering, planting /
  watering / removing, search & filters, guide accordion, copy summary,
  sample removal, erase-all, localStorage persistence, coach, intro)
- One real bug found and fixed during QA: the plant picker closed the sheet
  before reading which plot was pending, so picking a plant planted nothing.

## Built

15 November 2026 — morning daily-app run. November sowing is the seasonal
hook: cool nights and gentle sun make it the best planting month of the year
for most of India.
