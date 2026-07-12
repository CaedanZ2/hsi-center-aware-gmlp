# Public Technical Summary

## Project

**A Study on Hyperspectral Remote Sensing Image Recognition Based on Deep Learning**

Final-year project, 2025-2026.

## Research Question

How can a patch-based hyperspectral classifier exploit surrounding spectral-spatial context while remaining aligned with center-pixel supervision?

## Proposed Framework

The final framework combines:

- a 3D-CNN spectral-spatial encoder;
- channel-wise and spatial attention;
- a center-aware Gaussian weighting prior over spatial tokens;
- an HSI-specific gMLP token mixer;
- global pooling and a classification head.

The center-aware prior softly increases the importance of central tokens without removing contextual tokens. The gMLP Spatial Gating Unit models interactions across spatial token positions.

## Evaluation

Benchmarks:

- Indian Pines
- Pavia University
- Salinas

Metrics and analyses:

- Overall Accuracy (OA)
- Average Accuracy (AA)
- Cohen's Kappa
- per-class accuracy
- classification maps
- normalized confusion matrices
- parameter count
- MACs
- training and inference time
- component-wise ablation studies

## Verified Findings

- Indian Pines OA improved from 84.95% for the 3D-CNN baseline to 96.39% for the final model.
- Across the three datasets, the final model achieved 97.96% mean OA, 97.08% mean AA, and 97.62% mean Kappa.
- The proposed model achieved the strongest mean AA in the reported comparison.
- HybridSN achieved a higher mean OA and Kappa, so the proposed method is best characterized as a balanced classifier rather than universally superior.
- gMLP-based token mixing contributed the dominant ablation gain, while the center-aware prior provided an additional improvement on the most challenging class-imbalanced scene.

## Limitations

- The work is a senior team project rather than a peer-reviewed publication.
- Performance depends on the stated dataset partitions and experimental protocol.
- The proposed model is not the smallest or lowest-MAC model in the comparison.
- A clean and independently reproducible public code release has not yet been completed.
