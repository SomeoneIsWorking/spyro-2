# Prior art

Outside work on Spyro 2: Ripto's Rage! (USA) `SCUS_944.25`, SHA-1 `42633ff8cf1b43c49c5fe23d00eca6eb2703828b`, the build this tree matches. A reference names addresses; the psx-spyro
port's measurement decides behaviour. Address checks ran `decomp_pipeline.py --function-at` on our images
(2026-10-13); licences are GitHub SPDX ids; push dates checked 2026-11-13. Submodule pins named below are psx-spyro's
(2026-11-13, before this tree became its fork).

| project | URL | kind | license | target build | build match (addresses checked) | what we may take | notes |
|---|---|---|---|---|---|---|---|
| TheMobyCollective/spyro-2 | https://github.com/TheMobyCollective/spyro-2 | matching decomp (splat), EXE plus WAD overlays | CC0-1.0 | Spyro 2 `SCUS_944.25` | matched: `preparation/scus_944.25.yaml` sha1 `42633FF8…` equals ours; split points `0x800159C8` and `0x8001B2A8` equal our Ghidra body ends of `0x800156FC` and `0x8001B140`; `0x80043858` is its `mobydraw` start and a Ghidra entry (811 insns) | code and names (CC0), copied with attribution | Submodule `external/spyro-2` pin `d1cd3f36` (push 2026-11-06). `progress/exe.md` 102 of 330 EXE functions matched (was 71 on 2026-10-10); per-level overlay progress in `progress/level_*.md`. Mostly `func_` names. |
| retro-meister/Spyro2re | https://github.com/retro-meister/Spyro2re | RE/modding project with named symbol map (`symbols/funcs-u.txt`, `data-u.txt`) | none | Spyro 2 NTSC-U `SCUS_944.25` (`disc.json`) | matched: its `GAME_main 0x80011ADC`, `GAME_InitSound 0x80011B1C`, `GAME_CDLoadWADHeader 0x80011B3C`, `GAME_InitGeometry 0x80011D24` are function split addresses in spyro-2's tree (same SHA-1) | names only | 105 named functions; dormant since 2022-07-13. Best source of real names for Spyro 2. |
| retro-meister/rs2 | https://github.com/retro-meister/rs2 | Spyro 2 practice hack with symbol map (`symbols/funcs-u.txt`, `funcs-u-rs2.txt`) | none | Spyro 2 NTSC-U `SCUS_944.25` (`disc.json`) | not checked beyond serial; shares Spyro2re's symbol files | names only | 109 named functions; last push 2025-05-08. |
| wafflewizard1/SpyroGhidra | https://github.com/wafflewizard1/SpyroGhidra | Ghidra `.gzf` plus exported C, Spyro 1, 2, 3 1.0 NTSC | none | Spyro 2 NTSC, Spyro 3 1.0 NTSC | matched: Spyro 2 export has `FUN_80011e9c`, `FUN_80043858`, `FUN_80023bb4`; Spyro 3 export has `FUN_8002a834` and calls `FUN_8002ab38` and `FUN_8005d35c(0x100,0x78)` | names only | Dormant since 2024. Never import the `.gzf`; read the `.c` text only. |
| Uroogla/S2AP | https://github.com/Uroogla/S2AP | Archipelago randomizer client for Spyro 2 | MIT | Spyro 2 (region not checked) | not checked | RAM addresses (MIT), copied with attribution after measurement | Last push 2026-11-07. |
| JV-1054/Spyro-2-Riptos-Rage-Recomp | https://github.com/JV-1054/Spyro-2-Riptos-Rage-Recomp | static recompilation (psxrecomp) | none | Spyro 2 `SCUS-94425` | matched: `catalog_identity.json` entry `0x8005478C` and text size `0x57000` equal our header | nothing | Seeds and generated C on the noncommercial psxrecomp runtime; last push 2026-10-28. |
| marcovoc/spyro2-decomp | https://github.com/marcovoc/spyro2-decomp | matching decomp | CC0-1.0 | Spyro 2 PAL `SCES_021.04` | mismatched: none of `0x8001B140`, `0x800156FC`, `0x80043858`, `0x80011E9C` in `symbol_addrs.txt`; different SHA-256 | names only, after translation by function body (CC0) | Wrong region. Last push 2026-09-20. |
| FranklyGD/Spyro-Scope | https://github.com/FranklyGD/Spyro-Scope | live RAM and data viewer | GPL-3.0 | Spyro 1 NTSC-U, Spyro 2 NTSC, Spyro 3 NTSC v1.1 | not checked; Spyro 3 v1.1 is not our rev 0 | evidence only | Data-format reference; its terrain collision format (flag byte, water bit, slope) informs `docs/plans/more-vegetation.md`. |

Not found (2026-11-13): source for any Spyro 2 or 3 widescreen or 60 fps patch (the PCSX2-forum Spyro 3 widescreen
code targets NTSC-U v1.1, not our rev 0); a Spyro title on decomp.dev; a decomp of the sequels beyond the
TheMobyCollective splits. Searched GitHub repositories (titles, serials, "decomp", "recomp", "port", "widescreen",
"60fps"), decomp.dev and the web.

Not found (2026-11-12, for G006): any foliage, grass-density or vegetation mod for the PlayStation Spyro titles or
Reignited, or a grass-density enhancement in a decomp-based port of another title.
