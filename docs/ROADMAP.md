# Android Mastery — 42-lesson roadmap

Daily format: **10 min learn + 15 min hands-on + 5 min recap**. If a topic is difficult, split it across multiple days rather than rushing.

## Milestone 1 — Linux foundations
1. Your Linux environment — terminal, shell, home directory, Fedora basics.
2. Filesystem navigation — pwd, ls, cd, paths.
3. Files and directories — mkdir, touch, cp, mv, safe deletion.
4. Read and search files — cat, less, head, tail, grep, find.
5. Permissions and processes — permissions, ownership, ps, top.
6. Packages, PATH and pipes — dnf, PATH, pipes and redirection.

## Milestone 2 — ADB and debugging
7. Install platform-tools and verify adb version.
8. Developer options, USB debugging and RSA authorization.
9. Interpret adb devices -l states.
10. Use adb shell, getprop and basic inspection.
11. Install APKs and inspect packages; understand pull and push.
12. Filter logcat, capture small logs and redact sensitive details.

## Milestone 3 — Kotlin and app foundations
13. Kotlin values, variables, types, functions and string templates.
14. Null safety, collections, safe calls and the Elvis operator.
15. Classes, data classes, interfaces and enums.
16. Coroutines, suspend functions and structured concurrency.
17. Android project structure, Gradle, manifest and resources.
18. Jetpack Compose UI and state.

## Milestone 4 — Android internals and security
19. Android layers: apps, framework, ART, HAL, kernel and hardware.
20. App sandbox, UID isolation, runtime permissions and SELinux.
21. Boot chain: boot ROM, bootloader, kernel, init and system_server.
22. Partitions: boot, vendor_boot, vbmeta, super and logical partitions.
23. Verified Boot, AVB and rollback protection.
24. Logcat, ANRs, tombstones and crash traces.

## Milestone 5 — Root, recovery and device safety
25. Root concepts, su, Magisk and security trade-offs.
26. Boot image components and Android-version differences.
27. Recovery, package verification and ADB sideload.
28. Magisk module structure and safe disable/recovery paths.
29. Bootloop planning, backups and device-specific recovery routes.
30. Compatibility, integrity and risk assessment before modifications.

## Milestone 6 — AOSP and custom ROMs
31. AOSP source tree: frameworks, packages, system, hardware and build.
32. Repo tool, manifests, branches and source sync.
33. Linux build dependencies, Java versions, lunch targets and build systems.
34. Device trees, common trees, vendor blobs and kernel sources.
35. ROM build workflow and build artifacts.
36. Triage build failures and produce a minimal reproducible issue.

## Milestone 7 — Kernel and advanced debugging
37. Kernel architecture, processes, syscalls, drivers and device trees.
38. Kernel source, defconfig, Kconfig, Makefiles and toolchains.
39. Boot image formats, headers, ramdisks and compression.
40. CPU, memory, performance and thermal diagnostics.
41. Native crashes, JNI, ABI mismatches, symbols and tombstones.
42. Upstream contribution: clean patches, issue reports and code review.

## Safety rules
- Never run a command you cannot explain.
- Never flash an image unless it is for the exact device codename and compatible build.
- Before partition or boot-chain work, verify backups and a recovery route.
- Treat serial numbers, account details and unredacted logs as private.
- Start with read-only inspection commands; destructive operations are not beginner labs.