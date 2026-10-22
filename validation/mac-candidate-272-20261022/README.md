# Exact-candidate Mac acceptance — #272

22 October 2026, Vincent (`gugrusaurus`) with OpenAI Codex operating the native Mac UI. This is actual packaged application interaction, not a Gradle/source-test run or Ernest's personal run. Vincent did not author the person/Lesson edit commands; his persistence/shell/package contributions remain disclosed.

**Latest disposition after retry: core Mac flows, protected-session restrictions and restore/restart recovery PASS.** Four retry exits completed without the earlier shutdown exception. Help-menu activation also PASS after Vincent’s manual click and Codex readback; F1 passed in the original run. Final owner reconciliation remains required. No issue closure or release publication is claimed.

## Manual Help-menu completion

Vincent manually clicked **Help → Help** in the prepared candidate window and confirmed the click in this chat. Codex then inspected the actual screenshot and accessibility readback: the command catalogue appeared, `edit 1 n/Unfinished` remained intact, the two-Student view remained, and Alex S1’s L1 absence dated 2026-10-05 remained visible as former-enrolment history. Operational data stayed byte-identical. **PASS**; this supersedes the earlier unconfirmed-menu status. See [screenshot](retry/manual-help-menu.png), [readback](retry/manual-help-ax.txt) and [result](retry/manual-help-result.json). The click is attributed to Vincent, not automation. No selected-row preservation claim is added.

## Retry of remaining checks

At the user's request, repeated the outstanding checks using the exact same JAR/runtime in new disposable folders, with only one app process running at a time. The retry helper takes the target app explicitly, and does not query an exited binding (which can relaunch its app). These changes concern the automation, not product code. See [retry summary](retry/summary.json), [readbacks](retry/ui-transcript.json), [normal log](retry/normal.log) and [protected/recovered log](retry/protected.log).

- **Shutdown:** two normal launch/command/exit cycles, one protected-session exit and one recovered-session exit all stopped their processes. No `Exception in thread` or `Main Java thread is detached` appeared in either fresh log. The original intermittent diagnostic is retained, not claimed fixed or assigned a root cause.
- **Protected startup/interaction:** warning dismissed, main window usable, Help lists only `help`, `list` and `exit`; person edit, add and Lesson edit blocked. `list` remains available. The malformed original stays byte-identical; before/after copies are retained in `retry/`.
- **Recovery:** restored a known-good copy in the disposable folder while the protected session was running. Mutation remained blocked, demonstrating the session-long lock. After exit/restart the four records/two Lessons loaded normally; Student edit P3→P4 succeeded, restoring P3 succeeded, and retained former-member history was readable. Final restored data matches the known-good source copy exactly. See `retry/recovered-history.png`.
- **Help menu:** native click and keyboard activation attempts still did not expose a usable menu through this automation. One coordinate attempt returned `windowNotFoundAtPosition`; this is an automation limitation, not evidence of a menu defect. No Mac menu PASS is claimed. F1 and typed Help evidence remain valid; existing Windows menu evidence is separate.

Both retry candidate copies match the original JAR SHA-256. All retry Java processes were confirmed stopped. The original-run details below remain historical evidence; this section supersedes their incomplete protected-session disposition.

## Identity and environment

- Reviewed source: `ed32fe49901ea11070ff16086490d2d72adafcd1`.
- Downloaded from [the final source/checksum workflow artifact](https://github.com/AY2627S1-CS2103T-F13-3/tp/actions/runs/39706371977/artifacts/12395006972).
- `ponhub.jar`, 12,654,205 bytes, SHA-256 `5e24df511c9a5975c1c15e310ab03f2a852837e969359afe71fc8a37fa905456`. Hash matches before and after testing.
- Manifest PonHub / 1.4 / `ponhub.Main`; startup log reports `Starting PonHub v1.4`.
- macOS 27.0.1, build 26A434, arm64. Prescribed Azul `25.0.3.fx-zulu`, Zulu25.34+17-CA / Java 25.0.3+9-LTS with bundled JavaFX. Assertions enabled (`-ea`). See [runtime](runtime.txt) and [identity](identity.json).
- Disposable JAR folder `/private/tmp/mac-candidate-272-20261022/session`; no real operational data. A second malformed fixture used `protected-session` separately.
- A temporary `.app` launcher made the Java process identifiable to the native UI tool. It executes the unchanged JAR with the prescribed Java binary and `-Xdock:name`; no Java classes/resources/runtime settings were patched. Exact launcher text is retained. A direct launch before the UI run reached startup and was stopped before mutations.
- Default window 740×600 logical points, 1480×1200 captured pixels. Native zoom was also inspected (pixel dimensions in [screenshots.json](screenshots.json)); no OS display scaling was changed. This is not a full DPI/scaling matrix.

## Observed results

| Scenario | Result and evidence |
| --- | --- |
| Native startup and immediate keyboard command | PASS: usable main window, `help` without first clicking the command box; `01-startup-help.png`. No empty-screen-list failure reproduced on this machine. |
| Create combined fixture | PASS: Tutor T1, Students S1/S2, Parent P1, Lessons L1/L2; two Students enrolled in L1; independent present/absent on Monday 2026-10-05. `02-shared-attendance.png`. |
| Person/contact edit and clearing | PASS: S1 renamed Alex Lee, level P3, email cleared, own phone/address updated. Stable S1, roster/history preserved. `03-person-edit.png` and later readbacks. |
| Lesson and Tutor edits | PASS: L1 becomes Advanced Math, 16:30–17:30, R3; T1 renamed Mei Tan, current Lesson label updates. Same L1/T1 and both dated statuses. `04-lesson-and-tutor-edit.png`. |
| Rejections | PASS: bad level, duplicate Jamie/P1 identity, overlapping Tutor schedule against L2, and Tuesday change incompatible with retained Monday attendance all reject. Saved bytes unchanged. |
| No-ops | PASS: normalized `Alex  Lee`, identical Lesson edit and already-present mark report no change; saved bytes unchanged. `05-rejection-noop.png`, exact checkpoints below. |
| Parent relationships | PASS: Parent search by Alex/Advanced Math finds Pat with current Lesson context. Editing Pat's phone breaks the exact-phone match and refreshes the active result to zero; restoring it restores the result. `06-parent-relationship.png` and UI transcript. |
| Lesson search refresh | PASS: active Advanced Math search becomes empty after subject edit to English and returns L1 after restoring Advanced Math. |
| Attendance correction and former history | PASS: Alex corrected present→absent, unenrolled, retained 2026-10-05 L1 absence shown as former enrolment. `07-former-history.png`. |
| F1 | PASS: catalogue appears while unfinished `edit 1 n/Unfinished`, Student filter and history panel remain. `08-f1-preserves-draft-history.png`. No selected-person preservation claim is inferred from this test. |
| Window readability | PASS within observed default/zoom sizes: populated history row readable. Normal views scroll to reach offscreen records/details; no all-content-at-once claim. `09-zoomed-history.png`. |
| Same-JAR exit/restart | PASS: first `exit` logs shutdown and process disappears; relaunch same JAR/store. Stable IDs/counters, P3/contact changes, renamed Tutor, L1 schedule/subject/room, Jamie's membership and both absences survive. Former history visible. `10-restarted-lesson.png`, `11-restarted-history.png`. Operational bytes identical across restart/read-only checks. |
| Injected save failure and retry | PASS: made only the disposable data directory unwritable; `edit 1 l/P4` reported insufficient permission. Exact original bytes and visible P3 remained. Restored directory permission, retry succeeded; editing back to P3 restored the original complete bytes. `12-failed-save.png`, checkpoints and log. |
| Corrupt-file startup | Warning OBSERVED: separate malformed original remained unchanged; warning explicitly described CORRUPT/protection/recovery. `13-protected-warning.png`, `mac-protected.log`. Further interaction is incomplete, below. |

## Exact-byte checkpoints

- Before/after rejected and identical changes: `9465f84f82b0b095bb8f51d7743a61cee0def2f8b3f11b7afa8772b4674da71d`.
- Before/after restart, before failed save, after retry/restoration and final store: `eb9200f79b49cb8c2803e41b3497a587b1acb9a24c1d115ac1424abb0624effb`.
- Malformed protected original and after stopped attempt: `499d450f6bd66b35a3739462b4ff5513c43c8643797e1e38e25db13de71395e7`.

The JSON files are original bytes copied without reformatting. [File hashes](file-hashes.csv) cover the retained evidence. [UI transcript](ui-transcript.json) contains 52 command/action/attempt records, including automation attempts; this is not a claim of 52 successfully submitted commands. Native logs retain actual command submissions and feedback.

## Diagnostics and incomplete coverage

1. **Shutdown diagnostic:** after the second explicit `exit`, the log records `Stopping PonHub`, followed by `InvokeLaterDispatcher` / `RuntimeException: Main Java thread is detached` in JavaFX's Mac dispatcher. The app stopped and data remained unchanged. This needs lifecycle/runtime disposition; a completely clean shutdown is not claimed. See `mac-native.log`. The first exit/restart succeeded. A subsequent automation binding unexpectedly relaunched the main app without commands; it was stopped and is not counted as another acceptance flow.
2. **Protected-session interaction incomplete:** the corrupt-file warning was captured and dismissed with Return. After dismissal, native accessibility/window operations repeatedly timed out. No protected Help/blocked-command/recovery interaction PASS is claimed; the original corrupt file stayed unchanged. Retained `protected-timeout-threads.txt` (trailing whitespace normalized) is diagnostic data, not a proven deadlock or product root cause. The disposable process was stopped.
3. **Help menu not confirmed on Mac:** attempts to activate it did not expose a usable menu through this automation. F1 passed; existing Windows menu evidence retains its own identity. No menu defect is asserted from these automation attempts.
4. Initial accessibility `setValue` did not submit text; native keyboard replacement was used thereafter. One helper expected the wrong success wording (`Updated` versus actual `Edited`); the edit succeeded and subsequent UI/state checks verified it. Both attempts remain in the transcript and are not classified as application failures.
5. No full regression suite, additional OS scaling configurations or other-platform rerun is claimed. Existing Linux/Windows/owner results remain separate evidence. Any candidate change requires affected reconciliation.

## Handoff

This supplies actual prescribed-runtime Mac create/edit/reject/no-op/search/history/restart and save-failure evidence for #272/#271. Ernest should consume it alongside Windows/Linux evidence and give a final PASS/FAIL/NOT RUN disposition, explicitly resolving the shutdown diagnostic and any remaining protected-session/owner coverage. The previous Mac empty-screen-list attempt retains its original environment and outcome; this successful workflow does not erase it.

Both disposable Java app processes were stopped. The candidate JAR and main/protected checkpoint hashes were rechecked after cleanup. This evidence is retained on a dedicated fork branch for the authorized #272 issue handoff. The later manual Help session was left open after inspection; the earlier test processes had been stopped as recorded.
