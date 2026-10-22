# Affected packaged menu evidence — #364

22 October 2026, Vincent with OpenAI Codex assistance. **In progress: Windows native popup observations remain pending.** This folder records actual work and provides the remaining manual handoff without inferring a platform PASS.

## Source-branch correction

Replacement [PR #373](https://github.com/AY2627S1-CS2103T-F13-3/tp/pull/373) uses retained fork branch `fix-menu-contrast-364`, targeting team `master`, at exact implementation commit `052e6443ab771d089355c51f7512b30c30f03375`. It removes the reviewed `codex/` naming discrepancy without changing implementation/history. #368 is closed as superseded; its branch, substantive non-author review and checks remain. No approval is impersonated or transferred automatically.

Fresh [replacement CI](https://github.com/AY2627S1-CS2103T-F13-3/tp/actions/runs/39758860874) passes Ubuntu/macOS/Windows and Codecov. The earlier reviewer independently passed 35 affected checks, including Help/F1/draft/selection/bytes, on the identical implementation. Formal non-author approval/integration remains pending.

## Patched JAR identity

`ponhub.jar`, **12,654,259 bytes**, SHA-256 **`fb24845c2a3bc02f445c8a16ed34d8ddc040515e67d233e06fa8586b38bd18f7`**, PonHub / 1.4 / `ponhub.Main`. This is the exact pre-integration implementation above, not a final reviewed team candidate. JAR source differs from the old `ed32fe49` / `5e24df51…` acceptance; retain that old evidence under its original bytes.

The checksum-driven [Linux package run 39758810233](https://github.com/AY2627S1-CS2103T-F13-3/tp/actions/runs/39758810233) passes its complete existing 32-entry actual production-JAR command-box/edit/rejection/no-op/attendance/history/restart scenario. Downloaded artifact source and checksum were independently checked. [Exact JAR and retained evidence](https://github.com/AY2627S1-CS2103T-F13-3/tp/actions/runs/39758810233/artifacts/12417351513) are accessible for the Windows check. Copies of source, runtime, result and command inventory are retained here. Scope is Ubuntu 24.04.5 x86_64 / Zulu 25 / Xvfb; this is not a human popup or physical-display result.

## Actual Mac affected checks

macOS 27.0.1 / 26A434 / arm64, prescribed Azul `25.0.3.fx-zulu`, assertions enabled, actual unchanged checksum JAR in `/private/tmp/ponhub-menu364-preview`. A temporary native app launcher identifies the Java process; no application code/runtime patch is injected. Only fictitious disposable data is used.

The fresh fixture creates Mei T1, Alex S1 and Math L1; enrols/marks then unenrols Alex. Before Help, the Student filter and L1 former-member present record dated 2026-10-05 are visible, with unfinished `edit 1 n/Unfinished` in the command box. Native **F1 PASS**: catalogue appears while draft/filter/history and exact saved bytes remain unchanged. See before/F1 screenshots, AX readbacks, command transcript and original-byte before/after JSON. This does not add a selected-row preservation claim.

Vincent previously manually reported File/Help ordinary/hovered text “works” on these exact bytes; [saved report](https://github.com/AY2627S1-CS2103T-F13-3/tp/issues/364#issuecomment-6336490665). That operator report is not replaced by an automated click claim. The `mac-file-state.png` / `mac-file-raised.png` captures show the hovered File title with popup **closed**: CUA did not expose the popup, so they are not open-popup evidence. The real attached-control test covers both menus' ordinary/focused/disabled labels and title states; no disabled item is added to the running application solely to manufacture a native screenshot.

## Windows manual handoff — pending

Vincent confirmed a PC is available and was given the exact artifact link and these identity/launch commands, to run in a fresh empty folder containing only the copied JAR:

```powershell
java -version
Get-FileHash .\ponhub.jar -Algorithm SHA256
(Get-Item .\ponhub.jar).Length
java -ea -jar .\ponhub.jar
```

Pending runtime/hash output and actual screenshots: File/Help titles and open popup items with ordinary and hovered/focused states; keyboard selection; Help/F1 with an unfinished command retained. Use only fictitious data. Snipping Tool's delayed capture can help if activating capture dismisses an open popup. Windows evidence must retain the actual OS/architecture/Java distribution and distinguish reported observations from inspected images. The existing application's File/Help menus have no disabled entries; disabled contrast is covered by the meaningful automated fixtures.

## Release boundary

#364 remains open until the missing native observations and reviewed integration/handoff are saved. After #373 integration, #271 must establish the resulting team source/JAR/hash/manifest and reconcile changed inputs and affected packaged/menu acceptance before #274 publication. This pre-integration verification and branch repair do not authorize publication or close #271/#272. Ownership and agreed deadlines remain unchanged.
