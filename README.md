# EduTutor.AI

[![Najnovšia verzia](https://img.shields.io/github/v/release/princeofwellness/edututor-releases?label=verzia&color=E8A87C)](https://github.com/princeofwellness/edututor-releases/releases/latest)
[![Stiahnutia](https://img.shields.io/github/downloads/princeofwellness/edututor-releases/total?label=stiahnutia&color=E8A87C)](https://github.com/princeofwellness/edututor-releases/releases)
[![Platforma](https://img.shields.io/badge/platforma-Windows%2011-1a0e08?color=1a0e08)](https://github.com/princeofwellness/edututor-releases/releases/latest)
[![Licencia](https://img.shields.io/badge/licencia-proprietary-5a5048)](#licencia)

> *Slovenský AI tutor s lokálnym jazykovým modelom a živým 3D avatarom.*

---

## Stiahnutie

**[→ Stiahnuť najnovšiu verziu](https://github.com/princeofwellness/edututor-releases/releases/latest)**

Z najnovšej release stiahni:

| Súbor | Účel | Veľkosť |
|---|---|---|
| **`EduTutor-Setup-X.Y.Z.exe`** | Windows inštalátor — toto stačí | ~1.7 GB |
| `EduTutor-Setup-X.Y.Z.exe.sha256` | Kontrolný súčet (voliteľné) | 91 B |
| `Navod_na_instalaciu.html` | Slovenský sprievodca (voliteľné) | ~2 KB |
| `EduTutor_Technicka_dokumentacia.pdf` | Tech dokumentácia (voliteľné) | ~3 MB |

**`ue5-engine-X.Y.Z.zip`** (~1.7 GB) sa stiahne automaticky pri prvom spustení — netreba ho riešiť ručne.

---

## Inštalácia

1. Spusti stiahnutý `EduTutor-Setup-X.Y.Z.exe`
2. Preklikaj sa sprievodcom inštalácie
3. Otvor EduTutor z desktopovej ikony

Hotovo. Pri prvom spustení sa stiahne MetaHuman avatar (~1.7 GB) z tejto release stránky, ďalšie spustenia sú už okamžité.

### Systémové požiadavky

- Windows 11 (64-bit)
- 16 GB RAM odporúčané
- ~6 GB voľného miesta (+1.7 GB pre UE5 avatar)
- NVIDIA GPU s aktuálnym ovládačom (pre MetaHuman)
- Pripojenie na internet iba pri prvom spustení

---

## Čo to vie

- Slovenský AI tutor postavený na lokálnom Ollama (Gemma, Llama, Qwen, Mistral) alebo na cloud LLM (OpenAI, Anthropic, Groq, DeepSeek) — tvoj výber
- Živý MetaHuman avatar v Unreal Engine 5 s lipsync a emóciami
- Offline syntéza reči cez Piper (slovenský hlas Lukáš/Viktória) alebo cloud (Edge TTS, ElevenLabs, Azure)
- Slovenské rozpoznávanie reči cez faster-whisper
- RAG nad tvojimi PDF/MD dokumentmi
- Editovateľný systémový prompt — povedz tutorovi ako sa má správať

---

## Štruktúra release-ov

| Typ | Príklad | Stav |
|---|---|---|
| **Latest** | `v0.8.x` | Aktuálna stabilná verzia, odporúčaná |
| **Stable predošlé** | `v0.7.7` | Posledná predošlá stabilná, fallback ak Latest zlyhá |
| **Archív** | `v0.4.x – v0.6.x` | Označené ako prereleases, len pre historický záznam |

---

## Tento repozitár

Tento repo obsahuje **iba binárky** — žiadny zdrojový kód.

- **Zdrojový kód** je v privátnom repe `princeofwellness/edotutor` (vývoj, issue tracker)
- **Tento repo** slúži ako verejný distribučný mirror pre `.exe` + UE5 avatar zip
- Aplikácia po inštalácii automaticky cieli na tento repo pre `ue5-engine-X.Y.Z.zip` (URL je hardcoded v `main.mjs` — `UE5_RELEASE_REPO = 'princeofwellness/edututor-releases'`)

> ⚠ **Tento repo musí ostať PUBLIC.** Ak by sa prepol na private, inštalovaná aplikácia začne zlyhávať pri sťahovaní UE5 avatara s 404.

---

## Licencia

Proprietary. **SORRYWECAN s.r.o.** · grant `09I05-03-V04-00072`.

---

## English

This repo hosts public download assets for **EduTutor.AI**, a Slovak AI tutor desktop app with a live MetaHuman avatar. Source code lives in the private `princeofwellness/edotutor` repo; this is a distribution-only mirror.

To install: download the latest `EduTutor-Setup-X.Y.Z.exe` from [Releases](https://github.com/princeofwellness/edututor-releases/releases/latest) and run it. The UE5 avatar zip is fetched on first launch from this repo automatically — no manual steps required.
