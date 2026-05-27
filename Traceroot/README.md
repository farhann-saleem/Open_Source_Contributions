# Traceroot Contributions

Consolidated documentation for contributions to [Traceroot](https://github.com/traceroot-ai), a Y Combinator '25 open-source project.

---

## Traceroot
*   **Repository:** [traceroot-ai/traceroot](https://github.com/traceroot-ai/traceroot)
*   **PR:** [#938](https://github.com/traceroot-ai/traceroot/pull/938) (Merged)
*   **Issue:** [#937](https://github.com/traceroot-ai/traceroot/issues/937) (Detector evaluator reads duplicate spans)
*   **Impact:** Fixed an issue where the detector evaluator read duplicate spans before background merges completed. Added the `FINAL` keyword to the ClickHouse deduplication query for pre-merge rows in the `ReplacingMergeTree`, ensuring accurate evaluations.
