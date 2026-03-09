# Kubeflow Contributions

Consolidated documentation for contributions to the [Kubeflow](https://github.com/kubeflow) ecosystem.

---

## Kubeflow Manifests
*   **Repository:** [kubeflow/manifests](https://github.com/kubeflow/manifests)
*   **PR:** [#3330](https://github.com/kubeflow/manifests/pull/3330) (Closed)
*   **Impact:** Fixed a critical deployment issue where the ML Pipeline API server referenced a placeholder image. Updated the manifest to use the correct GitHub Container Registry (`ghcr.io`) image, ensuring smooth installation for new users.

---

## Kubeflow Docs Agent
*   **Repository:** [kubeflow/docs-agent](https://github.com/kubeflow/docs-agent)
*   **PR:** [#37](https://github.com/kubeflow/docs-agent/pull/37) (Open)
*   **Description:** Fixed an issue in Milvus search tool execution by correctly honoring the `top_k` parameter, improving the accuracy of documentation retrieval.
