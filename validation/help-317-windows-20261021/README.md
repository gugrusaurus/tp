# #317 guided Windows native acceptance — 21 October 2026

Executed manually by Vincent, guided by OpenAI Codex. The 58 supplied screenshots were visually inspected in this chat and preserved with original filenames in screenshots/. This is author-executed native evidence helping Ernest with the remaining display handoff; it is not an additional independent teammate review or final v1.4 candidate acceptance.

## Source, artifact and runtime

- Exact source: 93a907eacd87f9df75c735ac59a6eaafd65a4142 (merged #354).
- Built from a fresh source export using the repository wrapper, offline --no-daemon shadowJar: PASS.
- Packaged JAR: 12,661,623 bytes; SHA-256 D90DC3918CCE34591C6879415D22BFB55F59F42FB77B7D2D04E2FEAC5B15B945, unchanged after native checks.
- Manifest: PonHub 1.3; main class seedu.address.Main. Local acceptance artifact.
- Launch-Test.cmd explicitly selects C:\Program Files\Java\jdk-25.0.4.1\bin\java.exe; Oracle 25.0.4.1+1-LTS-5, project JavaFX 17.0.7 Windows dependency (also confirmed in preceding focused test runtime output).
- OS version observed through Environment.OSVersion: Windows NT 10.0.19045.0. The CIM edition/architecture query was denied; no independently collected edition/architecture assertion is made.
- Isolated run folder: ../help317-native-run. Synthetic fixture: 30 Students, T1, P1, eight Lessons and 60 S1 history records.

## Display matrix and manual results

| Actual resolution / Windows scale | Result |
| --- | --- |
| 1920x1080 / 100% | PASS for guided help/divider/scroll/copy/error/view-cycle/F1/menu/list/resize checks. Settings proof 7ee4e995; startup f06f2df0. |
| 1920x1080 / 125% | PASS for the same guided checks. Settings proof 12ae5daa; startup 4fcc1b06. |
| 1280x720 / custom 150% | PASS for the same guided checks. Resolution/custom-setting proofs 623080c8 and 20413209; user explicitly confirmed sign-out/sign-in before fresh launch. Startup dbbf252b. |

Actual settings screenshots plus the fresh packaged app and user confirmation support the native configurations. No JavaFX output-scale probe or pixel-coordinate measurement was performed in this run.

At each configuration:
- Dragged help divider in both directions/to both limits; final topic-help text reached at each limit. Text wraps and command dock remains accessible.
- Selected/copied help search into Notepad. Captures and user confirmations cover its beginning and final examples; this was not an exact character-by-character clipboard comparison.
- Chose a middle split and ran help -> showlesson lid/L1 d/2026-10-19 -> history 1 -> help for three cycles. Actual roster/history views appear in captures. Screenshots remain visually aligned; user confirmed no divider/command-box movement. No subpixel measurement claim is made. At 150%, the last extra help captures retain roster context; completion of all cycles is supported by the user's explicit confirmation, not inferred solely from those final images.
- Filtered to 30 Students, selected S2, typed unfinished help search, invoked F1 and actual Help menu. Captures show preserved draft, S2, filter, right-panel context and split.
- Submitted help search extra; shortened result area and scrolled to Examples: help, help list. Rejected input retained. The earlier one-line bare-search error is not counted as long-error scroll evidence.
- Reached final People card P1 and Lesson card L8; user confirmed independent scrolling.
- Compact, maximised and restored layouts captured; help submission demonstrated after restore. User confirmed People/Lesson divider dragging without issue, including the requested 125%/150% follow-up. Inputs/status remain accessible; long status paths abbreviate at compact size.

Representative cycle ends: 4121b43d (100%), 7064669f (125%), 57882bc0 / 1a1e334b / 2ce70de9 (150%, qualified above). F1/menu pairs: 15446e20/a882fb12, e0a217a0/f35fba6d, 2d20bf76/ea70d001. Final compact/restore at 150%: 72cfba78, 21818aa8, bbe4182c, afcae56a.

## Integrity and restoration

Fixture SHA-256 before and after: 11E5406B985EEE361161274D4B653DB4AC341EEAECEB92F06FDF9C099B8031DC (exact original fixture bytes preserved). JAR hash also unchanged. Application log records normal stopping.

User confirmed original display restored. Screenshot 3ef1315d shows 2560x1440 / 100% and extended displays, with normal scale selector active. Restoration of every monitor's individual settings is user-confirmed rather than separately photographed.

## Handoff and limits

These results supply the outstanding Windows display-matrix evidence for #317 on the merged divider fix. Preserve earlier Mac evidence under its own source/runtime scope. User is the shell implementation owner; do not relabel this as independent non-author acceptance. Owner/reviewer reconciliation and GitHub checklist/closure are separate actions. No issue state, assignment, deadline or release was changed while recording this report. Final-candidate #271/#272 and broader #321 gates remain separate.
