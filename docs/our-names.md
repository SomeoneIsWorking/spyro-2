# Our names (SCUS_944.25)

Names the psx-spyro port uses for this executable where they differ from or go beyond this tree's own.
The symbol map (`preparation/symbol_addrs.txt`) keeps the tree's names; ours enter it only where the tree has none. "Port file" is a psx-spyro path.

## Names that differ

| address | this tree | psx-spyro | port file | meaning |
|---|---|---|---|---|
| `0x80067E84` | `g_Camera` | `DrawSectionFactsProjectionRotation` | `titles/spyro2/core/draw_section.h` |  |
| `0x80069FF0` | `g_Spyro` | `SpyroDrawerSpyro` | `titles/spyro2/render/render_facts.h` |  |

## Names added to the map

| address | added as | was | port file | meaning |
|---|---|---|---|---|
| `0x80011E9C` | `BootPrefixFactsBootPrefix` | `func_80011E9C` | `titles/spyro2/core/boot_facts.h` |  |
| `0x80013A14` | `DrawSectionPlay` | `func_80013A14` | `titles/spyro2/core/draw_section.cpp` |  |
| `0x800155A0` | `DrawSectionFactsDispatcher` | `func_800155A0` | `titles/spyro2/core/draw_section.h` |  |
| `0x800156FC` | `BootPrefixFactsFrameDraw` | `func_800156FC` | `titles/spyro2/core/boot_facts.h` |  |
| `0x80019928` | `LevelExit` | `func_80019928` | `titles/spyro2/core/warp.cpp` | The portal entry: a portal index enters that portal's level; a negative index leaves for this level's portal in its homeworld, as the pause menu's Exit Level calls it at 0x80018420. |
| `0x8001A290` | `BossEntry` | `func_8001A290` | `titles/spyro2/core/warp.cpp` | The boss door's entry: game state 8 into the arena at the homeworld's id + 0x10. |
| `0x8001B140` | `BootPrefixFactsFrameUpdate` | `func_8001B140` | `titles/spyro2/core/boot_facts.h` |  |
| `0x8001B2A8` | `DrawSectionFactsFlatten` | `func_8001B2A8` | `titles/spyro2/core/draw_section.h` |  |
| `0x8001B390` | `RenderFactsOverlayLinkEntry` | `func_8001B390` | `titles/spyro2/render/render_facts.h` |  |
| `0x8001BDB0` | `DrawSectionFactsPositionCopy` | `func_8001BDB0` | `titles/spyro2/core/draw_section.h` |  |
| `0x8001C2F8` | `DrawSectionFactsCameraBuilder` | `func_8001C2F8` | `titles/spyro2/core/draw_section.h` |  |
| `0x80023BB4` | `TerrainFactsEntry` | `func_80023BB4` | `titles/spyro2/render/render_facts.h` |  |
| `0x80029170` | `SkyFactsEntry` | `func_80029170` | `titles/spyro2/render/render_facts.h` |  |
| `0x800296D0` | `SkyWaveConsumer` | `func_800296D0` | `titles/spyro2/render/render_facts.h` |  |
| `0x80041C50` | `DrawMotionAllocator` | `func_80041C50` | `titles/spyro2/render/render_facts.h` |  |
| `0x80041DBC` | `SpyroDrawerEntry` | `func_80041DBC` | `titles/spyro2/render/render_facts.h` |  |
| `0x80043858` | `MobyFactsEntry` | `func_80043858` | `titles/spyro2/render/render_facts.h` |  |
| `0x80044504` | `RenderFactsMobyDrawerEntry` | `func_80044504` | `titles/spyro2/render/render_facts.h` | jal at 8004C564; its translation is the entry's centre, loaded at 800445A8. |
| `0x80046FD8` | `RenderFactsMobyDeferredEntry` | `func_80046FD8` | `titles/spyro2/render/render_facts.h` | The walk's deferred buffer's drawer, the object pass's third call (8004C56C). |
| `0x80048D18` | `TerrainFactsSectorVisibility` | `func_80048D18` | `titles/spyro2/render/render_facts.h` |  |
| `0x800499D4` | `RenderFactsMobyShadowsEntry` | `func_800499D4` | `titles/spyro2/render/render_facts.h` | The close list's drawer, the object pass's fourth call; its texture words sit at the walk's v0 on return. |
| `0x8004A374` | `RenderFactsTextLayoutsEntry` | `func_8004A374` | `titles/spyro2/render/render_facts.h` |  |
| `0x8004A59C` | `RenderFactsTextLayoutsEntry_8004A59C` | `func_8004A59C` | `titles/spyro2/render/render_facts.h` |  |
| `0x8004D604` | `CinematicLetterboxEntry` | `func_8004D604` | `titles/spyro2/render/render_facts.h` |  |
| `0x800520CC` | `SpriteEmitter` | `func_800520CC` | `titles/spyro2/render/hud_anchor.h` |  |
| `0x80052498` | `HudSlideFunction` | `func_80052498` | `titles/spyro2/render/render_facts.h` |  |
| `0x8005251C` | `CounterDrawer` | `func_8005251C` | `titles/spyro2/render/hud_anchor.h` |  |
| `0x80054518` | `CreditsCheatEffect` | `func_80054518` | `titles/spyro2/core/debug_menu.cpp` | The cheat matcher 0x800543DC, run by the pause menu 0x800176A4, calls the effect with the matched table row; row 1 rolls the credits (0x8001A910, state 10). |
| `0x8005478C` | `Crt0Entry` | `func_8005478C` | `titles/spyro2/core/runtime.cpp` |  |
| `0x80057AE8` | `LibgteSetGeomScreen` | `func_80057AE8` | `titles/spyro2/core/runtime.cpp` |  |
| `0x80057AF8` | `LibgteSetGeomOffset` | `func_80057AF8` | `titles/spyro2/core/runtime.cpp` | libgte SetGeomScreen 0x80057AE8 and SetGeomOffset 0x80057AF8, called from 0x80011D24. |
| `0x80057B20` | `GpuTimeoutArm` | `func_80057B20` | `titles/spyro2/core/runtime.cpp` |  |
| `0x80058108` | `RuntimeCdRead` | `func_80058108` | `titles/spyro2/core/runtime.cpp` | libcd CdRead(dest, source, mode). |
| `0x80058810` | `RuntimeCdSync` | `func_80058810` | `titles/spyro2/core/runtime.cpp` | libcd CdSync, polled until it reports CS_SELF. |
| `0x80058858` | `CdCommand` | `func_80058858` | `titles/spyro2/core/runtime.cpp` | libcd CdCommand(com, parm, result). |
| `0x80058994` | `CdControlF` | `func_80058994` | `titles/spyro2/core/runtime.cpp` | libcd CdControlF(com, param): every CD_cw call passes a2 = 0 (0x80058A1C, 0x80058A44, 0x80058A68) and the last sends async (a3 = 1 at 0x80058A70). Native because CD_cw's wait at 0x8005C900 polls a status byte only libcd's interrupt raises ( |
| `0x80058EDC` | `RuntimeVSync` | `func_80058EDC` | `titles/spyro2/core/runtime.cpp` | libetc VSync: a negative argument returns the field delta. |
| `0x80061BD8` | `g_RenderGlobalsCameraSineTable` | `D_80061BD8` | `titles/spyro2/render/render_facts.h` | 80061BD8: the sine table FUN_8001B61C indexes; FUN_8001B664 reads its cosine a quarter turn on. |
| `0x80061C58` | `g_SkyWaveSine` | `D_80061C58` | `titles/spyro2/render/render_facts.h` |  |
| `0x80061F60` | `g_TerrainFactsQuadCells` | `D_80061F60` | `titles/spyro2/render/render_facts.h` |  |
| `0x80061F70` | `g_TerrainFactsQuadPieces` | `D_80061F70` | `titles/spyro2/render/render_facts.h` |  |
| `0x80061FB0` | `g_TerrainFactsQuadCracks` | `D_80061FB0` | `titles/spyro2/render/render_facts.h` |  |
| `0x80061FE0` | `g_TerrainFactsQuadCracks_80061FE0` | `D_80061FE0` | `titles/spyro2/render/render_facts.h` |  |
| `0x80062040` | `g_TerrainFactsPageRemaps` | `D_80062040` | `titles/spyro2/render/render_facts.h` |  |
| `0x80062080` | `g_TerrainFactsInnerPoints` | `D_80062080` | `titles/spyro2/render/render_facts.h` |  |
| `0x80062090` | `g_TerrainFactsTriangleCells` | `D_80062090` | `titles/spyro2/render/render_facts.h` |  |
| `0x800620A0` | `g_TerrainFactsTrianglePieces` | `D_800620A0` | `titles/spyro2/render/render_facts.h` |  |
| `0x800620E0` | `g_TerrainFactsTriangleCracks` | `D_800620E0` | `titles/spyro2/render/render_facts.h` |  |
| `0x80062170` | `g_TerrainFactsTriangleCracks_80062170` | `D_80062170` | `titles/spyro2/render/render_facts.h` |  |
| `0x80062290` | `g_TerrainFactsTriangleSubTexture` | `D_80062290` | `titles/spyro2/render/render_facts.h` |  |
| `0x800622A0` | `g_TerrainFactsPieceTexture` | `D_800622A0` | `titles/spyro2/render/render_facts.h` |  |
| `0x800622E0` | `g_TerrainFactsPieceShift` | `D_800622E0` | `titles/spyro2/render/render_facts.h` |  |
| `0x80062360` | `g_TerrainFactsTriangleUvs` | `D_80062360` | `titles/spyro2/render/render_facts.h` |  |
| `0x80062460` | `g_TerrainFactsTriangleUvs_80062460` | `D_80062460` | `titles/spyro2/render/render_facts.h` |  |
| `0x80062560` | `g_TerrainFactsTrianglePieces_80062560` | `D_80062560` | `titles/spyro2/render/render_facts.h` |  |
| `0x8006257C` | `g_TerrainFactsQuadPieces_8006257C` | `D_8006257C` | `titles/spyro2/render/render_facts.h` |  |
| `0x80062674` | `g_IntroCardDeltaTable` | `D_80062674` | `titles/spyro2/render/intro_card_facts.h` |  |
| `0x80062868` | `g_MobyFactsKeyframeBlend` | `D_80062868` | `titles/spyro2/render/render_facts.h` |  |
| `0x800633F4` | `g_ConversationTablesTable` | `D_800633F4` | `titles/spyro2/render/render_facts.h` |  |
| `0x80063418` | `g_ConversationTablesTable_80063418` | `D_80063418` | `titles/spyro2/render/render_facts.h` |  |
| `0x80063430` | `g_HudSlideInTable` | `D_80063430` | `titles/spyro2/render/render_facts.h` |  |
| `0x80063448` | `g_HudSlideOutTable` | `D_80063448` | `titles/spyro2/render/render_facts.h` |  |
| `0x800634B8` | `g_HudElementWidths` | `D_800634B8` | `titles/spyro2/render/hud_element.cpp` | The element's width and height in pixels, one byte per size index. |
| `0x800634D0` | `g_Heights` | `D_800634D0` | `titles/spyro2/render/hud_element.cpp` |  |
| `0x800636A4` | `g_TextGlyphCells` | `D_800636A4` | — | u16 per character code: bits 0-4 cell column (u 12·col), 5-7 row (v 9·row), 8-11 advance, 12-15 signed y offset; low byte 0xFF no cell |
| `0x800637A4` | `g_TextEscapes` | `D_800637A4` | — | '@' escapes to 0x800637D2: (char, byte offset into g_TextGlyphCells; bit 7 an accent drawn back over the last letter) |
| `0x800637D4` | `g_TextColours` | `D_800637D4` | — | ten SPRT colour words, chosen by the layouts' colour argument or '@' + digit |
| `0x80064440` | `g_RenderFactsMobyDeferredPaletteTable` | `D_80064440` | `titles/spyro2/render/render_facts.h` |  |
| `0x80064940` | `g_LevelIndexTable` | `D_80064940` | `titles/spyro2/core/warp.cpp` | Byte per level id: its index into the name and homeworld tables. |
| `0x800649B4` | `g_LevelNames` | `D_800649B4` | `titles/spyro2/core/warp.cpp` |  |
| `0x80064B84` | `g_LevelHomeworlds` | `D_80064B84` | `titles/spyro2/core/warp.cpp` |  |
| `0x80066354` | `g_GpuTimeoutDeadline` | `D_80066354` | `titles/spyro2/core/runtime.cpp` | libgpu DrawSync's timeout: its deadline and poll-count words and the arm and check leaves. |
| `0x80066358` | `g_GpuTimeoutPollCount` | `D_80066358` | `titles/spyro2/core/runtime.cpp` |  |
| `0x800663B8` | `g_CdReadyCallbackPointer` | `D_800663B8` | `titles/spyro2/core/runtime.cpp` | libcd's CdReadyCallback word (0x800582A4 stores it). |
| `0x80066618` | `g_VSyncQueryCounter` | `D_80066618` | `titles/spyro2/core/boot_facts.h` | A negative VSync returns this guest vblank count (lw at 0x80058F40, ++ at 0x8005ACB0); docs/issues/0160. |
| `0x80066F00` | `g_PortalsPortalTable` | `D_80066F00` | `titles/spyro2/core/warp.cpp` | Trigger 0x8002AAFC's records and the portals its type 6 enters (0x80019928(index) at 0x8002AD98). |
| `0x80066F14` | `g_MobyFactsFirstRecordWord` | `D_80066F14` | `titles/spyro2/render/render_facts.h` |  |
| `0x80066F18` | `g_DrawMotionParticles` | `D_80066F18` | `titles/spyro2/render/render_facts.h` |  |
| `0x80066F88` | `g_StateHook` | `D_80066F88` | `titles/spyro2/core/draw_section.cpp` |  |
| `0x80066F90` | `g_LevelId` | `D_80066F90` | `titles/spyro2/core/boot_facts.h` | The level FUN_80019230 stores at 0x800192E8. |
| `0x80066FA4` | `g_MobyFactsDrawerParameter` | `D_80066FA4` | `titles/spyro2/render/render_facts.h` |  |
| `0x80066FB8` | `g_CreditLettersPool` | `D_80066FB8` | `titles/spyro2/render/render_facts.h` |  |
| `0x80066FC0` | `g_DrawSectionFactsCurrentBuffer` | `D_80066FC0` | `titles/spyro2/core/draw_section.h` |  |
| `0x80066FFC` | `g_DrawSectionFactsOrderingTable` | `D_80066FFC` | `titles/spyro2/core/draw_section.h` |  |
| `0x80067000` | `g_RenderGlobalsOverlayPair` | `D_80067000` | `titles/spyro2/render/render_facts.h` |  |
| `0x8006700C` | `g_SkyWaveTick` | `D_8006700C` | `titles/spyro2/render/render_facts.h` |  |
| `0x8006701C` | `g_CinematicLetterboxHeight` | `D_8006701C` | `titles/spyro2/render/render_facts.h` |  |
| `0x80067030` | `g_DrawSectionFactsPrimitiveCursor` | `D_80067030` | `titles/spyro2/core/draw_section.h` |  |
| `0x80067034` | `g_DrawSectionFactsScratchEnd` | `D_80067034` | `titles/spyro2/core/draw_section.h` |  |
| `0x800670C8` | `g_DrawSectionFactsGate` | `D_800670C8` | `titles/spyro2/core/draw_section.h` |  |
| `0x80067130` | `g_ConversationTimer` | `D_80067130` | `titles/spyro2/render/render_facts.h` |  |
| `0x80067134` | `g_ConversationMode` | `D_80067134` | `titles/spyro2/render/render_facts.h` |  |
| `0x8006715C` | `g_ExitDestination` | `D_8006715C` | `titles/spyro2/core/warp.cpp` | The level game state 7 fades out of and loads, set by the portal entry. |
| `0x80067168` | `g_DrawSectionFactsBinMark` | `D_80067168` | `titles/spyro2/core/draw_section.h` |  |
| `0x80067170` | `g_DrawSectionFactsScratchSize` | `D_80067170` | `titles/spyro2/core/draw_section.h` |  |
| `0x800673D4` | `g_TerrainFactsSectorTable` | `D_800673D4` | `titles/spyro2/render/render_facts.h` |  |
| `0x800673D8` | `g_TerrainFactsSectorCount` | `D_800673D8` | `titles/spyro2/render/render_facts.h` |  |
| `0x800673E8` | `g_PortalsTriggerTable` | `D_800673E8` | `titles/spyro2/core/warp.cpp` | Trigger 0x8002AAFC's records and the portals its type 6 enters (0x80019928(index) at 0x8002AD98). |
| `0x800673F4` | `g_TerrainFactsTextureTable` | `D_800673F4` | `titles/spyro2/render/render_facts.h` |  |
| `0x80067400` | `g_TerrainFactsFarDepth` | `D_80067400` | `titles/spyro2/render/render_facts.h` |  |
| `0x80067404` | `g_TerrainFactsVisibleSectorCount` | `-` | `titles/spyro2/render/render_facts.h` |  |
| `0x80067408` | `g_TerrainFactsFogColour` | `D_80067408` | `titles/spyro2/render/render_facts.h` |  |
| `0x8006765C` | `g_GemCounter` | `D_8006765C` | `titles/spyro2/render/hud_anchor.h` | The two counter elements FUN_80053E78 passes to the counter drawer (80053F48 / 80053F94). |
| `0x80067664` | `g_OrbCounter` | `D_80067664` | `titles/spyro2/render/hud_anchor.h` |  |
| `0x80067D00` | `g_DrawMotionGlows` | `D_80067D00` | `titles/spyro2/render/render_facts.h` |  |
| `0x80067E00` | `g_TitleTick` | `D_80067E00` | `titles/spyro2/core/warp.cpp` | The title image's tick and the start index state 5 passes to 0x80019230. |
| `0x80067E0C` | `g_TitleScreenState` | `D_80067E0C` | `titles/spyro2/core/logo_facts.h` | The title screen's own state word; 2 holds the finished logo while "press start" waits. |
| `0x80067E14` | `g_StartIndex` | `D_80067E14` | `titles/spyro2/core/warp.cpp` |  |
| `0x80067E98` | `g_DrawSectionFactsViewRotation` | `-` | `titles/spyro2/core/draw_section.h` |  |
| `0x80067EAC` | `g_DrawSectionFactsCameraPosition` | `-` | `titles/spyro2/core/draw_section.h` |  |
| `0x80067EB8` | `g_DrawSectionFactsDrawCameraPosition` | `-` | `titles/spyro2/core/draw_section.h` |  |
| `0x80067EC4` | `g_TerrainFactsFogLevel` | `-` | `titles/spyro2/render/render_facts.h` |  |
| `0x80067EC8` | `g_DrawSectionFactsCameraAngles` | `-` | `titles/spyro2/core/draw_section.h` |  |
| `0x80067ED0` | `g_CameraMode` | `-` | `titles/spyro2/core/boot_facts.h` | Camera controller FUN_8001FA58's mode and sub-state. |
| `0x80067ED4` | `g_CameraSubState` | `-` | `titles/spyro2/core/boot_facts.h` |  |
| `0x80068078` | `g_DrawMotionSprites` | `D_80068078` | `titles/spyro2/render/render_facts.h` |  |
| `0x800681B8` | `g_SkyFactsSectors` | `D_800681B8` | `titles/spyro2/render/render_facts.h` |  |
| `0x800681C0` | `g_RenderFactsMobyDeferredFogColour` | `D_800681C0` | `titles/spyro2/render/render_facts.h` |  |
| `0x800681C8` | `g_DrawSectionFactsGameState` | `D_800681C8` | `titles/spyro2/core/draw_section.h` |  |
| `0x8006820C` | `g_MobyFactsExitV0` | `D_8006820C` | `titles/spyro2/render/render_facts.h` |  |
| `0x80068214` | `g_MobyFactsCloseCursorHome` | `-` | `titles/spyro2/render/render_facts.h` |  |
| `0x800683F0` | `g_TerrainFactsFoggedColours` | `D_800683F0` | `titles/spyro2/render/render_facts.h` |  |
| `0x80068C08` | `g_SkyWaveWave` | `D_80068C08` | `titles/spyro2/render/render_facts.h` |  |
| `0x80068C94` | `g_MobyFactsMeshSlotTable` | `D_80068C94` | `titles/spyro2/render/render_facts.h` |  |
| `0x800698D4` | `g_DrawMotionShadow` | `-` | `titles/spyro2/render/render_facts.h` |  |
| `0x800698F0` | `g_GameSubState` | `D_800698F0` | `titles/spyro2/render/render_facts.h` | The game state's step word: the level load's and the loading screen's sub-state. |
| `0x80069928` | `g_DrawSectionFactsBuffer0` | `D_80069928` | `titles/spyro2/core/draw_section.h` |  |
| `0x8006999C` | `g_DrawSectionFactsBuffer1` | `-` | `titles/spyro2/core/draw_section.h` |  |
| `0x80069F30` | `g_DrawMotionMeshes` | `D_80069F30` | `titles/spyro2/render/render_facts.h` |  |
| `0x8006A2B4` | `g_DrawMotionTrails` | `D_8006A2B4` | `titles/spyro2/render/render_facts.h` |  |
| `0x8006A9EC` | `g_RenderGlobalsRegisterSaveArea` | `D_8006A9EC` | `titles/spyro2/render/render_facts.h` |  |
| `0x8006AA1C` | `g_DrawMotionFlame` | `D_8006AA1C` | `titles/spyro2/render/render_facts.h` |  |
| `0x8006B300` | `g_RenderGlobalsVisibilityGroups` | `D_8006B300` | `titles/spyro2/render/render_facts.h` |  |
| `0x8006B400` | `g_DrawMotionBeams` | `D_8006B400` | `titles/spyro2/render/render_facts.h` |  |

## Code sites

Addresses inside a function (return addresses, branch joins) the port hooks or reads.

| address | function + offset | port name | port file | meaning |
|---|---|---|---|---|
| `0x80023C04` | `func_80023BB4+0x50` | `TerrainFactsVisibilityCallSite` | `titles/spyro2/render/render_facts.h` |  |
| `0x800291A8` | `func_80029170+0x38` | `SkyFactsVisibilityCallSite` | `titles/spyro2/render/render_facts.h` |  |
| `0x8004C56C` | `func_8004C534+0x38` | `RenderFactsMobyDrawerFieldPassReturn` | `titles/spyro2/render/render_facts.h` |  |
| `0x80057AF4` | `func_80057AE8+0xC` | `GpuTimeoutCheck` | `titles/spyro2/core/runtime.cpp` |  |
