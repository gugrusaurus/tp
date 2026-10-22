# Combined v1.4 candidate freeze — 22 October 2026

Prepared by Vincent Lin (gugrusaurus) with OpenAI Codex assistance.

- Selected team application source: c92c689ee8802fb2cb3957832c25dd9407099dbf.
- Git tree: 5bc9ac1d4fd7ab4364fd23988dbebda54f9875bc.
- Includes ordinary integrations #373 (menu), #374 (compact feedback) and #375 (four live heading tooltips).
- Exact file: ponhub.jar; 12,655,415 bytes.
- SHA-256: 8fbd0e5414d91c006984489b71083445da41d22f76f37c2fbc49a681d79ac9d6.
- Manifest: Manifest-Version 1.0; Implementation-Title PonHub; Implementation-Version 1.4; Main-Class ponhub.Main.

Built from clean selected source with the repository Gradle wrapper: Java Oracle 25.0.4.1+1-LTS-5, Windows 10 build 19045/x64; `gradlew.bat --offline --no-daemon shadowJar`, BUILD SUCCESSFUL, 3 tasks executed. Initial sandbox cache access was denied; elevated attempt exposed inherited JAVA_HOME=Java 11. Setting JAVA_HOME explicitly to Java 25 produced the successful build. No build configuration, application inputs or runtime libraries were changed.

Exact source tree equals reviewed #375 head 3912aeeeee22816c85b2e0b4ad09f4be2e2005d4 (git diff empty). Rebuilt JAR hash equals the independently recorded #375 package hash. Head CI 39767604619 passed Ubuntu/macOS/Windows, with substantive non-author review and ordinary integration recorded by the team. No new full suite or combined-source native PASS is claimed by this freeze.

Compared with old accepted ed32fe49901ea11070ff16086490d2d72adafcd1, production changes are only HistoryListPanel.java, LessonListPanel.java, new ResultHeadingTooltip.java, DarkTheme.css and MainWindow.fxml. Build/dependency configuration, wrapper and other application inputs are unchanged. Prior 5e24df51… baseline and fb24845c… menu-only evidence retain their own identities.

## Ernest's bounded affected-package check — pending

Download this exact ponhub.jar and verify size/hash before launch. In an isolated writable fixture with Java 25 (architecture-appropriate Azul 25.0.3.fx-zulu on Mac), check compact and tall startup, divider expansion/shrinking, complete long help, all four live heading tooltips, readable File/Help ordinary/highlighted popup states, keyboard navigation, F1/menu Help draft/filter/selection/history preservation and operational-byte preservation. Retain actual runtime/platform/screenshots and source/JAR identity. This is the bounded #363/#369 reconciliation, not cancelled #362's broad round.

## Material reconciliation

Release notes now pin this source and describe the three integrated corrections. Older layout-dependent screenshots are removed from the proposed release body, preserved unchanged as historical media in media-provenance.md with their original ed32fe49 / 5e24df51… identity and credits. They do not demonstrate this candidate's compact feedback/tooltips. Ernest's new affected-check screenshots may be selected for current layout media only after their actual identity/results are recorded; no replacement image or native PASS is invented.

Freeze is ready for Ernest's check. Final affected acceptance, materials review and Zhi Yu's #274 publication/public-download checks remain separate. No release/tag/issue closure or deadline change performed.
