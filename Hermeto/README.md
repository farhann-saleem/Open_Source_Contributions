# Hermeto Contribution

Contribution to [Hermeto](https://github.com/hermetoproject/hermeto).

## PR Details
*   **PR:** [#1373](https://github.com/hermetoproject/hermeto/pull/1373)
*   **Status:** Merged
*   **Description:** Fixed `gomod` toolchain detection by preserving symlink names. Discovered and resolved issue [#1372](https://github.com/hermetoproject/hermeto/issues/1372) where `Path.resolve()` was incorrectly filtering out Go binaries on snap-based systems.

*   **PR:** [#1338](https://github.com/hermetoproject/hermeto/pull/1338)
*   **Status:** Merged
*   **Description:** Fixed garbled text in `usage.md` and updated a stale link in `dependency_confusion.md`.

*   **PR:** [#1330](https://github.com/hermetoproject/hermeto/pull/1330)
*   **Status:** Merged
*   **Description:** Fixed incorrect CLI option name `--output-dir` to `--output` in `cargo.md` documentation.

*   **PR:** [#1346](https://github.com/hermetoproject/hermeto/pull/1346)
*   **Status:** Open
*   **Description:** Implemented a technical fix for HTTP 429 (Too Many Requests) retry logic. Introduced a `RetryAfterJitterRetry` class to correctly respect the `Retry-After` header in the async path and added comprehensive unit tests using parametrization.

*   **PR:** [#1377](https://github.com/hermetoproject/hermeto/pull/1377)
*   **Status:** Approved ✅
*   **Description:** Improved error handling in the `cargo` backend by wrapping generic subprocess errors in `PackageManagerError`. This prevents leaking raw Python tracebacks to the user when `cargo vendor` fails for reasons other than lockfile mismatches.

## Issues & Bug Discovery
*   **Issue:** [#1376](https://github.com/hermetoproject/hermeto/issues/1376)
*   **Description:** Identified an error handling inconsistency in the `cargo` backend where raw `CalledProcessError` exceptions were leaking Python tracebacks. Aligned the behavior with other backends (gomod, yarn, bun) by implementing proper error wrapping. Resolved via PR [#1377](https://github.com/hermetoproject/hermeto/pull/1377).

*   **Issue:** [#1372](https://github.com/hermetoproject/hermeto/issues/1372)
*   **Description:** Identified a critical flaw in how Hermeto detected Go toolchains on systems where Go is installed via `snap`. Discovered that `Path.resolve()` was stripping the symlink names needed for version identification. Resolved via PR [#1373](https://github.com/hermetoproject/hermeto/pull/1373).
