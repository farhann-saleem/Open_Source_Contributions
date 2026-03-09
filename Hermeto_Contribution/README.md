# Hermeto Contribution

Contribution to [Hermeto](https://github.com/hermetoproject/hermeto).

## PR Details
*   **PR:** [#1373](https://github.com/hermetoproject/hermeto/pull/1373)
*   **Status:** Approved ✅ (Awaiting Merge)
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
