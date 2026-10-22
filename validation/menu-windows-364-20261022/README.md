# Windows menu evidence — 22 October 2026

Manual interactions and screenshots supplied by Vincent; inspected and recorded with OpenAI Codex assistance.

Pre-integration implementation 052e6443ab771d089355c51f7512b30c30f03375, associated with PR #373 (replacement for #368). Copied artifact verified: 12,654,259 bytes; SHA-256 fb24845c2a3bc02f445c8a16ed34d8ddc040515e67d233e06fa8586b38bd18f7. Java Oracle 25.0.4.1, assertions enabled. OS/runtime details in ../runtime.txt. Isolated folder, initially no operational data file.

Four original screenshots preserved unchanged. File/Help popup ordinary labels are visibly light on dark; highlighted Exit and Help/F1 text is black on orange. Showing menu titles are black on orange; other title remains light on dark. Screenshots establish visual readability, not a numerical contrast measurement or keyboard input provenance. Empty initial application views visible throughout.

Pending: manual keyboard navigation, Help menu activation and F1 retaining unfinished input; populated filter/selection/history preservation and operational-byte checkpoints. No disabled items exist in these production menus. No final integrated-candidate acceptance or issue closure claimed.

## Empty-view Help and keyboard check

Vincent supplied two screenshots following the F1 and F10/arrow/Enter instructions and explicitly confirmed: "keyboard navigation worked, draft survived". Both images show the Help catalogue and exact draft `edit 1 n/Unfinished` with empty person/Lesson views. PASS for these operator-reported input routes and visible draft retention. Screenshots alone do not prove keystroke provenance. Populated context/byte checks remain pending.

## Populated-view Help checks — PASS

Windows 10 build 19045 / X64, Oracle JDK 25.0.4.1+1-LTS-5, assertions enabled. Nine supplied screenshots total were inspected and retained unchanged.

Fixture executed manually by Vincent: create Mei T1 and Alex S1/P3; create Math L1/Mon/1600–1700/R1; filter Students; enrol S1; mark present 2026-10-05; unenrol; show S1/L1 history. Before Help, Alex is selected, only the Student is listed and L1 present/former-enrolment history is visible. Draft is `edit 1 n/Unfinished`.

Vincent invoked F1 and Help > Help and confirmed both actions preserved draft, history and Alex selection. Both resulting screenshots visibly corroborate the retained draft, selected Alex, single-person filtered view and same former-enrolment history while the Help catalogue appears. The command was not submitted.

Before/after operational JSON SHA-256 is identical: b4cb3bd05f8b6dc9e24252d7a1bad11a44721c2ab5c5ae7902c4085dc0a21a70. Original checkpoint JSON files retained. JAR rechecked unchanged at fb24845c2a3bc02f445c8a16ed34d8ddc040515e67d233e06fa8586b38bd18f7. These hashes establish byte preservation at checkpoints, not the absence of every filesystem write.

## Final scope and handoff

The Windows manual checks requested in the affected-evidence handoff are complete: ordinary/highlighted File/Help popup readability, keyboard navigation and F1/menu Help draft preservation, plus populated Student/selection/former-history preservation and unchanged operational bytes. Earlier pending notes describe interim status and are superseded by these results.

This is Vincent's actual manual run, guided and recorded with OpenAI Codex. It is not an independent non-author review, disabled-popup native check, full display-scaling matrix or final integrated-candidate acceptance. Formal review/integration and #271/#274 source/JAR reconciliation remain separate. No GitHub issue closure or publication performed.
