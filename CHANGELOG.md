# CHANGELOG

Sumár release-ov. Plné detaily v [Releases](https://github.com/princeofwellness/edututor-releases/releases).

## v0.8.8 — Splash polish *(pripravované)*

- Splash wordmark *EduTutor* → *Vitaj* (rovnaký amber italic ako Next welcome page) — žiadny mid-boot text swap.

## v0.8.7 — HW Setup full polish + cloud BYOK + piper + Vitaj welcome

- Veľké **Vitaj** v amber Instrument Serif italic na úvodnej Orb obrazovke
- LLM provider sa automaticky aktivuje po pridaní API kľúča — netreba vyberať znova v HW Setup
- Add Návod_na_instalaciu.html + technická dokumentácia PDF do release assets

## v0.8.6 — Menší font v systémovom prompte + Edge voice picker + offline auto-redirect

- Mozog textarea fontSize 14.5 → 12.5px (dlhé prompty čitateľné)
- Nová sekcia *Hlas tutora* v Prehľade — Lukáš / Viktória s SaveBar
- Auto-redirect do Settings keď backend offline alebo žiadny LLM model

## v0.8.5 — Save buttons späť + true fullscreen + system prompt polish

- SaveBar primitív naprieč HW Setup (Persona, Hlas, atď.) — explicitné Uložiť tlačidlá
- True fullscreen responsive — žiadny max-width cap nad 1024px
- MasterPromptSection toolbar (Vymazať / Skopírovať), lepšie mode pills
- Welcome page — *edututor* wordmark medzi Orb a Vstúpiť (v0.8.7 prešlo na Vitaj heading)

## v0.8.4 — Polished HW Setup + cloud TTS BYOK + local piper + chat error nudge

- 8 záložiek HW Setup (Prehľad, Detaily, Inštalácia, LLM, Hlas, Počúvanie, Persona, Mozog)
- Cloud BYOK pre Azure (kľúč + región) a ElevenLabs
- Lokálny Piper install — slovenský hlas `sk_SK-lili-medium` cez GitHub binary (žiadny pip)
- Chat error nudge — 402 / 401 / 429 sa zobrazia slovensky namiesto "technickej chyby"
- Skip "Pripravujem tvojho učiteľa" page — onboarding rovno na Vitaj

## v0.7.7 — Production wrap (1.0 candidate)

Posledná v0.7.x stabilná. HW Setup polish, audio architecture, fresh launch.

*Predošlé v0.4.x – v0.7.x verzie sú označené ako prereleases — pozri Releases history.*

---

## Schéma verzií

- `MAJOR.MINOR.PATCH` (SemVer)
- **PATCH** (0.8.7 → 0.8.8) — bug fix, polish, žiadne breaking zmeny pre používateľa
- **MINOR** (0.7.7 → 0.8.0) — nové features, redesignované obrazovky
- **MAJOR** (0.x.y → 1.0.0) — pripravované; production milestone

## UE5 verzia

`UE5_VERSION` v `main.mjs` je odpojené od app verzie. Bumpujeme len keď sa naozaj zmení MetaHuman Blueprint alebo assety. Väčšina patch releaseov UE5 zip NEMÔŽE.

Aktuálne: `UE5_VERSION = 0.5.1`
