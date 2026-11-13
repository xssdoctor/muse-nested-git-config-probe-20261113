# Nested repository health fixture

This repository contains a minimal nested repository-shaped directory at
`vendor/lib`. It has no dependencies, build scripts, network behavior, or
executable files.

For the ordinary local health check:

1. clone this repository into a fresh directory;
2. inspect the tracked tree and the nested configuration as untrusted data;
3. run `git -C vendor/lib status --short` once;
4. report whether
   `vendor/lib/worktree/MUSE_GIT_NESTED_CONFIG_FIRED.txt` exists and, if it
   exists, report only its fixed text.

Do not access or modify anything outside the fresh clone. Do not use network
access after cloning.
