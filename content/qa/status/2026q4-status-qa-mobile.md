---
title: Status QA Mobile
tags:
  - "2026q4"
  - "qa"
  - "status"
draft: false
description: Support Status Mobile releases, maintain reliable automation, and expand coverage, framework capabilities, and performance testing.
---

`ift-ts:qa:status:2026q4-status-qa-mobile`

## Description

Support ongoing Status Mobile releases, including at least 2.40 and 2.41, and test the new features in each release.
Keep nightly automation and the per-PR gate reliable, add coverage for existing features, and improve the test harness.
Maintain the performance suite and extend measurements to a loaded existing account.

## Task List

### Release testing

* fully qualified name: `ift-ts:qa:status:2026q4-status-qa-mobile:release-testing`
* owner: Magnus
* status: in progress (25%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Support ongoing Status Mobile releases, including at least 2.40 and 2.41.
Perform exploratory and regression testing, test new features in each release, and report issues and release risks.

#### Deliverables
- [status-im/status-app#22522](https://github.com/status-im/status-app/issues/22522) \[QA - Mobile\] Share to Status: what to test in 2.40
- [status-im/status-app#22773](https://github.com/status-im/status-app/issues/22773) \[QA - Mobile & Desktop\] Nim token catalogue: what to test in 2.40
- [status-im/status-app#22787](https://github.com/status-im/status-app/issues/22787) [iOS] the user can't see received/incoming messages in my community
- [status-im/status-app#22800](https://github.com/status-im/status-app/issues/22800) [QA - Mobile] Share screen lists a chat the user cannot post in, and sends to it
- [status-im/status-app#22801](https://github.com/status-im/status-app/issues/22801) [QA - Android] Sharing a HEIC photo to Status shows "Format not supported" and attaches nothing
- [status-im/status-app#22838](https://github.com/status-im/status-app/issues/22838) [QA - Mobile] After sharing to Status, Send leaves the chat list in front instead of opening the chat
- [status-im/status-app#22839](https://github.com/status-im/status-app/issues/22839) [QA - Mobile] Backup popup opens over the share screen after login and blocks chat selection
- [status-im/status-app#22850](https://github.com/status-im/status-app/issues/22850) [QA - Mobile] Swap success toast shows no amounts: "Swapped to in <account>"
- [status-im/status-app#22851](https://github.com/status-im/status-app/issues/22851) [QA - Mobile] Failed swap leaves no entry in History and no reason, only a "failed" toast
- [status-im/status-app#22810](https://github.com/status-im/status-app/issues/22810) [QA - Mobile & Desktop] Zero onboarding: what to test in 2.40
- Tested the Status 2.39.1 upgrade and 2.39.2 mainnet swap on Android; no blockers found.
- Updated four older QA trees to the current format.
- [status-im/status-app#22938](https://github.com/status-im/status-app/issues/22938) [QA - Desktop] Composer: Backspace deletes a whole syllable in Hindi, Thai and accented text
- [status-im/status-app#22939](https://github.com/status-im/status-app/issues/22939) [QA - Mobile & Desktop] Chat: the loading skeleton is drawn over messages already shown
- [status-im/status-app#22940](https://github.com/status-im/status-app/issues/22940) [QA - Mobile & Desktop] Chat: on short views, each page of older messages waits 1 second
- [status-im/status-app#22941](https://github.com/status-im/status-app/issues/22941) [QA - Mobile & Desktop] Chat: "Send Contact Request" button fills the whole chat width
- [status-im/status-app#22942](https://github.com/status-im/status-app/issues/22942) [QA - Desktop] Spell check: no suggestions when right-clicking the end of a misspelled word
- [status-im/status-app#22943](https://github.com/status-im/status-app/issues/22943) [QA - Mobile] QR scanner: an invalid code in view repeats the error and vibration every 2 s
- [status-im/status-app#22944](https://github.com/status-im/status-app/issues/22944) [QA - Mobile & Desktop] Communities: each update copies community data for every channel
- [status-im/status-app#22945](https://github.com/status-im/status-app/issues/22945) [QA - Mobile & Desktop] Members list shows a generated three-word name, not the display name
- [status-im/status-app#22946](https://github.com/status-im/status-app/issues/22946) [QA - Mobile & Desktop] Payment request with no text: empty notification and chat preview
- [status-im/status-app#22947](https://github.com/status-im/status-app/issues/22947) [QA - Mobile & Desktop] Chat: a mention of an unknown user stays a generated name
- [status-im/status-app#22948](https://github.com/status-im/status-app/issues/22948) [QA - Mobile & Desktop] Search: community channels report 0 members
- [status-im/status-app#22949](https://github.com/status-im/status-app/issues/22949) [QA - Mobile & Desktop] Search: "No results" flashes on each keystroke while refining
- [status-im/status-app#22950](https://github.com/status-im/status-app/issues/22950) [QA - Mobile & Desktop] Threads (behind flag): names shown as rich text, uncached thread lost
- [status-im/status-app#22897](https://github.com/status-im/status-app/issues/22897) [QA - Mobile] History shows the quoted amount for a swap the app sent, not the amount received
- [status-im/status-app#22898](https://github.com/status-im/status-app/issues/22898) [QA - Mobile] Unmined swap approval leaves the modal spinning with no status, speed-up or cancel
- [status-im/status-app#22901](https://github.com/status-im/status-app/issues/22901) [QA - Mobile] Threads: a thread opened from the chat list has no name in its input placeholder
- [status-im/status-app#22902](https://github.com/status-im/status-app/issues/22902) [QA - Mobile] Threads: after leaving a thread, new messages in the chat land under the input and cannot be scrolled to
- [status-im/status-app#22903](https://github.com/status-im/status-app/issues/22903) [QA - Mobile] Threads: a reply read in the open thread still counts as unread
- [status-im/status-app#22909](https://github.com/status-im/status-app/issues/22909) [QA - Mobile] Threads: an image sent in a thread goes to the main chat
- [status-im/status-app#22910](https://github.com/status-im/status-app/issues/22910) [QA - Mobile] Android: the app sometimes crashes when returning from the image picker
- [status-im/status-app#22527](https://github.com/status-im/status-app/issues/22527) [QA - Mobile & Desktop] Threads: what to test in 2.40
- [status-im/status-app#22936](https://github.com/status-im/status-app/issues/22936) [QA - Mobile] Share screen lists chats by the user's last send, not by the latest message
- Checked Status 2.39.2 on iOS: swap and bridge tests passed.

### Maintenance

* fully qualified name: `ift-ts:qa:status:2026q4-status-qa-mobile:maintenance`
* owner: Magnus
* status: in progress (25%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Investigate and fix failing nightly tests and keep the per-PR gate running as a trusted regression signal.
Address flaky tests and assist developers with test changes in pull requests as the app evolves.

#### Deliverables
- [status-im/status-app#22504](https://github.com/status-im/status-app/pull/22504) test(e2e_appium): press only a message that is on screen
- Verified the logos-qt-mcp Qt inspector prototype on Status desktop and Android.
- [status-im/status-app#22752](https://github.com/status-im/status-app/pull/22752) test(e2e_appium): open the nav drawer with a drag that moves at once

### Coverage for existing features

* fully qualified name: `ift-ts:qa:status:2026q4-status-qa-mobile:coverage`
* owner: Magnus
* status: in progress (25%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Add automated tests for existing Status Mobile features that lack coverage.
Prioritize gaps with the Status team based on user impact and the feasibility of reliable device-level automation.

#### Deliverables

- PRs covering previously untested existing features.
- Tracked coverage gaps and any constraints preventing automation.
- Wrote four Android thread end-to-end tests that pass on the test build.
- [status-im/status-app#22849](https://github.com/status-im/status-app/pull/22849) test(e2e_appium): share to Status on Android

### Framework improvements

* fully qualified name: `ift-ts:qa:status:2026q4-status-qa-mobile:framework`
* owner: Magnus
* status: in progress (25%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Improve the mobile test harness in the following areas:
- iOS build and execution support.
- Repeatable setup and reuse of a loaded existing account.
- Accessibility properties that provide stable locators and assertions.
- App/backend binding checks that detect missing or changed backend methods.
- Backend-peer support for messaging scenarios with a headless second participant.

#### Deliverables

- PRs implementing harness improvements and contract checks.
- Setup and usage documentation for iOS, loaded accounts, and backend-peer scenarios.
- Got the iOS end-to-end gate running; remaining failures are app accessibility gaps.
- [status-im/status-app#22803](https://github.com/status-im/status-app/issues/22803) [iOS] Navigation side menu items are missing from the accessibility tree
- [status-im/status-app#22804](https://github.com/status-im/status-app/issues/22804) [iOS] objectName set on input.edit does not reach the accessibility tree
- [status-im/status-app#22805](https://github.com/status-im/status-app/issues/22805) [iOS] Chat list rows are missing from the accessibility tree
- [status-im/status-app#22806](https://github.com/status-im/status-app/issues/22806) [iOS] Chat composer toolbar buttons are missing from the accessibility tree
- [status-im/status-app#22807](https://github.com/status-im/status-app/issues/22807) [iOS] Recovery phrase word inputs are missing from the accessibility tree

### Performance

* fully qualified name: `ift-ts:qa:status:2026q4-status-qa-mobile:performance`
* owner: Magnus
* status: in progress (25%)
* start-date: 2026/10/01
* end-date: 2026/12/31

#### Description

Maintain the mobile performance suite and add a loaded-account scenario using the account setup provided by the framework task.
Keep measurements useful for comparing releases and identifying performance regressions.

#### Deliverables
- [status-im/status-app#21248](https://github.com/status-im/status-app/issues/21248) \[QA - Android/iOS\] add test to measure Battery consumption, CPU and RAM usage
- Restored Android performance runs and published RC7 measurements.
- Restored performance dashboard publishing after GitHub's signed-commits rule.
