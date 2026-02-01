# 🔧 Kubeflow Manifests Fix

## 📌 Context
**Repository:** [kubeflow/manifests](https://github.com/kubeflow/manifests)  
**PR:** [#3330](https://github.com/kubeflow/manifests/pull/3330)

Kubeflow manifests are used to deploy Kubeflow on Kubernetes. This specific contribution targeted the deployment configuration for the ML Pipeline API server.

## ⚠️ The Problem
Users attempting to deploy the platform-agnostic multi-user K8s-native environment encountered errors because the deployment file referenced a placeholder image (`domain.local/apiserver:local`) instead of a valid container registry image. This caused the pod to fail during image pull.

## 🛠️ The Solution
I identified the incorrect image reference and updated the manifest to use the correct image from the GitHub Container Registry (`ghcr.io`).

**Changes:**
- Updated deployment YAML to point to the correct image source.
- Verified that the kustomize build generated valid output.

## 🚀 Impact
This fix ensures that the default installation instructions work correctly for new users, preventing frustration and reducing the barrier to entry for setting up Kubeflow pipelines.
